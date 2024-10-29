# Use Python base image
FROM python:3.9-slim

# Set the working directory
WORKDIR /usr/src/app

# Copy the application code
COPY app.py .

# Expose the web server port
EXPOSE 8000

# Run the Python HTTP server
CMD ["python", "app.py"]