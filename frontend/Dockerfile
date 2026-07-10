FROM nginx
COPY code /usr/share/nginx/html
# COPY expense.conf /etc/nginx/default.d/expense.conf
RUN rm -rf /etc/nginx/nginx.conf
COPY nginx.conf /etc/nginx/nginx.conf
COPY expense.conf /etc/nginx/default/expense.conf