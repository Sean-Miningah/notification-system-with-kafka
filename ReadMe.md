# Realtime Notification System Using Go and Kafka 

Kafka is a distributed event streaming platform

### Kafka's core components 
#### Events 
Can be thought of as a message or a piece of data representing a change or an action. Consider an event 
* Event key: `"1"` (unique identifier of a user)
* Event value: `"Bruno started following you."`

#### Brokers 
Is a server that runs the Kafka software and stores data. 

#### Topics 
They represent categories under which data or events are stored.
For instance, a topic name is `"agents"`

#### Producers
Are entities that write messages to Kafka such a go/python program or service. When a producer has an event to send, it chooses a topic to address the event to 

#### Consumers 
Consumers read and process eventes or messages from Kafka. 
Consumers can subscribe to one or more topics to receive the messages. 

#### Partitions 
Each topic in Kafka can be further divided into partitions. They are segments with a topic that enable Kafka to manage data more efficiently.

#### Consumer Groups 
Individual consumers handle messages from specfic partitions, consumers groups manage coordination acros multiple consumers 

A consumer group consists of multiple consumers collaboratively processing messages from different partitions of a topic. This ensures that each message from a partition is processed by just one consumer in the group. 

#### Replicas 
Replicaton ensures data safety. In larget Kafka deployments, storing multiple data replicas is commmon to help recover from unexpected failures 

#### KRaft 
Manages metadata directly within Kafka