```python
from . import views

    url(r'^admin/', admin.site.urls),
    url(r'^$', views.home, name='home')
```