FROM python:2.7-stretch
MAINTAINER Jules (landojules535@yahoo.fr)
RUN groupadd -r julesG -g 433 && \
    useradd -u 431 -r -g julesG -s /sbin/nologin -c "Docker image user" jules
RUN apt-get update -y && apt-get install python-dev python3-dev libsasl2-dev python-dev libldap2-dev libssl-dev -y
RUN pip install flask==1.1.2 flask_httpauth==4.1.0 flask_simpleldap python-dotenv==0.14.0
ADD student_age.py /
RUN mkdir /data
VOLUME ["/data"]
EXPOSE 5000
CMD [ "python", "./student_age.py" ]
USER jules
