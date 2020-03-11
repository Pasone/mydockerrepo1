# our base image
FROM alpine

# Install python and pip
RUN apk add --update py-pip

# install Python modules needed by the Python app
COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

# copy files required for the app to run
COPY app.py /usr/src/app/
COPY templates/index.html /usr/src/app/templates/

# tell the port number the container should expose
EXPOSE 5000

# run the application
CMD ["python", "/usr/src/app/app.py"]
