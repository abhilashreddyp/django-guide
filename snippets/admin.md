from django.contrib import admin
from .models import Join

admin.site.register(Join)


class JoinAdmin(admin.ModelAdmin):
    list_display = ['__str__', 'email'] #Filed to be visualised in the admin panel
    class Meta:
        model = Join

admin.site.register(Join, JoinAdmin)
