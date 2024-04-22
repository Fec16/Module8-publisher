# Tutorial-8

### Reflection
1. How many data your publisher program will send to the message broker in one run? <br>
*The publisher program will send five pieces of data to the message broker in a single execution. This is because there are five calls to the `publish_event` method, each sending a `UserCreatedEventMessage` to the message broker.*

2. The url of: `amqp://guest:guest@localhost:5672` is the same as in the subscriber program, what does it mean? <br>
*The URL `amqp://guest:guest@localhost:5672` is commonly used to connect to a message broker using the Advanced Message Queuing Protocol (AMQP). In this URL:*
    - *`amqp://` specifies the protocol, which is AMQP.*
    - *`guest:guest` specifies the username and password for authentication. In this case, both the username and password are `guest`.*
    - *`localhost` specifies the hostname or IP address of the machine where the message broker is running. `localhost` means the message broker is running on the same machine as the program.*
    - *`5672` specifies the port number on which the message broker is listening for incoming connections. This is the default port for AMQP.*

    *If the publisher and subscriber programs utilize the same URL, it signifies that they're both linked to the identical message broker instance, operating on the same device, and employing identical authentication details and port number. This guarantees that the publisher can transmit messages to the same message broker instance subscribed by the subscriber.*