# Lab Report 1

# cd with nothing
![Image](cd_none.png)

Working directory: user@sahara ~
The tilde(~) signifies that this is the home directory.
No change, because there was no directory provided.

# cd with directory

![cd_directory](cd_directory.png)
Working directory before: user@sahara ~
working directory after: user@sahara ~/lecture1/messages

This changed folders to the subfolder messages, which is stored in the folder lecture1.
The leftmost folder name 'lecture1' is the enclosing folder, 'messages' is the folder inside 'lecture1'
Providing a directory is important when trying to access files in enclosing folders.

# cd with file
![Image](cd_text.png)

Working directory: ~/lecture1/messages
Even though the file exists, it is not possible to cd into a file.
It's not possible to cd into a file, because the file name is not a directory.
This is why the system returns an error message.
