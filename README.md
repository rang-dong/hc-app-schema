# Bảng mã lệnh điều khiển
## Device
### Điều khiển 1 thiết bị
#### Mẫu bản tin thục hiện
```
{
    "CMD": "DEVICE",
    "DATA":
        {
        "DEVICE_ID": "b717f8d8-6f18-43c0-ae46-69c32998f653",
        "PROPERTIES":[
            {
                "ID": 0,
                "VALUE": 1
            }
        ]
    }
}
```
#### Mẫu bản tin phản hồi
```
Giống bản tin gửi đi nhưng được gửi vào topic phản hồi
``` 
## Group
### Điều khiển một nhóm thiết bị
#### Mẫu bản tin thục hiện
```
{
    "CMD": "GROUP",
    "DATA":
    {
        "GROUP_ID": "b717f8d8-6f18-43c0-ae46-69c32998f653",
        "PROPERTIES":[
            {
                "ID": 0,
                "VALUE": 1
            }
        ]
    }
}
```
#### Mẫu bản tin phản hồi
```
{
    "CMD": "DEVICE",
    "DATA":
    {
        "DEVICE_ID": "b717f8d8-6f18-43c0-ae46-69c32998f653",
        "PROPERTIES":[
            {
                "ID": 0,
                "VALUE": 1
            }
        ]
    }
}
``` 
## EVENTTRIGGER
### Thực hiện EventTrigger với ID tương ứng
#### Mẫu bản tin thục hiện
```
{
    "CMD": "EVENT_TRIGGER",
    "DATA":
    {
        "EVENT_TRIGGER_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2"
    }
}
```
#### Mẫu bản tin phản hồi
```
{
    "CMD": "EVENT_TRIGGER",
    "DATA":
    {
    "EVENT_TRIGGER_ID": "aa3549d4-5471-4d75-b0b2-b70fa5c10fb2",
    "DEVICE_ID": "b717f8d8-6f18-43c0-ae46-69c32998f653"
    }
}
``` 
# Bảng mã lệnh phục vụ cài đặt/cấu hình
## GROUP
### Tạo một nhóm, "TYPE":"CREATE"
#### Mẫu bản tin thục hiện
```
{
    "CMD": "GROUP",
    "TYPE": "CREATE",
    "DATA": {
        "GROUP_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
        "CATEGORY_ID": 12,
        "NAME": "abc",
        "DEVICES": [
            "b717f8d8-6f18-43c0-ae46-69c32998f653",
            "b717f8d8-6f18-43c0-ae46-69c32998f654"
        ]
    }
}
```
#### Mẫu bản tin phản hồi
```
Thành công
{
 "CMD": "GROUP",
 "TYPE": "DEVICE_RESPONSE",
 "DATA": {
 "GROUP_ID": "aa3549d4-5471-4d75-b0b2-b70fa5c10fb2",
 "DEVICE_ID": "b717f8d8-6f18-43c0-ae46-69c32998f653",
 "STATUS": "SUCCESS"
 }
}
``` 
## GROUP
### Điều khiển 1 thiết bị
#### Thêm thiết bị vào nhóm "TYPE": "ADD_DEVICE"
```
{
 "CMD": "GROUP",
 "TYPE": "ADD_DEVICE",
 "DATA": {
    "GROUP_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "DEVICES": [
        "b717f8d8-6f18-43c0-ae46-69c32998f653",
        "b717f8d8-6f18-43c0-ae46-69c32998f654"
    ]
 }
}
```
### Mẫu bản tin phản hồi
```
Thành công
{
 "CMD": "GROUP",
 "TYPE": "DEVICE_RESPONSE",
 "DATA": {
     "GROUP_ID": "aa3549d4-5471-4d75-b0b2-b70fa5c10fb2",
     "DEVICE_ID": "b717f8d8-6f18-43c0-ae46-69c32998f653",
     "STATUS": "SUCCESS"
 }
}
``` 
## GROUP
### Xóa thiết bị trong nhóm"TYPE":"REMOVE_DEVICE"
### Mẫu bản tin thục hiện
```
{
 "CMD": "GROUP",
 "TYPE": "REMOVE_DEVICE",
 "DATA": {
    "GROUP_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "DEVICES": [
        "b717f8d8-6f18-43c0-ae46-69c32998f653",
        "b717f8d8-6f18-43c0-ae46-69c32998f654"
    ]
 }
}
```
### Mẫu bản tin phản hồi
```
{
 "CMD": "GROUP",
 "TYPE": "REMOVE_DEVICE",
 "DATA": {
    "GROUP_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "DEVICE_ID": "b717f8d8-6f18-43c0-ae46-69c32998f653",
    "STATUS": "SUCCESS"
 }
}
``` 
## GROUP
### Xóa cả nhóm "TYPE": "DELETE"
### Mẫu bản tin thục hiện
```
{
 "CMD": "GROUP",
 "TYPE": "DELETE",
 "DATA":
 {
    "GROUP_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2"
 }
}
```
### Mẫu bản tin phản hồi
```
{
 "CMD": "GROUP",
 "TYPE": "DELETE",
 "DATA":
 {
    "GROUP_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2"
 }
}
``` 
## Device
### SCAN
#### Mẫu bản tin thục hiện
```
Bản tin phản hồi khi 1 thiết bị được thêm vào mạng
{
 "CMD": "TYPE_DEVICE",
 "DATA":
 {
    "DEVICE_ID": "b717f8d86f1843c0ae4669c32998f653",
    "DEVICE_KEY": "b717f8d86f1843c0ae4669c32998f653",
    "NET_KEY": "b717f8d86f1843c0ae4669c32998f653",
    "APP_KEY": "b717f8d86f1843c0ae4669c32998f653",
    "CATEGORY_ID": 23002
 }
}
```
#### Mẫu bản tin phản hồi
```

``` 
## Device
### STOP
#### Mẫu bản tin thục hiện
```
{
 "CMD":"STOP"
}
```
### Mẫu bản tin phản hồi
```
{
 "CMD":"STOP"
}
``` 
## Device
### RESET_NODE
#### Mẫu bản tin thục hiện
```
{
 "CMD":"RESET_NODE",
 "DATA":[
    "b717f8d8-6f18-43c0-ae46-69c32998f653",
    "b717f8d8-6f18-43c0-ae46-69c32998f654"
 ]
}
```
### Mẫu bản tin phản hồi
```
Từng thiết bị sẽ phản hồi về sau khi xóa khỏi mạng BLE
{
 "CMD":"RESET_NODE",
 "DEVICE_ID": "b717f8d8-6f18-43c0-ae46-69c32998f653"
}
``` 
## SET_SCENE_FOR_DEVICE
### TYPE: "CREATE" cảm biến
#### Mẫu bản tin thục hiện
```
{
 "CMD": "SCENE_FOR_SENSOR_LIGHT_PIR",
 "TYPE": "CREATE",
 "DATA": {
    "DEVICE_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "EVENT_TRIGGER_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "EVENT_TRIGGER_TYPE_ID":1,
        "LIGHT_SENSOR":
        {
            "LOW_LUX":200,
            "HIGHT_LUX":600,
            "COMPARISON_OPERATOR_ID":7,
            "DEVICE_ATTRIBUTE_ID": 12
        },
        "PIR_SENSOR":
        {
            "PIR":1,
            "COMPARISON_OPERATOR_ID":1,
            "DEVICE_ATTRIBUTE_ID": 10
        }
 }
}
```
#### Mẫu bản tin phản hồi
```
{
 "CMD": "SCENE_FOR_SENSOR_LIGHT_PIR",
 "DATA": {
 "DEVICE_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
 "EVENT_TRIGGER_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
 "LIGHT_SENSOR":
 {
    "LOW_LUX":200,PIR
    "HIGHT_LUX":600,
    "COMPARISON_OPERATOR_ID":7,
    "DEVICE_ATTRIBUTE_ID": 12
 },
 "PIR_SENSOR":
 {
    "PIR":1,
    "COMPAIRISON_OPERATOR_ID":1,
    "DEVICE_ATTRIBUTE_ID": 12
 }
 }
}
``` 
## SET_SCENE_FOR_DEVICE
### TYPE: "CREATE" công tắc
#### Mẫu bản tin thục hiện
```
{
 "CMD": "SCENE_FOR_REMOTE_AC",
 "TYPE": "CREATE",
 "DATA": {
    "DEVICE_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "COMPARISON_OPERATOR_ID":1,
    "EVENT_TRIGGER_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "DEVICE_ATTRIBUTE_ID":12,
    "EVENT_TRIGGER_TYPE_ID":1,
    "DEVICE_ATTRIBUTE_VALUE":
        {
            "BUTTON_VALUE": "BUTTON_1",
            "MODE_VALUE": 1
    }
 }
}
{
 "CMD": "SCENE_FOR_REMOTE_DC",
 "TYPE": "CREATE",
 "DATA": {
    "DEVICE_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "COMPARISON_OPERATOR_ID":1,
    "EVENT_TRIGGER_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "DEVICE_ATTRIBUTE_ID":12,
    "EVENT_TRIGGER_TYPE_ID":1,
    "DEVICE_ATTRIBUTE_VALUE":
        {
            "BUTTON_VALUE": "BUTTON_1",
            "MODE_VALUE": 1
    }
 }
}
```
#### Mẫu bản tin phản hồi
```
{
 "CMD": "SCENE_FOR_REMOTE_AC",
 "DATA": {
    "DEVICE_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "COMPARISON_OPERATOR_ID":1,
    "EVENT_TRIGGER_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "DEVICE_ATTRIBUTE_ID":[12,13],
    "DEVICE_ATTRIBUTE_VALUE":
        {AC
            "BUTTON_VALUE": "BUTTON_1",
            "MODE_VALUE": 1
    }
 }
}
{
 "CMD": "SCENE_FOR_REMOTE_DC",
 "DATA": {
    "DEVICE_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "COMPARISON_OPERATOR_ID":1,
    "EVENT_TRIGGER_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "DEVICE_ATTRIBUTE_ID":[12,13],
    "DEVICE_ATTRIBUTE_VALUE":
        {AC
            "BUTTON_VALUE": "BUTTON_1",
        "MODE_VALUE": 1
    }
 }
}
``` 
## SET_SCENE_FOR_DEVICE
### TYPE: "EDIT" cảm biển
#### Mẫu bản tin thục hiện
```
{
 "CMD": "SCENE_FOR_SENSOR_LIGHT_PIR",
 "TYPE": "EDIT",
 "DATA": {
    "DEVICE_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "EVENT_TRIGGER_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "LIGHT_SENSOR":
    {
        "LOW_LUX":200,
        "HIGHT_LUX":600,
        "COMPARISON_OPERATOR_ID":7,
        "DEVICE_ATTRIBUTE_ID": 12
    },
    "PIR_SENSOR":
    {
        "PIR":1,
        "COMPARISON_OPERATOR_ID":1,
        "DEVICE_ATTRIBUTE_ID": 12
    }
 } }
```
### Mẫu bản tin phản hồi
```
{
 "CMD": "SCENE_FOR_SENSOR_LIGHT_PIR",
 "DATA": {
    "DEVICE_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "EVENT_TRIGGER_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "LIGHT_SENSOR":
        {
            "LOW_LUX":200,
            "HIGHT_LUX":600,
            "COMPARISON_OPERATOR_ID":7,
            "DEVICE_ATTRIBUTE_ID": 12
    },
    "PIR_SENSOR":
        {
            "PIR":1,
            "COMPAIRISON_OPERATOR_ID":1,
            "DEVICE_ATTRIBUTE_ID": 12
    }
 } }
``` 
## SET_SCENE_FOR_DEVICE
### TYPE: "EDIT" công tắc
#### Mẫu bản tin thục hiện
```
{
 "CMD": "SCENE_FOR_REMOTE_DC",
 "TYPE": "EDIT",
 "DATA": {
    "DEVICE_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "COMPARISON_OPERATOR_ID":1,
    "EVENT_TRIGGER_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "DEVICE_ATTRIBUTE_VALUE":
        {
            "BUTTON_VALUE": "BUTTON_1",
            "MODE_VALUE": 2
        }
 } 
}
{
 "CMD": "SCENE_FOR_REMOTE_AC",
 "TYPE": "EDIT",
 "DATA": {
    "DEVICE_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "COMPARISON_OPERATOR_ID":1,
    "EVENT_TRIGGER_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "DEVICE_ATTRIBUTE_VALUE":
        {
            "BUTTON_VALUE": "BUTTON_1",
            "MODE_VALUE": 2
    }
 } 
}
```
### Mẫu bản tin phản hồi
```
{
 "CMD": "SCENE_FOR_REMOTE_DC",
 "DATA": {
    "DEVICE_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "DEVICE_UNICAST_ID": 332,
    "COMPARISON_OPERATOR_ID":1,
    "EVENT_TRIGGER_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "DEVICE_ATTRIBUTE_VALUE":
        {
            "BUTTON_VALUE": "BUTTON_1",
            "MODE_VALUE": 2
    }
 }
}AC 
{
 "CMD": "SCENE_FOR_REMOTE_AC",
 "DATA": {
    "DEVICE_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "DEVICE_UNICAST_ID": 332,
    "COMPARISON_OPERATOR_ID":1,
    "EVENT_TRIGGER_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "DEVICE_ATTRIBUTE_VALUE":
        {
            "BUTTON_VALUE": "BUTTON_1",
        "MODE_VALUE": 2
    }
 }
}
``` 
## SET_SCENE_FOR_DEVICE
### TYPE: "DELETE"
#### Mẫu bản tin thục hiện
```
{
 "CMD": "SCENE_FOR_SENSOR_LIGHT_PIR",
 "TYPE": "DELETE",
 "DATA": {
    "DEVICE_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "EVENT_TRIGGER_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2"
 } }
```
### Mẫu bản tin phản hồi
```
{
 "CMD": "SCENE_FOR_SENSOR_LIGHT_PIR",
 "TYPE": "DELETE",
 "DATA": {
    "DEVICE_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "EVENT_TRIGGER_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2"
 } }
``` 
## SET_SCENE_FOR_DEVICE
### TYPE: "DELETE"
#### Mẫu bản tin thục hiện
```
{
 "CMD": "SCENE_FOR_REMOTE_AC",
 "TYPE": "DELETE",
 "DATA": {
    "DEVICE_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "EVENT_TRIGGER_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "DEVICE_ATTRIBUTE_VALUE":
    {
        "BUTTON_VALUE": "BUTTON_1",
        "MODE_VALUE": 1
    }
 } 
}
{
 "CMD": "SCENE_FOR_REMOTE_DC",
 "TYPE": "DELETE",
 "DATA": {
    "DEVICE_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "EVENT_TRIGGER_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "DEVICE_ATTRIBUTE_VALUE":
    {
        "BUTTON_VALUE": "BUTTON_1",
        "MODE_VALUE": 1
    }
 } 
}
```
### Mẫu bản tin phản hồi
```
{
 "CMD": "SCENE_FOR_REMOTE_AC",
 "TYPE": "DELETE",
 "DATA": {
    "DEVICE_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "DEVICE_ATTRIBUTE_VALUE":
    {
        "BUTTON_VALUE": "BUTTON_1",
        "MODE_VALUE": 1
    }
 }
}
{
 "CMD": "SCENE_FOR_REMOTE_DC",
 "TYPE": "DELETE",
 "DATA": {
    "DEVICE_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "DEVICE_ATTRIBUTE_VALUE":
    {
        "BUTTON_VALUE": "BUTTON_1",
        "MODE_VALUE": 1
    }
 } 
}
``` 
## EVENT_TRIGGER
### TYPE: "CREATE" Tạo 1 EVENT_TRIGGER
#### Mẫu bản tin thục hiện
```
{
 "CMD": "EVENT_TRIGGER",
 "TYPE": "CREATE",
 "DATA": {
    "EVENT_TRIGGER_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "GROUP_ID": "97ab44a3-e788-46a1-9c07-79f39d6be33f",
    "EVENT_TRIGGER_TYPE_ID": 1,
    "PRIORITY": 1,
    "HAS_TIMER": 1,
    "START_AT": "10:56:1",
    "END_AT": "11:1:15",
    "EACH_DAY":["EACHMONDAY","EACHTUESDAY"],
    "DEVICES": [
        {
        "DEVICE_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
        "PROPERTIES": [
        {
            "ID": 0,
            "VALUE": 1
        }
    ]
 }
 ],
 "GROUPS": [
    {
        "GROUP_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
        "PROPERTIES": [
            {
                "ID": 0,
                "VALUE": 1
            }
        ]
    }
 ]
 }}
```
### Mẫu bản tin phản hồi
```
{
 "CMD": "EVENT_TRIGGER",
 "TYPE": "CREATE",
 "DATA": {
    "EVENT_TRIGGER_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "GROUP_ID": "97ab44a3-e788-46a1-9c07-79f39d6be33f",
    "EVENT_TRIGGER_TYPE_ID": 1,
    "PRIORITY": 1,
    "HAS_TIMER": 1,
    "START_AT": "10:56:1",
    "END_AT":"11:1:15"
 } 
}
{
 "CMD": "EVENT_TRIGGER_OUTPUT_DEVICE_MAPPING",
 "TYPE": "ADD",
 "DATA": {
    "EVENT_TRIGGER_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "GUID": "97ab44a3-e788-46a1-9c07-79f39d6be33f",
    "EVENT_TRIGGER_TYPE_ID": 1,
    "STATUS": "SUCCESS",
    "DEVICES": [
    {
        "DEVICE_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
        "DEVICE_UNICAST_ID": 4
    }
 ]
 }}
``` 
## EVENT_TRIGGER
### TYPE: "EDIT" Sửa 1 EVENT_TRIGGER
#### Mẫu bản tin thục hiện
```
{
 "CMD": "EVENT_TRIGGER",
 "TYPE": "EDIT",
 "DATA": {
    "EVENT_TRIGGER_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "GROUP_ID": "97ab44a3-e788-46a1-9c07-79f39d6be33f",
    "EVENT_TRIGGER_TYPE_ID": 1,
    "PRIORITY": 1,
    "HAS_TIMER": 1,
    "START_AT": "10:1:15",
    "END_AT":"12:1:15",
    "EACH_DAY":["EACHMONDAY","EACHTUESDAY"]
 } }
```
### Mẫu bản tin phản hồi
```
{
 "CMD": "EVENT_TRIGGER",
 "TYPE": "EDIT",
 "DATA": {
    "EVENT_TRIGGER_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "GROUP_ID": "97ab44a3-e788-46a1-9c07-79f39d6be33f",
    "EVENT_TRIGGER_TYPE_ID": 1,
    "PRIORITY": 1,
    "HAS_TIMER": 1,
    "START_AT": "10:1:15",
    "END_AT":"12:1:15"
 } }
``` 
## EVENT_TRIGGER
### TYPE: "DELETE" Xóa 1 EVENT_TRIGGER
#### Mẫu bản tin thục hiện
```
{
 "CMD": "EVENT_TRIGGER",
 "TYPE": "DELETE",
 "DATA": {
    "EVENT_TRIGGER_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2"
 } }
```
### Mẫu bản tin phản hồi
```
{
 "CMD": "EVENT_TRIGGER",
 "TYPE": "DELETE",
 "DATA": {
    "EVENT_TRIGGER_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2"
 } }
``` 
## EVENT_TRIGGER_OUTPUT_DEVICE_MAPPING
### TYPE: "ADD" Nếu :"EVENT_TRIGGER_TYPE_ID" : 1 "GUID": ID của SCENE thêm trường "SCENE_UNICAST_ID": 4
#### Mẫu bản tin thục hiện
```
{
 "CMD": "EVENT_TRIGGER_OUTPUT_DEVICE_MAPPING",
 "TYPE": "ADD",
 "DATA": {
    "EVENT_TRIGGER_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "GUID": "97ab44a3-e788-46a1-9c07-79f39d6be33f",
    "EVENT_TRIGGER_TYPE_ID": 1,
    "DEVICES": [
    {
        "DEVICE_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
        "PROPERTIES": [
        {
            "ID": 1201,
            "VALUE": 1
        }
    ]
 }
 ],
 "GROUPS": [
    {
        "GROUP_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
        "PROPERTIES": [
        {
            "ID": 0,
        "VALUE": 1
        }
        ]
    }
 ]
 }}
```
### Mẫu bản tin phản hồi
```
{
 "CMD": "EVENT_TRIGGER_OUTPUT_DEVICE_MAPPING",
 "TYPE": "ADD",
 "DATA": {
    "EVENT_TRIGGER_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "GUID": "97ab44a3-e788-46a1-9c07-79f39d6be33f",
    "EVENT_TRIGGER_TYPE_ID": 1,
    "STATUS": "SUCCESS",
    "DEVICE_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2"
 }}
``` 
## EVENT_TRIGGER_OUTPUT_DEVICE_MAPPING
### TYPE: DELETE
#### Mẫu bản tin thục hiện
```
{
 "CMD": "EVENT_TRIGGER_OUTPUT_DEVICE_MAPPING",
 "TYPE": "DELETE",
 "DATA": {
    "EVENT_TRIGGER_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "GUID": "97ab44a3-e788-46a1-9c07-79f39d6be33f",
    "EVENT_TRIGGER_TYPE_ID": 1,
    "DEVICES": [
        "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2"
    ],
    "GROUPS": [
    "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2"
 ]
 }}
```
### Mẫu bản tin phản hồi
```
{
 "CMD": "EVENT_TRIGGER_OUTPUT_DEVICE_MAPPING",
 "TYPE": "DELETE",
 "DATA": {
    "EVENT_TRIGGER_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "GUID": "97ab44a3-e788-46a1-9c07-79f39d6be33f",
    "DEVICE_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2"
 }}
``` 
## DEVICE_UPDATE_STATUS
### Bản tin cập nhật trạng thái thiết bị khi vừa mở app
#### Mẫu bản tin thục hiện
```
{
 "CMD": "DEVICE_UPDATE",
 "TIME_UPDATE":"YYYY MM D HH:MM" }
```
### Mẫu bản tin phản hồi
```
{
 "CMD": "DEVICE_UPDATE",
 "DATA": {
    "DEVICE_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "ID": 0,
    "VALUE": 1
 }
}
 {
 "CMD": "DEVICE_UPDATE",
 "DEVICE_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
 "STATUS":"OFFLINE"
 }
}
``` 

