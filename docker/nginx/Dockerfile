FROM nginx

ARG SSL_CERTIFICATE
ARG SSL_CERTIFICATE_KEY

ENV SSL_CERTIFICATE=${SSL_CERTIFICATE}
ENV SSL_CERTIFICATE_KEY=${SSL_CERTIFICATE_KEY}

RUN printf '%s' "$SSL_CERTIFICATE" > /etc/nginx/ssl.cert
RUN printf '%s' "$SSL_CERTIFICATE_KEY" > /etc/nginx/ssl.key

COPY nginx/nginx.conf /etc/nginx/nginx.conf

EXPOSE 80 443