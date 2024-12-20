

FROM python:3.9-slim

# Upgrade pip to the latest version
RUN pip install --no-cache-dir --upgrade pip

# Set the working directory
WORKDIR /app

# Copy the requirements file and install dependencies
COPY requirements.txt /app
RUN pip install --no-cache-dir -r requirements.txt

# Copy the application files
COPY devops /app/devops

# Expose the application port
EXPOSE 8000

# Run the application
CMD ["python3", "/app/devops/manage.py", "runserver", "0.0.0.0:8000"]