## RULE
### TYPE": "CREATE" tạo rule với các thông số được cài đặt theo thông số người dùng lựa chọn
### *Lưu ý: VD: Nếu không có thời gian bỏ trường thời gian START_AT,END_AT
#### Mẫu bản tin thục hiện
```
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
        "DEVICE_ID":"aa3549d4-5471-4d75-b0b2-b70fa5c10fb26666666666666",
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
 }}
```
### Mẫu bản tin phản hồi
```
{
 "CMD": "EVENT_TRIGGER",
 "DATA":{
    "EVENT_TRIGGER_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "STATUS": "SUCCESS"
 }}
``` 

## RULE
### TYPE: EDIT giống bản tin CREATE nhưng các thông số bị thay đổi
#### Mẫu bản tin thục hiện
```
{
 "CMD": "EVENT_TRIGGER",
 "TYPE": "EDIT",
 "DATA": {
    "EVENT_TRIGGER_ID": "aaaa",
    "GROUP_ID": "111",
    "EVENT_TRIGGER_TYPE_ID": 2,
    "PRIORITY": 3,
    "HAS_TIMER": 1,
    "START_AT": "10:56:1",
    "END_AT": "11:1:15",
    "HAS_REPEATER":1,
    "EACH_DAY":["EACHMONDAY","EACHTUESDAY"],
    "LOGICAL_OPERATOR_ID":-1,
    "DEVICES": [
    {
        "DEVICE_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
        "PROPERTIES": [
        {
            "ID": 0,
            "VALUE": 1
        },
        {
            "ID": 2,
            "VALUE": 50
        }
        ]
    }
    {
        "DEVICE_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
        "PROPERTIES": [
        {
            "ID": 0,
            "VALUE": 1
        }
        ]
    }
    ],
    "GROUPS": [
    {
        "GROUP_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
        "PROPERTIES": [
        {
            "ID": 0,
            "VALUE": 1
        }
    ],
    "SCENE": [
    {
        "SCENE_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2"
    }
    ]
 }
 ]
 }}
```
### Mẫu bản tin phản hồi
```

``` 

