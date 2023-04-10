# There no one at all
from django.db import migrations, models
 import django.utils.timezone


 class Migration(migrations.Migration):

     dependencies = [
         ('blog', '0001_initial'),
     ]

     operations = [
         migrations.AddField(
             model_name='post',
             name='counted_views',
             field=models.IntegerField(default=0),
         ),
         migrations.AddField(
             model_name='post',
             name='created_date',
             field=models.DateTimeField(auto_now_add=True, default=django.utils.timezone.now),
             preserve_default=False,
         ),
         migrations.AddField(
             model_name='post',
             name='published_date',
             field=models.DateTimeField(null=True),
         ),
         migrations.AddField(
             model_name='post',
             name='status',
             field=models.BooleanField(default=False),
         ),
         migrations.AddField(
             model_name='post',
             name='updated_date',
             field=models.DateTimeField(auto_now=True),
         ),
     ]
