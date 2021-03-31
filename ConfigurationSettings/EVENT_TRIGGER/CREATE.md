# EVENT_TRIGGER

## TYPE: "CREATE" Tạo 1 EVENT_TRIGGER
TYPE: "CREATE"
HC nhận được bản ghi thêm EvenTrigger sẽ lưu dữ liệu vào bảng EvenTrigger, kiểm tra trường EventTriggerTYPEID nếu bằng 1 (cảnh) thì sẽ gửi bản tin tạo cảnh xuống GateWay
### Gửi đi

```json
{
   "CMD":"EVENT_TRIGGER",
   "TYPE":"CREATE",
   "DATA":{
      "EVENT_TRIGGER_ID":"aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
      "GROUP_ID":"97ab44a3-e788-46a1-9c07-79f39d6be33f",
      "EVENT_TRIGGER_TYPE_ID":1,
      "PRIORITY":1,
      "HAS_TIMER":1,
      "START_AT":"10:56:1",
      "END_AT":"11:1:15",
      "EACH_DAY":[
         "EACHMONDAY",
         "EACHTUESDAY"
      ],
      "DEVICES":[
         {
            "DEVICE_ID":"aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
            "DEVICE_UNICAST_ID":4,
            "PROPERTIES":[
               {
                  "ID":0,
                  "VALUE":1
               }
            ]
         }
      ],
      "GROUPS":[
         {
            "GROUP_ID":"aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
            "GROUP_UNICAST_ID":4,
            "PROPERTIES":[
               {
                  "ID":1201,
                  "VALUE":1
               }
            ]
         }
      ]
   }
}
```
### Mẫu phản hồi
```json
{
   "CMD":"EVENT_TRIGGER",
   "TYPE":"CREATE",
   "DATA":{
      "EVENT_TRIGGER_ID":"aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
      "GROUP_ID":"97ab44a3-e788-46a1-9c07-79f39d6be33f",
      "SCENE_UNICAST_ID":4,
      "EVENT_TRIGGER_TYPE_ID":1,
      "PRIORITY":1,
      "HAS_TIMER":1,
      "START_AT":"10:56:1",
      "END_AT":"11:1:15"
   }
}
```
```json
{
   "CMD":"EVENT_TRIGGER_OUTPUT_DEVICE_MAPPING",
   "TYPE":"ADD",
   "DATA":{
      "EVENT_TRIGGER_ID":"aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
      "GUID":"97ab44a3-e788-46a1-9c07-79f39d6be33f",
      "SCENE_UNICAST_ID":4,
      "EVENT_TRIGGER_TYPE_ID":1,
      "STATUS":"SUCCESS",
      "DEVICES":[
         {
            "DEVICE_ID":"aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
            "DEVICE_UNICAST_ID":4
         }
      ]
   }
}
```