ARG BUILD_FROM
FROM ${BUILD_FROM}

RUN apk add --no-cache jq git

ARG BUILD_VERSION
RUN git clone --depth 1 https://github.com/tobsch/mcp-picnic.git /app
WORKDIR /app
RUN npm install && npm run build

COPY run.sh /run.sh
RUN chmod +x /run.sh

CMD ["/run.sh"]
