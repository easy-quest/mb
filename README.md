###### 					Начальная настройка

```bash
pipenv install django
pipenv shell
django-admin startproject mysite .
python manage.py startapp pages
```
```python
# helloworld_project/settings.py
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
	'posts', # new
]
```
```python
# pages_project/settings.py
TEMPLATES = [
    {
        ...
        'DIRS': [os.path.join(BASE_DIR, 'templates')],
        ...
    },
]
```
```python
# pages_project/settings.py
ALLOWED_HOSTS = ['*']
```
```python
LANGUAGE_CODE = 'ru-ru'

TIME_ZONE = 'Europe/Moscow'
```

###### Установка Git


```bash
./sh.sh
```

pipenv install gunicorn


Run 'python manage.py migrate' 

```shell
scp zzz@zzzi.site:/home/zzz/mysite/*sh  ~/mysite/.bin
```
python manage.py test
pipenv install gunicorn
sudo npm i -g heroku
heroku login
./git.sh 

Пипенв оказался в виртуальной среде, поэтому она автоматически использовала эту среду вместо того, чтобы создать собственную для любого проекта.Ты можешь set PIPENV_IGNORE_VIRTUALENVS=1  caЧтобы заставить Pipenv игнорировать эту среду и вместо этого создать свой собственный.n Ты устанавливаешь PIPENV_VERBOSITY=-1 to подавить это предупреждение.


python manage.py makemigrations posts
python manage.py migrate posts
python manage.py migrate posts
python manage.pyreatesuperuser
zzz

# Tests 
Раньше мы тестировали только статические страницы, поэтому мы использовали  SimpleTestCase(простой тест). Но теперь, когда наша домашняя страница работает с базой  данных, нам нужно использовать TestCase, которая позволит нам создать «тестовую» базу  данных, которую мы можем проверить. Другими словами, нам не нужно запускать тесты в  нашей реальной базе данных, но вместо этого можно создать отдельную тестовую базу  данных, заполнить ее образцами данных, а затем протестировать ее.
Начнем с добавления образца записи в текстовое поле базы данных, а затем проверим,  правильно ли она хранится в базе данных. Важно, чтобы все наши методы тестирования  начинались с test_, чтобы Django знал что тестировать! Код будет выглядеть следующим  образом:

Tests Раньше мы тестировали только статические страницы, поэтому мы использовали  SimpleTestCase(простой тест). Но теперь, когда наша домашняя страница работает с базой  данных, нам нужно использовать TestCase, которая позволит нам создать «тестовую» базу  данных, которую мы можем проверить. Другими словами, нам не нужно запускать тесты в  нашей реальной базе данных, но вместо этого можно создать отдельную тестовую базу  данных, заполнить ее образцами данных, а затем протестировать ее.
Начнем с добавления образца записи в текстовое поле базы данных, а затем проверим,  правильно ли она хранится в базе данных. Важно, чтобы все наши методы тестирования  начинались с test_, чтобы Django знал что тестировать! Код будет выглядеть следующим  образом: