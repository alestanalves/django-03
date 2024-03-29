# Django

<a href = "https://docs.djangoproject.com/en/2.2/topics/db/models/">
<img src="https://user-images.githubusercontent.com/48387196/65687547-ee795000-e03f-11e9-90cc-ed6c56d8b185.png"  width="80" /></a>

<a href = "https://github.com/AlestanAlves/django-03/blob/master/LICENSE">
<img src="https://user-images.githubusercontent.com/48387196/65687713-31d3be80-e040-11e9-80e0-ebf7c4fd4736.png"  width="80" /></a>
 
<a href = "https://docs.djangoproject.com/en/2.2/">
<img src="https://user-images.githubusercontent.com/48387196/65687977-a9a1e900-e040-11e9-9f2f-8418272a3063.png"  width="80" /></a>


- **Rodar servidor em outra porta:** `python3 manage.py runserver 9000`
- **Criar um usuario do admin:** `python3 manage.py createsuperuser`
- **Importar todas as models de um app no admin.py:** `from website.models import *`
- **Em admin.py adicionar os dados no /admin:** `admin.site.register(Coach)`
- **Criar super usuario:** `python manage.py createsuperuser`
- **form:get:** `gera uma informação via URL`
- **form:post:** `gera informação via post`
- **form action:** `toda vez que criar um formulario no django tem que colocar isso {% csrf_token %}`
- **form action:** `action="/" para ir para algum lugar`
- **Criar na view o objeto de cadastro:** `

 - **Criar arquivo de migração** `python manage.py makemigrations`
- **Aplicar migração na base de dados** `python manage.py migrate`

_obs: Tente não excluir o histórico de migrações. :) :)_

- **Criar um super usuário:** `python3  manage.py createsuperuser`
- **No windows:** `winpty python manage.py createsuperuser`
 
- **Importar todas as models de um app:** `from {website}.models import * `
- **Registrar no admin.py:** `admin.site.register(Coach)`

- **Colocar na model Coach**
```
    def __str__(self):
        return self.nome 
```

### Minhas urls:
```
from django.contrib import admin
from django.urls import path
from website import views
```
```
urlpatterns = [
    path('admin/', admin.site.urls),
    path('', views.index)
]
```

## Passo a passo:

- **Criar models**
``` 
    - makemigrations
    - migrate
```

- **URL**
```
    -criação de rotas chamando suas views
```
- **View**
```
    - função com request utilizado
    - request.method == "POST"
```

- **Templates**
``` 
    - páginas html (formulários)
    - crsf token - carimbo
    - action: a url que chama a view
```

## CSRF TOKEN

<img src="https://www.digitalmunition.me/wp-content/uploads/2018/04/csrf-cross-site-request-forgery-620x350-c.png" />
