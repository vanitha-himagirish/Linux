
## Linux
Popular version of UNIX OS. Linux is the best-known and most-used open source operating system.

#### Components of Linux:
1. Kernel  - It is the core part of Linux and responsible for all major activities of OS. It provides abstraction to hide low level hardware details to system or application programs.
2. System Libraries - Special function or programs using which we can access kernel’s features.
3. System Utility – Responsible for specialized, individual level tasks

#### Kernel mode vs User mode
1. Kernel mode – Privileged mode with full access to all resources of computer.
2. User mode – has no access to system hardware and kernel code. User programs/utilities uses System libraries to access kernel function

#### Important features of Linux
- Portable
- Opensource
- Multiuser
- Multiprogramming – Multiple applications can be run at the same time
- Hierarchical File system
- Shell 

#### Architechture of Linux
- Hardware Layer
- Kernel - core component and it interacts directly with the hardware.
- Shell - It is an interface to kernel hiding complexity of kernel's functions from users.
- Utilities - Provides users most of the functionalities of OS

#### Terminal
- Command Line or terminal is a text based interface to the system
- Terminal is just a mechanism to transfer information. 

#### Shell
- For the operating system to understand the information, a shell is needed.
- A shell in Linux is a program that interprets the commands you enter in a terminal window, so the operating system can understand what you want to do.
- There are many shell programs, such as Bash, Zsh, Csh, Ksh etc.
- Bash is the default shell on most Linux distributions. When you open a terminal window, a Bash shell is automatically started.
- To check which shell you are using now, run the following command.

#### Paths
1. Absolute path - Specifies a loation in relation to root directory. Always they begin with / .
2. Relative path - It is the relation to where we are currently in the system and will not begin with /.

Some of the common notations used :
- ~(tilde) - Shortcut to home directory
- .(dot) - Reference to the current directory
- ..(dot dot) - Reference to parent directory

#### Virtual Machines
- Typically called an image
- It behaves like an actual computer
- Runs in a window much like any other program
- The physical computer is typically called the “host” and the VMs are referred to as the “guests”.

#### Hypervisor
- is computer software, firmware or hardware that creates and runs virtual machines
- A hypervisor, also known as a virtual machine monitor or VMM, is software that creates and runs virtual machines (VMs).
- A hypervisor allows one host computer to support multiple guest VMs by virtually sharing its resources, such as memory and processing. 
- There are two main hypervisor types, referred to as “Type 1” (or “bare metal”) and “Type 2” (or “hosted”). A type 1 hypervisor acts like a lightweight operating system and runs directly on the host’s hardware, while a type 2 hypervisor runs as a software layer on an operating system, like other computer programs. 




            
