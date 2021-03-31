# **_Bảng mã lệnh điều khiển_**

# DEVICE
## Điều khiển 1 thiết bị
Điều khiển một thiết bị có ID “b717f8d8-6f18-43c0-ae46-69c32998f653”, thiết lập giá trị cho thuộc tính có ID=0 thành 1
#### Gửi đi

```json
{
   "CMD":"DEVICE",
   "DATA":{
      "DEVICE_ID":"b717f8d8-6f18-43c0-ae46-69c32998f653",
      "DEVICE_UNICAST_ID":9,
      "PROPERTIES":[
         {
            "ID":0,
            "VALUE":1
         }
      ]
   }
}


```

#### Phản hồi
```json
Giống bản tin gửi đi nhưng được gửi vào topic phản hồi
```


# EVENTTRIGGER
## Thực hiện EventTrigger với ID tương ứng
Thực hiện EventTrigger có ID=123
#### Gửi đi

```json
{
   "CMD":"EVENT_TRIGGER",
   "DATA":{
      "EVENT_TRIGGER_ID":"aa3549d4-5471-4d75-b0b2-  b70fa5c10fb2"
   }
}
```

#### Phản hồi
```json
{
   "CMD":"EVENT_TRIGGER",
   "DATA":{
      "EVENT_TRIGGER_ID":"aa3549d4-5471-4d75-b0b2-  b70fa5c10fb2",
      "DEVICE_ID":"b717f8d8-6f18-43c0-ae46-69c32998f653",
      "DEVICE_UNICAST_ID":9
   }
}

```


# Group
## Điều khiển một nhóm thiết bị
Điều khiển nhóm có ID=b717f8d8-6f18-43c0-ae46-69c32998f653, thiết lập giá trị thuộc tính ID=0 thành 1 cho tất cả các thiết bị trong nhóm
#### Gửi đi

```json
{
   "CMD":"GROUP",
   "DATA":{
      "GROUP_ID":"b717f8d8-6f18-43c0-ae46-69c32998f653",
      "GROUP_UNICAST_ID":49152,
      "PROPERTIES":[
         {
            "ID":0,
            "VALUE":1
         }
      ]
   }
}
```

#### Phản hồi
```json
{
   "CMD":"DEVICE",
   "DATA":{
      "DEVICE_ID":"b717f8d8-6f18-43c0-ae46-69c32998f653",
      "DEVICE_UNICAST_ID":9,
      "PROPERTIES":[
         {
            "ID":0,
            "VALUE":1
         }
      ]
   }
}
```

# **_Bảng mã lệnh phục vụ cài đặt/cấu hình_**
# GROUP

## Tạo một nhóm "TYPE": "CREATE"
Tạo một nhóm mới gồm 3 thiết bị
### Gửi đi

```json
{
   "CMD":"GROUP",
   "TYPE":"CREATE",
   "DATA":{
      "GROUP_ID":"aa3549d4-5471-4d75-b0b2-  b70fa5c10fb2",
      "CATEGORY_ID":12,
      "NAME":"abc",
      "DEVICES":[
         {
            "DEVICE_ID":"b717f8d8-6f18-43c0-ae46-69c32998f653",
            "DEVICE_UNICAST_ID":9
         },
         {
            "DEVICE_ID":"b717f8d8-6f18-43c0-ae46-69c32998f654",
            "DEVICE_UNICAST_ID":8
         },
         {
            "DEVICE_ID":"b717f8d8-6f18-43c0-ae46-69c32998f655",
            "DEVICE_UNICAST_ID":7
         }
      ]
   }
}
```
### Mẫu phản hồi

Thành công
```json
{
   "CMD":"GROUP",
   "TYPE":"DEVxICE_RESPONSE",
   "DATA":{
      "GROUP_ID":"aa3549d4-5471-4d75-b0b2-b70fa5c10fb2",
      "GROUP_UNICAST_ID":49152,
      "DEVICE_ID":"b717f8d8-6f18-43c0-ae46-69c32998f653",
      "DEVICE_UNICAST_ID":5,
      "STATUS":"SUCCESS"
   }
}
```

## Thêm thiết bị vào nhóm "TYPE": "ADD_DEVICE"
 Thêm 3 thiêt bị vào nhóm đã có sẵn
 
 ### Gửi đi
```json
{
   "CMD":"GROUP",
   "TYPE":"ADD_DEVICE",
   "DATA":{
      "GROUP_ID":"aa3549d4-5471-4d75-b0b2-  b70fa5c10fb2",
      "GROUP_UNICAST_ID":49152,
      "DEVICES":[
         {
            "DEVICE_ID":"b717f8d8-6f18-43c0-ae46-69c32998f653",
            "DEVICE_UNICAST_ID":9
         },
         {
            "DEVICE_ID":"b717f8d8-6f18-43c0-ae46-69c32998f654",
            "DEVICE_UNICAST_ID":8
         },
         {
            "DEVICE_ID":"b717f8d8-6f18-43c0-ae46-69c32998f655",
            "DEVICE_UNICAST_ID":7
         }
      ]
   }
}
```
### Mẫu phản hồi

