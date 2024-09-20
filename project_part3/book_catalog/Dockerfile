# Your Solution
# Use an official Python runtime as the base image
FROM python:3.11-alpine

# Set the working directory in the container
WORKDIR /app/

# Copy the requirements.txt file into the container
COPY book_catalog/requirements.txt .

# Install required packages from requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Copy the entire book_catalog directory into the container
COPY /book_catalog/ .

# Expose port 9000 to allow external access to the FastAPI service
EXPOSE 9000

# Command to run the FastAPI application using uvicorn, listening on port 9000
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "9000"]
