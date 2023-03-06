### **Link with App Urls\_\_\_**

```python
from django.urls import path, include

urlpatterns = [
    path('admin/', admin.site.urls),
    path('', include('app1.urls'))
]
```
