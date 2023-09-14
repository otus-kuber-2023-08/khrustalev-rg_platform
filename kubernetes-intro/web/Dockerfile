FROM nginx:1.25.2
WORKDIR /app
RUN chown 1001:1001 /var/cache/nginx
RUN mkdir /etc/nginx/logs && chown -R 1001:1001 /etc/nginx/logs
RUN usermod -u 1001 www-data
COPY nginx.conf /etc/nginx/nginx.conf
COPY homework.html ./
USER 1001:1001
EXPOSE 8000