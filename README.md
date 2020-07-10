from django.contrib import admin
from .models import Category
from .models import Location
from .models import JobListing

# Register your models here.
class CategoryAdmin(admin.ModelAdmin):
    list_display = ['text', 'details']
admin.site.register(Category, CategoryAdmin)
admin.site.register(Location)
class JobListingAdmin(admin.ModelAdmin):
    list_display = ['title', 'company', 'description']

admin.site.register(JobListing, JobListingAdmin)
