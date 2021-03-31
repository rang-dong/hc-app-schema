# RULE
## "TYPE": "EDIT" giống bản tin CREATE nhưng các thông số bị thay đổi
### Gửi đi

```json
{
   "CMD":"EVENT_TRIGGER",
   "TYPE":"EDIT",
   "DATA":{
      "EVENT_TRIGGER_ID":"aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
      "GROUP_ID":"97ab44a3-e788-46a1-9c07-79f39d6be33f",
      "EVENT_TRIGGER_TYPE_ID":2,
      "PRIORITY":3,
      "HAS_TIMER":1,
      "START_AT":"10:56:1",
      "END_AT":"11:1:15",
      "HAS_REPEATER":1,
      "EACH_DAY":[
         "EACHMONDAY",
         "EACHTUESDAY"
      ],
      "LOGICAL_OPERATOR_ID":-1,
      "STATUS_ID":1,
      "DEVICES":[
         {
            "DEVICE_ID":"aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
            "DEVICE_UNICAST_ID":4,
            "PROPERTIES":[
               {
                  "ID":0,
                  "VALUE":1
               },
               {
                  "ID":2,
                  "VALUE":50
               }
            ]
         },
         {
            "DEVICE_ID":"aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
            "DEVICE_UNICAST_ID":6,
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
            ],
            "SCENE":[
               {
                  "SCENE_ID":"aa3549d4-5471-4d75-b0b2- b70fa5c10fb2"
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
   "DATA":{
      "EVENT_TRIGGER_ID":"aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
      "STATUS":"SUCCESS"
   }
}
```