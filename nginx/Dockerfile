FROM nginx:alpine
COPY ./default.conf /tmp/default.conf.temp
ENV FLASK_APP_HOST=flask_app
ENV FLASK_APP_PORT=5000
RUN sed  's@FLASK_APP_HOST@'"$FLASK_APP_HOST"'@' /tmp/default.conf.temp > /tmp/default.conf.ip
RUN sed  's@FLASK_APP_PORT@'"$FLASK_APP_PORT"'@' /tmp/default.conf.ip > /etc/nginx/conf.d/default.conf