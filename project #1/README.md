# Project #1. System Call


## Make System Calls  
- `int getreadcount(void)`    
Returns the value of a counter which is incremented every time any process calls the read() system call.   
You have to define a variable for the values of read counter. (e.g. readcount)  

- Make a user program readcount using getreadcount() system call for testing.  

---     
## Changed files  
### user.h   
### usys.S  
### syscall.h   
### syscall.c   
### sysproc.c    
### proc.c   
### Makefile   
### getreadcount()    
