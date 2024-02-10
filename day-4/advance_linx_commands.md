# Advance Linux Commands
### User Management
- ```cat /etc/passwd``` -> this command shows list of all users in system

    ![Alt text](image-2.png)

    The info about user is in specific format as:
    ```
    username : x : user id : user group id : : /home/username : /bin/bash 
    ```

- ```id <username>``` -> by using this command we can get id of user

    ![Alt text](image-3.png)

- ```sudo useradd -m <username>``` -> this will create user with mentioned username

    ![Alt text](image-4.png)

- ```passwd <username>``` -> this will set password of user 

    ![Alt text](image-5.png)

- ```sudo userdel -r <username>``` -> this command deletes mentioned user. If the user is part of a group then it will not be deleted directly, hence we will have to first remove him from the group and then we can delete him.

    ![Alt text](image-6.png)

### Group Management
- ```sudo groupadd <groupname>``` -> this will creates group with mentioned name

    ![Alt text](image-7.png)

- ```sudo usermod -G <groupname> <username>``` -> this command adds user to existing group

    ![Alt text](image-8.png)

    ***note: If we add a user to a group then it automatically gets removed from the previous groups, we can prevent this by the command given below***

- ```sudo usermod -G <groupname> <username>``` -> this command adds user to existing group without removing previous groups

    ![Alt text](image-9.png)

- ```sudo gpasswd -M <user1>, <user2> ... <group>``` -> To add multiple users to a group simultaneously, you can utilize the gpasswd command with the -M option. This command allows you to specify a list of usernames separated by commas.

    ***note: this will overwrite existing users in group***

### grep, find, awk commands
- grep command ```grep <options> pattern <files>```
    ```<options>```: These are command-line flags that modify the behavior of grep. 

    ```<pattern>```: This is the regular expression you want to search for. To know more about regular expresion [click here](https://www.geeksforgeeks.org/write-regular-expressions/).
    
    - case insensetive search

        ![Alt text](image-10.png)
    
    - Displaying the count of number of matches

        ![Alt text](image-11.png)

    - Display the file names that matches the pattern

        ![Alt text](image-12.png)
    
    - Checking for the whole words in a file

        ![Alt text](image-13.png)

    - Show line number while displaying the output using grep -n

        ![Alt text](image-14.png)
    
    - Matching the lines that start with a string

        ![Alt text](image-15.png)

    - Matching the lines that end with a string

        ![Alt text](image-16.png)

- find command

    ```find <path> <options> <expression>```

    path: Starting directory for the search.
    Example: find /path/to/search

    options: Additional settings or conditions for the search.
    Example: find /path/to/search -type f -name "*.txt"

    expression: Criteria for filtering and locating files.
    Example: find /path/to/search -type d -name "docs"

    - Find A Specific File
        
        in below example, it seeks "test.txt" within current folder

        ![Alt text](image-17.png)
    
    - Search Files with a Pattern Using

        In this case, it identifies files ending with ‘.txt’ within the current directory.

        ![Alt text](image-18.png)
    
    - Empty Files and Directories

        ![Alt text](image-19.png)
    
- awk command

    Consider following content of file employee.txt
    ```
    ajay manager account 45000
    sunil clerk account 25000
    varun manager sales 50000
    amit manager account 47000
    tarun peon sales 15000
    deepak clerk sales 23000
    sunil peon sales 13000
    satvik director purchase 80000
    ```

    - Default behavior of Awk: By default Awk prints every line of data from the specified file.

        ```awk '{print}' employee.txt```
    
    - Print the lines which match the given pattern.
        ![Alt text](image-20.png)
    
    - Printing specfic columns
        ![Alt text](image-21.png)

    - Display Line Number
        ![Alt text](image-22.png)

    - Display Line From specific line number to specific line number
        ![Alt text](image-23.png)

- file permission
    
    ```chmod <permisions> <file/directory>``` to change permissions of file/directory we can use command

    we can cahnge file permission's using to way one is using letters and other is using numbers (octal)

    - using letters
        
        - to give either read or write or execute permisson to user/group/other, following are the exapmles

            - ```chmod u+w <file/directory>``` -> this will append write permission to user for mentioned file/dir
            - ```chmod o+x <file/dirr>``` -> this will append execute permission to others for mentioned file/dir
            - ```chmod u+w,g+r,o+x <file/dir>``` -> this will append write permission to user, read permision to group and execute permission to others for mentioned file/dir
            - ```chmod o-x <file/dir>``` ->this will remove execute permission from user for mentioned file/dir
    
    - using numbers
        
        for numeric permission following table is required
        |Octal|Binary|Permissions|
        |:-:|:-:|:-:|
        |0|000|---|
        |1|001|--x|
        |2|010|-w-|
        |3|011|-wx|
        |4|100|r--|
        |5|101|r-x|
        |6|110|rw-|
        |7|111|rwx|

        in short, we can say value for 'r' is '4', value for 'w' is '2' and value for 'x' is '1', using sumation we can assign permissions

        - ```chmod 755 <file/dir>``` means
        user has all permissions i.e rwx: 4 + 2 + 1 = 7
        group has read and execute permissions not write i.e r-x: 4 + 1 = 5
        similar to others