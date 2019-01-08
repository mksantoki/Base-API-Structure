# Base-API-Structure
#### Base API Structure for All Endpoins

- Success API Response
```
{
"status":"success",
"data":{
},
"message":"Message for user",
"code":200
}
```

- Fail API Response
```
{
"status":"fail",
"data":{
},
"message":"Phone already exists",
"code":0
}
```

- status :- Status is use to identify response. (success/fail)
- data   :- Data will use according requirement like(JsonArray/JsonObject)
- message :- Message is use to display message to user.For understand what happen with application and it will increase good user experience.
- code :- Code is use to identify issue and perform action according it.

#### Base Header For All endpoint

```

{
"osVersion":"SDK Version",
"appVersion":"1.0",
"platform":"Android/iOs",
"deviceId":"UUID",
"language-type":"en/hi"
"authentication":"token"
}
```

- osVersion :- OS Version is SDK version. (19/20/21)
- appVersion :- App Version is application version.(1.0/1.1)
- platform :- Platform is use to identify device platform.
- deviceId :- DeviceId is use to identify device uniquely.
- language-type :- Language type is use to identify user current selected language

####  Advantage

- First is every endpoint contain same response
- When we face any fail response from server. We display this message to user. Base on language selection.
- Using header param we easy identify issue. Example identify device os/platform/ etc

