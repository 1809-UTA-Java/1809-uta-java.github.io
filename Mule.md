# Mule
## Flows and Subflows 
A mule application can consist of a signle flow or break up processing into discrete flows and subflows which can be connected together. The latter is usually done in order to break applications into functional modules / error-handlers that can be used over and over again **(DRY)**. Flows and subflows are like function calls where events are passed in as inputs and modified events are what is returned. They can be connected with **Flow Reference components** under the component tab in your Mule Palette and other ways (not important right now).

** Flows ** typically start with a source, such as a HTTP listener, to trigger their executions. They can be configured to be initially stopped in the Runtime Manager for when you do not want a source to start a them right away. The **Flow Reference component** is used to trigger flows without a source. Individual flows should utilize **DRY** by having specific flows for:
- API requests from a web client
- processing the event
- returning an appropriate response
- etc.

**Subflow** is a scope that groups together a sequence of event processes (like a flow), but do not start with an event source and do not have their own error handling. They can be called from either another flow or sublfow through a **Flow Reference component**.

## Building Blocks
**Connectors**
- Endpoint
- Send and receive 
- Host, address, port

**Components**
- General
- Scripts
- Web services

**Transformers**
- Transforms and payloads

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