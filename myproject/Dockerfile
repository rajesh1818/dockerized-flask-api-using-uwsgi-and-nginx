FROM python:3.8.0a2-stretch

WORKDIR /myproject
COPY . /myproject

RUN pip --no-cache-dir install -r /myproject/requirement.txt
RUN chmod +x /myproject/entrypoint.sh

ENV PYTHONPATH "${PYTHONPATH}:/myproject"

CMD ["uwsgi", "myproject.ini"]
