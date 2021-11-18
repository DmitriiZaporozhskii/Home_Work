# Home_Work
Дополнить файл с инструкцией по работе с git и направить pull request в этот репозиторий. Файл с инструкцией необходимо дополнить информацией о работе с удаленными репозиториями.

# pull request 
1. *делаем форк (fork)интересуещего  нас репозитория*
2. *мы делаем git clone для нашей версии этого репозитория*
3. *мы создаем ветку с предлагаемыми изменениями*
4. *производим все изменения только в этой ветке*
5. *отправляем эти изменения на свой аккаунт* *git push*
6. *в окно на github появляется возможность отправить (pull request)*
## Работа с удаленным репозиторием

1. **создали аккаунт на github/com**
2. **создать локальный репозиторий**
3. **"подружить" ваш локальный и удаленный репозиторий .github при создании нового репозитория поскажет как это можно сделать)**
4. **отправить (push) ваш локальный репозиторий в удаленный на(Github)
,при этом вам,возможно,нужно будет авторизоваться на удаленном репозитор**
5. **провести изменение "с другого компьютера ".**
6. **Выкачать  *git pull* актуальное состояние из удаленного репозитория.**


# Что такое git
*Это система версий.Она помагает сделать сохранение ваших файлов.помогает работать в команде через создание новых веток для каждой отдельной задачи.*

# Подготовка репозитория
*Настройка имени и почты:*

* git config user.name
* git config user.email

*Инициализация репозитория:*
* git init

# Создание <сохранений>
*Для того чтобы добавить файлы к комиту:*
* git add file_name

*для добавления всех файлов к комиту*
* git add .

*Для того, чтобы зафиксировать изменение нужно прописать :*

* git commit -m "some info about commit (Некоторая информация о комите)"

*Если мы хотим добавить к комиту все файлы:*
* git commit -a -m "some info about coomit"


# Проверка состояния репозитория 
*Команды:*
* git status

     Выводит информацию о состояние нашего репозитория(т.е. о файлах которые были изменены)
* gir diff

   Показывает разницgiу между текущими изменениями и теми что закомичены 
       
* git show 
  Показывет каие изменения зафиксированны в последнем комите
* git show branch
  показывает какие изменения зафиксированный в комите с кодом branch_code(его можно найти в git log) 

# Перемещение между сохранениями
При помощи команды rebase вы можете взять все изменения, которые попали в коммиты на одной из веток, и повторить их на другой.
 * git checkout 
 *Позваляет перейти к другой версии коммите*

* git rebase
*Способ интегрировать изменения из одной ветки в другую*

*  git rebase --abort
 *Отменить процесс rebase набрав в консоли*

# Журнал изменений
* git log
*Показывает все внесенные изменения* 
* git log --graph
*Древовидный вид комитов*

* git log --stat
*Выводим список коммитов и показываем статистику по каждому*

*Поиск коммитов по всем веткам*
__git log --all --grep='< given-text >'__

# Ветки в git
 *Показывает все ветки:*
 * git branch
 
 *Создание новой ветки:*
 * git branch branch_name

 *Переход между ветками:*
 * git checkout branch_name

# Слияние веток и решение конфликтов
* git merge branch_name

    Добавить информацию из ветки branch_name в текущию ветку
    *конфликт веток решается с помощью ручного изменения файла и комита с этими изменениями*
# Удаление веток
*Команда branch c тегом -d удалить ветку с именем branch_name:*
* git branch -d branche_name
# Справка
*Вызывается с помощью тега --help*
* git log --help
* git commit --help


# Инструкция по работе с гитом

1.Настройка имени и почты:
* git config user.name
* git config user.email
2.Инициализация репозитория:
* git init
3.Работа с репозиторием:
* изменение файлов и добавление через git add
* Фиксирования изменений в файлах через git commit
* Проверка состояния репозитория  через git log и git diff
# Начальные команды

 ## git init
 *Инициализирует  локальный репозиторий*

## git add 
*Добавляет наши файлы для отслеживания изменений*

Нужно прописать название файла:
**git add file_name**

Можно добавить все файлы:
**git add .**

## git commit 

*Фиксирует изменения файлов*

Вызов(перед использование нужнофайлы с помощью add):
**git commit -m "commit info"**
 
 Вызов(все измененные файлы будут закомичены):
**git commit -a -m"commit info"**

Отмена коммита, создание нового коммита:
**git revert <commit-ish>**


 ## git checkout

*Позваляет перейти к другой версии коммите*

*Вернуться к первоначальному состоянию:*
**git checkout master**

*Быстры переход к предыдущей ветви*
**git checkout -**

*Создание новой ветки без истории*
**git checkout --orphan <branch_name>**

## git diff

*Посмотреть разницу между текущими файлами и теми что закомичены*

*Изменения, выполненные для коммита*
**git diff --cached**

## git log
*Показывает все внесенные изменения*

*Поиск коммитов по всем веткам*
__git log --all --grep='< given-text >'__

## git status 
*Показывает состояние репозитория*
## git branch
*Показывает на какой ветке находимся*
 
 *Создание новой ветки:*
 **git branch name**
 
 *Удаление ветви*
 **git branch -d name**

 *Все ветки, которые уже соединены с веткой master*
**git branch --merged master**

## git marge name
*Слияние ветвей*

## git help 
*Полезные руководства по git*