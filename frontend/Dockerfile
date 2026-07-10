#1. Its working
# FROM nginx
# COPY code /usr/share/nginx/html
# # RUN rm -rf /etc/nginx/nginx.conf
# RUN rm -rf /etc/nginx/conf.d/default.conf
# COPY nginx.conf /etc/nginx/nginx.conf
# COPY expense.conf /etc/nginx/default.d/expense.conf

#its not working
# FROM nginx
# COPY code /usr/share/nginx/html
# # RUN rm -rf /etc/nginx/nginx.conf
# # RUN rm -rf /etc/nginx/conf.d/default.conf
# # COPY nginx.conf /etc/nginx/nginx.conf
# # COPY expense.conf /etc/nginx/default.d/expense.conf


#2. Host network
FROM nginx
COPY code /usr/share/nginx/html
# RUN rm -rf /etc/nginx/nginx.conf
RUN rm -rf /etc/nginx/conf.d/default.conf
COPY nginx.conf /etc/nginx/nginx.conf
COPY expense.conf /etc/nginx/default.d/expense.conf