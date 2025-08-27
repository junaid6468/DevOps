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



