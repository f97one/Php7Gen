FROM nginx:stable
ENV TZ Asia/Tokyo
RUN echo "${TZ}" > /etc/timezone \
    && dpkg-reconfigure -f noninteractive tzdata
