# Типы конфигурации Git
* Локальная `.git\config`
* Глобальная `\Users\USERNAME\\.gitconfig`
* Системная `\Program Files\Git\etc\gitconfig`
# Опции команды git config
* --local `git config example` или `git config --local example`
* --global `git config --global example`
* --system `git config --system example`
## Задаём имя пользователя
`git config --global user.name "Ваше имя или никнейм"`
## Задаём электронную почту пользователя
`git config --global user.email "Ваша почта"`
## Задаём параметр отвечающий за окончания строк
`git config --system core.safecrlf warn`

Eсли что-то пойдёт не так во время подготовки к замене CRLF на LF.
* `true` Git отменит операцию, если не будет возможности откатить изменения назад из LF в CRLF.
* `warn` Git выдаст предупреждение, но не отменит операцию.
## Задаём параметр исправляющий вывод кириллицы
`git config --system core.quotepath off`

Исправление вывода кириллицы после использования команды `git status`
## Просматриваем заданные параметры с помощью команды git config
Чтобы просмотреть глобальный конфигурационный файл `git config --list --global`

* `--global` — позволяет обратиться к глобальной конфигурации
* `--list` — выводит список всех параметров из конфигурационного файла

Есть опция `--show-origin`, которая выводит дополнительно путь до конфигурационного файла  
`git config --list --global --show-origin`

Зачастую команду используют без указания конфигурационного файла `git config --list --show-origin`
