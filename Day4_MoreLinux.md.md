### Linux File Hierarchy
- Linux/UNIX have a special file system than windows.
- File system is a directory structure that the OS uses.
### System Files
* System Files are files used by the system software( OS )
* **Windows**: System files appear under the local disk C:
* **Linux**: System files appear under the directory ( /)
### File structure in detail
1. / ( root )
* Every single file and directory starts from the root directory
* The only root user has the right to write under this directory
* /root is the root user’s home directory, which is not the same as /
2. bin - Binary executables
* Essential command binaries that need to be available in single-user mode; for all users.
 example 
`cat ls cp pwd`
3. /boot - Boot loader files
* Kernel initrd, vmlinux, grub f iles are located under /boot
4. /dev - Essential Device files
* These include terminal devices, usb, or any device attached to the system.
5. /etc - et cetera
* Contains configuration files required by all programs. ○ This also contains startup and shutdown shell scripts used to start/stop individual programs
6. /home - Home directory
* Home directories for all users to store their personal files.
7. /lib - Libraries essential for the binaries in /bin & /sbin
* Library filenames are either ld* or lib*.so.*
8. /media - Mount points for removable media such as CD-ROMs
* Temporary mount directory for removable devices
* Examples, /media/cdrom for CD-ROM; /media/floppy for floppy drives; /media/cd recorder for CD writer.
9. /mnt - Temporarily mounted file
* Temporary mount directory where sysadmins can mount filesystems
10. /opt - Optional application software packages
* Contains add-on applications from individual vendors. ○ Add-on applications should be installed under either /opt/ or /opt/ sub-directory.
11. /sbin - Essential system binaries
* Just like /bin, /sbin also contains binary executables. ○ The linux commands located under this directory are used typically by system administrator, for system maintenance purpose.
12. /tmp - Temporary Files
* Directory that contains temporary files created by system and users. ○ Files under this directory are deleted when system is rebooted.
13. /usr - User Utilities
* Contains binaries, libraries, documentation, and source-code for second level programs
* /usr/bin contains binary files for user programs. If you can’t find a user binary under /bin, look under /usr/bin. For example: at, awk, cc, less, sc
#### Text Editor
*Linux command line text editors
* VIM
* Nano
* Emacs
* Neovim
#### Linux Graphical Text editors
* Sublime
* Vs code
* Gedit
* Pluma
### VIM
* Before vi the primary editor used on Unix was the line editor
* User was able to see/edit only one line of the text at a time
* a very powerful
* It is hard to learn, specially for windows users
* Command mode -> where you can do command
* Input mode -> where you can write
` vim [yourfile]`
* insert mode `i`
* `:w` save
* `:q` quit
* `:wq!` save and quit   ! force
* `:u` undo
### Nano
* The GNU nano text editor is a user-friendly, free and open-source text editor that usually comes pre-installed in modern Linux systems.
* Ctrl + S - save 
* Alt + U - Undo the ^ is equal to ‘Ctrl’
* Alt + E - Redo
* Ctrl + X - Exit
* Ctrl+shift+C - copy
* Ctrl+shift+X - Cut
* Ctrl+shift+V - Paste
### Linux User Management
* On Computer system, person who uses the computer is called “ user” ● Every Users have Group.
* Users have their own file & applications.
* To know our name on linux -> “ whoami “
* Those users have power/privilege. 
* On linux there's 2 kinds users.
* Root id = 0 
* Normal User id start with 1-999
* if users want to have a root access they add **sudo** in front of the command
* `sudo[yourcommand]`
* **sudo** used to pass permission denied
### Creating Users
* Useradd -> simple
* Adduser -> Detailed
```
sudo useradd[username]
sudo adduser[username]
```
* The User files are stored inside **/etc/passwd**
* When you create a user it creates a group with that name.
* `sudo su` to access root user