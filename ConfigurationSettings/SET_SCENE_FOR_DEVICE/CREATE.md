# SET_SCENE_FOR_DEVICE

## TYPE: "CREATE"
TYPE: "CREATE"
Gán cảnh vào nút cho device (công tắc cảnh hoặc cảm biến)


sensor: thêm cảnh có EVENT_TRIGGER_ID: "aa3549d4-5471-4d75-b0b2-  b70fa5c10fb2" với điều kiện ánh sáng và điều kiện chuyển động cho cảm biến có "DEVICE_ID": "aa3549d4-5471-4d75-b0b2-  b70fa5c10fb2",
### Gửi đi

```json
{
   "CMD":"SET_SCENE_FOR_SENSOR",
   "TYPE":"CREATE",
   "DATA":{
      "DEVICE_ID":"aa3549d4-5471-4d75-b0b2-  b70fa5c10fb2",
      "DEVICE_UNICAST_ID":332,
      "EVENT_TRIGGER_ID":"aa3549d4-5471-4d75-b0b2-  b70fa5c10fb2",
      "LIGHT_SENSOR":{
         "LOW_LUX":200,
         "HIGHT_LUX":600,
         "COMPARISON_OPERATOR_ID":7,
         "DEVICE_ATTRIBUTE_ID":12
      },
      "PIR_SENSOR":{
         "PIR":1,
         "COMPARISON_OPERATOR_ID":1,
         "DEVICE_ATTRIBUTE_ID":12
      }
   }
}
```
```json
{
   "CMD":"SET_SCENE_FOR_REMOTE",
   "TYPE":"CREATE",
   "DATA":{
      "DEVICE_ID":"aa3549d4-5471-4d75-b0b2-  b70fa5c10fb2",
      "DEVICE_UNICAST_ID":332,
      "COMPAIRISON_OPERATOR_ID":1,
      "EVENT_TRIGGER_ID":"aa3549d4-5471-4d75-b0b2-  b70fa5c10fb2",
      "DEVICE_ATTRIBUTE_ID":12,
      "DEVICE_ATTRIBUTE_VALUE":{
         "BUTTON_VALUE":"BUTTON_1",
         "MODE_VALUE":1
      }
   }
}
```
### Mẫu phản hồi
```json
{
   "CMD":"SET_SCENE_FOR_SENSOR",
   "DATA":{
      "DEVICE_ID":"aa3549d4-5471-4d75-b0b2-  b70fa5c10fb2",
      "DEVICE_UNICAST_ID":332,
      "EVENT_TRIGGER_ID":"aa3549d4-5471-4d75-b0b2-  b70fa5c10fb2",
      "LIGHT_SENSOR":{
         "LOW_LUX":200,
         "HIGHT_LUX":600,
         "COMPARISON_OPERATOR_ID":7,
         "DEVICE_ATTRIBUTE_ID":12
      },
      "PIR_SENSOR":{
         "PIR":1,
         "COMPAIRISON_OPERATOR_ID":1,
         "DEVICE_ATTRIBUTE_ID":12
      }
   }
}
```
```json
{
   "CMD":"SET_SCENE_FOR_REMOTE",
   "DATA":{
      "DEVICE_ID":"aa3549d4-5471-4d75-b0b2-  b70fa5c10fb2",
      "DEVICE_UNICAST_ID":332,
      "COMPARISON_OPERATOR_ID":1,
      "EVENT_TRIGGER_ID":"aa3549d4-5471-4d75-b0b2-  b70fa5c10fb2",
      "DEVICE_ATTRIBUTE_ID":[
         12,
         13
      ],
      "DEVICE_ATTRIBUTE_VALUE":{
         "BUTTON_VALUE":"BUTTON_1",
         "MODE_VALUE":1
      }
   }
}
```