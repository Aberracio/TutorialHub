# Инструкция для работы с Git и удалёнными репозиториями

## Что такое Git?
Git - это одна из реализаций распределённых систем контроля версий, имеющая как и локальные, так и удалённые репозитории. Является самой популярной реализацией систем контроля версий в мире.

## Подготовка репозитория
Для создание репозитория необходимо выполнить команду *git init*  в папке с репозиторием и у Вас создаться репозиторий (появится скрытая папка .git)

## Создание коммитов

### Git add
Для добавления измений в коммит используется команда *git add*. Чтобы использовать команду *git add* напишите *git add <имя файла>*

### Просмотр состояния репозитория
Для того, чтобы посмотреть состояние репозитория используется команда *git status*. Для этого необходимо в папке с репозиторием написать *git status*, и Вы увидите были ли измения в файлах, или их не было.

### Создание коммитов
Для того, чтобы создать коммит(сохранение) необходимо выполнить команду *git commit*. Выполняется она так: *git commit -m "<сообщение к коммиту>*. Все файлы для коммита должны быть *ДОБАВЛЕНЫ* и сообщение к коммиту писать *ОБЯЗАТЕЛЬНО*.

## Журнал изменений
Для того, чтобы перемещаться между коммитами, используется команда *git checkout*. Используется она в папке с репозиторием следующим образом: *git checkout <номер коммита>*.

## Перемещение между сохранениями
Для того, чтобы перемещаться между коммитами, используется команда *git checkout*. Используется она в папке с пепозиторием следующим образом: *git checkout <номер коммита>*

## Ветки в Git

## Создание ветки

Для того, чтобы создать ветку, используется команда *git branch*. Делается это следующим образом в папке с репозиторием: *git branch <название новой ветки>*

## Слияние веток
Для того, чтобы добавить ветку в текущую ветку, используется команда *git merge <name branch>*

### Вернуться к актуальному состоянию и продолжить работу
Для того, чтобы вернуться к актуальному состоянию, используется команда *git checkout master*.

### Увидеть разницу между текущим и закоммиченным файлом
Для того, чтобы увидеть разницу, используется команда *git diff*.

# Синтаксис языка Markdown

Справочник по Markdown от Microsoft: https://docs.microsoft.com/ru-ru/contribute/markdown-reference

✦ # Заголовок – выделение заголовков. Количество символов “#” задаёт уровень заголовка (поддерживается 6 уровней).

✦ = или - – подчёркиванием этими символами (не менее 3 подряд) выделяют заголовки первого (“=”) и второго (“-”) уровней.

✦ ** Полужирное начертание** или __ Полужирное начертание__

✦ * Курсивное начертание * или _ Курсивное начертание _

✦ *** Полужирное курсивное начертание ***

✦ ~~ Зачёркнутый текст ~~

✦ * Строка – ненумерованные списки, символ “*” в начале строки

✦ 1, 2, 3 ... – нумерованные списки

# Как работает Git

Если посмотреть на картинку, то становится чуть проще с пониманием. Каждый кружок, это commit. Стрелочки показывают направление, из какого commit сделан следующий. Например C3 сделан из С2 и т. д. Все эти commit находятся в ветке под названием main. Это основная ветка, чаще всего ее называют master . Прямоугольник main* показывает в каком commit мы сейчас находимся, проще говоря указатель.

![image](https://habrastorage.org/getpro/habr/upload_files/81d/ab6/de0/81dab6de02b4179fc1bc8c119dfce9ca)

В итоге получается очень простой граф, состоящий из одной ветки (main) и четырех commit. Все это может превратиться в более сложный граф, состоящий из нескольких веток, которые сливаются в одну.

![image](https://habrastorage.org/getpro/habr/upload_files/137/e03/4ea/137e034eadd3c4459a734354a029fb1a)

Клонирование существующего репозитория: git clone

Если проект уже настроен в центральном репозитории, наиболее распространенным способом создать его локальный клон является команда clone. Клонирование, как и команда git init, обычно выполняется один раз. Получив рабочую копию, разработчик в дальнейшем выполняет все операции контроля версий из своего локального репозитория.

Команду git clone выполняют для создания копии (клонирования) удаленного репозитория. В качестве параметра в команду git clone передается URL-адрес репозитория. Git поддерживает несколько различных сетевых протоколов и соответствующих форматов URL-адресов. В этом примере используется SSH-протокол Git. URL-адреса SSH в Git имеют следующий шаблон: git@HOSTNAME:USERNAME/REPONAME.git

Ниже приведены значения шаблонных параметров:

HOSTNAME: bitbucket.org

USERNAME: rhyolight

REPONAME: javascript-data-store

После исполнения команды последние версии файлов из главной ветки удаленного репозитория будут загружены и помещены в новый каталог. Имя нового каталога будет соответствовать параметру REPONAME. В данном случае это javascript-data-store. В каталоге будет вся история удаленного репозитория и только что созданная главная ветка.

Дополнительную информацию об использовании команды git clone и поддерживаемых форматах URL-адресов в Git см. на странице git clone: https://www.atlassian.com/ru/git/tutorials/setting-up-a-repository/git-clone 

Команды: git pull - стягиваем с github, git push - отправляем на github