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