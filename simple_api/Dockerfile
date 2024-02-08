FROM python:2.7-buster
WORKDIR /
COPY . /
RUN apt-get update -y && apt-get install python-dev python3-dev libsasl2-dev libldap2-dev libssl-dev -y
RUN pip install flask==1.1.2 flask_httpauth==4.1.0 flask_simpleldap python-dotenv==0.14.0
VOLUME "/data"
EXPOSE 5000
ENV student_age_file_path student_age.json
CMD ["python", "student_age.py"]
