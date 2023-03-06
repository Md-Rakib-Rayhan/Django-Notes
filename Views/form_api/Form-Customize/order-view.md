order forms.py thekei hoy but caile akhaneu kora jay

### **Ordering (konter por konta)**

Normal Output:

![img](./normal.jpg)

code:
```python
def home(request):
    fm = myForm()

    fm.order_fields(field_order=['roll', 'email', 'name'])

    return render(request, 'app_F_Edit/index.html', {'form':fm})
```

Output:

![img](./order.jpg)

Note: field_order a sodho 1ta likheu kora jay r baki golo ager niyome thakbe sodho jeta likse oita upore thakbe





