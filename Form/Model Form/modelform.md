## **Basic Strature**

```python
from .models import MyUser

class UserForm(forms.ModelForm):
    class Meta:
        model = MyUser
        fields = ("name", "password", "email")
```

Aitar jonno Models.py
```python
class MyUser(models.Model):
    name = models.CharField(max_length=50)
    email = models.EmailField( max_length=254, blank=True)
    password = models.CharField(max_length=100)
```

Notes: 
1. kon model er class use korte hobe ta "model" a define kora hoy. r uporer 'forms.py' a je vabe code ase seitai defalut stacture ('model = MyUser' kon model class use korbe seta define kora)

2. 'Userform' a model-class theke kon kon field asbe seta "fields" use kore define kora hoy && konta age konta pore dite hobe seitau define kora jay

3. models.py a Model-class 'MyUser' "blank=True" aita form.py a "required=False" hisebe ney, mane  value na dileu submit hobe


<br>

---

<br>
<br>

## **Aro jevabe kora jay** 

```python
class regisrationForm(forms.ModelForm):
    class Meta:
        model = MyUser
        fields = '__all__'
```
aitar mane sob models class er sob fields output/render hobe

<br>

```python
class regisrationForm(forms.ModelForm):
    class Meta:
        model = MyUser
        exclude = ['name']
```
aitar sob fields output/render hobe sodhu 'name' fields bad diye



