# Message Queue (AMQP)

AppsDock OS uses an AMQP based infrastructure to handle asynchronous messages, which allows executing long-running processes in the background by implementing async event handlers or async command executions via Message Bus within AppsDock OS.

## Composition

AppsDock OS provides a dedicated AMQP-Agent that acts as a consumer and mediator of messages. AppsDock OS avoids processing messages via CLI in consumer mode directly due to potential environment inequality between CLI and PHP-FPM and disregard of PHP-FPM process worker benefits. Instead, the dedicated AMQP-Agent consumes the messages from AMQP server and executes, controls and monitors asynchronous PHP-FPM process workers, which process the messages.  

![Service Structure](../assets/images/amqp/service-structure.svg)

*[AMQP]: Advanced Message Queuing Protocol
*[OS]: Operating System