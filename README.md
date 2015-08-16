# Gradle Kafka Test Plugin

>Apache Kafka is publish-subscribe messaging rethought as a distributed commit log.

[Gradle] plugin for managing an [Apache Kafka] instance for testing purposes in your build, e.g. before and after running integration tests of microservices with an event-based interface.

## Version
0.1.0

## Plugin Usage
To use the plugin, include in your build script:

    buildscript {
        repositories {
            jcenter()
       }
       dependencies {
           classpath 'com.adikanski:gradle-kafka-test-plugin:0.1.0'
        }
    }
## Task Types
There are two custom task types to start and shutdown a Kafka instance provided by the plugin

`KafkaTestStartTask` is used to spin up an instance of Kafka. This will also start a ZooKeeper instance, as it is a required for Kafka.

`KafkaTestShutdownTask` is used to shutdown both the Kafka and the ZooKeeper instance. All resources will be deleted, so that no messages and topics are kept between different restarts of the server instances.

### Usage Example

## Tech Acknowledgements
Gradle Kafka Test Plugin uses a number of open source projects to work properly:

* [Gradle] - _The_ Java build tool
* [Apache Curator] - An event bus and commit log
* [Apache Curator] - A ZooKeeper Keeper


License
----

MIT

[Gradle]:http://gradle.org
[Apache Kafka]:http://kafka.apache.org
[Apache Curator]:http://curator.apache.org
