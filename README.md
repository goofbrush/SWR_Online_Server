# SWR_Online_Server
The SWR Online server

## Releases
Pre-compiled binaries can be found here: https://github.com/goofbrush/SWR_Online_Server/releases

## Requirements
- [ASIO](https://think-async.com/Asio/) (Networker)
- [Linux] GCC Compiler
- [Windows] GCC( [mingw](https://sourceforge.net/projects/mingw/) ) or MSVC( [Visual Studio](https://visualstudio.microsoft.com/downloads/) ) </br>

Note, for mingw environments I reccomend using [Atom](https://atom.io/) and installing the [GCC Compiler package](https://atom.io/packages/gcc-make-run)
## Compiling

### Obtaining Files
Make sure to use the recurse option, otherwise no submodules will be cloned
```Shell
git clone --recurse-submodules https://github.com/goofbrush/SWR_Online_Server.git
```
### [Linux] Compiling using GCC
```
cd SWR_Online_Server
g++ SimpleServer.cpp -o server -pthread
./server
```
### [Windows] Compiling using GCC
- Dont use git bash to compile, for a reason that is beyond all comprehension, it fails. Tested it works with mingw and atom
- Replace the -I option with the path to ASIOs include directory, heres an example:
```
cd SWR_Online_Server
g++ SimpleServer.cpp -o server -lws2_32 -lwsock32 -IC:\asio-1.18.1\include -pthread
./server
```

### [Windows] Compiling using Visual Studio
- Move all Files into a new project
- Right Click the Project in the Solution Explorer
- Click Properties
- Go to VC++ Directories
- Add the path to ASIO to "Includes Directories"
  - Example: $(VC_IncludePath);$(WindowsSDK_IncludePath);C:\asio-1.18.1\include
- Compile!
