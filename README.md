# InWorldz aperture texture and mesh server

Aperture is a simple not quite compliant HTTP/1.1 server that sends texture and
mesh data to viewer software connected to the InWorldz grid

### Sample cmake build command for windows

This fork of aperture has been modified for compilation on linux.  Building on windows has likely been affected.

cmake .. -DCMAKE_BUILD_TYPE=Debug -DCURL_LIBRARY=C:\lib\curl-7.44.0\builds\libcurl-vc-x64-debug-dll-ipv6-sspi-winssl\lib\libcurl_debug.lib -DCURL_INCLUDE_DIR=C:\lib\curl-7.44.0\include -DPROTOBUF_LIBRARY=C:\lib\protobuf-2.6.1\vsprojects\x64\Debug\libprotobuf.lib -DPROTOBUF_INCLUDE_DIR=C:\lib\protobuf-2.6.1\src -DPROTOBUF_PROTOC_EXECUTABLE=C:\lib\protobuf-2.6.1\vsprojects\x64\Debug\protoc.exe
-G "Visual Studio 14 2015 Win64"

### Directions for Ubuntu 16.04 LTS

These are the basic commands in order based off of my terminal history, they may not be precise.

1. Install cmake, protobuf-compiler, libboost1.58-all-dev
1. clone aperture
1. cd aperture
1. mkdir build
1. cd build
1. cmake ..
1. make
1. Create the configuration file

A bare-bones aperture.cfg file is:
<pre>
http_listen_port = <port number>
caps_token = 2960079
whip_url = whip://<password>@<ip>:32700
</pre>