## RULE
### TYPE: DELETE
#### Mẫu bản tin thục hiện
```
{
 "CMD": "EVENT_TRIGGER",
 "TYPE": "DELETE",
 "DATA": {
    "EVENT_TRIGGER_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2"
 }}
```
### Mẫu bản tin phản hồi
```
{
 "CMD": "EVENT_TRIGGER",
 "TYPE": "DELETE",
 "DATA": {
    "EVENT_TRIGGER_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2"
 }}
``` 
## RULE
### TYPE: STATUS
#### Mẫu bản tin thục hiện
```
{
 "CMD": "EVENT_TRIGGER",
 "TYPE": "STATUS",
 "DATA": {
    "EVENT_TRIGGER_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "STATUS_ID": 0
 }}
```
### Mẫu bản tin phản hồi
```
{
 "CMD": "EVENT_TRIGGER",
 "TYPE": "STATUS",
 "DATA": {
    "EVENT_TRIGGER_ID": "aa3549d4-5471-4d75-b0b2- b70fa5c10fb2",
    "STATUS_ID": 0
 }}
``` 
# Một số lệnh phản hồi đặc biệt
## Bản tin phản hồi khi thiết bị được thêm vào mạng
```
{
 "CMD": "TYPE_DEVICE",
 "DATA":
 {
    "DEVICE_UNICAST_ID": 123,
    "DEVICE_ID": "b717f8d86f1843c0ae4669c32998f653",
    "DEVICE_KEY": "b717f8d86f1843c0ae4669c32998f653",
    "NET_KEY": "b717f8d86f1843c0ae4669c32998f653",
    "APP_KEY": "b717f8d86f1843c0ae4669c32998f653",
    "DEVICE_TYPE_ID": 23002
 }
}
```
## Bản tin phản hồi thiệt độ, độ ẩm, bụi mịn :2.5;10;1.0
```
{
 "CMD":"SENSOR_VALUE",
 "DATA":{
    "DEVICE_ID":"b717f8d8-6f18-43c0-ae46-69c32998f653",
    "TEMPERATURE_VALUE":30
 }
}
{
 "CMD":"SENSOR_VALUE",
 "DATA":{
    "DEVICE_ID":"b717f8d8-6f18-43c0-ae46-69c32998f653",
    "HUMIDITY_VALUE":30
 }
}
{
 "CMD":"SENSOR_VALUE",
 "DATA":{
    "DEVICE_ID":"b717f8d8-6f18-43c0-ae46-69c32998f653",
    "PM2.5_VALUE":30
 }
}
{
 "CMD":"SENSOR_VALUE",
 "DATA":{
    "DEVICE_ID":"b717f8d8-6f18-43c0-ae46-69c32998f653",
    "PM1_VALUE":30
 }
}
{
 "CMD":"SENSOR_VALUE",
 "DATA":{
    "DEVICE_ID":"b717f8d8-6f18-43c0-ae46-69c32998f653",
    "PM10_VALUE":30
 }
}
```
## Bản tin phản hồi pin, lux, pir
```
{
 "CMD":"SENSOR_VALUE",
 "DATA":{
    "DEVICE_ID":"b717f8d8-6f18-43c0-ae46-69c32998f653",
    "POWER_VALUE":30
 }
}
{
 "CMD":"SENSOR_VALUE",
 "DATA":{
    "DEVICE_ID":"b717f8d8-6f18-43c0-ae46-69c32998f653",
    "LUX_VALUE":30
 }
}
{
 "CMD":"SENSOR_VALUE",
 "DATA":{
    "DEVICE_ID":"b717f8d8-6f18-43c0-ae46-69c32998f653",
    "PIR_VALUE":30
 }
}
```
## Bản tin phản hồi trạng thái nút nhấn
```
{
 "CMD": "REMOTE",
 "DATA": {
    "DEVICE_ID": "b717f8d8-6f18-43c0-ae46-69c32998f653",
    "BUTTON_VALUE": "BUTTON_1",
    "MODE_VALUE": 1
 }
}
```
## Bản tin phản hồi trạng thái cảm biến khói
```
{
 "CMD": "SENSOR_VALUE",
 "DATA": {
    "DEVICE_ID": "b717f8d8-6f18-43c0-ae46-69c32998f653",
    "SMOKE_VALUE":1
 }
}
```
## Bản tin phản hồi cảm biến cửa
```
{
 "CMD": "SENSOR_VALUE",
 "DATA": {
    "DEVICE_ID": "b717f8d8-6f18-43c0-ae46-69c32998f653",
    "HANG_VALUE":1,
    "DOOR_VALUE":1
 }
}
```
