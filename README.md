# Linux
## Лабораторная работа №7

# Вопросы:
## 1 Как отобразить 4 последних выполненных команды? 
history 4

## 2 Перевести задание в фоновый режим в bash можно командой 
bg 

## 3 Какая комбинация клавиш переключит вас на 4-ю виртуальную консоль? 
Ctrl+Alt+F4 

## 4 Какая переменная среды содержит путь к домашнему каталогу? 
PWD 

## 5 Установить в bash переменную MYVAR в качестве системной можно командой? 
export MYVAR 

## 6 Какие комбинации клавиш позволят выделить несколько файлов в Midnight Commander? 
Tab, Ctrl+I 

## 7 Что выведет на экран этот сценарий?
```
 #!/bin/bash
 VAR=`echo 'test'`
 VAR2=`echo '$VAR'`
 echo $VAR2
```
вывод: $VAR
 
## 8 Что выведет на экран это сценарий?
```
 #!/bin/bash
 cd /etc
 VAR="$PWD"
 if [ -n "$VAR" ]; then
 echo "$VAR"
 else
 echo '$VAR'
 fi 
```
вывод: /etc

## 9 Что выведет на экран этот сценарий?
```
 #!/bin/bash 
 A=1
 B=2
 if [ $A -eq $B  ]; then
 echo '$A'
 else
 echo "$B"
 fi 
```
вывод: 2

## Задача
```
 Написать скрипт который получает в качестве аргумента 3 значения, a, b,c,d 
 a - высота прямоугольника
 б - ширина прямоугольника
 с 0/1 - пустой или заполненный
 d - символ из которого следует рисовать
 ```
 ```
#!/bin/bash
let A=$1-1
let B=$2-1
for ((i = 0; i < $1; i++)); do
	for ((j = 0; j < $2; j++)); do
		if [ $i -eq 0 -o $i -eq $A ] 
			then
			echo -n $4
		else 
			if [ $j -eq 0 -o $j -eq $B ] 
				then
				echo -n $4
			else					
				if [ $3 -eq 0 ]
					then
					echo -n " "
				else echo -n $4
				fi
			fi
		fi
	done
	echo ''
done

```
