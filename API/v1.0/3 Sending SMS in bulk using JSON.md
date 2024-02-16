

**Description**: Creates SMS on the server to send. After that, the phone with the Smsgateway24 application calls the server and takes the SMS and sends it from your sim card Download the application at the link  
Endpoint: **https://smsgateway24.com/getdata/addalotofsms**  
Method:: *GET*, *POST*

Parameters of the request:

| Variable | Type | Description | Value |
| ---- | ---- | ---- | ---- |
| **datajson** | string | required |  ```{"token":"df427bfcf113c9a21c67718035076b5b","smsdata":[{"sendto":"015752982212","body":"Test message","sim":1,"timetosend":"2019-07-01 23:50:00","device_id":260},{"sendto":"+4915752982212","body":"Test message 2","sim":1,"timetosend":"2019-07-01 23:50:00","device_id":260,"urgent":1}]}<br>``` |
|  |  |  |  |

  

JSON-formatted response::

|Variable|Type|Description|
|---|---|---|
|error|int|0 \| 1 - indicates whether there is an error in processing the request|
|message|string|Error message, empty if everything is in order.|

 [Link to code example Curl](https://github.com/smsgateway24/phpexample/blob/master/src/curl/gettoken.php)  
 [Link to code example Guzzle](https://github.com/smsgateway24/phpexample/blob/master/src/guzzle/gettoken.php)
 
 Request example:  

 ```json
{
   "token":"df427bfcf113c9a21c6771803501",
   "smsdata":[
        {
            "sendto":"015752982212",
            "body":"Your password is 12345",
            "sim":1,
            "timetosend":"2019-07-01 23:50:00",
            "device_id":260,
            "customerid":122,
            "urgent":1
        },
        {
            "sendto":"015752982212",
            "body":"Regular SMS. Not urgnet",
            "sim":1,
            "timetosend":"2019-07-01 23:50:00",
            "device_id":260,
            "customerid":122,
            "urgent":0
        }
    ]
}
```
