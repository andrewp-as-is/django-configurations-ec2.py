<!--
https://readme42.com
-->


[![](https://img.shields.io/pypi/v/django-configurations-ec2.svg?maxAge=3600)](https://pypi.org/project/django-configurations-ec2/)
[![](https://img.shields.io/badge/License-Unlicense-blue.svg?longCache=True)](https://unlicense.org/)
[![](https://github.com/andrewp-as-is/django-configurations-ec2.py/workflows/tests42/badge.svg)](https://github.com/andrewp-as-is/django-configurations-ec2.py/actions)

### Installation
```bash
$ [sudo] pip install django-configurations-ec2
```

#### Features
+   `ALLOWED_HOSTS` - EC2 private ip
+   `LOGGING` - CloudWatch logging

##### `settings.py`
```python
from configurations import Configuration
from django_configurations_ec2 import AllowedHostsMixin, LoggingMixin

class Prod(AllowedHostsMixin,Configuration):
    ALLOWED_HOSTS=['.domain.com']
```

CloudWatch
```python
from configurations import Configuration
from django_configurations_ec2 import LoggingMixin

class Prod(LoggingMixin,Configuration):
    ...
```

##### `.env`
```bash
DJANGO_AWS_ACCESS_KEY_ID=ACCESS_KEY_ID
DJANGO_AWS_SECRET_ACCESS_KEY=SECRET_ACCESS_KEY
DJANGO_AWS_REGION_NAME=REGION_NAME
DJANGO_AWS_LOG_GROUP=LOG_GROUP
DJANGO_AWS_STREAM_NAME=STREAM_NAME
```

#### Links
+   [django-configurations](https://github.com/jazzband/django-configurations)

<p align="center">
    <a href="https://readme42.com/">readme42.com</a>
</p>
