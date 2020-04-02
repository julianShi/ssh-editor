# ssh-editor
This is a shell project that edits your remote files using your desktop editor

# Setup
Add the current path to the environment variable
```sh
. ./setupenv.sh
```

# Command options
This navigates to the folder of you specified.
```sh
cd   <your-dir>  
```

This downloads the file to your local computer and edit using your specified editor.
```sh
edit <file-name> 
```

This uploads/overwrites the file to the remote server.
```sh
add  <file-name> 
```

Exit the shell.
```sh
exit 
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
/home/yulinshi/$ edit hello # download the file to local and edit
/home/yulinshi/$ add hello # upload the file to remote
/home/yulinshi/test/$ cat hello # show the modified file in remote
World, how are you?
```
