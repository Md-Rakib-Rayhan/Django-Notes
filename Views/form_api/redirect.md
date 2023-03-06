### **Redirect & Error**

```python
from django.http import HttpResponseRedirect

def success(request):
    return render(request, 'app_F_Edit/success.html')


def valid(request):
    if request.method == 'POST':
        fm = validForm(request.POST)
        if fm.is_valid():
            data = fm.cleaned_data
            print(data)
            return HttpResponseRedirect('/edit/success/') # ai urls a uporer function call kora ase
    else:
        fm = validForm()
    
    return render(request, 'app_F_Edit/validating.html', {'form': fm})
```

Error-NOTE: Sob true hoyar por "fm.is_valid():" aitau true hobe Redirect hobe -- But jodi false hoy tahole aita Client je vul input dise seita dekhabe and aita dekhanor jonno last a "return" ta "Else" er vitor deya hoynai  
-- jodi aita kora na hoy tahole system error asbe