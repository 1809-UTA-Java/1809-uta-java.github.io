# Mule
## Mule Event
An event source receives a trigger (HTTP, JDBC, FTP, JMS) and create a corresponding mule event object and forwards the processing. Mule events are immutable. Any change to an instance of a mule event results in the creation of a new mule event instance. An event is composed of a ** MuleMessage **, ** MuleSession **, and ** MuleContext **. 

## Messages
** Mule Message ** is composed of different parts:
- payload
- properties
- attachments (optional)
- exception payload (optional)

** Message Sources ** can be inbound endpoints, pollers, or cloud connectors. Only a single message source is allowed in a flow. A composite message source must be used to allow for multiple inbound endpoints.

** Message Processors ** take care of performing all the message handling operations in Mule. They include:
- ** outbound endpoints: ** dispatch messages to whatever destination you want
- ** transformers: ** modify messages
- ** routers: ** ensure messages are disturbed to the right destinations
- ** components: ** perform business operations on messages

** Message Exchange Patterns (MEP) ** define the timely coupling that will occur at a particular inbound or outbound endpoint. 
- ** One-way ** where no synchronous response is expected from the interaction but will still receive status code of sent message
- ** Resquest-response ** where a synchronous response is expected so it'll wait for a response before proceeding

## Flows 
A mule application can consist of a signle flow or break up processing into discrete flows and subflows which can be connected together. The latter is usually done in order to break applications into functional modules / error-handlers that can be used over and over again **(DRY)**. Flows and subflows are like function calls where events are passed in as inputs and modified events are what is returned. They can be connected with **Flow Reference components** under the component tab in your Mule Palette and other ways (not important right now).

** Flows ** typically start with a source, such as a HTTP listener, to trigger their executions. They can be configured to be initially stopped in the Runtime Manager for when you do not want a source to start a them right away. The **Flow Reference component** is used to trigger flows without a source. Individual flows should utilize **DRY** by having specific flows for:
- API requests from a web client
- processing the event
- returning an appropriate response
- etc.

**Subflow** is a scope that groups together a sequence of event processes (like a flow), but do not start with an event source and do not have their own error handling. They can be called from either another flow or sublfow through a **Flow Reference component**. The whole mule message is passed & its context are passed into a subflow. The complete context of the result of the subflow is passed back to the main flow.

** Private Flows ** are another type of reusable flow. Private flows:
- can define a different processing / exception strategy from the calling flow
- are materialized at runtime meaning they have specific statistics and debug properties attached to them
- can be controlled & monitored independently 

## Building Blocks
**Connectors**
- Endpoint
- Send and receive 
- Host, address, port

**Components**
- General
- Transform message
- Logger
- Flow reference
- Scripts
- Web services

**Transformers** (components used to set or remove part of the Mule event)
- Transforms
- Set payload
- Set variable
- Remove variable

**Filters**
- 12 + included
- and, or, not
- Custom

**Routers**
- Message flow
- Splitting
- Re-sequencing
- Aggregation

**Scopes**
- Wrappers
- Processing blocks

**Exception Strategies**
- Errors 
- Faults
- Strategies

## OTHER
** RAML ** stands for RESTful API Modeling Language. It is designed to describe a RESTful API.

** Saas ** is a software as a service. Examples are Netflix, Amazon Prime, Google apps, etc. Elimnates the need to install and run apps on individual computers.
