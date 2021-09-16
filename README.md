# SWR_Online_Client
The SWR Online server

## Usage
### Requirements
- gcc Compiler
- ASIO

### Compiling
```Shell
git clone --recurse-submodules https://github.com/goofbrush/SWR_Online_Server.git
cd SWR_Online_Server
g++ SimpleServer.cpp -o server -pthread
[LINUX] ./server
[WINDOWS] start server.exe
```
