forms.py
```python
class htmlForm(forms.Form):
    name = forms.CharField(initial='rakib', help_text='plz Enter your name between 20 character okay.')
```

### **Html a Customization**
```django
<form action="">
        <div>
            <label for="{{form.name.id_for_label}}">Name</label>
            {{form.name}}
        </div>
        <div>
            {{form.name.label_tag}}
            {{form.name}}
        </div>
        <div>
            {{form.name.label}}
            <br>
            {{form.name.value}}
            <br>
            {{form.name.html_name}} {% comment %} html input tag a je name atribute thake oita {% endcomment %}
            <br>
            {{form.name.help_text}}
            <br>
            {{form.name.field.required}} {% comment %} required er value dekhar jonno {% endcomment %}
        </div>
    </form>
```

Output:

![img](./C-out.jpg)

<br>

---

<br>
<br>


### **Use Loop**
```django
 <form action="" method="get">
        {% for fm in form %}
        {{fm.label_tag}}
        {{fm}}
        {% endfor %}
        <input type="submit" value="Submit">
    </form>
```

Output:

![img](./loop.jpg)

<br>

---

<br>
<br>

### **Jodi Hidden field thake**
forms.py a hidden fields
```python
class hideForm(forms.Form):
    ...
    key = forms.IntegerField(widget=forms.HiddenInput())
```

Normal form render korle thik motoi ase  
but loop use korle arokom ase

![img](./loop-plm.jpg)

aita nicer moto likle thik hoye jabe
```django
<form action="" method="get">
        {% for vn in form.visible_fields %}
        {{vn.label_tag}}
        {{vn}}
        {% endfor %}

        {% for hn in form.hidden_fields %}
        {{hn}}
        {% endfor %}
        <input type="submit" value="Submit">
    </form>
```

![img](./loop.jpg)

r code o thik motoi thakbe

![img](./code.jpg)