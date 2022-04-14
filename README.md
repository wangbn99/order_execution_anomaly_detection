# order_execution_anomaly_detection

## Machine Learning with PySpark

PySpark is an interface to Apache Spark in Python. It allows you to analyze data interactively in a distributed environment. If your data volume is large, such as transaction detail and execution data, you need to find a stable storage to store these daily data, and also you need to have a cheap and powerful computing tool to process and analyze this data. hadoop HDFS and Jupyter with pyspark is a good choice for you. PySpark provides some features such as Spark SQL, DataFrame and MLlib (machine learning), which is is really BA friendly.

## Data
The daily order execution data is stored in daily partition in hdfs as parquet format files. As a data scientist, we can extract some and save in our user dedicated folder as csv format file. The data schema is as follws:
```
Field name        Field type
Id                String
Symbol            String
LastMkt           String
Datetime          String
Brokerid          String
Traderid          String
Clientid          String
Account           String
Country           String
effectiveTime     String
expireTime        String
timeInForce       String
exposureDuration  String
tradingSession    String
tradingSessionSub String
settlType         String
settlDate         String
Currency          String
currencyFXRate    Float
execType          String
ExDestination     String
trdType           String
matchType         String
Side              String
OrdStatus         String
OrdType           String
orderQty          Int
Price             Float
exchangeCode      String
refQuoteId        String
refOrderId        String
trdPlatform       String
```
Please refer to https://www.onixs.biz/fix-dictionary/4.2/fields_by_name.html for the meaning of detailed data fields.
