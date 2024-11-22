# modapto-message-bus

## Overview

MODAPTO's Message Bus component is a Kafka Cluster deployment initialized with 3 Brokers and 3 Controllers utilizing KRaft algorithm to select leaders amongst the brokers.

An initial configuration is attached for the Message Bus deployment with some of the utilized topics. Additionally, the deployment comes with a Kafka UI, Kafka REST Proxy and Kafka Schema Registry.

**NOTE:** At the moment only the single broker/controller deployment is supported. This configuration will be used for development purposes and in production the above setup will be configured.

## Table of Contents

1. [Installation](#installation)
2. [Deployment](#deployment)
3. [Usage](#usage)
4. [License](#license)
5. [Contributors](#contributors)

### Installation

Clone the repository:

```sh
git clone https://github.com/Modapto/message-bus.git
cd message-bus
```

### Deployment

1. Install or make sure Docker is running

2. Configure the .env for deployment and multi-brokers.env file with the parameters required

3. Deploy Kafka Cluster (Production) from Docker Compose:

    For Production:

   ```sh
    docker compose --profile all up -d
   ```

    For Development:

    ```sh
    docker compose -f docker-compose-single-broker.yml up -d
   ```

4. After some time Kafka UI will be available on: `http://localhost:8095`.

5. To terminate Docker compose simply run:

    For Production:

    ```sh
    docker compose --profile all down
    ```

    For Development:

    ```sh
    docker compose -f docker-compose-single-broker.yml down
    ```

### Usage

In order to use the Message Bus component in Production configure to connect to : **localhost:9095,localhost:9096,localhost:9097**, whilst for the Development connect to **localhost:9092**

## License

This project has received funding from the European Union's Horizon 2022 research and innovation programm, under Grant Agreement 101091996.

For more details about the licence, see the [LICENSE](LICENSE) file.

## Contributors

- Alkis Aznavouridis (<a.aznavouridis@atc.gr>)
