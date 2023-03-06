## **Customize with widget___**
widget used for customize  form field (like - Input Type,Class, id)

### **widget a html input type change kora**

Normally amra avabe input type diye thaki:-> name = forms.CharField()

but ai system a kiso kiso input type thake nah, tai widget use kora thaki
```python
class editWithwidget(forms.Form):
    password = forms.CharField(widget=forms.PasswordInput())
```

**Output**
```html
 ...
 <input type="password" name="password" required id="id_password">
```

Widget a input type somoho golo holo
-
Text Input Widget, Password Input Widget, Number Input Widget, Email Input Widget, URL Input Widget, Checkbox Input Widget, Select Widget, Radio Select Widget, Date Input Widget, Time Input Widget, DateTime Input Widget, File Input Widget, etc.

Notes : TextInput er moddhe -> CharField, TextField ai doitai pore akhane charfield likele hobe nah

<br>

---

<br>
<br>

## **Class, Id, others attribute Set/Change kora**
amra widget type set korar por tar vetor attrs likhe dictionay akare bivinno attribute set korte pari like :-> class, id

```python
name = forms.CharField(widget=forms.TextInput(attrs={'class':'container', 'id':'Helloname', 'placeholder': 'Enter Email'}))
```

**Output**

```html
 <input type="text" name="name" class="container" id="Helloname" required>
```
