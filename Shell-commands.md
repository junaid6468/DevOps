BASIC SHELL COMMANDS

date  ==> #checking date 
pwd ==> #checking current directory
ls ==> #listing files in directory
cd ==> #changing directory
mkdir directory_name ==> #creating a directory
ls -l ==> gives details about the file
touch file_name ==> to create a new file 
rm file_name ==> to remove a file 
rm -r directory_name ==> to remove a directory
rmdir directory_name ==> used to remove empty directories
clear ==> used to clear terminal
cat filename ==> used to read the content inside the file
echo ==> used to print on console
echo "data to be printed" > filename ==> prints the given data in a new or existing file (this command overwites the existing data)
echo "data to be printed" >> filename ==> append the data in new line
zcat ==> used to read zip files
head filename ==> used to print top 5 lines from the file
tail filename ==> used to print last 5 lines from the file
tail -f filename ==> used to monitor the file continously if any new logs are added inside it
more file_name ==> for quick access of a file
less file_name ==> for detailed access of a file

ADVANCE SHELL COMMANDS

cp sourcefile destinationdr ==> copy the file in the directory
mv sourcefile destination ==> moves the file in the directory also used for renaming
wc filename ==> gives content details of file like number of words e.t.c. \\ wc can be done for multiple files
#soft-link
ln -s path_of_file soft_link_file_name ==> creates a softlink file which is shortcut of the file given in path and this can be altered once created it is deleted once main file is deleted
#hard-link
ln path_of_file hard_link-file_name ==> create a hardlink file which is shortcut of the file give in the path and cannot be altered once created it remains as it is even if the actual file is deleted
cut -b 1-n file_name ==> gives specific bytes of file as per requirement
#tee
echo "content" | tee file_name ==> used to print the content both on display and in the newfile
sort filename ==> sorts the lines in file in alphabetical order
diff file1 file2  ==> to check the difference between the files
vi filename ==> opens file in vi editor

USER MANAGEMENT

useradd - creates a use
adduser - creates a user with home directory
Cat /etc/passwd - to check if a user is created
passwd user_name - setup a password for the mentioned user
Cat /etc/gshadow - to check if password is setup(encrypted password can be seen)
userdel - deletes an user 
su - user_name - switch user

Difference between useradd and adduser?
useradd is simple way of creating a user without asking much information -- useful in shell scripting
adduser takes a good amount of data about the user.

Can we restore a forgotten password?
Though we can get an encrypted password but we cannot get the actual password it is near to impossible to restore.


chage -M 90 username - 90(days) used to set policies like to change the password for every 90 days in this case

passwd -l username - used to lock a user account
passwd -u username - used to unlock a user account 
usermod -l new_username old_user_name - changes username

GROUPS:

groupadd name - used to create a group
cat /etc/group - used to check the creation of the group
usermod -aG group_name user_name - used to add user the a group

 FILE PERMISSIONS:

 R - read W - write X - execute
Chmod u=rwx filename - permission to user
Chmod o=rwx filename - permission to others
Chmod g=rwx filename - permissions to group

Chmod 777 filename 

Same for directories or folder

Chown owner:creator filename - changes to the desired owner


PROCESS MANAGEMENT 

VIEWING:

ps - used to view the running processes by current user

ps aux - used to view all the processes of all users

ps aux | nl or ps aux | wc -l - to get the count of the running processes

ps -ef - same use but does not shows the cpu and memory utilisation


KILLING:

kill pid - kills a process

kill -9 pid - force kills the process

kill -STOP pid - stops the process temporarily 

kill -CONT pid - resumes the stopped process


Priority and de-priority:

Renice -n 10 -p pid -> it goes from -19 to 20.... -19 refers to high priority and 20 refers to low priority 

MONITORING 

top - used to get realtime data about all processes

htop - same info as top but in a more good visual representation

vmstat - reports the system performance

Free -m - gives static info about memory usage 

Free -h - gives static info in a human readable format

nproc - gives number of cpus available 

df -h - to check the disk space

du -sh * - disk utilisation folder by folder

iostat - display CPU and disk I/O statistics
