# Writing shell scripts
A shell script is file containing a series of commands. the shell reads this file and carries out the commands as though they have been entered directly on the command line.

a shell script is a file that contains ascii text. To create a shell script, you need to use a text editor.

Use vi to use text editor, make sure to name your file after typing the vi command

	#!/bin/bash
	#My first script
	echo "Hello World!"
	
	vi filename, press i for insert text, esc to quit and :wq to quit completely.
	
	on mac you need to set permission as chmod 755 filename
	but apparently on window, it isnt necessary

You could ./hello_world but setting a path where all the files are stored in would be much more easily accessible. For example, all the commands are stored at $PATH. You could add your own path directory by the following

	Export PATH=$PATH:directory

Now you could type file name and run your first shell script without typing the directory.
