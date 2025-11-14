# FROM openresty/openresty:alpine

# RUN apk add --no-cache build-base pcre-dev openssl-dev zlib-dev linux-headers curl

# # Download OpenResty source
# WORKDIR /usr/local/src
# RUN curl -L https://openresty.org/download/openresty-1.25.3.2.tar.gz -o openresty.tar.gz \
#     && tar -xzf openresty.tar.gz \
#     && cd openresty-* \
#     && ./configure \
#         --prefix=/opt/openresty \
#         --with-pcre-jit \
#         --with-ipv6 \
#         --without-http_redis2_module \
#         --with-http_iconv_module \
#         --with-http_postgres_module \
#         -j8 \
#     && make -j8 \
#     && make install


# COPY default.conf /usr/local/openresty/nginx/conf/conf.d/default.conf

# EXPOSE 80

# CMD ["/opt/openresty/nginx/sbin/nginx", "-g", "daemon off;"]

FROM openresty/openresty:alpine

COPY default.conf /etc/nginx/conf.d/default.conf

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
