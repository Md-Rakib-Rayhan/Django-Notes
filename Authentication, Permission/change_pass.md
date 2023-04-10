## **Change Password**

jaja lagbe
```python
# basic
from django.shortcuts import render, redirect
from django.contrib import messages

# main
from django.contrib.auth.forms import PasswordChangeForm, SetPasswordForm
from django.contrib.auth import update_session_auth_hash
```

<br>
<br>

## Change Password By old password
```python
def change_pass_by_old(request):
    if request.user.is_authenticated: # jodi login thake
        if request.method == 'POST':
            fm = PasswordChangeForm(user=request.user, data=request.POST)
            if fm.is_valid():
                fm.save() # ager password match hoise kina seta ai form ai check kore fele
                #password change kora hole auto metic logout hobe jay karon session a old pass thake er jonno abar login korte hoy
                update_session_auth_hash(request, fm.user) # logout jate nah hoy
                messages.success(request, 'Your password changed successfully')
                return redirect('/profile/')
                
        else:
            fm = PasswordChangeForm(user=request.user) # kon user er jonno password change kora lagbe - er jono user
        return render(request, 'auth_app/sing_inup.html', {'form': fm, 'changepass': 'changepass'})# same form multiple use er jonno changepass ami use korsilam
    
    else:
        return redirect('/singin/')
```



<br>
<br>

---

<br>

## set pass (ai link email a deya hoy)
```python
def setpass(request):
    if request.user.is_authenticated:
        if request.method == 'POST':
            fm = SetPasswordForm(user=request.user, data=request.POST)
            if fm.is_valid():
                fm.save()
                #password change kora hole auto metic logout hobe jay karon session a old pass thake er jonno abar login korte hoy
                update_session_auth_hash(request, fm.user) # logout jate nah hoy
                messages.success(request, 'Your password changed successfully')
                return redirect('/profile/')
                
        else:
            fm = SetPasswordForm(user=request.user) # kon user er jonno password change kora lagbe - er jono user
        return render(request, 'auth_app/sing_inup.html', {'form': fm, 'setpass': 'setpass'})
    
    else:
        return redirect('/singin/')
```
