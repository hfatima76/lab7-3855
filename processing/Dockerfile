#uses an ubuntu image
FROM ubuntu:latest
# install pythong an pip on top of the base images
RUN apt-get update && apt-get install -y python3 python3-pip
WORKDIR /app
# install all the dependencies from the requirement.txt file
COPY requirements.txt .
RUN pip3 install -r requirements.txt
# copy the application files to the image
COPY . .
# run the connextion application (app.py) when the image is run
CMD ["python3", "app.py"]
