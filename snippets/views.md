1. Imports

```
from django.shortcuts import render
from .forms import EmailForm, JoinForm
from .models import Join
```

2. Home view
    
    1. Using regular django forms 
    
    ```
    def home(request):
        form = EmailForm(request.POST or None)
        if from.is_valid():
            email = form.cleaned_data['email']
            new_join, new = Join.objects.get_or_create(email=email)  
        
        context = {"form": form}
        template = 'home.html'
        return render(request, template, context)
    ```    
    
    2. Using django model forms

    ```
    def home(request):
        form = JoinForm(request.POST or None)
        if from.is_valid():
            new_join = form.save(commit=False)
            new_join.ip_address = get_ip(request)  
            new_join.save()
            
        context = {"form": form}
        template = 'home.html'
        return render(request, template, context)
    ```

3. Get the ip address

```
def get_ip(request):
    try:
        x_forward = request.META.get("HTTP_X_FORWARDED_FOR")
        if x_forward:
            ip = x_forward.split(",")[0]
        else:
            ip = request.META.get("REMOTE_ADDR")
    except:
        ip = ""
    return ip
```
