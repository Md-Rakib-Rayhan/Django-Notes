### **Redirectr**

```python
from django.http import HttpResponseRedirect

def valid(request):
    ....
    return HttpResponseRedirect('/edit/success/') # ai urls a niser function call kora ase


def success(request):
    return render(request, 'app_F_Edit/success.html')
```