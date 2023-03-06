### **Basic**

```python
class Student(models.Model):
    stuid = models.IntegerField()
    stuname = models.CharField(max_length=70)
    stuemail = models.EmailField(max_length=70)
    stupassword = models.CharField(max_length=70)
    comment = models.CharField(max_length=70, default='not available')
```