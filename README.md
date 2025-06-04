in this commit I tested some git clean commands

at first I created some files and 2 empty dir:
	touch some_binar{1..3}.bin
	mkdir bin tmp

then I used the command:
	git clean -f -n 	# showing what would happen if we run the command without any consequences 
	git clean -f -d -n	# same thing as last one but includes deleting directories
	git clean -f -d 	# running the commands with all consequenses


in this commit as u see I renamed some file's name
I used this command:
	git mv [old name] [new name]