Thành công
```json
{
   "CMD":"GROUP",
   "TYPE":"DEVxICE_RESPONSE",
   "DATA":{
      "GROUP_ID":"aa3549d4-5471-4d75-b0b2-b70fa5c10fb2",
      "GROUP_UNICAST_ID":49152,
      "DEVICE_ID":"b717f8d8-6f18-43c0-ae46-69c32998f653",
      "DEVICE_UNICAST_ID":5,
      "STATUS":"SUCCESS"
   }
}
```

## Xóa thiết bị trong nhóm "TYPE": "REMOVE_DEVICE" 

Xóa 3 thiết bị trong nhóm
### Gửi đi
```json
{
   "CMD":"GROUP",
   "TYPE":"REMOVE_DEVICE",
   "DATA":{
      "GROUP_ID":"aa3549d4-5471-4d75-b0b2-  b70fa5c10fb2",
      "GROUP_UNICAST_ID":49152,
      "DEVICES":[
         {
            "DEVICE_ID":"b717f8d8-6f18-43c0-ae46-69c32998f653",
            "DEVICE_UNICAST_ID":9
         },
         {
            "DEVICE_ID":"b717f8d8-6f18-43c0-ae46-69c32998f654",
            "DEVICE_UNICAST_ID":8
         },
         {
            "DEVICE_ID":"b717f8d8-6f18-43c0-ae46-69c32998f655",
            "DEVICE_UNICAST_ID":7
         }
      ]
   }
}
```
### Mẫu phản hồi
```json
{
   "CMD":"GROUP",
   "TYPE":"REMOVE_DEVICE",
   "DATA":{
      "GROUP_ID":"aa3549d4-5471-4d75-b0b2-  b70fa5c10fb2",
      "GROUP_UNICAST_ID":49152,
      "DEVICE_ID":"b717f8d8-6f18-43c0-ae46-69c32998f653",
      "DEVICE_UNICAST_ID":5,
      "STATUS":"SUCCESS"
   }
}
``` 

## Xóa cả nhóm "TYPE": "DELETE"
Xóa nhóm đang tồn tại
### Gửi đi
```json
{
   "CMD":"GROUP",
   "TYPE":"DELETE",
   "DATA":{
      "GROUP_ID":"aa3549d4-5471-4d75-b0b2-  b70fa5c10fb2",
      "GROUP_UNICAST_ID":49152
   }
}
```
### Mẫu phản hồi
```json
{
   "CMD":"GROUP",
   "TYPE":"DELETE",
   "DATA":{
      "GROUP_ID":"aa3549d4-5471-4d75-b0b2-  b70fa5c10fb2",
      "GROUP_UNICAST_ID":49152
   }
}
```
# DEVICE

## SCAN
Đưa thiết bị vào mạng
### Gửi đi

```json
{
   "CMD":"SCAN"
}
```
### Mẫu phản hồi
Bản tin phản hồi khi 1 thiết bị được thêm vào mạng
```json
{
   "CMD":"TYPE_DEVICE",
   "DATA":{
      "DEVICE_UNICAST_ID":123,
      "DEVICE_ID":"b717f8d86f1843c0ae4669c32998f653",
      "DEVICE_KEY":"b717f8d86f1843c0ae4669c32998f653",
      "NET_KEY":"b717f8d86f1843c0ae4669c32998f653",
      "APP_KEY":"b717f8d86f1843c0ae4669c32998f653",
      "CATEGORY_ID":23002
   }
}
```
## STOP
Dừng quá trình đưa thiết bị vào mạng
### Gửi đi

```json
{
   "CMD":"STOP"
}
```
### Mẫu phản hồi
```json
{
   "CMD":"STOP"
}
```

## RESET_NODE
Xóa 1 hoặc nhiều thiết bị trong mạng
### Gửi đi

```json
{
   "CMD":"RESET_NODE",
   "DATA":[
      {
         "DEVICE_ID":"b717f8d8-6f18-43c0-ae46-69c32998f653",
         "DEVICE_UNICAST_ID":9
      },
      {
         "DEVICE_ID":"b717f8d8-6f18-43c0-ae46-69c32998f654",
         "DEVICE_UNICAST_ID":8
      },
      {
         "DEVICE_ID":"b717f8d8-6f18-43c0-ae46-69c32998f655",
         "DEVICE_UNICAST_ID":7
      }
   ]
}
```
### Mẫu phản hồi
Từng thiết bị sẽ phản hồi về sau khi xóa khỏi mạng BLE

```json

{
   "CMD":"RESET_NODE",
   "DEVICES":{
      "DEVICE_ID":"b717f8d8-6f18-43c0-ae46-69c32998f653",
      "DEVICE_UNICAST_ID":9
   }
}
```
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
## TYPE: "EDIT"

