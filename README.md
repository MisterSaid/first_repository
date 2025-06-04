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

in this commit as u see I changed nothing, but I tasted the command:
	git diff
and
	git diff HEAD

the first one shows us a changes between our's last commit and our's untracked files
the last one shows us a changes between our's last commit and our's staged files

params of that's command:
	--cached / --staged
	--word-diff


it would be grammar correct using this command:
	git commit --amend --no-edit
if u fixed problem from the last commit that made ur app unworking 
