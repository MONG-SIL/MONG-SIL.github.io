---
layout: post
title: Get Started with Kafka
color: rgb(147, 85, 41)
tags: [kafka]
---

[Kafka ®](https://kafka.apache.org/) is part of the apache foundation and is described as a distributed streaming platform that
is used for building real-time data pipelines and streaming apps. 
It is horizontally scalable, fault-tolerant, wicked fast, and runs in production in thousands of companies.

![kafka logo](https://raw.githubusercontent.com/sylhare/kafka/master/logo.png)

> Check the Kotlin Kafka examples for developers at [sylhare/kafka](https://github.com/sylhare/kafka)


## Introduction to Kafka Platform

### Topics

Producer writes to a `topic`.
Consumers polls and reads the messages from `topic`.
Messages can be read multiple times depending on your retention policy. (Which offsets when you are going to read from) 

### with Broker

`Topics` are more efficient when they are on multiple `partitions`. 
Those `partitions` are on one or multiple `brokers`, which are used for resilience, because if one `broker` goes done the messages
written / read on the `Topic` will still be able to be processed by other `brokers`.

With no keys the messages or record will be sent to the partition using round robin. If there is a key, 
it will use this key to define the partition example:
```
5 partition, message with key = 7 -> <key> mod( <partition> ) = 2 
> Which mean message of key 7 will go to partition 2 in this case.
```

### Replicas 

You can set a replica factor so that you will have a replica of each of the Topic partition in the other brokers.
Ideally you set it to three, those wil create ISR `in sync replicas`.

The event is first sent to the leader then when it has committed on the transaction log, the event is sent to the next follower.
Replicas are identical up to a specified point called the high-water mark which correspond to the last committed message.
After each event processed by the leader it will then rise the high water mark for the replicas to process.

The data retention is made with the segments which are files that stores/logs the events that have been sent on the partition.
Messages that are read are said to be `committed` to the log. So we know which message has been listened to and when.
If a consumer fails to read a message, another consumer can review the log to start back at the right event in the queue.

## Configuration Elements

ACK -> Acknowledge. There are three settings :
  - `acks=0` will not wait for the acknowledgement of the server
  - `acks=1` will wait for the leader to write on local log
  - `ack=all` Producer will wait for all in sync replicas (ISR) to have acknowledged the receipt of the record within delivery time

The `retries` for the amount of time it will retry (Until `MAX_INT`).
You can set a `retry.backoff.ms` to pause in between retries. (default to 100ms)    

The `delivery.timeout.ms` puts a limit to report the result or failure from a producer:
send() - batching - awaits send - retry - back off 

The offset is a simple integer number that is used by Kafka to maintain the current position of a consumer.
The `auto-offset-reset` can be set to:
 - `earliest` Go through all of the record since it lost the offset  
 - `latest` Go from the latest record when the offset is lost

## Interact with Kafka

There are usually two types of applications interacting with it:
- Producers that writes data
- Customers that read those data and react / transform them

### Producers 

`Producers` publish data (records) to the topics of their choice. 
The producer is responsible for choosing which record to assign to which partition within the topic. 
This can be done in a round-robin fashion simply to balance load or it can be done according to some semantic partition function (say based on some key in the record). 

### Consumers

Consumers label themselves with a consumer group name.
Consumer instances can be in separate processes or on separate machines. 

Consumers get the data in the partitions that was published by the producer.
Depending on the consumer that reads on the partition the record will be either: 
 - broadcast to all consumer groups that have the consumer in it
 - load balanced between consumers within the same consumer group

Everything will be handled by Kafka and can be configurable.

### Stream API

Kafka allows you to read all the records as stream and perform operation on them.
That Stream API allows to make even more performing consumers.

If you are familiar with java `stream()` or functional programming, then you know how
powerful streams can be. 

## Data Format

Kafka don't do well with big files `message.max.bytes` is recommended to 1mb.
Plain text is not very efficient, everything needs to be converted to text.
We want to use a schema to structure the data.

Avro (an other apache open source project) used for serialization of the data.
It's like an optimized json, faster to process and more robust ot change.