TYPE: "EDIT"
Sửa cảnh gán cho device (công tắc cảnh hoặc cảm biến)
### Gửi đi

```json
{
   "CMD":"SET_SCENE_FOR_SENSOR",
   "TYPE":"EDIT",
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
   "TYPE":"EDIT",
   "DATA":{
      "DEVICE_ID":"aa3549d4-5471-4d75-b0b2-  b70fa5c10fb2",
      "DEVICE_UNICAST_ID":332,
      "COMPARISON_OPERATOR_ID":1,
      "EVENT_TRIGGER_ID":"aa3549d4-5471-4d75-b0b2-  b70fa5c10fb2",
      "DEVICE_ATTRIBUTE_VALUE":{
         "BUTTON_VALUE":"BUTTON_1",
         "MODE_VALUE":2
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
      "DEVICE_ATTRIBUTE_VALUE":{
         "BUTTON_VALUE":"BUTTON_1",
         "MODE_VALUE":2
      }
   }
}
```
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

## TYPE: "DELETE" Xóa 1 EVENT_TRIGGER
TYPE: "DELETE"

### Gửi đi

```json
{
   "CMD":"EVENT_TRIGGER",
   "TYPE":"DELETE",
   "DATA":{
      "EVENT_TRIGGER_ID":"aa3549d4-5471-4d75-b0b2-  b70fa5c10fb2"
   }
}
```
### Mẫu phản hồi
```json
{
   "CMD":"EVENT_TRIGGER",
   "TYPE":"DELETE",
   "DATA":{
      "EVENT_TRIGGER_ID":"aa3549d4-5471-4d75-b0b2-  b70fa5c10fb2"
   }
}
```
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
## TYPE: DELETE
### Gửi đi

```json
{
   "CMD":"EVENT_TRIGGER_OUTPUT_DEVICE_MAPPING",
   "TYPE":"DELETE",
   "DATA":{
      "EVENT_TRIGGER_ID":"aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
      "GUID":"97ab44a3-e788-46a1-9c07-79f39d6be33f",
      "SCENE_UNICAST_ID":4,
      "EVENT_TRIGGER_TYPE_ID":1,
      "DEVICES":[
         {
            "DEVICE_ID":"aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
            "DEVICE_UNICAST_ID":4
         }
      ],
      "GROUPS":[
         {
            "GROUP_ID":"aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
            "GROUP_UNICAST_ID":4
         }
      ]
   }
}
```
### Mẫu phản hồi
```json
{
   "CMD":"EVENT_TRIGGER_OUTPUT_DEVICE_MAPPING",
   "TYPE":"DELETE",
   "DATA":{
      "EVENT_TRIGGER_ID":"aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
      "GUID":"97ab44a3-e788-46a1-9c07-79f39d6be33f",
      "SCENE_UNICAST_ID":4,
      "DEVICE_ID":"aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
      "DEVICE_UNICAST_ID":4
   }
}
```
# DEVICE_UPDATE_STATUS

## Bản tin cập nhật trạng thái thiết bị khi vừa mở app
```json
{
   "CMD":"DEVICE_UPDATE",
   "TIME_UPDATE":"2021-03-27 06:30:02.101"
}
```
### Gửi đi

```json
{
   "CMD":"DEVICE_UPDATE",
   "TIME_UPDATE":"YYYY-MM-DD HH:MM:SS.SSS"
}
```
### Mẫu phản hồi
```json
{
   "CMD":"DEVICE_UPDATE",
   "DATA":{
      "DEVICE_ID":"aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
      "PROPERTIES":[
         {
            "ID":0,
            "VALUE":1
         },
         {
            "ID":1,
            "VALUE":1
         },
         {
            "ID":2,
            "VALUE":50
         }
      ]
   }
}
```
# RULE

## "TYPE": "CREATE" tạo rule với các thông số được cài đặt theo thông số người dùng lựa chọn


*Lưu ý: VD: Nếu không có thời gian bỏ trường thời gian START_AT, END_AT
### Gửi đi

```json
{
   "CMD":"EVENT_TRIGGER",
   "TYPE":"CREATE",
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
            "DEVICE_ID":"aa3549d4-5471-4d75-b0b2- b70fa5c10fb26666666666666",
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
            ]
         }
      ],
      "SCENE":[
         {
            "SCENE_ID":"a"
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


## "TYPE": "DELETE"
### Gửi đi

```json
{
   "CMD":"EVENT_TRIGGER",
   "TYPE":"DELETE",
   "DATA":{
      "EVENT_TRIGGER_ID":"aa3549d4-5471-4d75-b0b2- b70fa5c10fb2"
   }
}
```
### Mẫu phản hồi
```json
{
   "CMD":"EVENT_TRIGGER",
   "TYPE":"DELETE",
   "DATA":{
      "EVENT_TRIGGER_ID":"aa3549d4-5471-4d75-b0b2- b70fa5c10fb2"
   }
}
```
