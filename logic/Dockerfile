FROM python:2.7.12

ENV PORT=4567
ENV FILLER_URL=http://localhost:4568
ENV CHARGER_URL=http://localhost:6082

ADD . /app/

RUN apt-get update && apt-get install -y nginx
RUN pip install flask requests

RUN useradd -ms /bin/bash usafe
RUN chown -R usafe:usafe /app

WORKDIR /app

USER usafe

EXPOSE $PORT

CMD ["python", "logic.py"]
