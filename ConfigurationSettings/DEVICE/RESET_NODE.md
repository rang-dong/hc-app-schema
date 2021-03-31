# DEVICE
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