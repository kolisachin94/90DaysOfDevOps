The core components of Linux (kernel, user space, init/systemd):

Linux Kerenel:
- The kernel is the core of the operating system.
- It manages hardware, memory, processes, and system resources.
- It provides a bridge between applications and the underlying hardware.

User Space
- User space contains everything that runs outside the kernel.
- It includes shells, applications, libraries, and system utilities.
- Programs in user space interact with the kernel through system calls.
- It’s where users actually run and control software.

Init System (systemd)
- The init system is the first process started by the kernel.
- It initializes the system and launches essential services.
- systemd manages service startup, logging, and system states.
- It controls shutdown, reboot, and overall service supervision.

How processes are created and managed:
Process creation and management in Linux revolves around several key concepts and system calls such as fork, exec, wait, init/systemd, and signals.

A process is a program in execution.
Every process has:

PID (Process ID)
PPID (Parent Process ID)
State (running, sleeping, stopped, zombie)
Memory space
CPU scheduling information

Linux mainly uses two system calls to create processes:
(A) fork() – Create a Copy of the Parent
(B) exec() – Replace Process Image.
(C) vfork()
(D) clone() 

Process Management in Linux:
 (A) Process Scheduler
Linux uses CFS (Completely Fair Scheduler).
It determines:
- which process gets CPU
- for how long
- process priority (nice value)

(B) Signals – For Process Control
Signals are software interrupts.
Common ones:

SIGKILL (9) → immediately kills process
SIGTERM (15) → request to terminate
SIGSTOP → pause
SIGCONT → resume

Use commands:
kill -9 PID
kill -15 PID

(C) Process States
View using:
ps -aux
top
htop

What systemd does and why it matters:

init/systemd – The First Process- The first process created during boot has PID 1.
Old systems used: init
Modern systems use: systemd
It Starts system services, Manages daemons, Manages user sessions

List 5 commands you would use daily:
- Commands that we used on daily basis are:
- 1- ls
- 2- df -h
- 3- mkdir.
- 4- Touch
- 5- Vi Editor.
