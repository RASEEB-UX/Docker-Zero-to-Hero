FROM python:3.12-slim

# Set up working directory
WORKDIR /app

# Copy the requirements file
COPY requirements.txt .

# Install virtual environment package if needed
RUN python3 -m venv /app/venv

# Activate virtual environment and install dependencies
RUN /app/venv/bin/pip install -r requirements.txt

# Copy the rest of the app code
COPY . .

# Use the virtual environment to run the app
CMD ["/app/venv/bin/python", "app.py"]
