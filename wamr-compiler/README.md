
### Build wamrc AOT compiler

Both wasm binary file and AOT file are supported by iwasm. The wamrc AOT compiler is to compile wasm binary file to AOT file which can also be run by iwasm. Execute following commands to build **wamrc** compiler for Linux:

```shell
cd wamr-compiler
./build_llvm.sh (or "./build_llvm_xtensa.sh" to support xtensa target)
mkdir build && cd build
cmake .. (or "cmake .. -DWAMR_BUILD_PLATFORM=darwin" for MacOS)
make
# wamrc is generated under current directory
```

For **Windows**：
```shell
cd wamr-compiler
python build_llvm.py
mkdir build && cd build
cmake ..
cmake --build . --config Release
# wamrc.exe is generated under .\Release directory
```