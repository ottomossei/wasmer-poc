# wasmer-poc
## OKR
 - Objective
     - Investigation of wasmer (WebAssembly runtime)
 - Key Results
     - [x] Confirmation of wasmer startup on linux
     - [x] Establish how to compile C to wasm
     - [x] Interaction with WebAssembly modules in C.

## Setup environment
Refer to [Dockerfile](https://github.com/ottomossei/wasmer-poc/blob/main/.devcontainer/Dockerfile)  
https://docs.wasmer.io/integrations/c/setup

check wasm config
```bash
wasmer config --pkg-config
```

## Example
Implement [example](https://github.com/ottomossei/wasmer-poc/tree/main/example)  
https://docs.wasmer.io/integrations/examples
