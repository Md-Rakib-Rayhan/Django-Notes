### **Load Static / CSS in HTML\_\_\_**

1. Use this in top

   ```django
   {% load static %}
   ```

2. Link the location

   ```html
   <link rel="stylesheet" href="{% static 'app1/css/style.css' %}" />
   <link rel="stylesheet" href="{% static 'style.css' %}" />

   <!-- or -->

   <link rel="stylesheet" href="/static/style.css" />
   ```

   image, javascript er jonnou same

<br>

---

<br>
<br>

### **url\_\_**

```html
<a href="/about">About</a><!-- derect link -->
<!-- or - best way -->
<a href="{% url 'About' %}">About</a>
<!-- or -->
{% url 'About' as ab %}
<a href="{{ab}}">About</a>
<!-- urls er sathe value set kore pathanor jonno -->
<a href="{% url 'pdetails' arg1=value arg2=value %}">Product Details</a>
<a href="{% url 'pdetails' value1 value2 %}">Product Details</a>
```

more example
![image here](./url-link.jpg)
