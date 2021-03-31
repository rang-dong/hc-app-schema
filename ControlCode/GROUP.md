
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

