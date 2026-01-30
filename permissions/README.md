# ALU Shell Scripts - Permissions

This directory contains scripts for learning Linux file permissions, ownership, and user management.

## Scripts Description

### 0-iam_betty
Switches the current user to the user `betty`. Uses the `su` command.

### 1-who_am_i
Prints the effective username of the current user.

### 2-groups
Prints all the groups the current user is part of.

### 3-new_owner
Changes the owner of the file `hello` to the user `betty`.

### 4-empty
Creates an empty file called `hello`.

### 5-execute
Adds execute permission to the owner of the file `hello`.

### 6-multiple_permissions
Adds execute permission to the owner and the group owner, and read permission to other users, to the file `hello`.

### 7-everybody
Adds execution permission to the owner, the group owner and the other users, to the file `hello`.

### 8-James_Bond
Sets the permission to the file `hello` as follows:
- Owner: no permission at all
- Group: no permission at all  
- Other users: all the permissions

### 9-John_Doe
Sets the mode of the file `hello` to: `-rwxr-x-wx`

### 10-mirror_permissions
Sets the mode of the file `hello` the same as `olleh`'s mode.

### 11-directories_permissions
Adds execute permission to all subdirectories of the current directory for the owner, the group owner and all other users. Regular files are not changed.

### 12-directory_permissions
Creates a directory called `my_dir` with permissions 751 in the working directory.

### 13-change_group
Changes the group owner to `school` for the file `hello`.

### 14-change_owner_and_group
Changes the owner to `vincent` and the group owner to `staff` for all the files and directories in the working directory.

### 15-symbolic_link_permissions
Changes the owner and the group owner of `_hello` (a symbolic link) to `vincent` and `staff` respectively.

### 16-if_only
Changes the owner of the file `hello` to `vincent` only if it is owned by the user `guillaume`.

## Requirements
- All scripts are exactly two lines long
- All files end with a new line
- First line of all files is `#!/bin/bash`
- No use of backticks, `&&`, `||`, or `;`
- All files are executable
- Tested on Ubuntu 20.04 LTS

## Usage
```bash
# Make scripts executable (if not already)
chmod u+x script_name

# Run any script
./script_name

