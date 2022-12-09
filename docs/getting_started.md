# Getting Started

#### Steps on getting started with the [IoT Management](https://github.com/vkylamba/IoT-Monitoring)
1. Install docker and docker-compose
2. Clone the [repo](https://github.com/vkylamba/IoT-Monitoring)
3. Change to the `IoT-Monitoring` directory
4. Create .env file from the template.  
   ```sh
        cp src/iot_server/env.template src/iot_server/env.template/.env
    ```
5. Start docker container with docker-compose:  
    ```sh
        docker-compose up
    ```
6. Create db `iotdatabase` in clickhouse with the root user with the following command:  
    ```sh
         echo " CREATE DATABASE iotdatabase;" | curl -u root:root http://localhost:8123/ --data-binary @-
    ```
