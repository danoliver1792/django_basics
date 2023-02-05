<h1>Básico com Django</h1>
<p>Instalando a lib:
pip install django

Para criar um projeto Django, no PyCharm:
django-admin startproject my_project
cd .\my_project\
ls

django-admin startapp my_app

Seleciona manage.py

ctrl + shift + F10 para executar

Erro de código informado

Clica em edit configurations

Escreva "runserver" em parameters

C:\Users\Danrlei\PycharmProjects\venv\Scripts\python.exe C:\Users\Danrlei\PycharmProjects\my_project\manage.py runserver 
Watching for file changes with StatReloader
Performing system checks...

System check identified no issues (0 silenced).

You have 18 unapplied migration(s). Your project may not work properly until you apply the migrations for app(s): admin, auth, contenttypes, sessions.
Run 'python manage.py migrate' to apply them.
February 05, 2023 - 16:25:13
Django version 4.1.6, using settings 'my_project.settings'
Starting development server at http://127.0.0.1:8000/
Quit the server with CTRL-BREAK.

Instalar o App para retornar um "Hello World" com uma rota 
django-admin startapp core

Atribui o App core na linha de código abaixo do arquivo "settings.py"
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'core'
]

Criando uma rota no arquivo "urls.py"
urlpatterns = [
    path('admin/', admin.site.urls),
    path('hello/', views.hello)
]


O hello/ vai nos levar para o método que irá retornar algo na tela, isso em "views.py" em core
def hello(request):
    return HttpResponse('Hello World')

Teremos um Hello World com:
http://127.0.0.1:8000/hello/
