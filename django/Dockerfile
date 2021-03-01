# Base Image
FROM python:3.9.2

# Working Directory
WORKDIR /share

# Update and Installation
RUN apt-get update && \
  apt-get upgrade -y && \
  apt-get install -y git && \
  apt-get install -y default-mysql-client && \
  apt-get install -y gettext && \
  rm -rf /var/lib/apt/lists/*

# Python Package Install
ADD requirements.txt .
RUN pip install --trusted-host pypi.python.org -r requirements.txt

# Port
EXPOSE 8000

# Command
CMD ["/bin/bash"]
