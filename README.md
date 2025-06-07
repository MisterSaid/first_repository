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

"
	# вызов локальной справки по команде git diff
	git diff --help

	# вывод изменений после последнего коммита (не добавленных в индекс)
	git diff

	# вывод изменений после последнего коммита (включая добавленные в индекс)
	git diff HEAD
	
	# вывод изменений, добавленных в индекс
	git diff --staged
	git diff --cached
	
	# фоматирование изменений по словам (а не по строкам)
	git diff --word-diff
	
	# исключение пустых строк из вывода
	git diff -w
	
	# вывод изменений после HEAD~1 (и до HEAD)
	git diff HEAD~1
	
	
	# указание хэша коммита для вывода изменений после него
	git diff 8a8b14c
	
	# вывод разницы между двумя указанными коммитами
	git diff 8a8b14c b0272be
	
	# вывод изменений в конкретном файле после указанного коммита
	git diff HEAD~1 web_pages/index.html

	# сравнение двух произвольных файлов (даже вне git-репозитория)
	git diff index.html page2.html

	# вызов локальной справки по команде git difftool
	git difftool --help

	# указание хэша коммита для вывода изменений после него с помощью утилиты difftool
	git difftool 8a8b14c
"


