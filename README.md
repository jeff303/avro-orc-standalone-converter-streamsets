# avro-orc-standalone-converter-streamsets
Standalone Avro to ORC file converter using StreamSets Data Collector code.

## Building

### Dependencies

#### mapreduce-protolib

The project depends on a module called `mapreduce-protolib` from the
[StreamSets Data Collector](https://github.com/streamsets/datacollector/).  Unfortunately, the jar (and its
dependencies) are not published separately anywhere.  Therefore, you will need to do the following to prepare them.

##### Build from source
Follow the build instructions for the Data Collector project to get your environment set up, but the following Maven
command should be sufficient to build and install everything needed by this project:

    mvn install -DskipTests
    
### Build Command

This project uses Gradle wrapper.  Once the dependency mentioned above has been built, you can run the following
to build this project and generate its run script:

    ./gradlew install

## Running

Assuming the build command above completed successfully, the following command should work to run the conversion:

    build/install/avro-orc-standalone-converter-streamsets/bin/avro-orc-standalone-converter-streamsets /path/to/input.avro /path/to/output.orc

Simply replace the parameters with your own Avro input file, and output file to be generated.

