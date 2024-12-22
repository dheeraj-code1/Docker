# Use a specific Ubuntu version for better reproducibility
FROM ubuntu:22.04

# ENV DEBIAN_FRONTEND=noninteractive


WORKDIR /app


COPY requirements.txt .
COPY devops .


RUN apt-get update && apt-get install -y python3 python3-pip  && pip3 install -r requirements.txt 


ENV PIP_BREAK_SYSTEM_PACKAGES 1


ENTRYPOINT ["python3"]
CMD ["manage.py", "runserver", "0.0.0.0:8000"]