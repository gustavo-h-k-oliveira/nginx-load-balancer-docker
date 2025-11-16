FROM nginx:alpine
ARG INSTANCE_NAME=UNKNOWN

# Copia o build inteiro do Car Culture
COPY dist/ /usr/share/nginx/html/

# Insere a identificação da instância dentro do index.html
RUN sed -i "s/<!-- INSTANCE -->/${INSTANCE_NAME}/" /usr/share/nginx/html/index.html
