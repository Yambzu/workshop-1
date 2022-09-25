# workshop

## Соответствие групп и тем на практикум.

1. Что такое система контроля версий
2. Для чего нужна система контроля версий
3. Установка git на ваш ПК (в зависимости от системы)
4. Установка VSCode на ваш ПК
5. Что такое репозиторий и инструкция по созданию локальных репозиториев.
6. Базовая работа с локальным репозиторием
7. Что такое ветки и для чего они нужны при работе с системой контроля версий.
8. Базовая работа с ветками в git.
9. Что такое удаленный репозиторий и для чего он нужен
10. Базовая работа с удаленными репозиториями GitHub
11. Как строится и для чего нужна совместная работа в системах контроля версий
12. Инструкция по созданию pull request
13. Книги и полезные ссылки по изучению git.
14. Альтернативные системы контроля версий.


## Базовая работа с ветками в git (КОМАНДЫ)

* git branch                 # показать список веток
* git branch -v              # показать список веток и последний коммит в каждой
* git branch new_branch      # создать новую ветку с указанным именем на текущем коммите
* git branch new_branch 5589877 # создать новую ветку с указанным именем на указанном коммите
* git branch -f master 5589877  # переместить ветку master на указанный коммит
* git branch -f master master~2 # переместить ветку master на 2 коммита назад
* git checkout new_branch    # перейти в указанную ветку
* git checkout -b new_branch # создать новую ветку с указанным именем и перейти в неё
* git checkout -B master 5589877 # переместить ветку с указанным именем на указанный коммит и перейти в неё
* git merge hotfix           # влить в ветку, в которой находимся, данные из ветки hotfix
* git merge hotfix -m "Горячая правка" # влить в ветку, в которой находимся, данные из ветки hotfix (указано сообщение коммита слияния)
* git merge hotfix --log     # влить в ветку, в которой находимся, данные из ветки hotfix, показать редактор описания коммита, добавить в него сообщения вливаемых коммитов
* git merge hotfix --no-ff   # влить в ветку, в которой находимся, данные из ветки hotfix, запретить простой сдвиг указателя, изменения из hotfix «останутся» в ней, а в активной ветке появится только коммит слияния
* git branch -d hotfix       # удалить ветку hotfix (используется, если её изменения уже влиты в главную ветку)
* git branch --merged        # показать ветки, уже слитые с активной
* git branch --no-merged     # показать ветки, не слитые с активной
* git branch -a              # показать все имеющиеся ветки (в т.ч. на удаленных репозиториях)
* git branch -m old_branch_name new_branch_name # переименовать локально ветку old_branch_name в new_branch_name
* git branch -m new_branch_name # переименовать локально ТЕКУЩУЮ ветку в new_branch_name
* git push origin :old_branch_name new_branch_name # применить переименование в удаленном репозитории
* git branch --unset-upstream # завершить процесс переименования