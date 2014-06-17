#Установка и работа с GIT

Скачиваем **GIT** для Windows с официального [сайта](http://git-scm.com/).

Устанавливаем GIT.

Настраиваем для работы:

```$ git config --global user.name "Your Name Here"```

```$ git config --global user.email "your_email@example.com"```

Регистрируемся на [github](https://github.com) и создаем новый проект с названием "myproject".

Далее генерируем SSH ключ. Для этого заходим в git и вводим следующие команду:

```$ ssh-keygen -t rsa -C "your_email@example.com"```

Если все прошло успешно, ключ сгенерирован. Копируем его в буфер. для этого вводим следующую команду:

```$ clip < ~/.ssh/id_rsa.pub```

Заходим на [github](https://github.com) в свой профиль - Account settings - SSH keys - Add SSH key и вставляем туда скопированный ключ, сохраняем изменения.

Открываем git и для проверки успешного создания ключа вводим следующую команду:

```$ ssh -T git@github.com```

Если все успешно, вы увидите приветствие.
С настройкой SSH закончили. Открываем git и для создаем директорию для будущего проекта. Для єтого вводим следующую команду:

```$ mkdir ~/myproject```

Переходим в созданную папку:
```$ cd myproject```. Далее вводим команду ```$ git init ```
и создаем в папке проекта файл ```$ touch readme.txt```. Для внесения изменения в проект на github делаем следующее:
- ```$ git add readme.txt```
- ```$ git commit -m 'first commit'```
- ```$ git remote add origin git@github.com:username/myproject.git``` - "git@github.com:username/myproject.git" можно увидеть на странице вашего проекта на github.
- ```$ git push origin master``` - внесение изменений в проект.

Если все прошло успешно на github в вашем проекте появится 1 commit с внесенными измеениями. Более подробную информацию по данным действиям можно посмотреть [здесь](https://help.github.com/articles/set-up-git), [здесь](https://help.github.com/articles/create-a-repo) и [здесь](https://help.github.com/articles/generating-ssh-keys).






