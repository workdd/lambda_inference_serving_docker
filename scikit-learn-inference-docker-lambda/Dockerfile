FROM public.ecr.aws/lambda/python:3.8

COPY requirements.txt ./
RUN python3.8 -m pip install -r requirements.txt -t .

COPY ./train-code/scikit_learn_iris.py ./
RUN python scikit_learn_iris.py

COPY ./app/app.py   ./

CMD ["app.handler"]
