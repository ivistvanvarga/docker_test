FROM nginx:1.16.0

EXPOSE 8080/tcp
EXPOSE 80/tcp

LABEL maintainer="iv.istvan.varga@gmail.com"
COPY nginx.conf /etc/nginx/nginx.conf

# openssl req -x509 -newkey rsa:4096 -keyout privkey.pem -out cert.pem -days 365 -nodes -subj '/CN=nginx'
COPY certificates /etc/nginx/certificates


