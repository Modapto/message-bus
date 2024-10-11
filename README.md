# modapto-message-bus

## Overview

MODAPTO's Message Bus component is a Kafka Cluster deployment initialized with 3 Brokers and 3 Controllers utilizing KRaft algorithm to select leaders amongst the brokers.

An initial configuration is attached for the Message Bus deployment with some of the utilized topics. Additionally, the deployment comes with a Kafka UI, Kafka REST Proxy and Kafka Schema Registry.

## Table of Contents

1. [Installation](#installation)
2. [Deployment](#deployment)
3. [License](#license)
4. [Contributors](#contributors)

### Installation

Clone the repository:

```sh
git clone https://github.com/Modapto/message-bus.git
cd message-bus
```

### Deployment

1. Install or make sure Docker is running

2. Configure the .env file with the parameters required

3. Deploy Kafka Cluster from Docker Compose:

   ```sh
    docker compose --profile all up -d
   ```

4. After some time Kafka UI will be available on: `http://localhost:8095`.

5. To terminate Docker compose simply run:

    ```sh
    docker compose --profile all down
    ```

## License

This project has received funding from the European Union's Horizon 2022 research and innovation programm, under Grant Agreement 101091996.

For more details about the licence, see the [LICENSE](LICENSE) file.

## Contributors

- Alkis Aznavouridis (<a.aznavouridis@atc.gr>)
