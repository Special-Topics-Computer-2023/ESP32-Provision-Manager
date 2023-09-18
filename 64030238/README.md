# 64030238  

# ลิ้ง repo
[https://github.com/JASDA0000/ESPWIFIPROVISION.h](https://github.com/JASDA0000/ESPWIFIPROVISION.git)

## OUTPUT ก่อนต่อ WIFI
```
I (654) cpu_start: Starting scheduler on PRO CPU.
I (0) cpu_start: Starting scheduler on APP CPU.
I (748) wifi:wifi driver task: 3ffccf54, prio:23, stack:6656, core=0
I (748) system_api: Base MAC address is not set
I (748) system_api: read default base MAC address from EFUSE
I (768) wifi:wifi firmware version: 57982fe
I (768) wifi:wifi certification version: v7.0
I (768) wifi:config NVS flash: enabled
I (768) wifi:config nano formating: disabled
I (778) wifi:Init data frame dynamic rx buffer num: 32
I (778) wifi:Init management frame dynamic rx buffer num: 32
I (788) wifi:Init management short buffer num: 32
I (788) wifi:Init dynamic tx buffer num: 32
I (798) wifi:Init static rx buffer size: 1600
I (798) wifi:Init static rx buffer num: 10
I (808) wifi:Init dynamic rx buffer num: 32
I (808) wifi_init: rx ba win: 6
I (808) wifi_init: tcpip mbox: 32
I (818) wifi_init: udp mbox: 6
I (818) wifi_init: tcp mbox: 6
I (818) wifi_init: tcp tx win: 5744
I (828) wifi_init: tcp rx win: 5744
I (828) wifi_init: tcp mss: 1440
I (838) wifi_init: WiFi IRAM OP enabled
I (838) wifi_init: WiFi RX IRAM OP enabled
I (848) wifi_prov_scheme_ble: BT memory released
I (848) app: Already provisioned, starting Wi-Fi STA
I (858) wifi_prov_scheme_ble: BTDM memory released
I (858) phy_init: phy_version 4670,719f9f6,Feb 18 2021,17:07:07
I (968) wifi:mode : sta (24:d7:eb:0e:c8:d0)
I (968) wifi:enable tsf
I (3378) app: Disconnected. Connecting to the AP again...
I (5798) app: Disconnected. Connecting to the AP again...
I (8208) app: Disconnected. Connecting to the AP again...
ets Jul 29 2019 12:21:46

rst:0x1 (POWERON_RESET),boot:0x13 (SPI_FAST_FLASH_BOOT)
configsip: 0, SPIWP:0xee
clk_drv:0x00,q_drv:0x00,d_drv:0x00,cs0_drv:0x00,hd_drv:0x00,wp_drv:0x00
mode:DIO, clock div:2
load:0x3fff0030,len:6944
load:0x40078000,len:15500
load:0x40080400,len:3844
0x40080400: _init at ??:?

entry 0x4008064c
I (27) boot: ESP-IDF v5.0.2-dirty 2nd stage bootloader
I (27) boot: compile time 09:46:40
I (28) boot: chip revision: v3.0
I (31) boot.esp32: SPI Speed      : 40MHz
I (36) boot.esp32: SPI Mode       : DIO
I (40) boot.esp32: SPI Flash Size : 2MB
I (45) boot: Enabling RNG early entropy source...
I (50) boot: Partition Table:
I (54) boot: ## Label            Usage          Type ST Offset   Length
I (61) boot:  0 nvs              WiFi data        01 02 00009000 00006000
I (68) boot:  1 phy_init         RF data          01 01 0000f000 00001000
I (76) boot:  2 factory          factory app      00 00 00010000 0013d620
I (83) boot: End of partition table
I (87) esp_image: segment 0: paddr=00010020 vaddr=3f400020 size=2a130h (172336) map
I (158) esp_image: segment 1: paddr=0003a158 vaddr=3ffbdb60 size=050f8h ( 20728) load
I (167) esp_image: segment 2: paddr=0003f258 vaddr=40080000 size=00dc0h (  3520) load
I (168) esp_image: segment 3: paddr=00040020 vaddr=400d0020 size=b4858h (739416) map
I (440) esp_image: segment 4: paddr=000f4880 vaddr=40080dc0 size=1dd18h (122136) load
I (505) boot: Loaded app from partition at offset 0x10000
I (505) boot: Disabling RNG early entropy source...
I (517) cpu_start: Pro cpu up.
I (517) cpu_start: Starting app cpu, entry point is 0x40081438
```
## OUTPUT หลังต่อ WIFI
![image](https://github.com/JASDA0000/ESP32-Provision-Manager/assets/103983336/81f5143d-d1ab-4389-9fc1-b9f66891c32b)
```
I (129148) protocomm_nimble: mtu update event; conn_handle=0 cid=4 mtu=256

I (130428) security2: Using salt and verifier to generate public key...
I (159788) app: Received Wi-Fi credentials
        SSID     : TP-Link_E275
        Password : 50995164
I (164168) wifi:new:<2,0>, old:<1,0>, ap:<255,255>, sta:<2,0>, prof:1
I (164948) wifi:state: init -> auth (b0)
I (164958) wifi:state: auth -> assoc (0)
I (164978) wifi:new:<2,1>, old:<2,0>, ap:<255,255>, sta:<2,1>, prof:1
I (164978) wifi:state: assoc -> run (10)
I (164998) wifi:connected with TP-Link_E275, aid = 5, channel 2, 40U, bssid = 60:a4:b7:62:e2:75
I (164998) wifi:security: WPA2-PSK, phy: bgn, rssi: -62
I (165028) wifi:pm start, type: 1

I (165028) wifi:AP's beacon interval = 102400 us, DTIM period = 1
I (165028) wifi:new:<2,0>, old:<2,1>, ap:<255,255>, sta:<2,0>, prof:1
I (169028) app: Connected with IP Address:192.168.0.102
I (169028) esp_netif_handlers: sta ip: 192.168.0.102, mask: 255.255.255.0, gw: 192.168.0.1
I (169028) wifi_prov_mgr: STA Got IP
I (169038) app: Provisioning successful
I (169038) app: Hello World!
I (169748) wifi:<ba-add>idx:0 (ifx:0, 60:a4:b7:62:e2:75), tid:0, ssn:2, winSize:64
I (170038) app: Hello World!
I (171038) app: Hello World!
I (171218) NimBLE: GAP procedure initiated: stop advertising.

I (171218) NimBLE: GAP procedure initiated: stop advertising.

I (171228) NimBLE: GAP procedure initiated: terminate connection; conn_handle=0 hci_reason=19

E (171268) protocomm_nimble: Error setting advertisement data; rc = 30
I (171278) wifi_prov_mgr: Provisioning stopped
I (171278) wifi_prov_scheme_ble: BTDM memory released
I (172038) app: Hello World!
I (173038) app: Hello World!
```
## QR CODE 
![image](https://github.com/JASDA0000/ESP32-Provision-Manager/assets/103983336/2e0d20d1-834f-4899-8784-8c9dd92f68d7)

