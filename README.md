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
3) ls -l /  = to see the content inside / root folders
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
              
              
              
*****************************************************************************************************************

Day 5 - 

Partition in oracle virtul box

/= 20GB
/boot= 500 MB
swap = 8GB


USER and GROUP adminstrator.

USER -
UID - user identification number for users, but the system identifies these users by number 

        0 - root
        1-199= system users - system who uses the system
        200-999 = reserved id 
        1000-60,000 = normal user
        
        
Configuration files - maninly used to storefiles
      
      /etc/passwd = it will store user information
      /etcshadow =   it will store user password information
      /etc/group =   it will store group information
      /etc/gshadow=   it will store group password
      /etc/login.defs = to save the login default files
      /etc/skel = to save the login default files 


cat

/etc/passwd -
jithu:x:1000:1000:jithu:/home/jithu:/bin/bash

jithu - root user
x - password
1000- uid
1000 - gid
jithu - comments
/home - home directory 
/bin/bash  - shell

cat/etc/shadow -

jithu:xyxyxyxx:0:99999:7:::

jithu - root
xyxyxyxx- encrypted passwd
0 - minimm days of password
99999 - max days u can use the password
7 - before 7 days of expiring u ll get start getting reminder mails

cat/etc/group

jithu:x:1000:

jithu- grp name
x- group passrd
1000- gid
4th byte - no of members

cat /etc/gshadow

jithu:!::

jithu- group name
! - password
3rd - grp admin are there or not
4th - no of users

cat /etc/login.defs



User admin -
Group admin -



*************************************************************************************************************************

Day 6 


USER ADMINSTRATION -mainly covers 3 commands

	useradd		- used to add new users
	usermod		- used to modify
	userdel  	- used to dellete
	
useradd - #useradd oreo
			how to check the user is being created -  cat /etc/passwd  or ls -l /home
		
		2-to give password as root user for oreo
		#passwd oreo
		3- to give password from oreo account
		#passwd 
		
usermod - #usermod oreo
		1 -                      #usermod -u newuid	username
				                 #usermod -u 4567 oreo = change uid oforeo to 4567
				
		2 - to change home directory
				                 #usermod -d /new/directoty username  - eventhough u change the directory the home drectpry entry will be present in home
		3- for locking the user  #usermod -L username
		   for unlocking         #usermod -U username 
		4- for modifying shell
								 #usermod -s /bin/sh username 
		5 - to rename user
								 #usermod -l newname/oldname 
								 
		
userdel 			
		#userdel jithu   - jithu will deleted but home entry will present 
		#userdel -r username - this will delete completely
		
	
	

GROUP ADMINSTRATION

	1 - #groupadd groupname   			- to add new group  - cat /etc/group 
	2 - #groupmod -g GID groupname  	- to change the group id
	3 - #groupmod -n newname oldna  	- to change the group name
	4 - #groups user /#groups user1,2,3 - to list user groups name
	5 - #groupdel groupname 			- to delete the group
	
	
PASSWORD AGING INFORMATION

to see the passwd aging information of a user  - #chage -l jithu  - will show you default passwd details

to change that  - #chage jithu   - give values

PERMISSIONS 

1)Basic permission
2)Special permission
3)ACL   = access control list


BASIC PERMISSION  -


we have 3 permissions  - Read Write Execute

Read 	 	- r	- 4	(octa value)
Write		- w	- 2
Execute		- x	- 1

rw-r--r--

we have 3 ownerships

user(u)  - rw-
group(g) - r--
others(o) - r--

user /group/others means the user who created the file/folder, to which group it belongs, outsider can access or not


Default permissions=  basic permision - Umask

umask value for root user = 0022
umask value for nor user  = 0002

/etc/bashrc & /etc/profile will contains the information about the umask value 

0022/0002 - 1st byte we can ignore =022/002

max permision for files and folders

file :666(rw-rw-rw-)				folders :777(rwxrwxrwx)

--- 0
--x 1
-w- 2
-wx 3
r-- 4
rw- 6
r-x 5
rwx 7

for files the content will be text and dont need to execute access .

below shown are the calculation for the default permissin for files and folders under root and normal users


for root

file    666-
		022
		----
		644  = rw-r--r--
		
folder 	777-
		022
		----
		755		= rwxr-xr-x
		

for normal

file 	666-
		002
		----
		664			= rw-rw-r--
		
folder
		777-
		002
		----
		775			= rwxrwxr-x
		
		
for changing the default permission value we can use the command chmod

#chmod whom what which file/folder


whom = user/group/others
what = +,-,=
which = r,w,x
file /folder

chmod u+w a1   - will give the user execute acccess only for user

chmod a+w a1  -  will give execute access to user,group and others in  a single command

chmod a=x a1  - will give only execute access to user grp and others 

also we can use octa values like

chmod 123 a1   - will give --x-w--wx



------------------------------------------------------------------------------------------------------------------------------------

Day 7

Special Permissions

3 types of special permissions

1 - SET UID		= giving same permissions to multiple users  -check permission in ls -l /bin/passwd in root = u can see rwrs - s implies 
					ex helping us to change password at any time 
					how to add S mode  = chmod u + s /bin/passwd
					
2 - SET GID		= same as above ,difference is this is for groups ,by default the group name will be root now if i rename the group name to
					jaba and create a file/dir inside jaba, the group name of that file/dir will shown as root only not jaba
					to make it jaba we use SET GID
					
					chmod g+s 
					
3 - Sticky bit	=  official used social blogers, like everyone has the access ,but we cant have access to edit or update the file/folder




The first byte of UMASK 0000 is given to Special permission


ACL - Access control list permissions

The owner can give permisions to particular user called ACL

chmod 755 /home/*  - we are giving the access to all users

try above command in root user
login to one user create a file 
login to another user and try to access the above file from that user home directory - u can see the file ; but u cannot edit the file

setfacl -m u:oreo:rw:ac11   (user:whatpermission:filename)  - here we are giving read write access to oreo user on the file ac11 created under aj home dir

if u want to delete the permission switch to main user = setfacl -b ac11
getfacl filename  = shows who all other users have access to this file



YUM = yellow dog update modifier 


used to install the packages


rpm - package management in redhat 

yum to install and update packages and rpm for verification

all packages are inside repository 


we have 2 repository

AppStream(all traditional packages) and BaseOs(core OS packages)  = these all are together called modules


yum install nfs-utils  = before that we need to do one time setup chose iso file frm optical device then type below commnad

mount /dev/cdrom /media
df -h = to veriy
now we need to install somesetup (jaba)








	





	
	
	





              
              
























































































































