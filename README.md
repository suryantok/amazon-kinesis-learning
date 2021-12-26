# Learning Amazon Kinesis Development

The master branch provides completed code for the [Process Real-Time Stock Data Using KPL and KCL Tutorial][learning-kinesis]  in the [Kinesis Developer Guide][kinesis-developer-guide].

The tutorial uses KCL 2.2.9 to demonstrate how to send a stream of records to Kinesis Data Streams and implement an application that consumes and processes the records in near-real time. 

[learning-kinesis]:  https://docs.aws.amazon.com/streams/latest/dev/tutorial-stock-data-kplkcl.html
[kinesis-developer-guide]: http://docs.aws.amazon.com/kinesis/latest/dev/introduction.html

## License Summary

This sample code is made available under the MIT-0 license. See the LICENSE file.

## Compile
`mvn clean compile assembly:single`

## Running 
**Producer:** `java -cp ./target/amazon-kinesis-learning-0.0.1-jar-with-dependencies.jar  com.amazonaws.services.kinesis.samples.stocktrades.writer.StockTradesWriter StockTradeStream <region>`

**Consumer:**  `java -cp ./target/amazon-kinesis-learning-0.0.1-jar-with-dependencies.jar  com.amazonaws.services.kinesis.samples.stocktrades.processor.StockTradesProcessor <appName> StockTradeStream <region>`
