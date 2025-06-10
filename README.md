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


____________________________________________________________________
# вывод статистики по коммитам
git log --stat	

# просмотр патчей (делалей каждого изменения) по коммитам
git log -p

# ограничение количества комитов в выводе
git log -4

# опции можно сочетать в одной команде
git log –-stat -p
git log -4 --stat -p

# отображение веток в истории коммитов
git log --graph

git log --oneline README.txt
git log --stat	
git log --graph

# фильтр коммитов по автору
git log --author="Jordan McCullough" –-oneline

# форматирование: дата, автор, время, сообщение
git log -5 --pretty=format:"%h - %an - %as - %s"
git log -5 --pretty=format:"%h - %an - %as %n >> %s"

# читабельное предложение с помощью форматирования
git log --pretty=format:"This guy:%cn committed with hash '%h' on %cd"


# компактный отчёт о коммитах в репозитории группирует коммиты по авторам и выводит список их имён вместе с количеством сделанных ими коммитов и краткими описаниями этих коммитов
git shortlog

# показывает электронную почту автора рядом с его именем
git shortlog -e

# сортирует вывод по количеству коммитов, от большего к меньшему
git shortlog -n

# выводит только статистику (количество коммитов) без списка сообщений коммитов
git shortlog -s

# фильтрация коммитов по датам "до" и "после"
git shortlog --since="2012-01-01" --until="2012-12-31"



Полезные опции для git log --pretty=format

Опция	Описания вывода
%H	Хеш коммита

%h	Сокращённый хеш коммита

%T	Хеш дерева

%t	Сокращённый хеш дерева

%P	Хеш родителей

%p	Сокращённый хеш родителей

%an	Имя автора

%ae	Электронная почта автора

%ad	Дата автора (формат даты можно задать опцией --date=option)

%ar	Относительная дата автора

%cn	Имя коммитера

%ce	Электронная почта коммитера

%cd	Дата коммитера

%cr	Относительная дата коммитера

%s	Содержание

____________________________________________________________________

