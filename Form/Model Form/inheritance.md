## **Model Form Inheritance**

```python
class studentRegistration(forms.ModelForm):
    class Meta:
        model = Schoolregistration
        fields = ['student_name','email', 'password']

class teacherRegistration(studentRegistration):
    class Meta(studentRegistration.Meta):
        fields = ['teacher_name', 'email', 'password']
```

Notes:
1. 2tar jonno alada registration form asleu save 1 jaygay hobe karo 1tai model use hoise.

![img](./inheritance.jpg)

