from docker.io/nginx
EXPOSE 8080
RUN chgrp 0 -R  /etc/nginx/ && \
    chgrp 0 -R /var/cache/nginx/ && \
    chgrp 0 -R /usr/share/nginx/ && \
    chgrp 0 -R /var/run && \
    chmod 770 -R /usr/share/nginx/ && \
    chmod 770 -R /var/cache/nginx/ && \
    chmod 770 -R /usr/share/nginx/ && \
    chmod 770 -R /var/run/

COPY nginx.conf /etc/nginx/conf.d/default.conf
copy dist/ /usr/share/nginx/html/


ENTRYPOINT [ "nginx", "-g","daemon off;"]