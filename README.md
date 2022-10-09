# MySQL settings

### File: projectname > settings.py

```
import os

....

DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': os.environ.get('MYSQL_DATABASE'),
        'USER': os.environ.get('MYSQL_USER'),
        'PASSWORD': os.environ.get('MYSQL_PASSWORD'),
        'HOST': 'db',
        'PORT': 3306,
        'OPTIONS': {
            'init_command': 'SET default_storage_engine=INNODB'
        }
    }
}
```