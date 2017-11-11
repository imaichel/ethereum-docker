FROM ethereum/client-go:v1.7.2

RUN apk add --update bash

COPY ./.ethereum/privchain /root/.ethereum/privchain

RUN geth --datadir /root/.ethereum/privchain init /root/.ethereum/privchain/genesis.json
