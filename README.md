Welcome to your new Kafka Connect connector!

# Running in development

```
mvn clean package
export CLASSPATH="$(find target/ -type f -name '*.jar'| grep '\-package' | tr '\n' ':')"
$CONFLUENT_HOME/bin/connect-standalone $CONFLUENT_HOME/etc/schema-registry/connect-avro-standalone.properties config/MySourceConnector.properties
```


# Generate this base project using Maven (example below)

```
mvn archetype:generate -B -DarchetypeGroupId=io.confluent.maven -DarchetypeArtifactId=kafka-connect-quickstart -DarchetypeVersion=0.10.0.0 -Dpackage=com.github.navnandan.kafka.connect.base -DgroupId=com.github.navnandan.kafka.connect.base -DartifactId=kafka-connect-base -Dversion=1.0-SNAPSHOT
```
