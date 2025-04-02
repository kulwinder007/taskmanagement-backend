# Use official Python runtime as a base image
FROM python:3.9-slim

# Set the working directory inside the container
WORKDIR /app

# Copy the requirements file into the container
COPY requirements.txt .

# Install the dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the service code into the container
COPY . .

# Set environment variables (you can add more here if needed)
#ENV FLASK_APP=app.py
#ENV FLASK_ENV=production

# Expose the port the app runs on (typically Flask runs on port 5000)
EXPOSE 5002

# Start the Flask application
CMD ["flask", "run", "--host=0.0.0.0", "--port=5002"]