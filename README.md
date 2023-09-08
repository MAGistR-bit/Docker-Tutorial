# Docker-Tutorial
Instructions for working with Docker (starting a container, creating an image)

## 📝 Пишем Dockerfile (Write Dockerfile)
Dockerfile - текстовый файл, содержащий серию команд.
Заведите новую папку, перейдите в нее и создайте файл 
с именем "Dockerfile".

Dockerfile находится в репозитории, поэтому Вы можете ознакомиться
с его содержимым.

<details>
  <summary>English version</summary>
Dockerfile is a text file containing a series of commands.
Create a new folder, go to it and create a file named "Dockerfile".

Dockerfile is located in the repository, so you can familiarize
yourself with its contents.
</details>

## ⚙️ Собираем образ Docker
Чтобы собрать образ Docker, необходимо набрать команду, 
показанную ниже:
```dockerfile
docker build path_to_dockerfile
```
где path_to_dockerfile - путь к вашему Dockerfile

Выполнив данную команду, Вы получите образ Docker со своим идентификатором
(например, "66c76cea05bb"). К идентификатору неудобно обращаться,
поэтому Вы можете присвоить ему тег для удобства. 
Чтобы присвоить тег, введите следующую команду:
```dockerfile
docker tag your_image_identifier tag_name
```
где your_image_identifier - сгенерированный идентификатор,
tag_name - имя тега, которое Вы придумали

Просмотреть список локальных отзывов можно следующим образом:
```dockerfile
docker images -a
```
Вывод команды будет выглядеть примерно так:
```bash
REPOSITORY   TAG       IMAGE ID       CREATED        SIZE
todoapp      latest    2896ad0b56d0   3 hours ago    1.2GB
```
Теперь Вы можете собрать свою собственную копию образа Docker
из файла Dockerfile, воспроизводя среду, определенную кем-то другим.
