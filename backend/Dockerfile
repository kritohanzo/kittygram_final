FROM python:3.9-slim-bullseye 
WORKDIR /app
COPY requirements/requirements.project.txt .
RUN pip install -r requirements.project.txt --no-cache-dir
COPY . .
ENTRYPOINT ["migrate_collect_static.sh"]
CMD ["gunicorn", "--bind", "0.0.0.0:9000", "kittygram_backend.wsgi"] 
