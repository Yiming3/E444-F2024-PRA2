FROM python:3.12-slim
COPY . /app
WORKDIR /app
RUN pip install -r requirements.txt

ENV VIRTUAL_ENV=/home/app/venv

# python setup
RUN python -m venv $VIRTUAL_ENV
ENV PATH="$VIRTUAL_ENV/bin:$PATH"
RUN export FLASK_APP=app.py
RUN pip install -r requirements.txt

# define the port number the container should expose
EXPOSE 5001

CMD ["python", "app.py"]