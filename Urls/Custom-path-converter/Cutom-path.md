## **Custom Path Converter**

Build in converter golo str, int, slug etc  
but we can make own custom converter

## 1.
Frist Need to Create a file inside App  

file name -> converters.py

## 2.
Create By Logic

``` python
class forDigitYearConverter:
    regex = '[0-9]{4}'

    def to_python(self, value):
        return int(value)
    
    def to_url(self, value):
        return f'{value:4d}'
        # same
        # return '%4d' % value
```

Expailn :
-

0. anyclass
1. ```
    regex = '[which value]{length}
    ```
    * 0 theke 9 -> 0,1,2,3...9 -> mane only sob numberic caracter supported
     * max and min 4ta character supported, besi o nah kom o nah

<br>

2. ```
    def to_python(self, value):
        return int(value) 
    ```
    * normal str('1234') value k int a convertion -> url theke views a gele data int akare kaj korbe

<br>

3. ```
    def to_url(self, value):
        return f'{value:4d}'
    ```
    * value hobe mot 4 digit/character er

<br>

---

<br>

### **Set up to Urls.py**

```python
from django.urls import path, register_converter
from . import views, converters

register_converter(converters.forDigitYearConverter, 'yyyy')

urlpatterns = [
    ... ,
    path('session/<yyyy:myyear>', views.studentSession, name='students'),
]

```

Expalin:
-

0. import korte hobe register_converter, And amader converters.py

1. Conterver ti register korte hobe r atar nam set korte hobe, jemon build-in kiso thake str, int, slug etc
    * register_converter(classname, 'anyname')

2. next a amra atake aivabe use korte parbo ```<yyyy:anyPeramiter>```

3. aitar example http://127.0.0.1:8000/session/6842 
    * last a jekono 4ta nuberic character dile aita call hobe. 3,5 ta dile aita call hobe nah

