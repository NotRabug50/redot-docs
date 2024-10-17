allow\_comments  
False

# Configuring an IDE

We assume that you have already
[cloned](https://github.com/godotengine/godot) and
`compiled <toc-devel-compiling>` Godot.

You can easily develop Godot with any text editor and by invoking
`scons` on the command line, but if you want to work with an IDE
(Integrated Development Environment), here are setup instructions for
some popular ones:

android\_studio clion code\_blocks kdevelop qt\_creator rider
visual\_studio visual\_studio\_code xcode

It is possible to use other IDEs, but their setup is not documented yet.

If your editor supports the [language server
protocol](https://microsoft.github.io/language-server-protocol/), you
can use [clangd](https://clangd.llvm.org) for completion, diagnostics,
and more. You can generate a compilation database for use with clangd
one of two ways:

    # Generate compile_commands.json while compiling
    scons compiledb=yes

    # Generate compile_commands.json without compiling
    scons compiledb=yes compile_commands.json
