# ESP32-Provision-Manager
## การ provision การเชื่อมต่อ WiFi ให้กับ ESP32

ในการโปรแกรมให้ ESP32 เชื่อมต่อกับ network ถือเป็นความเสี่ยงชนิดหนึ่งที่อาจจะก่อความเสียหายต่อ network ได้
เนื่องจากเราต้องใส่ SSID และ Password   ที่จะเชื่อมต่อเข้ากับ WiFi Access point ไว้ในโปรแกรม (ในลักษณะ hard code)
และเมื่อนำโปรแกรมเข้าสู่ public domain เช่นนำขึ้นบน git หรือ share โดยวิธีอื่น ก็จะมีข้อมูล SSID และ Password ติดไปด้วย


วิธีการที่ปลอดภัยกว่า อาจจะทำได้โดยการป้อน SSID และ Password ในขณะที่เรากำลังนำ ESP32 ไปใช้งานร่วมกับ WiFi network
ซึ่งมีข้อดีอีกประการคือ สามารถใช้กับ WiFi ใดก็ได้ โดยไม่ต้องรู้ SSID และ Password ล่วงหน้า

เนื่องจากระบบ embedded ที่ใช้ ESP32 เป็นระบบเล็กๆ อาจจะไม่มี user interface  ที่เอื้อแก่การป้อนข้อมูล  SSID และ Password  ในรูปแบบตัวอักขระ
เราจึงอาศัยอุปกรณ์สื่อสาร smartphone ที่มีอยู่ให้เป็นประโยชน์ในการทำ provision

## สิ่งที่ต้องเตรียมพร้อม

1. Smartphone ที่สามารถเชื่อมต่อ WiFi และ Bluetooth ได้ เนื่องจากเราสามารถทำ provision ได้ทั้งทาง BLE หรือ AP
2. Application สำหรับการทำ provision (ซึ่ง Application นี้เป็น open source ทำให้เราสามารถ provision ข้อมูลอื่นๆ นอกเหนือจาก SSID และ Password ได้ด้วย)


## Work flow
1. สร้าง project บน ESP-idf โดยใช้ template `wifi_prov_mgr`
2. เพิ่มปุ่มสำหรับการทำ provision (GPIO Input) จำนวน 1 ปุ่ม
3. โหลดโปรแกรมลงสู่ ESP32
4. ใช้ Mobile application ในการ provision (ป้อน SSID และ Password)
5. ใช้งาน WiFi บน ESP32 ได้ตามปกติ

## [>> ใบงานการทดลอง ESP32 WiFi provision >>](1.Create-Project.md)

