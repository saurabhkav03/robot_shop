FROM nginx

ENV CATALOGUE_HOST=catalogue \
    USER_HOST=user \
    CART_HOST=cart \
    SHIPPING_HOST=shipping \
    PAYMENT_HOST=payment \
    RATINGS_HOST=ratings

COPY web/default.conf.template /etc/nginx/conf.d/default.conf.template
COPY web/static /usr/share/nginx/html


EXPOSE 8080