# Note: From Api er view a use kora pray sob jinis golo akhane use kora jay

<br>
<br>

### **Model Form**

<br>

### Update korar jonno__

```python
def AddUser(request):
    if request.method == "POST":
        dt = MyUser.objects.get(pk=2)
        fm = UserForm(request.POST, instance=dt)
        if fm.is_valid():
            fm.save()
    else:
        fm = UserForm()
    
    return render(request, 'make_error/error.html', {'form':fm})
```
<br>

### Niser sob ager motoi Form_api system use kora jay

### Save korar jonno__

```python
def AddUser(request):
    if request.method == "POST":
        fm = UserForm(request.POST)
        if fm.is_valid():
            nm = fm.cleaned_data['name']
            em = fm.cleaned_data['email']
            ps = fm.cleaned_data['password']
            userDt = MyUser(name = nm, email = em, password = ps)
            userDt.save()

    else:
        fm = UserForm()
    
    return render(request, 'make_error/error.html', {'form':fm})
```

<br>

### Update/ Delete korar jonno___

```python
def AddUser(request):
    if request.method == "POST":
        fm = UserForm(request.POST)
        fm = UserForm(request.POST)
        if fm.is_valid():
            fm.save()
            nm = fm.cleaned_data['name']
            em = fm.cleaned_data['email']
            ps = fm.cleaned_data['password']
            userDt = MyUser(id = 1, name = nm, email = em, password = ps)
            userDt.save()
            # niser 2 line delete korar jonno use hoy
            # userDt = MyUser(id = 1)
            # userDt.delete()

    else:
        fm = UserForm()
    
    return render(request, 'make_error/error.html', {'form':fm})
```
