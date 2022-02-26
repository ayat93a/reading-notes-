## **Terminal operation**
###   The Command Line
- What is it?
The command line, or the terminal, is a Character User Interface (CUI), it is a text-based system where You can type commands by the keyboard.
The command line typically presents you with a prompt. 
- how does it work?
When you type your command and press enter to run your command the output will appear. Most commands produce output and it will be listed straight under the issuing of the command and there are another commands that  just perform their task and don't display any information unless there was an error. ls is an example of commands that have an output while git add . is an example of the commandes that doesnot have an output unless there is an error occured.
- how do I get to one?
in my os , Windows, the terminal is Windows PowerShell

### Basic Navigation
there is a list of navigation commands to navigate through the directorires and determine the working location.
1. Print Working Directory (pwd).
 tells me what my current working directory is. As you're moving around, it can be easy to lose track of where you are at which maybe sometimes lead you to clone some repo for example or make some edit in the wrong directory.
2. list (ls).
 for me i prefer use ls to check if i am in the right directory ,speacially when i change directory by cd command, scince it can come with arguments.
 **ls -l return to you with a long list output, the list indicates if each the file is normal file or directory , the size of each one and the date of the last modification.
**/etc used to not to list our current directory but instead to list that directories contents.
3. Path.
**Absolute paths specify a location (file or directory) in relation to the root directory. You can identify them easily as they always begin with a forward slash ( / )
**Relative paths specify a location (file or directory) in relation to where we currently are in the system. They will not begin with a slash.
** ~ This is a shortcut for your home directory. eg, if your home directory is /home/ryan then you could refer to the directory Documents with the path /home/ryan/Documents or ~/Documents
 my device path : / ==> /home ==>  ~
 cd . ==> your currently directory
 cd .. ==> parent directory
4. shourtcuts 
i prefer to use the upper arrow to navigate command from the history commands and to usw tab to auto completation of the directory name.

### More About Files.
1. Theories about linux system 
2. everything is file
3. extensionless system
the system actually ignores the extension and looks inside the file to determine what type of file it is.it can sometimes be hard to know for certain what type of file a particular file is. there is a command called file which we can use to find this out.
3. Linux is Case Sensitive
4. Spaces in names
Spaces in file and directory names are valid but we need to be a little careful with them. to change directory to directory with name that have a space you must use Quotes or escape characters with a backslash ( \ ).
4. Hidden Files and Directories
If the file or directory's name begins with a . (full stop) then it is considered to be hidden.
To make a file or directory hidden all you need to do is create the file or directory with it's name beginning with a . or rename it to be as such. Likewise you may rename a hidden file to remove the . and it will become unhidden.
to show the hidden files use ls -a command.

### Manual Pages.
The manual pages are a set of pages that explain every command available on your system including what they do, the specifics of how you run them and what command line arguments they accept.
- to  invoke the manual page ==>  man
- to search on the Manual pages ==> man -k <search>

### File Manipulation
1. Making a Directory ==> mkdir
 mkdir -p ==> tells mkdir to make parent directories as needed
 mkdir -v ==> makes mkdir tell us what it is doing
2. Removing a Directory ==> rmdir 
a directory must be empty before it may be removed 
also rmdir support -p and -v
3. Creating a Blank File ==> touch
create a file automatically if we refer to it and it does not exist. 
4. Copying a File or Directory ==> cp
5. Moving a File or Directory ==>  mv 
6. Renaming Files and Directories ==> mv
provide a new name for the file or directory and as part of the move it will also renamed.
7. Removing a File (and non empty Directories) ==> rm 
if not empty ==> rm -r