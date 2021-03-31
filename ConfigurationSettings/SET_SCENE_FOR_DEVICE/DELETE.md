# SET_SCENE_FOR_DEVICE
## TYPE: "DELETE"
TYPE: "DELETE"
xóa cảnh gán với device (công tắc cảnh hoặc cảm biến)
### Gửi đi

```json
{
   "CMD":"SET_SCENE_FOR_SENSOR",
   "TYPE":"DELETE",
   "DATA":{
      "DEVICE_ID":"aa3549d4-5471-4d75-b0b2-  b70fa5c10fb2",
      "EVENT_TRIGGER_ID":"aa3549d4-5471-4d75-b0b2-  b70fa5c10fb2"
   }
}
```
```json
{
   "CMD":"SET_SCENE_FOR_REMOTE",
   "TYPE":"DELETE",
   "DATA":{
      "DEVICE_ID":"aa3549d4-5471-4d75-b0b2-  b70fa5c10fb2",
      "EVENT_TRIGGER_ID":"aa3549d4-5471-4d75-b0b2-  b70fa5c10fb2",
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
   "TYPE":"DELETE",
   "DATA":{
      "DEVICE_ID":"aa3549d4-5471-4d75-b0b2-  b70fa5c10fb2",
      "EVENT_TRIGGER_ID":"aa3549d4-5471-4d75-b0b2-  b70fa5c10fb2"
   }
}
```
```json
{
   "CMD":"SET_SCENE_FOR_REMOTE",
   "TYPE":"DELETE",
   "DATA":{
      "DEVICE_ID":"aa3549d4-5471-4d75-b0b2-  b70fa5c10fb2",
      "DEVICE_ATTRIBUTE_VALUE":{
         "BUTTON_VALUE":"BUTTON_1",
         "MODE_VALUE":1
      }
   }
}
```