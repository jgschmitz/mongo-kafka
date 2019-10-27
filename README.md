# MongoDB Kafka Connector

The Super official MongoDB Kafka Connector.


## Documentation

See the [pre-release documentation](./docs/README.md)

## Downloading

The connector will be published on [maven central](https://search.maven.org/search?q=g:org.mongodb.kafka%20AND%20a:mongo-kafka-connect).

## Support / Feedback

For issues with, questions about, or feedback for the MongoDB Kafka Connector, please look into
our [support channels](https://docs.mongodb.com/manual/support/). Please do not email any of the developers directly with issues or
questions - you're more likely to get an answer on the [mongodb-user](https://groups.google.com/group/mongodb-user) discussion forum.

At a minimum, please include in your description the exact version of the driver that you are using.  If you are having
connectivity issues, it's often also useful to paste in the Kafka connector configuration. You should also check your application logs for
any connectivity-related exceptions and post those as well.

## Bugs / Feature Requests

Think you’ve found a bug? Want to see a new feature in the Kafka driver? Please open a case in our issue management tool, JIRA:

- [Create an account and login](https://jira.mongodb.org).
- Navigate to [the KAFKA project](https://jira.mongodb.org/browse/KAFKA).
- Click **Create Issue** - Please provide as much information as possible about the issue type and how to reproduce it.

Bug reports in JIRA for the connector are **public**.

If you’ve identified a security vulnerability in a connector or any other MongoDB project, please report it according to the
[instructions here](https://docs.mongodb.com/manual/tutorial/create-a-vulnerability-report/).

## Versioning

The MongoDB Kafka Connector follows semantic versioning.
See the [changelog](./doc/changelog.md) for information about changes between releases.

## Build

### Note: The following instructions are intended for internal use.

Java 8+ is required to build and compile the source. To build and test the driver:

```
$ git clone https://github.com/mongodb/mongo-kafka.git
$ cd mongo-kafka
$ ./gradlew check -Dorg.mongodb.test.uri=mongodb://localhost:27017
```

The test suite requires mongod to be running. Note, the source connector requires a replicaSet.

## Maintainers

* Ross Lawley          ross@mongodb.com

Original Sink connector work by: Hans-Peter Grahsl : https://github.com/hpgrahsl/kafka-connect-mongodb

Additional contributors can be found [here](https://github.com/mongodb/mongo-kafka/graphs/contributors).

## IntelliJ IDEA

A couple of manual configuration steps are required to run the code in IntelliJ:

  - **Error:** `java: cannot find symbol. symbol: variable Versions`<br>
    **Fixes:** Any of the following: <br>
      - Run the `compileBuildConfig` task: eg: `./gradlew compileBuildConfig` or via Gradle > mongo-kafka > Tasks > other > compileBuildConfig
      - Set `compileBuildConfig` to execute Before Build. via Gradle > Tasks > other > right click compileBuildConfig - click on "Execute Before Build"
      - Delegate all build actions to Gradle: Settings > Build, Execution, Deployment > Build Tools > Gradle > Runner - tick "Delegate IDE build/run actions to gradle"
