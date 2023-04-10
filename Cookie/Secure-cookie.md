## **Singed Cookies**

**My expain ->**  
aita enception/criptograpy system use kore.  

aita actual value cookie te store na kore cripted value store kore, like-> md. rakib -> dad3#2@ddff

jeta solt te arekta value use kora ai enception kora hoy and ai solt value holo secret key ja client and server er ta same thake.

client nijeu cookie theke caileu value dekte parbe nah se dekbe sodho encripted valu aita 'dad3#2@ddff'

<br>
<br>

## **Set / Create**

```python
def setCookie(request):
    response = render(request, 'set_cookie.html')

    response.set_signed_cookie('name', 'Md. Imran', salt='nm')
    return response
```

![img](./9.png)

aita koto din thekbe etc other otion 'Cookie.md' te same oitai


<br>
<br>

---

<br>


## **GET**

Jodi client er cookie server er sathe na mele tahle 'defoult' ja ase "Geust" show hobe

'defoult' use na korle jodi cookie match nah hoy tahole sodho error dekhane


2 tar (get, set) solt same tote hobe

r max_age age set korle akhaneu dite hobe

```python
def getCookie(request):
    
    name = request.get_signed_cookie('name', default = 'Geust', salt='nm')
    return render(request, 'get_cookie.html', {'name':name})
```

![img](./10.png)

<br>

## R Delete ager motoi (Cookie.md)
