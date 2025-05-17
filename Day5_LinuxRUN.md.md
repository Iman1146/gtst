### Some advanced user commands
* `sudo passwd [username]` To change password of user
* `sudo usermod -u new_id username` To change user id
* `sudo userdel -r username` to delete
### Sudoers file
* The sudoers file is a file Linux and Unix administrators use to allocate system rights to system users.
* The user you created doesn’t have power to use original one.
* `sudo visudo`
* You can add the User you need to have access to the sudoers file, so he can use the sudo command.
### Linux File permission
* There is 5 main parts.
       - Permission 
       - Owners 
       - Date 
       - Size 
       - filename
#### Ownership
* Ownership is the owner of the file
* `chown user:group filename` to change ownership of a file
#### Permission
* There are 3 types of permissions. these are
      - Read ( r )
      - Write ( w ) 
      - Execute ( x )         
* The folders and files are differ with the ‘d’ and ‘-’ on the beginning of the permission.
* There still the permission have three parts.
* user -group-other 
* User ( u ) => power of user defined on the the ownership 
* Group (g )=> power of group defined on the the ownership 
* Other ( o ) => power of other users. 
* All ( a ) => power of all which can be found in the 3 above owners
* `chmod filename` to change permission of file
### CHMOD command
* This command helps to change file permission. 
* Those file permissions are read,write & execute. 
* Each of the permission have a number representations.
* Read -> 4 - r 
* Write -> 2 - w 
* Execute -> 1 - x
1. Parameters in symbol
* chmod a+x filename -> adding execute permission for all ( chmod
* chmod u+x filename -> adding execute permission for user 
* chmod g+x filename -> adding execute permission for group 
* chmod o+x filename -> adding execute permission for other
* chmod -x filename -> removing execute permission for all
* chmod a+rwx , u-rw , g-x , +x filename) o-xw filename -> gives rwx for all and removes something from all
2. Parameters in Number
* chmod 621 filename -> 6 for user, 2 for group, 1 for other ( 6 = 4+2 ), 6 =r w
* chmod 777 filename -> 7 for users, 7 for group , 7 for others (7 =4+2+1), 7 = rwx
### Special File Permissions
* There are another 3 special permissions, you may encounter on your pentest Journey. there are
         - SUID bits(s) - set user ID bit - add 4 infront of our numeric value -> 4000
         - SGID bits(S) - set group ID bit add 2 infront of our numeric value 2777 
         - Sticky bits(t) set other ID bit - add 1 in front of our numeric value -> 1602
* They are permissions like the execute(x), but they will set the execute permission to the user who settled them.
### Package installation on linux
* ON linux to install softwares you use package managers.
* On debian the package manager i called ‘APT’ also there is called ‘dpkg'
* Package managers are a free-software user interface that work with an online server to handle the installation and removal of software on Debian, and Debian-based Linux distributions.
### The repository
* This is the site/ server kali use to upload the packages
### Advanced package tool / apt /
* Apt is a free-software user interface that work with an online server to handle the installation and removal of software on Debian, and Debian-based Linux distributions.used for online and offline purpose.
* The old ‘apt’ used as ‘apt-get
```
sudo apt update 
sudo apt search
sudo apt install 
sudo apt remove 
sudo apt upgrade 
sudo apt purge
```
### Package dependencies
* A software can be built based on another program called ‘ modules’
* Those package managers install the software+dependencies
### Dpkg / Debian package manager /
* Dpkg is an offline package managing program.
```
sudo dpkg -i
sudo dpkg -r 
sudo dpkg -P
```
