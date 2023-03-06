### **Settings for install app\_\_\_**

```python
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
]
```

sobar nise app name add korte hobe

```python
INSTALLED_APPS = [
    ...,
    'django.contrib.staticfiles',
    'appname'
]
```

<br>

---

<br>
<br>

### **Settings for Tamplates\_\_\_**

```python
TEMPLATES = [
    {
        'BACKEND': 'django.template.backends.django.DjangoTemplates',
        'DIRS': [],
        'APP_DIRS': True,
        'OPTIONS': {
            'context_processors': [
                ...
            ],
        },
    },
]
```

Upore DIRS A Blank 3rd braket a, nicer code ti dite hobe r os ta sobar upore import kore nite hobe

```python
import os

'DIRS': [os.path.join(BASE_DIR, 'templates')],
```

<br>

---

<br>
<br>

### **Settings for Static File\_\_\_**

```python
import os

STATICFILES_DIRS = [
    os.path.join(BASE_DIR, 'static')
    ]
```

sodho BASE_DIR, 'static' aita liklei cole , same for templates also  
<br>
but aitai old/new sob version a cole tai aita use kori

<br>

---

<br>
<br>
