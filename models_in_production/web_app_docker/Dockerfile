FROM ubuntu:18.04

RUN apt-get update && apt-get install -y python3 python3-pip sudo

RUN useradd -m userdev

RUN chown -R userdev:userdev /home/userdev/

COPY --chown=userdev . /home/userdev/app

USER userdev

RUN cd /home/userdev/app/ && pip3 install -r requirements.txt

WORKDIR /home/userdev/app

EXPOSE 5000

ENV NAME Opentoall

CMD ["python3","app.py"]
