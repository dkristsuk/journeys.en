---
title: Constants
seo-title: Constants
description: Constants
seo-description: Learn about constants in advanced conditions
page-status-flag: never-activated
uuid: 269d590c-5a6d-40b9-a879-02f5033863fc
contentOwner: sauviat
products: SG_CAMPAIGN/CLASSIC
audience: rns
content-type: reference
topic-tags: journeys
discoiquuid: 5df34f55-135a-4ea8-afc2-f9427ce5ae7b
index: n
internal: n
snippet: y
---

# Constants {#concept_gp3_rj5_dgb}

Technically, a constant always contains a data type. In the literal expression, we only specify the value. The data type can be inferred from the value (for example string, integer, decimal, etc.). For specific cases such as time zones, we use dedicated functions for the representation: _toTimeZone("Europe/Paris")_.

Here is how constant expressions are represented:

|Data Type|Description|Literal Representation|Example|
|--- |--- |--- |--- |
|string|Common sequence of characters. It doesn't have any specific size except the implicit one that comes from the environment such as the amount of memory available.JSON format: StringSerialization format: UTF-8|`"<value>"``'<value>'`|`"hello world"` `'hello world'`|
|integer|Integer value from -2^63 to 2^63-1.JSON format: Number|`<integer value>`|42|
|decimal|Decimal number. It represents a floating value:largest positive finite value of type double, (2-2^-52)x2^1023smallest positive normal value of type double, 2-1022smallest positive nonzero value of type double, 2 p-1074JSON format: NumberSerialization format: using '.' as the decimal separator.|`<integer value>.<integer value>`|`3.14`|
|boolean|Boolean value written lowercase: true or falseJSON format: Boolean|`true` `false`|`true`|
|dateTimeOnly|It represents a date-time without a time-zone, often viewed as year-month-day-hour-minute-second-millisecond.It does not store or represent a time-zone. Instead, it is a description of the date, as used for birthdays, combined with the local time as seen on a wall clock. It cannot represent an instant on the time-line without additional information such as an offset or time-zone.Serialization format: ISO-8601 extended offset date-time format. It uses DateTimeFormatter.ISO_LOCAL_DATE_TIME to deserialize and serialize the value. [Learn more](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html#ISO_LOCAL_DATE_TIME)).|`toDateTimeOnly("<dateTimeOnly in ISO-8601 format>")``toDateTimeOnly(<year>, <month>, <day>, <hour>, <minute>, <second>)`|`toDateTimeOnly("1977-04-22T06:00:00")``toDateTimeOnly(1977, 4, 22, 6, 0, 0")`Examples of serialized dateTimeOnly:`2011-12-03T15:15:30``2011-12-03T15:15:30.123`|
|dateTime|Date time constant that also considers time zone.It represents a date-time with an offset from UTC. It can be viewed as an instant in time with the additional information of the offset. It is a way to represent a specific “moment” at a certain place of the world.JSON format: String. It must be encapsulated in a toDateTime function.Serialization format: ISO-8601 extended offset date-time format. It uses DateTimeFormatter.ISO_OFFSET_DATE_TIME to deserialize and serialize the value. [Learn more](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html#ISO_OFFSET_DATE_TIME). You can also pass an integer passing an epoch value. [Read more](https://www.epochconverter.com/).Timezone can be specified by an offset or a timezone code (example: Europe/Paris, Z - meaning UTC).|`toDateTime("<dateTime in ISO-8601 format>")``toDateTime(<integer value of an epoch in milliseconds>)`|toDateTime("1977-04-22T06:00:00Z")toDateTime("2011-12-03T15:15:30Z")toDateTime("2011-12-03T15:15:30.123Z")toDateTime("2011-12-03T15:15:30.123+02:00")toDateTime("2011-12-03T15:15:30.123-00:20")toDateTime(1560762190189)|
|timeZone|Id of a time zone using the java implementation such as "Europe/Paris".JSON format: String. It must be encapsulated in a TimeZone function.Serialization format: to deserialize a time zone ID, it uses the java function java.time.ZoneId.of. [Learn more](https://docs.oracle.com/javase/8/docs/api/java/time/ZoneId.html#of-java.lang.String-).|`toTimeZone("<time zone id>"`)|toTimeZone("Europe/Paris")|
|duration|It represents a time-based amount of time, such as '34.5 seconds'. It models a quantity or amount of time in terms of milliseconds.The supported temporal units are:milliseconds,seconds,minutes, hours, days with one day equals to 24 hours. Years and months are not supported since they're not a fixed amount of time. JSON format: String. It must be encapsulated in a toDuration function.Serialization format: To deserialize a time zone ID, it uses the java function java.time.Duration.parse: the formats accepted are based on the ISO-8601 duration format PnDTnHnMn.nS with days considered to be exactly 24 hours.[Learn more](https://docs.oracle.com/javase/8/docs/api/java/time/Duration.html#parse-java.lang.CharSequence-).|`toDuration("<duration in ISO-8601 format>")``toDuration(<duration in milliseconds>)`|`toDuration("PT5S") // 5 seconds``toDuration(500) // 500mstoDuration("PT20.345S") -- parses as "20.345 seconds"``toDuration("PT15M")     -- parses as "15 minutes" (where a minute is 60 seconds)``toDuration("PT10H")     -- parses as "10 hours" (where an hour is 3600 seconds)``toDuration("P2D")       -- parses as "2 days" (where a day is 24 hours or 86400 seconds)``toDuration("P2DT3H4M")  -- parses as "2 days, 3 hours and 4 minutes"``toDuration("P-6H3M")    -- parses as "-6 hours and +3 minutes"``toDuration("-P6H3M")    -- parses as "-6 hours and -3 minutes"``toDuration("-P-6H+3M")  -- parses as "+6 hours and -3 minutes"`|
|list|Comma separated list of expressions using square brackets as delimiters. Polymorphism is not supported, hence all the expressions contained in the list should have the same type.|`[<expression>, <expression>, ... ]`|["value1","value2"][3,5][toDuration(500),toDuration(800)]|