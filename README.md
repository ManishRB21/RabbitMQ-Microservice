### RabbitMQ Microservices with Node.js

This project implements Node.js microservices using RabbitMQ with a direct exchange type.

#### Components:

- *Consumers:*
  - `loggerMS`
  - `ErrorMS`

- *Producer:*
  - `infoMS`

#### Idea:

Make an API call to create a log by specifying the log type, which serves as the message routing key. The direct exchange then routes the message to the appropriate queues. `loggerMS` and `warningAndErrorMS` act as consumers, each listening on different queues with their own binding keys.

#### Running RabbitMQ with Docker:

- bash
  - `docker pull rabbitmq:3.10-management`
  - `docker run --rm -it -p 15672:15672 -p 5672:5672 rabbitmq:3.10-management`


Visit [http://localhost:15672](http://localhost:15672) for the RabbitMQ management website. Use the default credentials `guest/guest` to log in.

Feel free to customize this README for your GitHub repository. If you have any questions or need further assistance, don't hesitate to ask.
