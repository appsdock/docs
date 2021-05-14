# Message Queue (AMQP)

AppsDock OS uses an AMQP based infrastructure to handle asynchronous messages, which allows executing long-running processes in the background by implementing async event handlers or async command executions via Message Bus within AppsDock OS.

## Composition

AppsDock OS provides a dedicated AMQP-Agent that acts as a consumer and mediator of messages. AppsDock OS avoids processing messages via CLI in consumer mode directly due to potential environment inequality between CLI and PHP-FPM and disregard of PHP-FPM process worker benefits. Instead, the dedicated AMQP-Agent consumes the messages from AMQP server and executes, controls and monitors asynchronous PHP-FPM process workers, which process the messages.  

![Service Structure](../assets/images/amqp/service-structure.svg)

### Publisher (AppsDock OS)

AppsDock OS uses the MessageBus component to publish messages to the AMQP server directly.  It does not provide any kind of consuming the published messages via AMQP server due to this responsibility is adopted by the AppsDock AMQP-Agent. Instead, AppsDock OS provides an internal and secured API endpoint to handle published messages which are provided by the AMQP-Agent. The handling of these messages over API uses also the MessageBus component.

### Consumer (AppsDock AMQP-Agent)

The dedicated AMQP-Agent, which is a part of the AppsDock Dedicated Services, is a scalable AMQP message consumer service. This service consumes the messages from the AMQP server directly and manage their processes and states in conjunction with PHP-FPM workers.

## Message Types (Subjects)

AppsDock OS does support actually two kinds of message types: **event** and **command**.

The **event** message type is used to handle asynchronous event handlers via MessageBus.
The **command** message type is used to execute asynchronous command handlers via MessageBus.

Each message type uses a separate message queue.

## Workflow



*[AMQP]: Advanced Message Queuing Protocol
*[OS]: Operating System
*[CLI]: Command Line Interface
*[PHP]: Hypertext Preprocessor
*[FPM]: FastCGI Process Manager 