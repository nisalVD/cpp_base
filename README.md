# Quick start

- under `bin\config` change the `CMAKE_TOOLCHAIN_FILE` to correct path where vcpkg is at, and also the correct
  triplet for your current environment `VCPKG_TARGET_TRIPLET`
- just run the `bin\config` file depending on OS `.bat` windows `.sh` unix it will generate cmake build output
- then you can use `bin\build` to build and `bin\run` to run the program
- depedencies are managed by vcpkg so you can just add a dependecy the vcpkg.json file and
  it can be managed there

## Windows

if you are using MSBuild to compile the cpp code, you will need to use [Clang Power Tools](https://clangpowertools.com/)
to generate compile_commands.json if you are planning to use the clang lsp,
otherwise its generated via CMAKE
