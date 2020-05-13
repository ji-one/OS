## Project #2. Priority Scheduler


#### 1. Implement system calls related to process priority. 

- The default nice value is 20.  
- The range of valid nice value is [0,40].  
- Lower nice value cause more favorable scheduling.  
- When a process calls fork() system call, the nice value of child process is same as its parent process.   
- `setnice()`  
Get the nice value of process (0 ~ 40).   
Return 0 on success.  
Return -1 if there is no process corresponding to the pid or the nice value is invalid.


- `getnice()`   
Return the nice value of pid(process).    
Return -1 if there is no process correspoinding to the pid.  


- `ps()`    
The ps function prints out process(s)'s information, which includes pid, ppid, nice, status, and name of each process.
If the pid is 0, print out all processes' information. Otherwise, print out corresponding process's information.
If there is no process correspoinding to the pid, print out nothing.   
No return value.   
Make a user program(minitop) displays process status using ps system call.  


#### 2. Implement priority-based scheduler on xv6. 
- The lower nice value, the higher priority.  
- The highest priority process is selected for next running. 
- Tiebreak : FIFO fashion. 


---  
### Changed files

- defs.h  
Add definition of `setnice()`, `getnice()`, `ps()`.  

- Makefile   
Add `_minitop\` to execute minitop.c (also add test files). 

- minitop.c  
Make user program for `minitop()`  to displays  process status using ps system call. 

- proc.c    
`allocproc()` : Set default nice value.    
`fork()` : Set nice value of child process same as its parent process.    
`scheduler()` : Make priority scheduler.     
`getnice()` : Make system call getnice().        
Return the nice value of pid(process)   
`ps()` : Make system call ps().      
Prints out process(s)'s information.    
`setnice()` : Make system call setnice().     
Get the nice value(0~40) of process.     

- proc.h    
Add `nice` variable. 

- syscall.c  
Add system call for `setnice()`, `getnice()`, `ps()`.  

- syscall.h  
Add system call number for `setnice()`, `getnice()`, `ps()`.   

- sysproc.c  
Add interrupt function for `getnice()`, `setnice()`, `ps()`.   

- user.h  
Add system call for `setnice()`, `getnice()`, `ps()`.  

- usys.S   
Add system call for `setnice()`, `getnice()`, `ps()`.    
