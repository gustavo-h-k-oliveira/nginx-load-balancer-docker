FROM nginx:alpine

ARG INSTANCE_NAME=UNKNOWN
ENV INSTANCE_NAME=${INSTANCE_NAME}

# esta linha força o cache a invalidar quando INSTANCE_NAME muda
RUN echo "Building instance ${INSTANCE_NAME}"

COPY index.html /usr/share/nginx/html/index.html
RUN sed -i "s/<!-- INSTANCE -->/${INSTANCE_NAME}/" /usr/share/nginx/html/index.html
