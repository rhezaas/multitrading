# Stock Services

## Overview
I made this project to learn how multithreading works in java. The idea is to publish raw data and send it to the message broker, i'm using kafka in this case, and the consumer need to summarize the data to find the highest and the lowest price.

### Service #1
```
Read the provided text "raw.txt" and broadcast line by line to Kafka as the message broker.
```

### Service #2
```
Read the data from message broker summarize the data to find the highest and lowest price (per stock symbol).
```

## How to run

```bash
# Add kafka to your hosts
sudo nano /etc/hosts
127.0.0.1 kafka

# running docker compose
docker-compose -f docker-compose.yml up

# run service #2
./gradlew runConsumer

# run service #1
./gradlew runProducer

# output file at "output.txt"
```