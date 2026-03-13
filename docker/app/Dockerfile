FROM golang:1.25

RUN go install github.com/cespare/reflex@v0.3.1

COPY reflex.conf /
COPY start.sh /
COPY entrypoint.sh /

RUN sed -i 's/\r$//' /entrypoint.sh \
 && sed -i 's/\r$//' /start.sh \
 && chmod +x /entrypoint.sh /start.sh

ENTRYPOINT ["/entrypoint.sh"]
