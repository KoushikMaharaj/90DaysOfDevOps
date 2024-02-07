# Basic Linux Commands

### listing command
```ls <options> <arguments>``` -> list all sub directories and file in present directory

Examples:

- ``` ls -l ```--> list the files and directories in long list format with extra information
![Alt text](images/ls%20-l.png)

- ```ls -a ```--> list all including hidden files and directory
![Alt text](images/ls%20-a.png)

- ```ls *.sh``` --> list all the files having .sh extension.
![Alt text](images/ls%20*.sh.png)

- ```ls -i ``` --> list the files and directories with index numbers inodes
![Alt text](images/ls%20-i.png)

- ``` ls -d */``` --> list only directories.(we can also specify a pattern)
![Alt text](images/dir%20listing.png)

### Directory Commands
- ```pwd``` --> shows present working directory
![Alt text](images/pwd.png)

- ```cd path_to_directory``` --> change directory to the provided path
![Alt text](images/cd%20path_to_directory.png)

- ```cd ~ ``` or just  ```cd ``` --> change directory to the home directory
![Alt text](images/cd%20~.png)
![Alt text](images/cd.png)

- ``` cd - ``` --> Go to the last working directory.
![Alt text](images/cd%20-.png)

- ``` cd ..``` --> change directory to one step back.
![Alt text](images/cd%20...png)


- ``` cd ../..``` --> Change directory to 2 levels back.
![Alt text](images/go%20to%20back%202%20dir.png)

- ``` mkdir  directoryName``` --> to make a directory in a specific location
![Alt text](images/mkdir%20dirName.png)

- ``` mkdir .NewFolder ``` --> Make a hidden directory (also . before a file to make it hidden)
![Alt text](images/hiddenFolder.png)

- ```mkdir A B C D ``` --> Make multiple directories at the same time.
![Alt text](images/multiple%20directories.png)

- ```mkdir -p  E/F/G ``` --> Make a nested directory
![Alt text](images/nested%20directories.png)

### Copy Command
```cp <src path> <dest path>``` --> copy source files and directories to destination

### Move Command
- ```mv <src path> <dest path>``` --> copy source files to destination

- ```mv <old file> <new file with new name>``` --> rename the file