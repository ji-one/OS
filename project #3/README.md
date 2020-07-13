# Project #3. Stack growth

## 1. Initial size of stack  
- Prepare 1 page initally  
- Can be grow up to 4 pages  

## 2. Growth of stack
- Implementation of page fault handler  
- New page should be allocated to this process if current stack is full
- When stack pointer reaches guard page, occurs stack overflow and kill process  

---

## Changed files 
### trap.c  
### vm.c   
