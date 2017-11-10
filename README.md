#Brander test task: Учет работы сотрудников

Необходимо создать проект при котором менеджер системы может завести базу данных сотрудников.
 
В ней будут отображены дни при которых сотрудник был на работе, имел пропуски, а так же данные по зарплате.

В систему должен быть авторизованный доступ.
  
##Разделы:

* Листинг пользователей, в нем список имен сотрудников с персональными фотографиями, листинг пагинируемый
* Добавление/редактирование пользователя. Где менеджер может внести или изменить следущие данные пользователя:
     * Имя
     * Должность (выбор из списка)
     * Фотография
     * Рейт (цена 1го часа работы сотрудника)
* Страница где будут внесены дни когда сотрудник отсутствовал на рабочем месте
* Страница где будет отображена зарплата сотрудника за месяц с учетом его пропусков и рейта     
 

##Требование:
 Для выполнения задания необходимо сделать форк текущего репозитория в свой личный github аккаунт далее производить работу над проектом в своем репозитории.
 
 Результатом выполнения задания будет считаться ссылка на репозиторий
 
#Как развернуть проект на VAGRANT 

Для разворачивания проекта необходимо иметь установленными 

в папке проекта VirtualBox, Ansible, Vagrant (Установка: https://habrahabr.ru/post/305400/)

Билд проекта:

```
vagrant up --provision
```
 
Для того чтобы проект был доступен по домену http://brander.loc , необходимо добавить запись в файл hosts (https://ru.wikipedia.org/wiki/Hosts)

```
192.168.255.10  brander.loc
```
 
после билда, для того чтоб попасть в виртуальную машину с проектом:

````
vagrant ssh
````

В виртуальной машине проект будет доступен по пути: /var/www
