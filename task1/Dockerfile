FROM ubuntu:latest

# Update & upgrade
RUN apt-get update && apt-get upgrade -y

# Install Python and pip
RUN apt-get install -y python3 python3-pip

# Fix externally managed error (vacibdir!)
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Install Flask with pip3
RUN pip3 install flask

# Set working directory
WORKDIR /app

# Copy api.py into container
COPY ./api.py /app/api.py

# Run Flask app
CMD ["python3", "/app/api.py"]
