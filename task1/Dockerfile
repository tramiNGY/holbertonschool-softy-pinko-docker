# based on the latest ubuntu
FROM ubuntu:latest
# Update APT using apt-get update
RUN apt-get update
# Upgrade currently installed software through APT using apt-get upgrade -y
RUN apt-get upgrade -y
# installation python3 and pip
RUN apt-get install -y python3 python3-pip
# delete external management
RUN rm -f /usr/lib/python*/EXTERNALLY-MANAGED
# install flask
RUN pip3 install flask
# Define working directory
WORKDIR /app
# Copy flask script to image
COPY ./api.py /app/api.py
# Run flask app
CMD ["python3", "api.py"]