# Terminal cheatsheet

## `cd` - Change Directory

| Command       |                                               |
| ------------- | --------------------------------------------- |
| `cd`          | Home directory                                |
| `cd [folder]` | Change directory, e.g. cd Documents           |
| `cd ~`        | Home directory                                |
| `cd /`        | Root of the drive                             |
| `cd -`        | Previous directory or folder you last browsed |
| `cd ..`       | Move up to the parent directory               |
| `cd ../..`    | Move up two levels                            |

## `pwd` - Print working directory

| Command |                             |
| ------- | --------------------------- |
| `pwd`   | Show your working directory |

## `ls` - List Directory Contents

| Command   |                                                                                                                                                      |
| --------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ls`      | Display the name of files and subdirectories in the directory                                                                                        |
| `ls -C`   | Force multi-column output of the listing                                                                                                             |
| `ls -a`   | List all entries including those with .(period) and ..(double period)                                                                                |
| `ls -1`   | Output the list of files in one entry per line format                                                                                                |
| `ls -F`   | Display a / (slash) immediately after each path that is a directory, \* (asterisk) after executable programs or scripts, and @ after a symbolic link |
| `ls -S`   | Sort files or entries by size                                                                                                                        |
| `ls -l`   | List in a long format. Includes file mode, owner and group name, date and time file was modified, pathname, and more                                 |
| `ls -l /` | List of the file system from root with symbolic links                                                                                                |
| `ls -lt`  | List the files sorted by time modified (most recent first)                                                                                           |
| `ls -lh`  | Long listing with human readable file sizes in KB, MB, or GB                                                                                         |
| `ls -lo`  | List the file names with size, owner, and flags                                                                                                      |
| `ls -la`  | List detailed directory contents, including hidden files                                                                                             |

## `less` - Output

| Command            |                                                                                          |
| ------------------ | ---------------------------------------------------------------------------------------- |
| `less <file name>` | Output the contents of the file using the less command that supports pagination and more |

## `touch` - Create file

| Command             |                                         |
| ------------------- | --------------------------------------- |
| `touch <file name>` | Create a new file without any extension |

## `mkdir` - Create folder

| Command                      |                                              |
| ---------------------------- | -------------------------------------------- |
| `mkdir <dir>`                | Create new folder named `<dir>`              |
| `mkdir -p <dir>/<dir>`       | Create nested folders                        |
| `mkdir <dir1> <dir2> <dir3>` | Create several folders at once               |
| `mkdir "<dir>"`              | Create a folder with a space in the filename |

## `cp` - Copy

| Command                                  |                                                                    |
| ---------------------------------------- | ------------------------------------------------------------------ |
| `cp <file> <dir>`                        | Copy a file to the folder                                          |
| `cp <file> <newfile>`                    | Copy a file to the current folder                                  |
| `cp <file>~/<dir>/<newfile>`             | Copy a file to the folder and rename the copied file               |
| `cp -R <dir> <"new dir">`                | Copy a folder to a new folder with spaces in the filename          |
| `cp -i <file><dir>`                      | Prompts you before copying a file with a warning overwrite message |
| `cp <file1> <file2> <file3>/Users/<dir>` | Copy multiple files to a folder                                    |

## `mv` - Move

| Command                   |                                                                     |
| ------------------------- | ------------------------------------------------------------------- |
| `mv <file> <newfilename>` | Move/rename                                                         |
| `mv <file> <dir>`         | Move a file to the folder, possibly by overwriting an existing file |
| `mv -i <file> <dir>`      | Optional -i flag to warn you before overwriting the file            |
| `mv *.png ~/<dir>`        | Move all PNG files from current folder to a different folder        |

## `rm` - Remove

| Command                      |                                                                      |
| ---------------------------- | -------------------------------------------------------------------- |
| `rm <file>`                  | Delete a file (This deletes the file permanently; use with caution.) |
| `rm -i <file>`               | Delete a file only when you give confirmation                        |
| `rm -f <file>`               | Force removal without confirmation                                   |
| `rm <file1> <file2> <file3>` | Delete multiple files without any confirmation                       |

## `man` - Manual

| Command         |                                     |
| --------------- | ----------------------------------- |
| `man [command]` | Show the help manual of the command |
| `[command] -h`  | Get help about a command            |
