# Linux-Class
Linux is an open source OS.
oS is an interpretor between Hardware and user.

Components of OS -

Kernel- Core of OS ;Manage all services,application input output etc
  Windows - NT kernel
  Linux - VM Linuz
  
Shell- is an interpreter where we executes commands.
  different types of shell 
    Bourne shell
    C shell
    K shell
    T shell 
    BASH - Bourne again shell (defult shell)

scripting in linux is called Bash scripting.


File System- how they arrange the files  in a systematical arrangement is called file system.
   We have 4 different file system
   ext2 -
   ext3 -
   ext4 -
   xfs -  default 

Linux was introduced by Linux thorvalds in 1992 named as Linux 1.0 GNU 

Features-

OPen source
Securtiy - it is only having text files,firewall,SElinux(security enhanced linux).
Multi users - we can login as 6 different user and do different task.CNTL + ALT + F2-F6 (to create profile , CNTL + ALT + F1 gives GUI ; CNTL + ALT + F2-F6 gives CLI
Multi tasking - logined users can do different task at a time
Stability - 
Good hardware support - hardware support , plug and play
Portabilty - easy to  store the linx os
Good GUI -

Red hat  Linux  = Project based work
Ubuntu = study purpose
Carl Linux = cyber security
CentOS =

Certifications -

RHCSA Red hat certified system adminstrator
RHCE   Red hat certified engineer



DAY 2

Virtual box intro

Install oracle virtual box 6.1 and redhatlnuxpackage

2 tpes of linux ystem

Media Based - GUI and CLI

Network based - Kickstart and PXE(pre boot execution environment)


How the process happening in Virtual box

Background process - we will be loading the kernel (VM linux) -- load to initramfs(initial ram file system) -- 

Foreground process - start configuration 

Installer - Anaconda will stored all the files into /root/anaconda-ks.cfg

File names are called here as Directory Hierarchy structure .

Main directory is called root(/) which is having 25 sub folders which stores the commands, functions and kernel details

/bin    -(binary)               - all the commands will be stored                            2 types of users = adminstrator(root) and normal
/sbin   -(superbin)              -have all adminstrative user commands
/etc    -(editable text config)  -stores all the configuration files
/home   -                        -where we store all the resources of the normal user
/root   -                        -for root users to store the resource
/boot   -                        -stores booting files and linux kernel
/dev    - (device)               -contain device information if any devices connected
/var    -(variables)             - all the trouble shooting files,log files,mail queries
/usr    -                        - to store the details of linux operating system, save operational files of linux
/mnt    -
/media  -                           both mnt and media used as mount point  (for floppy and USB)
/proc   -(processing)            - stores the information  of system processing
/opt    -(optional)               - if u install any third party softwares that informaton will store here
/tmp    -(temp files)             -
/sys    -                         -stores system information
/lib    -(library)                -contains system libraries
/srv    -(services)               -contain services information
/run                              -will show active device information

lost + found = it is a file used to repair the system by itself


root= 13
boot = 500mb
swap= 8gb

remaining 11 gb we can use for partition.






















