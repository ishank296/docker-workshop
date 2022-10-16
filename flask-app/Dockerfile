#base image
FROM python:3.8
#change working directory
WORKDIR usr/src/app
# copy current dir files from local machine to containter
COPY ..
# execute command to install dependies
RUN pip install -r requirements.txt
# expose port on which the application will run
EXPOSE 5000
CMD ['python','./app.py']
