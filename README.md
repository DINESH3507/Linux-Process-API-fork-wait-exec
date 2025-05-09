# Linux-Process-API-fork-wait-exec-
Ex02-Linux Process API-fork(), wait(), exec()
# Ex02-OS-Linux-Process API - fork(), wait(), exec()
Operating systems Lab exercise


# AIM:
To write C Program that uses Linux Process API - fork(), wait(), exec()

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Write the C Program using Linux Process API - fork(), wait(), exec()

### Step 3:

Test the C Program for the desired output. 

# PROGRAM:
```
#include <stdio.h>
#include <sys/types.h>
#include <unistd.h>
int main(void)
{       //variable to store calling function's process id
        pid_t process_id;
        //variable to store parent function's process id
        pid_t p_process_id;
        //getpid() - will return process id of calling function
        process_id = getpid();
        //getppid() - will return process id of parent function
        p_process_id = getppid();
        //printing the process ids
        printf("The process id: %d\n",process_id);
        printf("The process id of parent function: %d\n",p_process_id);
        return 0; }
```

# OUTPUT:

![Screenshot from 2025-04-26 19-06-34](https://github.com/user-attachments/assets/8e0d2dcf-c2d7-4364-9436-dd521d222b32)

# PROGRAM:
```
#include <stdio.h>
#include<stdlib.h>
int main()
{ int pid; 
pid=fork(); 
if(pid == 0) 
{ printf("Iam child my pid is %d\n",getpid()); 
printf("My parent pid is:%d\n",getppid()); 
exit(0); } 
else{ 
printf("I am parent, my pid is %d\n",getpid()); 
sleep(100); 
exit(0);} 
}
```

# OUTPUT:

![Screenshot from 2025-04-26 19-20-17](https://github.com/user-attachments/assets/2bdf69bf-a63e-47d6-9b82-f1c5077bd193)

# PROGRAM:
```
#include <unistd.h>
#include <stdio.h>
#include <stdlib.h>
int main()
{
	printf("Running ps with execlp\n");
	execlp("ps", "ps", "ax", NULL);
	printf("Done.\n");
	exit(0);
}

```

# OUTPUT:

![Screenshot from 2025-04-26 19-28-21](https://github.com/user-attachments/assets/150b81fc-e098-4cc8-91ed-105ab7aebddb)



## C Program to print process ID and parent Process ID using Linux API system calls
















##OUTPUT














## C Program to create new process using Linux API system calls fork() and exit()













##OUTPUT








## C Program to execute Linux system commands using Linux API system calls exec() family


























##OUTPUT


















# RESULT:
The programs are executed successfully.
