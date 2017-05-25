# log4js-aliyun-log
This is a aliyun simple log service appender for log4js.

#Installation

    npm install log4js-aliyun-log --save

#Configuration

/config/logTest.json

    "appenders": {
      "type": "log4js-aliyun-log",
      "layout": {
        "type": "pattern",
        "pattern": "%p %c %m"
      },
      "aliyunKey":"aliyunKey",
      "aliyunSecret":"aliyunSecrect",
      "endpoint":"http://cn-hangzhou.sls.aliyuncs.com",
      "slsProject":"porjectname",
      "logStoreName":"logStoreName",
      "topic":"",
      "category": "test"
    }

most configure option is setting for [aliyun sdk's js](https://github.com/aliyun-UED/aliyun-sdk-js).

#Code example:

    var log4js = require('log4js');
    log4js.configure("./config/logTest.json");
    var logger=log4js.getLogger("test");
    logger.info("hello");
