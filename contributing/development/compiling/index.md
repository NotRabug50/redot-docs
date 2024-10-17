allow\_comments  
False

# Building from source

Godot prides itself on being very easy to build, by C++ projects'
standards. `Godot uses the SCons build system <doc_faq_why_scons>`, and
after the initial setup compiling the engine for your current platform
should be as easy as running:

    scons

But you will probably need to use at least some of the available options
to configure the build to match your specific needs, be it a custom
engine fork, a lightweight build stripped of extra modules, or an
executable targeting engine development.

The articles below should help you navigate configuration options
available, as well as prerequisites required to compile Godot exactly
the way you need.

**Basics of building Godot**

Let's start with basics, and learn how to get Godot's source code, and
then which options to use to compile it regardless of your target
platform.

getting\_source introduction\_to\_the\_buildsystem

**Building for target platforms**

Below you can find instructions for compiling the engine for your
specific target platform. Note that Godot supports cross-compilation,
which means you can compile it for a target platform that doesn't match
your current platform (say, target Linux while being on Windows). The
guides will try their best to cover all possible situations.

compiling\_for\_windows compiling\_for\_linuxbsd compiling\_for\_macos
compiling\_for\_android compiling\_for\_ios
cross-compiling\_for\_ios\_on\_linux compiling\_for\_web

**Other compilation targets and options**

Some additional universal compilation options require further setup.
Namely, while Godot does have C#/.NET support as a part of its main
codebase, it does not get compiled by default to reduce the executable
size for users who don't need C# for their projects.

Articles below explain how to configure the buildsystem for cases like
this, and also cover some optimization techniques.

compiling\_with\_dotnet compiling\_with\_script\_encryption\_key
optimizing\_for\_size
