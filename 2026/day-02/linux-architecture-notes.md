## rocWhat is Linux ?

It is a open source project created by Linus Torwalds, It has distributions/flavours For Example: CentOS, Ubuntu, RHOS, P.S. MacOS is UNIX

## WHY Linux ?

Majority of the servers are in Linux, the primary reason is because it is free and easy to use, Around 90%; Security is high and can be multiuser

## HOW Linux ?

![Architecture of Linux Operating System - LinuxSimply](https://linuxsimply.com/wp-content/uploads/2023/11/architecture.png)

Linux Has this A.S.K architechture where A is Applications, S is Shell, K is Kernel. Kernel is the heart of the linux. Which actually has the code written by Linus which is in C. Kernel is someone which talks to the H/W. Kernel has pre-compiled binaries of this C Programs. One Layer above is the Shell which is the CLI (Command Line Interface) where we can interact with the Kernel using the commands For Example. ls, mkdir, pwd, etc. So the flow goes like this lets just saye the user fires the echo command on the shell and goes to kernel, kernel has this binaries store for the echo  which are 010101 for example. the last layer is the Application layer which is mostly the GUI (Graphical user interface), Terminal is an Application

Application(GUI)  Shell(CLI) Kernel(Binaries) H/W

### What is the role of Kernel in system being started?

When user starts up the machine it i goes to BIOS, and BIOS fires up the Bootloader which knows where systemd is.

### What is systemd ?

Systemd has another name alled as init, it has the PID 1 the 'd' in systemd stands for daemon which generally means the Background process. Systemd is the process that starts another process like dockerd. sshd. SystemD in simple terms is an orchestrator/conductor of your machine it handles starting and stopping of the services, like WIFI, firewalls and many other services

Rules of Linux:

1. Everything in linux is Process
2. Everything in linux starts wih '/'
3. Everything in linux is file OR directory

## What are process ?

Process is simply a program that is running in your system, when you execute a command the system simply creates a process for it. Each process has a uniques PID (Process Id) and this ID is used by the system to uniqley identify the process, we can use ps command to list the process and ps -f to view the full information. Mainly there are two types of how process runs ?

1. Background process -> Runs in Background; Doesnt block the terminal, we can start the bckground process by simply adding the '&' at the end
2. Foreground process -> Blocks the terminal until finished.

### Types of process

1. [ ] Parent & Child Process -> Every process in linux is created by the parent process, Every new created process is a child process, most process have shell as there parent process
2. [ ] Zombie & Orphan Process -> When a child process finishes its execution it sends SIGCHILD signal to the parent process informing that it has compleleted the execution. when the parent process terminates before the child process finished the child becomes an orphan process. orphan process are adopted by PID 1 process. Zombie process are the ones which has finished the execution but still remains in the process table because parent process has not read there exit status
3. [ ] Daemon process -> These are the the background system process which continously provides services
