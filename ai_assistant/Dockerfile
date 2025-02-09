# Use an official Python runtime as a parent image
FROM python

# Prevent python from writting .pyc files to disc & enable stdout/stderr logging
ENV PYTHONDONTWRITEBYTECODE=1 \
    PYTHONUNBUFFERED=1

# Set work directory
WORKDIR /app

# Install dependencies
COPY requirements.txt /app/
RUN pip install --upgrade pip && pip install -r requirements.txt

# Copy project
COPY . /app/

# Collect static files if needed
#RUN Python manage.py collecstatic --noinput

# Run server in dev environment
CMD ["python","manage.py","runserver", "0.0.0.0:8000"]

# In production start Gunicorn
#CMD ["gunicorn", "myproject.wsgi:application", "--bind", "0.0.0.0:8000"]

# Tip for the migrations
# Run manually after the container starts or usingt an entrypoint script (entrypoint.sh)