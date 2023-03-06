### **Save From API to Database**

models a 'user' class r forms a 'urform' class doitai name, r email fields kora hoise

### Sample

```python
from .forms import urform
from .models import user

def Sud(request):
    if request.method == 'POST':
        fm = urform(request.POST)
        if fm.is_valid():
            nm = fm.cleaned_data['name']
            em = fm.cleaned_data['email']
            # myuser = user(name = nm, email = em)
            # myuser = user(id = 1, name = nm, email = em)
            myuser = user(id = 1)
            # myuser.save()
            myuser.delete()
    else:
        fm = urform()
    return render(request, 'make_error/save_u_d.html', {'form':fm})
```

<br>

### Save

```python
    myuser = user(name = nm, email = em)
    myuser.save()
```

### Update

```python
    myuser = user(id = 1, name = nm, email = em) # specify which user/id you want to update
    myuser.save()
```

### Delete

```python
    myuser = user(id = 1) # specify user/id
    myuser.delete()
```


