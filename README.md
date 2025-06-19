<a id="readme-top">boo! scared?</a>

<details>
	<summary>Table of contest</summary>
	<ol>
		<li>
			<a href="#about-the-project">About The Project</a>
			<ul>
				<li><a href="#built-with"></a></li>
			</ul>
		</li>
		<li>
			<a href="#getting-started">Getting Started</a>
			<ul>
				<li><a href="#prerequisites">Prerequisites</a></li>
				<li><a href="#installation">Installation</a></li>
			</ul>
		</li>
		<li><a href="#usage">Usage</a></li>
		<li><a href="#roadmap">Roadmap</a></li>
		<li><a href="#contributing">Contributing</a></li>
		<li><a href="#license">License</a></li>
		<li><a href="#contact">Contact</a></li>
		<li><a href="#acknowledgments">Acknowledgments</a></li>
	</ol>
</details>


## In this commit I tested some git clean commands

__at first__ I created some files and 2 empty dir:
```sh
touch some_binar{1..3}.bin
mkdir bin tmp
```

then I used the command:
	git clean -f -n 	# showing what would happen if we run the command without any consequences 
	git clean -f -d -n	# same thing as last one but includes deleting directories
	git clean -f -d 	# running the commands with all consequenses


## renamed some file's name

used command:
```sh
git mv [old name] [new name]
```

***

<p align="right"> <a href="#readme-top">back to top</a> </p>

changed nothing, but tasted `git diff` and `git diff HEAD` command:

the first one shows us a changes between our's last commit and our's untracked files
the last one shows us a changes between our's last commit and our's staged files

params of that's command:
- --cached / --staged
- --word-diff


it would be grammar correct using this command:
```sh
git commit --amend --no-edit
```

if u fixed problem from the last commit that made ur app unworking 


```sh
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
```

***

<p align="right"> <a href="#readme-top">back to top</a> </p>


```sh
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
```


### Полезные опции для git log --pretty=format

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

***

<p align="right"> <a href="#readme-top">back to top</a> </p>

```sh
# вывод reference log
# отображает только локальную историю
git reflog

# перемещение в другой репозиторий и вывод аналогичной информации о нем
cd ../hellogitworld
pwd
git reflog

# Сценарий использования: Восстановление удаленного коммита
# 
git reflog
git log --oneline
git reset --hard HEAD~1
git log --oneline
git reflog
git reset --hard 10f7044
git log –oneline

# Сценарий использования: Удаление старых записей
# 
git reflog
git reflog expire --expire=7.days --all --verbose
git reflog

git reflog expire --expire=1.minutes --all –-verbose
git reflog

# запуск сборщика мусора Git
git gc
```

***
<p align="right"> <a href="#readme-top">back to top</a> </p>

git add -f [filename] # forced adding file in index

***

## Testing markup

### Lines

___
---
***

### escape character

/******

### quotes

> "In my imagination ur mom said my son would be named as she said so ur name is said" - somebody said

## unnumeral list
- apple
- banana
- etc

### numeral list:
1. one
2. two
3. why am I doing it?
4. stop it
5. I am doing it for the reason I am shecking markup language in README

### authors link
* <https://stepik.org/lesson/1726518/step/2?unit=1750282>
* [source](https://stepik.org/lesson/1726518/step/2?unit=1750282)
* [source](https://stepik.org/lesson/1726518/step/2?unit=1750282 "click here to see where I took theory for my practise")
* <a href="#readme-top">click here</a>

<p align="right"> <a href="#readme-top">back to top</a> </p>

### PICTURES

* ![image sample](https://i.pinimg.com/736x/82/e8/b5/82e8b5506791f1a90e3049ddf6cf1ec4.jpg)
* [![image sample](https://i.pinimg.com/736x/82/e8/b5/82e8b5506791f1a90e3049ddf6cf1ec4.jpg)](https://poki.com/ru/g/under-the-red-sky)

### ROADMAP

- [ ] know how to make README.md file
- [x] practice ur knowleges
- [ ] should we have fun in studying?
	- [X] No
	- [ ] Yeas

### Tables

|NAME     |URL                                                    |LOGO| 
|:-|:-:|-:|
|Django   |https://docs.djangoproject.com/en/5.2/topics/http/urls/|<img src="https://i.pinimg.com/originals/4a/97/41/4a97418dae84b5064a2f720a98646376.jpg" width=50>| 
|React    |https://react.dev/                                     |<img src="https://avatars.mds.yandex.net/i?id=950e19c6750b6bf3f43ed914ca807af9_l-4383860-images-thumbs&n=13" width=50>|

### comments

<!-- comment 1 -->
[comment]: # (comment 2)
[//]: # (comment 2)

### emoji

- :smile:

