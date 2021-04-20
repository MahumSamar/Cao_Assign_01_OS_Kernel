My final output of the above OS kernel is:
![img 1](/Cao_Assign/images/final.png)
#### Softwares
---
The software that were used are:
1. Visual Studio Code for coding
2. Docker to simplify development process
3. Qemu to emulate OS
4. NASM, grub, and GCC-cross-x86_64-elf used by docker to simplify its implementation. 
#### Set Up Image
---
The commands that I used are as follows:
- To build the docker image 
`docker build buildenv -t myos-buildenv`
#### Build
---
- After that spin up this image as a container. I was using windows so used this command
Windows (CMD): `docker run --rm -it -v "%cd%":/root/env myos-buildenv`
- Then used build command 
`make build-x86_64`
#### Image
---
- And emulated it with Qemu
`"C:\Program Files\qemu\qemu-system-x86_64" -cdrom dist/x86_64/kernel.iso`
#### Reference
---
1. Youtube Videos
    - [Video 1](https://www.youtube.com/watch?v=FkrpUaGThTQ)
    - [Video 2](https://www.youtube.com/watch?v=wz9CZBeXR6U)
2. Github
    - [Episode 2](https://github.com/davidcallanan/os-series/tree/ep1)
    - [Episode 2](https://github.com/davidcallanan/os-series/tree/ep2)
