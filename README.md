1 
## 	Создал репозиторий на  сайте  https://github.com/Parcius/CreateRobot
## и скопировал на домашний компьютер с помощью команды из командной строки:
```
		git clone https://github.com/Parcius/CreateRobot.git 			CreateRobot
```
2 
##	Захожу в папку CreateRobot на ПК и ввожу команду 
```
     	git status
```
##   	Вижу сообщение       

		Текущая ветка: master

 3 
	
##	Создаю программу для управления фрезерным трех осевым станком, в двух файлах *.py
##	Создаю файлы и вложенную папку. 

	CreateRobot/milling_machine.py :
	
Tool_rotor_speed = 12000 rpm
X_stroke = 2000 mm
Y_stroke = 1000 mm
Z_stroke =  800 mm 

	CreateRobot/Speed_control/Speed_controller.py :

X_axis_speed = 3000 m/min
Y_axis_speed = 4000 m/min
Z_axis_speed = 2500 m/min


##	Ввожу команду  git add *  в корневой папке репозитория на ПК и получаю сообщение

		новый файл:    README.md
		новый файл:    Speed_control/Speed_controller.py
		новый файл:    Speed_control/readme_speed.md
		новый файл:    milling_machine.py

4
##	Делаю комит

		git commit

##	Ввожу сообщение:  «Создание станка»

##	Получаю на экране:

		[master (корневой коммит) bf01709] Создание станка
 		4 files changed, 11 insertions(+)
 		create mode 100644 README.md
 		create mode 100644 Speed_control/Speed_controller.py
 		create mode 100644 Speed_control/readme_speed.md
 		create mode 100644 milling_machine.py

5 
	
##	Ввожу команду

		git remote add origin 					https://github.com/Parcius/CreateRobot.git

##	Получаю сообщение 
	
	fatal: внешний репозиторий origin уже существует


##	Ввожу команду

		git remote show
	
##	Показывает 
		Origin

6
##	Ввожу
 		git branch -M main
		git push -u origin main

##	Запрашивает имя пользователя и пароль. Генерирую токен на сайте и ввожу. Выводит сообщение :

	Перечисление объектов: 7, готово.
	Подсчет объектов: 100% (7/7), готово.
	При сжатии изменений используется до 2 потоков
	Сжатие объектов: 100% (7/7), готово.
	Запись объектов: 100% (7/7), 667 байтов | 667.00 КиБ/с, 	готово.
	Всего 7 (изменения 0), повторно использовано 0 (изменения 0)
	To https://github.com/Parcius/CreateRobot.git
	 * [new branch]      main -> main
	Ветка «main» отслеживает внешнюю ветку «main» из «origin».

##	Вижу появление данных репозитория на сайте



7
##	Ввожу команду

		git branch Axis_4
		и 
		git branch

##	вижу сообщение

	  Axis_4
	* main

##	Ввожу

		git checkout Axis_4

##	сообщение

##	Переключились на ветку «Axis_4»

8 
##	Открываю файл CreateRobot/milling_machine.py  и добавляю строку:  A_rotary_table = 360 deg
	
	Tool_rotor_speed = 12000 rpm
	X_stroke = 2000 mm
	Y_stroke = 1000 mm
	Z_stroke =  800 mm 

	A_rotary_table = 360 deg

##	Открываю файл  CreateRobot/Speed_control/Speed_controller.py и добавляю строку:  A_axis_speed = 10 rpm

	X_axis_speed = 3000 m/min
	Y_axis_speed = 4000 m/min
	Z_axis_speed = 2500 m/min

	A_axis_speed = 10 rpm

##     В файлы readme.md добавляю комментарии

9
##	Затем
	
	git status

	Изменения, которые не в индексе для коммита:
  	(используйте «git add <файл>...», чтобы добавить файл в индекс)
  	(используйте «git restore <файл>...», чтобы отменить изменения в рабочем каталоге)
	изменено:      README.md
	изменено:      milling_machine.py
	изменено:      Speed_control/Speed_controller.py
	изменено:      Speed_control/readme_speed.md

	git add *

	git status

	Текущая ветка: Axis_4
	Изменения, которые будут включены в коммит:
 	 (используйте «git restore --staged <файл>...», чтобы убрать из индекса)
	изменено:      README.md
	изменено:      Speed_control/Speed_controller.py
	изменено:      Speed_control/readme_speed.md
	изменено:      milling_machine.py

	git commit -m "Add fourth axis"

	[Axis_4 e178f05] Add fourth axis
	 4 files changed, 8 insertions(+)

10
##	Затем отправляю на удаленный репозиторий

		git push --set-upstream origin Axis_4

	Перечисление объектов: 13, готово.
	Подсчет объектов: 100% (13/13), готово.
	При сжатии изменений используется до 2 потоков
	Сжатие объектов: 100% (7/7), готово.
	Запись объектов: 100% (7/7), 782 байта | 782.00 КиБ/с, готово.
	Всего 7 (изменения 2), повторно использовано 0 (изменения 0)
	remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
	remote: 
	remote: Create a pull request for 'Axis_4' on GitHub by visiting:
	remote:      https://github.com/Parcius/CreateRobot/pull/new/Axis_4
	remote: 
	To https://github.com/Parcius/CreateRobot.git
	 * [new branch]      Axis_4 -> Axis_4
	Ветка «Axis_4» отслеживает внешнюю ветку «Axis_4» из «origin».

##	Захожу на github  и вижу что появилась ветвь Axis_4 
## и в ней файлы изменены, и имеют добавленные строки. 

    		A_axis_speed = 10 rpm

		A_rotary_table = 360 deg

##	А в main  файлы остались прежними 

11
##	Перехожу в командную строку и переключаюсь в главную ветку
		git checkout main
  
	Переключились на ветку «main»
	Эта ветка соответствует «origin/main».

##	Затем объединяю

		git merge Axis_4
  
	Обновление bf01709..e178f05
	Fast-forward
 	README.md                         | 2 ++
 	Speed_control/Speed_controller.py | 2 ++
 	Speed_control/readme_speed.md     | 2 ++
 	milling_machine.py                | 2 ++
 	4 files changed, 8 insertions(+)

##	Переключаюсь по очереди на разные ветки и вижу что файлы в них имеют идентичное содержание

##	Затем захожу на сайт Github выбираю 

		Pull requests
		New pull request
		View pull request

##	Вижу сообщение 

		«This branch has no conflicts with the base branch»

##	Выбираю:

		Merge pull request
		Confirm merge

##	Появляется сообщение: 

		Pull request successfully merged and closed

##	Захожу в окно репозитория и просматриваю файлы, они идентичны в ветках main и  Axis_4
