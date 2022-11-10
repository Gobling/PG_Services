FROM ubuntu

# Update Linux
RUN apt-get update
RUN apt-get dist-upgrade

# Install components
RUN apt-get install pip -y
RUN pip install Pillow

RUN apt-get install git -y
RUN pip install Flask
RUN pip install -U flask-cors
RUN pip install requests

# Copy the python code file into the docker container
COPY fileserver.py /fileserver/

# Start the server
CMD ["python3", "/fileserver/fileserver.py"]
