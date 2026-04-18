# Use the latest version of Ubuntu as a parent image
FROM ubuntu:latest

# Update the package lists
RUN apt-get update

# Upgrade installed packages
RUN apt-get upgrade -y

# Install Python3 and pip3
RUN apt-get install -y python3 python3-pip

# Fix externally managed environment issue
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Install Flask using pip3
RUN pip3 install flask
RUN pip3 install flask-cors

# Set the working directory
WORKDIR /app

# Copy api.py into the container
COPY ./api.py /app/api.py

# Run the Flask app
CMD ["python3", "api.py"]
