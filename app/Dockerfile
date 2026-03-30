FROM python:3.14.3-alpine
COPY requirements.txt /
# layer caching in docker means this will only install if requirements have changed
RUN pip install -r /requirements.txt
COPY . /python_server
WORKDIR /python_server
EXPOSE 8001
CMD ["python", "main.py"]
