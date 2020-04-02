# ssh-editor
This is a shell project that edits your remote files using your desktop editor

# Setup
Please setup sshkey autentication before using this tool.

You can edit the line
```
export EDITOR=
```
in file [setupenv.sh](setupenv.sh) to specify your desktop editor. Otherwise, the default sublime editor is used. 

Add the current path to the environment variable. 
```sh
. ./setupenv.sh
```

# Command options
This navigates to the folder of you specified.
```sh
cd   <your-dir>  
```

Itemize files in the current directory, for the use of the download and upload commands.
```sh
list
```

This downloads the file to your local computer and edit using your specified editor.
```sh
download <file-name> 
```

Edit the file using your specified editor if this file is downloaded to your local computer.
```sh
edit <file-name> 
```

List all local files not synchronized with remote. 
```sh
status
```

This uploads/overwrites the file to the remote server.
```sh
upload  <file-name> 
```

Exit the shell.
```sh
exit 
```

List all local files not synchronized with remote.
```sh
status
```

All linux commands are supported.

# Example 
Execute the shell by
```sh
% sshEditor yourname@remotehost
```

In the shell, you can
```
/home/yulinshi/$ mkdir test # make a directory in remote
/home/yulinshi/$ cd test # navigate in the folders
/home/yulinshi/$ touch hello # create a file in remote
/home/yulinshi/$ download hello # download the file to local and edit
/home/yulinshi/$ edit hello # edit the local file
/home/yulinshi/$ status
-- Files not uploaded to remote server:
   /home/yulinshi/test/hello
-- Type "yes" to upload all local files to remote: no
/home/yulinshi/$ upload hello # upload the file to remote
/home/yulinshi/test/$ cat hello # show the modified file in remote
World, how are you?
```

# Limitations
The sshkey is the only authentication method supported currently. 
