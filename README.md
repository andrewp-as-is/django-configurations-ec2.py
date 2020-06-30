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
+   `ALLOWED_HOSTS` - appends EC2 private ip
+   `LOGGING` - CloudWatch logs

##### `settings.py`
```python
from django_configurations_ec2 import EC2Configuration

class Prod(EC2Configuration,...):
    ALLOWED_HOSTS=['.domain.com']
```

##### `.env`
```bash
DJANGO_AWS_CLOUDWATCH_ENABLED=true # optional, default true
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