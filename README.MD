1. Install deps:

```
pip install -r requirements.txt 
```
2. Run broker

```
docker run -d -p 5672:5672 rabbitmq
```
3. Set you TWILIO_ACCOUNT_SID and TWILIO_AUTH_TOKEN environment variables.
```
export TWILIO_ACCOUNT_SID='foo'
export TWILIO_AUTH_TOKEN='foo'
```
4. Run worker process.

```
celery -A djangoProject1 worker -l INFO
```

5. Run Django web server

```
python manage.py runserver
```