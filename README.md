# Внедрение системы контроля версий

Демонстрация преимуществ использования системы контроля версий и сервиса GitHub.com

## Начало работы
* Перейти по ссылке https://github.com/on1ine/gitNT.git
* Скачать проект на локальный ПК по ссылке Download ZIP (Clone or download)

### Prerequisites

* Windows: https://git-scm.com/download/win
* Mac: https://git-scm.com/download/mac

## Установка и запуск

* Linux Debian/Ubuntu:
```html
apt-get install git
```
* Linux Fedora: 
```html
yum install git или dnf install git
```
Дождитесь окончания установки и введите команду:
```html
git --version
```
Если на экране отобразиться версия, то установка прошла успешно.

## Настройка 

Git хранит историю в привязке к имени пользователя и email.
Чтобы задать имя пользователя и email необходимо выполнить
следующие команды:
```html
git config --global user.name "Vasya Pupkin"
git config --global user.email vasya@localhost
```

### Редактор
Git использует по умолчанию редактор Vim (он достаточно тяжёл для
начинающих пользователей).
Мы можем задать редактор попроще (Nano) с помощью команды:
```html
git config --global core.editor nano
```

## Создание репозитория 
Репозиторий создаётся в конкретном каталоге с помощью команды:
```html
git init
Initialized empty Git repository in C:/project/.git/
```

## Добавление файлов
Git будет следить только за теми файлами, которые вы добавили в «список
отслеживаемых».
Cделать это можно с помощью команды:
```html
git add index.html
```
где index.html – это имя добавляемого файла.
* git add * добавит в список отслеживаемых файлов все файлы в текущем каталоге и подкаталогах;
* git add *.js добавит в список отслеживаемых файлов все файлы с расширением .js в текущем каталоге и подкаталогах.

## Текущий статут
Команда git status позволяет отследить текущий статус нашего репозитория:
```html
git status

On branch master
No commits yet
Changes to be committed:
(use "git rm --cached <file>..." to unstage)
new file: README.md
new file: css/style.css
new file: index.html
new file: js/app.js
```

## Фиксация изменений
1. Добавить файл в stage с помощью команды git add index.html
2. Закоммитить изменения с помощью команды git commit
```html
git commit -a -m "add index.html"
```
Флаг -a ( --all ) говорит о том, что мы добавляем в stage все удалённые/изменённые файлы (но не новые, новые нужно добавлять отдельно).

Флаг -m "Сообщение коммита" ( --message="Сообщение
коммита" ) позволяет не открывать редактор, а указывать сообщение
прямо в командной строке.

