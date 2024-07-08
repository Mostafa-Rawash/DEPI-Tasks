FROM alpine

# WORKDIR /flask-app

RUN apk add --no-cache python3 py3-pip

COPY requirements.txt .

RUN python3 -m venv venv
RUN source venv/bin/activate

RUN venv/bin/pip3 install --no-cache-dir -r requirements.txt

COPY app.py .

EXPOSE 5000


CMD ["venv/bin/python3", "app.py"]
