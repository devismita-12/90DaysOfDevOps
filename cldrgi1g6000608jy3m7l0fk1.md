# Day 6 Task

### **File Permissions**

File Permissions describe the allowed operations by various users. Concerning file permissions, all users are categorized into the following 4 types.

User Categories: user/owner -Represented by 'u'

group: Represented by 'g'

others: Represented by 'o'

all: Represented by 'a'

## Permission Types:

* r: Read
    
* w: Write
    
* x: Execute
    

## Operations related to permissions:

We can perform the following 3 operations.

1. \+ -&gt;Add particular permission to user|group|other|all
    
2. \- -&gt;Remove a particular permission to user|group|other|all
    
3. \= -&gt;Assignment a particular permission to user|group|other|all
    

### chmod Command:

chmod means change mode.

We can use chmod command to change file or directory permissions.

Syntax: $ chmod &lt;user\_category&gt; file\_name/directory\_name

For user add execute permission, for group add write permission, for others remove read permission $ chmod u+x,g+w,o -r demo.txt

Only owner and super user (root) can change file permissions.

### How to check Permissions of existing File:

By using the ls -l command:

\-rw-rw-r-- 1 ubuntu ubuntu 0 Feb 5 13:41 file1.txt

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675360826331/dd1b6d29-c489-4a25-87c4-dc80abe99b74.png align="center")

Total 9 permissions. The first 3 are user permissions, the next 3 are group permissions and the next 3 are others permissions.

user permissions: rw - user can perform both read and write operations but not execute operation

group permissions: r w- group members can perform only read operation and cannot perform write and execute operations

others permissions: r -- other members can perform only read operation and cannot perform write and execute operations.

User Permissions + Group Permission ns + Others Permissions order is important

Read permission + Write Permission + Execute Permission order is important

E g 1: $ chmod u+x demo.txt adding execute permission to the user

E g 2: $ chmod u+w,g+rw,o+r demo.txt adding write permission to the user adding read and write permissions to the group adding read permission to the others

E g 3: $chmod u+x,g-w,o+w demo.txt adding execute permission to the user removing write permission from the group adding write permission to the others

E g 4: $ chmod u=rw,g=rw,o=r demo.txt

Now user permissions: rw

group permission: rw

others permission: r--

E g 5: $ chmod a=- demo.txt

Now user permissions: ---

group permission: ---

others permission: ---

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675604858566/caab4c20-af56-40bb-82c5-7ba4b975672e.jpeg align="center")

### chown Command:

chown means change owner.  
The only root user can perform this activity.

### **chgrp command:**

chgrp means change group.

The only root user can perform this activity.

**What is ACL?**  
Access control list (ACL) provides an additional, more flexible permission mechanism for file systems. It is designed to assist with UNIX file permissions. ACL allows you to give permissions for any user or group to any disc resource.

Think of a scenario in which a particular user is not a member of the group created by you but still you want to give some read or write access, how can you do it without making the user a member of the group, here comes in picture Access Control Lists, ACL helps us to do this trick.

ACLs are used to make a flexible permission mechanism in Linux. From Linux man pages, ACLs are used to define more fine-grained discretionary access rights for files and directories.

**setfacl** and **getfacl** are used for setting up ACL and showing ACL respectively.

```plaintext
getfacl test/declarations.h
```

  
getfacl file1.txt

file: file1.txt

owner: ubuntu

group: ubuntu

user::rw-

group::rw-

other::r--

**List of commands for setting up ACL :**

```plaintext
1) To add permission for user
setfacl -m "u:user:permissions" /path/to/file

2) To add permissions for a group
setfacl -m "g:group:permissions" /path/to/file 

3) To allow all files or directories to inherit ACL entries from the directory it is within
setfacl -dm "entry" /path/to/dir

4) To remove a specific entry
setfacl -x "entry" /path/to/file

5) To remove all entries
setfacl -b path/to/file
```