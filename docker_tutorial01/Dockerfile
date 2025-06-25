#Base image
# This is the base image that your Dockerfile will build upon.
FROM python:3.12  
#This tells Docker:
#"Start building my image using the official Python version 3.12 image."
# 🔍 What happens behind the scenes:
# - Docker downloads the python:3.11-slim image from Docker Hub.

#- It uses that as the base to build your own image.

#-  Then your instructions (COPY, RUN, etc.) are added on top of it.

WORKDIR /app 
# This sets the working directory inside the container to /app.


COPY ./app ./app

#🧠 Summary:
#Command	   | What it does
#COPY	         Copies files/folders from your PC to image
#COPY . .	     Copies everything from current dir
#COPY src/ /app	  Copies src/ into /app inside image


RUN pip install -r requirements.txt


EXPOSE 8000

CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8000"]

