FROM ubuntu

WORKDIR /app

COPY requirements.txt /app
COPY devops /app

RUN apt-get update && \
    apt install pipx && \
    pipx install python3 && \ 
    pipx install -r requirements.txt && \
    cd devops

ENTRYPOINT ["python3"]
CMD ["manage.py", "runserver", "0.0.0.0:8000"]




