# Project #1. System Call


## Make System Calls  
- `int getreadcount(void)`    
Returns the value of a counter which is incremented every time any process calls the read() system call.   
You have to define a variable for the values of read counter. (e.g. readcount)  

- Make a user program readcount using getreadcount() system call for testing.  

---     
## Changed files  
### user.h   
Add system call for `getreadcount()`.    
### usys.S  
Add system call for `getreadcount()`. 
### syscall.h   
Add system call number for `getreadcount()`.
### syscall.c   
Add system call for `getreadcount()`.
### sysproc.c   
Declare `readcount` as extern.    
Add interrupt function for `getreadcount()`.
### sysfile.c
Add `readcount` variable and initialize to 0.   
Add `readcount` variable to the `sys_reaed()` and when funtion is called, the value of `readcount` is incread by 1.     
### Makefile 
Add `_readcount\` to execute readcount.c
### readcount.c  
Make user program for `readcount()`  

