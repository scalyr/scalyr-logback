Scalyr Logging
---

This library provides a simple Appender implementation to send log messages to the [Scalyr](https://www.scalyr.com) logging service using [logback](http://logback.qos.ch/) or [log4J](http://logging.apache.org/log4j/1.2/).
With this library, any Java code which uses the log4j or logback APIs can easily integrate with Scalyr.

To use this Appender:

1. Add the appropriate dependency to your project ([logback](https://github.com/scalyr/scalyr-logback/tree/master/scalyr-logback)) or [log4j](https://github.com/scalyr/scalyr-logback/tree/master/scalyr-log4j))
2. Configure Scalyr:
  * LogBack: In your logback configuration file, add a com.scalyr.logback.ScalyrAppender. See sample [logback.groovy](https://github.com/scalyr/scalyr-logback/blob/master/scalyr-logback/src/test/resources/logback.groovy)
  * Log4J: In your log4J configuration file, add a com.scalyr.log4j.ScalyrAppender. See sample [log4j.properties](https://github.com/scalyr/scalyr-logback/blob/master/scalyr-log4j/src/test/resources/log4j.properties)
3. Once you have log messages flowing into Scalyr, you can set up parsing rules. The easiest way to do that is to go to https://www.scalyr.com/parsers?parser=logback and click the "Leave It to Us" button. This will send a sample of your log data to the Scalyr staff, and we'll respond the same day with a custom-built parser.

See the [LogBack test](https://github.com/scalyr/scalyr-logback/blob/master/scalyr-logback/src/test/java/com/scalyr/logback/Test.java) for usage examples.
