FROM python:3.9-slim

WORKDIR /app

# Copy the common directory
COPY ./common /app/common

# Copy the extraction application directory
COPY ./application/extraction /app/application/extraction

# Copy the requirements file
COPY ./application/extraction/requirements.txt /app/requirements.txt

# Install dependencies
RUN pip install --no-cache-dir -r /app/requirements.txt

# Set the Python path
ENV PYTHONPATH /app

# Run the extraction service
CMD ["python", "application/extraction/start_extraction.py"]
