# CRON Parser utility

This java based utility is used to parse the given Cron expression of the below input fields.

[minute] [hour] [day of month] [month] [day of week] [command]

Apache Maven is used to the build and to run the unit tests of the utility.

## Limitations

This utility doesn't handle @yearly.

Day of the month doesn't verify if a month has Less than 31 days or not. 

This utility doesn't handle L W and ? characters in the Cron Expression.

## Steps to Build the application
Java 8 or more and Apache maven 3.1.X version is required to build the application.

From the project root, Run the below maven command to build and unit test the application:

mvn clean install

## Steps to Run the utility:

1) Download CronParserTakeHome.jar

2) Open Command Line tool and cd to the folder that contains the downloaded jar.

3) Run the Below command to use the utility

java -jar CronParserTakeHome.jar Cron_expression 

Example:

```bash
java -jar CronParserTakeHome.jar "*/15 0 1,15 * 1-5 /usr/bin/find"
```

For the input Cron expression "*/15 0 1,15 * 1-5 /usr/bin/find" the expected output is as below:

```bash
minute        0 15 30 45
hour          0
day of month  1 15
month         1 2 3 4 5 6 7 8 9 10 11 12
day of week   1 2 3 4 5
command       /usr/bin/find
```


