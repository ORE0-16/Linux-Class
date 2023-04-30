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



Basic commands in Linux - 

[root@localhost~]#
root - login user
localhost - server name/host name
~ = home directory of user
# = shows root user


for local user

[jithu@localhost~]$

~ = will shows the present working directory(pwd) (wherever the folder we are shows by that part)

pwd = shows the full path ; if it is root pwd=/root ;for normal user pwd=/home/jithu
cd  = change directory ; cd documents = [root@localhostdocuments]#

command syntax

command option argument   = option means what option u need to do with that command ; argument = target file/folder name

ls -a Documents
cat -l
more -lh

-a = hidden files
-l = longlist

ls -lt = will list based on timestamp


1) ls - list the directories and files in your system.

2) ls -l = long listing which provide you entire list about the files and direcotry 
output of above command  - drw_r_x_r_x 2 root root 6 april 29 12:00 Documents
divided into 9 fields =  d|rw_r_x_r_x| 2 |root |root| 6 |april 29| 12:00 |Documents

d/- = indicates file /folder
d = folder/directory
- = file
l = link file(copy of the file)

rw_r_x_r_x = permission of the file

3 types of permssion

Read -r
Write -w
Execute  -x

rw_= user
r_x = group
r_x = others

2 = hard count
if is a file itshows the no of copies
if it is directory - it will show no of sub directories

root = created user

root = group

6 = size of the file or folder

Date
Time
File/directory name


3) ls -a   = to list the hidden files

4) ls -t   = list files and directories based on modified time

5) ls -r   = list in reverse order 

we can comibine ls and option commands together  =  ls -la



_-----------------------------------------

Day 3 - COmmands

---------------------------------------------

For reading files

cat - to view the content of the file  

more - it is like a book ,will show content page by page

less  - shows content from last page to first page

head  - #head -5/etc/password  = it will show first  5 lines

tail  - it will show last 5 lines.


**************************************************************

To switch between the users

su  - substitute user - to switch between users -

[root@hostexample~]# su jithu  = [jithu@hostexampleroot]$  = here the present working directory will be root folder to change that use su - jithu

su - jithu = [jithu@hostexample~]$       su - = login as root user

sudo = if we are logged in as normal user and we need the preveliage of root user 


******************************************************************

to see the user details , all the below commands show the login user details

w  = 

who = 

whoami

logname


*********************************************************************
To see the Kernel details

#uname -r  = shows the kernel version 

#uname -v = more details about the version

#uname -n
#hostname
#hostnamectl 

all above 3 will give the details of hostname

#tty = shows the terminal number


*********************************************************************

which  = find location   ; which cat = shows the path of cat command 

whereis = find location of original file,copies,manual page etc  ; whereis cat = gives original page and manual page

wc = word count - to find no of lines,no of words,no of characters  #wc etc/passerd   = 25 120 2300

wc -l = only no of lines
wc -w = only no of words
wc -m = only no of characters


man = man cat = will give the manual details 

history  = whaterver history we have done , will show the details of last 48 commands

!40 = will show you 40th command and its output

history -c = to clear the history
clear /Control L = to clear the page




*********************************************************************

Creation of files ; no special characters are allowed 

cat       =   used for create and read file ; to create a text file ; but we cant modify existing data ; we can add data -appending
              #cat>filename         ; 
              #cat>abcd (press enter)
              Welcome to redhat
              hello programming   (press enter)
              (press control + c) to come out of the file 
              
              if i again try to add one line to this file using the above steps the existing data will lost to avoid this we use apppending logic
              
              #cat>>abcd
              hi hello
              cntrl+C
              
              cat abcd
              Welcome to redhat
              hello prg
              hi hello
              
              cat>.hiddenfile   = to create hidden file 
              
                     

touch     =   used to create empty files ;we can modify timestamps ; multiple files ; we cannot pass data using touch
              #touch filename - to create new file
              
              #touch existingfile  = to modify that file timestamp  = ls -l = to verify the timestamp changes
              
              #touch a{5..9}  = will create multiple file with name a5,a6,a7,a8,a9
              
          

vi        = Visual editor ; modified version of vi is called VIM 

            #vi filename
            
            in vi we have 3 modes
              1) Command mode
              2) Insert mode
              3) Extended mode
              
            first mode will be command mode we can only edit using keyboard shortcuts 
            if you press I u can be in insert mode - where u can add data
            
            press esc + shift + : = will take you from insert mode to extended mode , in extended mode we can save and exit by giving :wq!
            
            pressing escape will take you to command mode first then by pressing shift+: it will take you to extended mode
            
         
         
 *******************************************************************************************************
 
 mdir     = to create folders
            #mkdir b{1..5}
            #mkdir .filename
            #mkdir maindirectory/subdirectory - to create sub folders 



copy       = #cp source destination      ; destination file data get overriden if there is existing data

move        = #mv source destination     ;   used to move data and renaming; if the destination file is not there the actual input file name gets change

delete      = #rm filename               ;
              #rm -d directory           ; to delete empty directory(dir without ny files)
              #rm -r directory           ; to delete dir with some data 
              
              
              
























































































































