# 64030074 Thani Paknam
repo : https://github.com/tnpn2545/ESP32WIFIPROVISION

OUTPUT หลังต่อ WIFI
```
PS D:\COM_P3\KLA\ALL\ESP32_WiFi_Provision> set IDF_PATH=C:\Users\gamem\esp\esp-idf
PS D:\COM_P3\KLA\ALL\ESP32_WiFi_Provision> C:\Espressif\python_env\idf4.4_py3.8_env\Scripts\python.exe C:\Users\gamem\esp\esp-idf\tools\idf_monitor.py -p COM6 -b 115200 --toolchain-prefix xtensa-esp32-elf- --target esp32 d:\COM_P3\KLA\ALL\ESP32_WiFi_Provision\build\wifi_prov_mgr.elf
--- WARNING: GDB cannot open serial ports accessed as COMx
--- Using \\.\COM6 instead...
--- idf_monitor on \\.\COM6 115200 ---
--- Quit: Ctrl+] | Menu: Ctrl+T | Help: Ctrl+T followed by Ctrl+H ---
.255.240, gets Jul 29 2019 12:21:46

rst:0x1 (POWERON_RESET),boot:0x12 (SPI_FAST_FLASH_BOOT)
configsip: 0, SPIWP:0xee
clk_drv:0x00,q_drv:0x00,d_drv:0x00,cs0_drv:0x00,hd_drv:0x00,wp_drv:0x00
mode:DIO, clock div:2
load:0x3fff0030,len:6652
ho 0 tail 12 room 4
load:0x40078000,len:15060
load:0x40080400,len:3836
0x40080400: _init at ??:?

entry 0x4008069c
I (29) boot: ESP-IDF v4.4.6 2nd stage bootloader
I (29) boot: compile time 15:04:26
I (29) boot: Multicore bootloader
I (32) boot: chip revision: v3.0
I (36) boot.esp32: SPI Speed      : 40MHz
I (41) boot.esp32: SPI Mode       : DIO
I (45) boot.esp32: SPI Flash Size : 4MB
I (50) boot: Enabling RNG early entropy source...
I (55) boot: Partition Table:
I (59) boot: ## Label            Usage          Type ST Offset   Length
I (66) boot:  0 nvs              WiFi data        01 02 00009000 00006000
I (74) boot:  1 phy_init         RF data          01 01 0000f000 00001000
I (81) boot:  2 factory          factory app      00 00 00010000 0013d620
I (89) boot: End of partition table
I (93) esp_image: segment 0: paddr=00010020 vaddr=3f400020 size=1eb18h (125720) map
I (147) esp_image: segment 1: paddr=0002eb40 vaddr=3ffbdb60 size=014d8h (  5336) load
I (149) esp_image: segment 2: paddr=00030020 vaddr=400d0020 size=ac170h (704880) map
I (408) esp_image: segment 3: paddr=000dc198 vaddr=3ffbf038 size=03984h ( 14724) load
I (414) esp_image: segment 4: paddr=000dfb24 vaddr=40080000 size=1e164h (123236) load
I (479) boot: Loaded app from partition at offset 0x10000
I (479) boot: Disabling RNG early entropy source...
I (491) cpu_start: Multicore app
I (491) cpu_start: Pro cpu up.
I (491) cpu_start: Starting app cpu, entry point is 0x40081214
0x40081214: call_start_cpu1 at C:/Users/gamem/esp/esp-idf/components/esp_system/port/cpu_start.c:151

I (0) cpu_start: App cpu up.
I (509) cpu_start: Pro cpu start user code
I (509) cpu_start: cpu freq: 160000000
I (509) cpu_start: Application information:
I (513) cpu_start: Project name:     wifi_prov_mgr
I (519) cpu_start: App version:      1
I (523) cpu_start: Compile time:     Nov  7 2023 15:03:54
I (529) cpu_start: ELF file SHA256:  057c56f251366149...
I (535) cpu_start: ESP-IDF:          v4.4.6
I (540) cpu_start: Min chip rev:     v0.0
I (545) cpu_start: Max chip rev:     v3.99 
I (550) cpu_start: Chip rev:         v3.0
I (555) heap_init: Initializing. RAM available for dynamic allocation:
I (562) heap_init: At 3FFAFF10 len 000000F0 (0 KiB): DRAM
I (568) heap_init: At 3FFB6388 len 00001C78 (7 KiB): DRAM
I (574) heap_init: At 3FFB9A20 len 00004108 (16 KiB): DRAM
I (580) heap_init: At 3FFC8900 len 00017700 (93 KiB): DRAM
I (586) heap_init: At 3FFE0440 len 00003AE0 (14 KiB): D/IRAM
I (593) heap_init: At 3FFE4350 len 0001BCB0 (111 KiB): D/IRAM
I (599) heap_init: At 4009E164 len 00001E9C (7 KiB): IRAM
I (607) spi_flash: detected chip: generic
I (610) spi_flash: flash io: dio
I (615) cpu_start: Starting scheduler on PRO CPU.
I (0) cpu_start: Starting scheduler on APP CPU.
I (694) wifi:wifi driver task: 3ffccf2c, prio:23, stack:6656, core=0
I (694) system_api: Base MAC address is not set
I (694) system_api: read default base MAC address from EFUSE
I (714) wifi:wifi firmware version: 1ba8b6a
I (714) wifi:wifi certification version: v7.0
I (714) wifi:config NVS flash: enabled
I (714) wifi:config nano formating: disabled
I (724) wifi:Init data frame dynamic rx buffer num: 32
I (724) wifi:Init management frame dynamic rx buffer num: 32
I (734) wifi:Init management short buffer num: 32
I (734) wifi:Init dynamic tx buffer num: 32
I (734) wifi:Init static rx buffer size: 1600
I (744) wifi:Init static rx buffer num: 10
I (744) wifi:Init dynamic rx buffer num: 32
I (754) wifi_init: rx ba win: 6
I (754) wifi_init: tcpip mbox: 32
I (754) wifi_init: udp mbox: 6
I (764) wifi_init: tcp mbox: 6
I (764) wifi_init: tcp tx win: 5744
I (764) wifi_init: tcp rx win: 5744
I (774) wifi_init: tcp mss: 1440
I (774) wifi_init: WiFi IRAM OP enabled
I (784) wifi_init: WiFi RX IRAM OP enabled
I (784) wifi_prov_scheme_ble: BT memory released
I (794) app: Already provisioned, starting Wi-Fi STA
I (794) wifi_prov_scheme_ble: BTDM memory released
I (804) phy_init: phy_version 4771,450c73b,Aug 16 2023,11:03:10
I (884) wifi:mode : sta (94:b5:55:f6:f1:00)
I (884) wifi:enable tsf
I (894) wifi:new:<6,0>, old:<1,0>, ap:<255,255>, sta:<6,0>, prof:1
I (894) wifi:state: init -> auth (b0)
I (904) wifi:state: auth -> assoc (0)
I (914) wifi:state: assoc -> run (10)
I (954) wifi:connected with Solomon, aid = 1, channel 6, BW20, bssid = 4a:ef:22:9f:09:5b
I (954) wifi:security: WPA2-PSK, phy: bgn, rssi: -49
I (964) wifi:pm start, type: 1

I (974) wifi:<ba-add>idx:0 (ifx:0, 4a:ef:22:9f:09:5b), tid:0, ssn:2, winSize:64
I (1004) wifi:AP's beacon interval = 102400 us, DTIM period = 1
I (1964) app: Connected with IP Address:172.20.10.3
I (1964) esp_netif_handlers: sta ip: 172.20.10.3, mask: 255.255.255.240, gw: 172.20.10.1
I (1964) app: Hello World!
I (2964) app: Hello World!
I (3964) app: Hello World!
I (4964) app: Hello World!
I (5964) app: Hello World!
I (6964) app: Hello World!
I (7964) app: Hello World!
I (8964) app: Hello World!
I (9964) app: Hello World!
I (10964) app: Hello World!
I (11964) app: Hello World!
I (12964) app: Hello World!
I (13964) app: Hello World!
I (14964) app: Hello World!
I (15964) app: Hello World!
I (16964) app: Hello World!
I (17964) app: Hello World!
I (18964) app: Hello World!
I (19964) app: Hello World!
I (20964) app: Hello World!
I (21964) app: Hello World!
I (22964) app: Hello World!
I (23964) app: Hello World!
I (24964) app: Hello World!
I (25964) app: Hello World!
I (26964) app: Hello World!
I (27964) app: Hello World!
I (28964) app: Hello World!
I (29964) app: Hello World!
I (30964) app: Hello World!
I (31964) app: Hello World!
I (32964) app: Hello World!
```
QR CODE
![image](https://github.com/tnpn2545/ESP32-Provision-Manager/assets/115066414/deaca57a-8272-48b1-9906-9b1850f16197)
