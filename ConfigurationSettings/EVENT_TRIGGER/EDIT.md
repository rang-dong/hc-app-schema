# EVENT_TRIGGER
## TYPE: "EDIT" Sửa 1 EVENT_TRIGGER
TYPE: "EDIT"
HC nhận được bản tin sửa EVEN_TRIGGER theo các thông số người dùng cài đặt
### Gửi đi

```json
{
   "CMD":"EVENT_TRIGGER",
   "TYPE":"EDIT",
   "DATA":{
      "EVENT_TRIGGER_ID":"aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
      "GROUP_ID":"97ab44a3-e788-46a1-9c07-79f39d6be33f",
      "SCENE_UNICAST_ID":4,
      "EVENT_TRIGGER_TYPE_ID":1,
      "PRIORITY":1,
      "HAS_TIMER":1,
      "START_AT":"10:1:15",
      "END_AT":"12:1:15",
      "EACH_DAY":[
         "EACHMONDAY",
         "EACHTUESDAY"
      ]
   }
}
```
### Mẫu phản hồi
```json
{
   "CMD":"EVENT_TRIGGER",
   "TYPE":"EDIT",
   "DATA":{
      "EVENT_TRIGGER_ID":"aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
      "GROUP_ID":"97ab44a3-e788-46a1-9c07-79f39d6be33f",
      "SCENE_UNICAST_ID":4,
      "EVENT_TRIGGER_TYPE_ID":1,
      "PRIORITY":1,
      "HAS_TIMER":1,
      "START_AT":"10:1:15",
      "END_AT":"12:1:15"
   }
}
```