FROM ethereum/client-go:v1.8.12

RUN apk add --update bash
RUN geth --datadir /root/.ethereum init /root/.ethereum/genesis.json
VOLUME ["/root/.ethereum"]
