### **Customize**

### To add Custom labels__
```python
class UserForm(forms.ModelForm):
    class Meta:
        model = MyUser
        fields = ("name", "password", "email")

        labels = {"name": "Enter Your Name", "password": "Enter Your Password"}

```

### To add Custom help_text (aita form a nise dekhano hoy)__
```python
        help_texts = {"name": "Start Your Name With Md"}
```

### To add Custom widgets and error_messages __
```python
        error_messages ={"password": {"required": "Password likhte hobe bro"}}

        widgets = {"password": forms.PasswordInput(), "email": forms.EmailInput(attrs={"placeholder": "Enter Email", "class": "helo"})}
```

### Update/customize with new 'name' Field__
```python
class UserForm(forms.ModelForm):
    name = forms.CharField(max_length=60) # priority hight
    class Meta:
        model = MyUser
        fields = ("name", "password", "email")

        labels = {"name": "Enter Your Name", "password": "Enter Your Password"}
        help_texts = {"name": "Start Your Name With Md"}
```

Notes:
1. akhane abar 'name' field toiri korle aitar priority high hobe jar jonno models.py & Class Meta er vetor kora sob customize overwrite korbe mane ager customize batil.

2. aitate Form Api er moto sob kiso Customize kora jabe. Meta, othoba abar fields create kore - doitatei hobe.