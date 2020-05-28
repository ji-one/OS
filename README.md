# OS-2020

#### - Setting up Xv6

##### setting up environments
    1. Install Ubuntu 16.04.6 LTS
    2. sudo apt-get upgrade
    3. sudo apt-get install build-essential
    4. sudo apt-get install gcc-multilib
    5. sudo apt-get install git
    
##### install xv6
    1. cd
    2. git clone git://github.com/mit-pdos/xv6-public.git
    3. cd xv6-public
    4. make
    
##### install qemu 
    1. sudo apt-get install qemu
    
##### run xv6
    1. cd
    2. cd xv6-public
    3. make qemu-nox
    
##### stop xv6
    1. Ctrl-A + X
   
#### - CSCOPE

##### install cscope
    $ sudo apt-get install cscope
    
##### using cscope with Vim
    $ wget http://cscope.sourceforge.net/cscope maps.vim
    $ mkdir -p ~/.vim/plugin
    $ cp cscope_maps.vim ~/.vim/plugin
    
##### creating cscope databse
    $ cscope -Rb
    - for Linux Kernel
    $ make cscope

#### - How to compress code
    
    $ cd xv6-public
    $ make clean
    $ cd ..
    $ tar -czvf putyourfilename.tar.gz ./xv6-public
    
    please command $ make clean before compressing
    

#### - How to decompress code

    $ tar -zxvf putyourfilename.tar.gz
    
  
--- 
### project list   
#### [No.0 Install xv6](https://github.com/ji-one/OS-2020/tree/master/project%20%230)   
- Print student ID and name in the xv6 boot message
  
#### [No.1 System call](https://github.com/ji-one/OS-2020/tree/master/project%20%231)  
- Make system call that returns the value of a counter which is incremented every time any process calls the read() system call. Also make user program for testing.
  
#### [No.2 Scheduling](https://github.com/ji-one/OS-2020/tree/master/project%20%232)  
- Implement system calls related to process priority (setnice, getnice, ps)
- Implement priority-based scheduler on xv6  


---
### LICENSE  
MIT License

Copyright (c) 2020 jiwon kim

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

