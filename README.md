# SWR_Online_Server
The SWR Online server

## Usage
### Requirements
- ASIO ( Get from https://think-async.com/Asio/ or any Linux Repository )
- [Linux] GCC Compiler
- [Windows] GCC or Visual Studio

## Compiling
```Shell
git clone --recurse-submodules https://github.com/goofbrush/SWR_Online_Server.git
```
### [Linux] Using GCC
```
cd SWR_Online_Server
g++ SimpleServer.cpp -o server -pthread
./server
```
### [Windows] Using GCC
Replace the -I option with the path to ASIOs include directory, heres an example:
```
cd SWR_Online_Server
g++ SimpleServer.cpp -o server -pthread -lws2_32 -lwsock32 -IC:\asio-1.18.1\include
./server
```

### [Windows] Using Visual Studio
- Move all Files into a new project
- Right Click the Project in the Solution Explorer
- Click Properties
- Go to VC++ Directories
- Add the path to ASIO to "Includes Directories"
  - Example: $(VC_IncludePath);$(WindowsSDK_IncludePath);C:\asio-1.18.1\include
- Compile!
