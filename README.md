# LR6
## __Лабораторная работа №6__
### __Система контроля версий__
_Цель лабораторной работы_: изучение базовых возможностей системы управления версиями, опыт работы с Git Api, опыт работы с локальным и удаленным репозиторием.

# Ход выполнения лабораторной работы
> Скриншоты лабораторной работы находятся в папке screenshots, каждый из них имеет название, соответствующее номеру пункта, выполнение которого необходимо подкрепить этим самым скриншотом. Например, скриншот для пункта 1 соответственно имеет название _1.PNG_
## Пункт 1
Необходимо создать аккаунт на сайте GitHub (_см. [рис. 1](https://github.com/VladykaM/LR6/blob/Report/screenshots/6.1.jpg)_). 
## Пункт 2
Далее при помощи Fork создается копия [репозитория лабораторной работы](https://github.com/Kurtyanik/LR6/) в личное хранилище (_см. [рис. 2](https://github.com/VladykaM/LR6/blob/Report/screenshots/6.2.jpg)_).
## Пункт 3
Соглано лабораторной работе, необходимо установить Git (_см. [рис. 3](https://github.com/VladykaM/LR6/blob/Report/screenshots/6.3.jpg)_).
## Пункт 4
Далее с помощью _git config --global user_name_ и _git config --global user_email_ был настроен клиент git (_см. [рис. 4](https://github.com/VladykaM/LR6/blob/Report/screenshots/6.4.jpg)_).
## Пункт 5
Затем на диске С в папке infa была создана копия своего личного удалённого репозитория на компьютер (_см. [рис. 5](https://github.com/VladykaM/LR6/blob/Report/screenshots/6.5.jpg)_).
## Пункт 6
Теперь нужно добавить файл через интерфейс GitHub и подтянуть изменения в локальный репозиторий. На скриншоте 6 (_см. [рис. 6](https://github.com/VladykaM/LR6/blob/Report/screenshots/6.6.jpg)_) представлены файлы, находящиеся в локальном репозитории, до обновленния данных и после. Их поиск осуществляется командой _ls -1_, а обновление информации - _git pull_.
## Пункты 7, 8
Далее необходимо получить историю операций для веток и просмотреть последние изменения. Первое осуществлялось с помощью команды _git reflog branch_name_, а второе - с помощью _log_ (_см. [рис. 7, 8](https://github.com/VladykaM/LR6/blob/Report/screenshots/6.7-8.jpg)_).
## Пункт 9
Затем нужно выполнить слияние в ветку master. С помощью команды _git merge branch_name_ ветки _master_ и _branch1_ были объединены (содержимое branch1 появилось в ветке master, _см. [рис. 9](https://github.com/VladykaM/LR6/blob/Report/screenshots/6.9.jpg)_).
## Пункт 10
Теперь необходимо удалить побочную ветку. Для этого была использована команда _git branch -d branch_name_ (_см. [рис. 10](https://github.com/VladykaM/LR6/blob/Report/screenshots/6.10.jpg)_).
## Пункт 11
Для наглядной работы с репозиторием необходимо сделать изменения и зафиксировать их, оставляя комментарии. Поочередно в репозиторий были добавлены три текстовых файла: asd.txt, wasd.txt, qwerty.txt, созданные командой _echo "text" >> name.txt_. Извенения фиксировались командой _git add_, для создания коммита - _git commit -m "text"_, для обновления информации в репозитории - _git push_ (_см. [рис. 11.1](https://github.com/VladykaM/LR6/blob/Report/screenshots/6.11-1.jpg); [рис. 11.2](https://github.com/VladykaM/LR6/blob/Report/screenshots/6.11-2.jpg); [рис. 11.3](https://github.com/VladykaM/LR6/blob/Report/screenshots/6.11-3.jpg)_).
## Пункт 12
С помощью _git revert HEAD --no-edit_ был осуществлен откат коммита (_см. [рис. 12](https://github.com/VladykaM/LR6/blob/Report/screenshots/6.12.jpg)_).

# Лог команд
git config --global user.name "4315 Владыкин М. В."

git config --global user.email "Vladykin.m05@gmail.com"

cd /c/infa

git clone https://github.com/VladykaM/LR6

ls -1

git pull

ls -1

git reflog

git log

git checkout branch1

ls -1

git checkout master

ls -1

git merge branch1

ls -1

git branch -d branch1

git push origin --delete branch1

git commit -m "Удалена побочная ветка"

echo "MJ is GOAT" >> wasd.txt

git add wasd.txt

git status

git commit -m "Добавлен первый файл"

echo "LJ is not GOAT" >> asd.txt

git add asd.txt

git status

git commit -m "Добавлен второй файл"

echo "Belov is Russian GOAT" >> qwerty.txt

git add qwerty.txt

git status

git commit -m "Добавлен третий файл"

git push

git revert HEAD --no-edit

git commit -m "Откат коммита"

git push


# История операций
С помощью команды _git log --pretty=format:"%h - %ad - %an: %s" --date=short_ была получена история операций в укороченном виде.

976edb8 - 2024-11-18 - 4315 Владыкин М.В.: Папка скриншотов

15ab872 - 2024-11-17 - 4315 Владыкин М.В.: Revert "Создан третий файл"

0e0a125 - 2024-11-17 - 4315 Владыкин М.В.: Создан третий файл

cd8b85d - 2024-11-17 - 4315 Владыкин М.В.: Создан второй файл

4df0c43 - 2024-11-17 - 4315 Владыкин М.В.: Создан первый файл

22e0426 - 2024-11-17 - 4315 Владыкин М.В.: Разрешен конфликт

b8d9b84 - 2024-11-17 - VladykaM: Create abc.txt

e36fd3a - 2024-11-17 - VladykaM: Create misha

921f53b - 2020-11-21 - Kurtyanik: Обновление информации

0f9f50d - 2020-11-21 - Kurtyanik: Заполнил файл

c08a654 - 2020-11-21 - Kurtyanik: Файл создан пустым

3c6e913 - 2020-11-21 - Kurtyanik: Initial commit
