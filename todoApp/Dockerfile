# Base image
FROM python:3.10-slim

# Set environment variables
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

# Set working directory
WORKDIR /app

# Install dependencies
COPY requirements.txt /app/
RUN pip install --upgrade pip && pip install -r requirements.txt

# Copy project files
COPY . /app/

# Expose port (change to your app's port if different)
EXPOSE 8000

# Run server (adjust if using different WSGI server or settings)
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
