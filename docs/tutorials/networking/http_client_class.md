article\_outdated  
True

# HTTP client class

`HTTPClient <class_HTTPClient>` provides low-level access to HTTP
communication. For a higher-level interface, you may want to take a look
at `HTTPRequest <class_HTTPRequest>` first, which has a tutorial
available `here <doc_http_request_class>`.

Warning

When exporting to Android, make sure to enable the `INTERNET` permission
in the Android export preset before exporting the project or using
one-click deploy. Otherwise, network communication of any kind will be
blocked by Android.

Here's an example of using the `HTTPClient <class_HTTPClient>` class.
It's just a script, so it can be run by executing:

console GDScript

c:godot&gt; godot -s http\_test.gd

console C#

c:godot&gt; godot -s HTTPTest.cs

It will connect and fetch a website.

gdscript GDScript

extends SceneTree

\# HTTPClient demo \# This simple class can do HTTP requests; it will
not block, but it needs to be polled.

func \_init():  
var err = 0 var http = HTTPClient.new() \# Create the Client.

err = http.connect\_to\_host("www.php.net", 80) \# Connect to host/port.
assert(err == OK) \# Make sure connection is OK.

\# Wait until resolved and connected. while http.get\_status() ==
HTTPClient.STATUS\_CONNECTING or http.get\_status() ==
HTTPClient.STATUS\_RESOLVING: http.poll() print("Connecting...") await
get\_tree().process\_frame

assert(http.get\_status() == HTTPClient.STATUS\_CONNECTED) \# Check if
the connection was made successfully.

\# Some headers var headers = \[ "User-Agent: Pirulo/1.0 (Godot)",
"Accept: */*" \]

err = http.request(HTTPClient.METHOD\_GET, "/ChangeLog-5.php", headers)
\# Request a page from the site (this one was chunked..) assert(err ==
OK) \# Make sure all is OK.

while http.get\_status() == HTTPClient.STATUS\_REQUESTING:  
\# Keep polling for as long as the request is being processed.
http.poll() print("Requesting...") await get\_tree().process\_frame

assert(http.get\_status() == HTTPClient.STATUS\_BODY or
http.get\_status() == HTTPClient.STATUS\_CONNECTED) \# Make sure request
finished well.

print("response? ", http.has\_response()) \# Site might not have a
response.

if http.has\_response():  
\# If there is a response...

headers = http.get\_response\_headers\_as\_dictionary() \# Get response
headers. print("code: ", http.get\_response\_code()) \# Show response
code. print("\*\*headers:\n", headers) \# Show headers.

\# Getting the HTTP Body

if http.is\_response\_chunked():  
\# Does it use chunks? print("Response is Chunked!")

else:  
\# Or just plain Content-Length var bl =
http.get\_response\_body\_length() print("Response Length: ", bl)

\# This method works for both anyway

var rb = PackedByteArray() \# Array that will hold the data.

while http.get\_status() == HTTPClient.STATUS\_BODY:  
\# While there is body left to be read http.poll() \# Get a chunk. var
chunk = http.read\_response\_body\_chunk() if chunk.size() == 0: await
get\_tree().process\_frame else: rb = rb + chunk \# Append to read
buffer.

\# Done!

print("bytes got: ", rb.size()) var text = rb.get\_string\_from\_ascii()
print("Text: ", text)

quit()

csharp

using Godot;

public partial class HTTPTest : SceneTree { // HTTPClient demo. // This
simple class can make HTTP requests; it will not block, but it needs to
be polled. public override async void \_Initialize() { Error err;
HTTPClient http = new HTTPClient(); // Create the client.

> err = http.ConnectToHost("www.php.net", 80); // Connect to host/port.
> Debug.Assert(err == Error.Ok); // Make sure the connection is OK.
>
> // Wait until resolved and connected. while (http.GetStatus() ==
> HTTPClient.Status.Connecting || http.GetStatus() ==
> HTTPClient.Status.Resolving) { http.Poll(); GD.Print("Connecting...");
> OS.DelayMsec(500); }
>
> Debug.Assert(http.GetStatus() == HTTPClient.Status.Connected); //
> Check if the connection was made successfully.
>
> // Some headers. string\[\] headers = { "User-Agent: Pirulo/1.0
> (Godot)", "Accept: */*" };
>
> err = http.Request(HTTPClient.Method.Get, "/ChangeLog-5.php",
> headers); // Request a page from the site. Debug.Assert(err ==
> Error.Ok); // Make sure all is OK.
>
> // Keep polling for as long as the request is being processed. while
> (http.GetStatus() == HTTPClient.Status.Requesting) { http.Poll();
> GD.Print("Requesting..."); if (OS.HasFeature("web")) { // Synchronous
> HTTP requests are not supported on the web, // so wait for the next
> main loop iteration. await ToSignal(Engine.GetMainLoop(),
> "idle\_frame"); } else { OS.DelayMsec(500); } }
>
> Debug.Assert(http.GetStatus() == HTTPClient.Status.Body ||
> http.GetStatus() == HTTPClient.Status.Connected); // Make sure the
> request finished well.
>
> GD.Print("Response? ", http.HasResponse()); // The site might not have
> a response.
>
> // If there is a response... if (http.HasResponse()) { headers =
> http.GetResponseHeaders(); // Get response headers. GD.Print("Code: ",
> http.GetResponseCode()); // Show response code. GD.Print("Headers:");
> foreach (string header in headers) { // Show headers.
> GD.Print(header); }
>
> > if (http.IsResponseChunked()) { // Does it use chunks?
> > GD.Print("Response is Chunked!"); } else { // Or just
> > Content-Length. GD.Print("Response Length: ",
> > http.GetResponseBodyLength()); }
> >
> > // This method works for both anyways. List&lt;byte&gt; rb = new
> > List&lt;byte&gt;(); // List that will hold the data.
> >
> > // While there is data left to be read... while (http.GetStatus() ==
> > HTTPClient.Status.Body) { http.Poll(); byte\[\] chunk =
> > http.ReadResponseBodyChunk(); // Read a chunk. if (chunk.Length ==
> > 0) { // If nothing was read, wait for the buffer to fill.
> > OS.DelayMsec(500); } else { // Append the chunk to the read buffer.
> > rb.AddRange(chunk); } }
> >
> > // Done! GD.Print("Bytes Downloaded: ", rb.Count); string text =
> > Encoding.ASCII.GetString(rb.ToArray()); GD.Print(text);
>
> } Quit(); }

}
