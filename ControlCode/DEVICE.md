
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

