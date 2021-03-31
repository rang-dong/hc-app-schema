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
