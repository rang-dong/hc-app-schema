# EVENT_TRIGGER_OUTPUT_DEVICE_MAPPING

## TYPE: "ADD"

Nếu :
"EVENT_TRIGGER_TYPE_ID" : 1
"GUID": ID của SCENE thêm trường "SCENE_UNICAST_ID": 4,
### Gửi đi

```json
{
   "CMD":"EVENT_TRIGGER_OUTPUT_DEVICE_MAPPING",
   "TYPE":"ADD",
   "DATA":{
      "EVENT_TRIGGER_ID":"aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
      "GUID":"97ab44a3-e788-46a1-9c07-79f39d6be33f",
      "SCENE_UNICAST_ID":4,
      "EVENT_TRIGGER_TYPE_ID":1,
      "DEVICES":[
         {
            "DEVICE_ID":"aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
            "DEVICE_UNICAST_ID":4,
            "PROPERTIES":[
               {
                  "ID":1201,
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