# POC2: Kafka -> Storm -> Kafka flow
Demonstrates filtering on Streaming data simulated via a Kafka topic.
Sample data used is [Airline Ontime](https://www.transtats.bts.gov/Tables.asp?DB_ID=120&DB_Name=Airline%20On-Time%20Performance%20Data&DB_Short_Name=On-Time) data. The (raw) data is filtered by Storm, and the cleaned-up data is pushed to another Kafka topic.

### Prerequisites
* Kafka running on localhost with a topic named `raw` and `proc`

### Building
`mvn package -DskipTests=true`

### Running
`{project-dir}$ storm jar target/poc2-1.1.1.jar org.pgmx.cloudpoc.poc2.topology.KafkaLocalReaderTopology`