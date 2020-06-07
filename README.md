# MCUNotes
## 掌控板
-[Specification](http://wiki.dfrobot.com.cn/index.php?title=(SKU:DFR0608)%E6%8E%8C%E6%8E%A7%E6%9D%BF)

-[Pin to IO mapping](http://wiki.dfrobot.com.cn/index.php?title=%E6%96%87%E4%BB%B6:%E6%8E%8C%E6%8E%A7%E6%9D%BF_ESP32%E5%BC%95%E8%84%9A%E8%AF%B4%E6%98%8E.png)

-[How to use LedControl to drive ledmatrix in arduino handbit ](https://playground.arduino.cc/Main/LedControl/)

-Comments:

  **PinXX is 掌控板‘s Pin. if you use mpython or mind+ to use PinXX directly in your code. if you use 掌控板 in arduino IDE, use IOXX in your arduino code.**
```c++
#include "LedControl.h"

int dataPin = 33; // 33 is IO33 map to Pin0 on board       Pin0 ---> IO33
int clockPin = 26; // 21 is IO21 map to Pin1 on board      Pin8 ---> IO26
int csPin = 32; // 19 is IO19 map to Pin14 on board        Pin1 ---> IO32 

LedControl lc = LedControl(dataPin,clockPin,csPin,4);

void setup() {
  // put your setup code here, to run once:
 lc.shutdown(0,false);
 Serial.begin(9600);
 Serial.print(lc.getDeviceCount());
}

void loop() {
  // put your main code here, to run repeatedly:
// Serial.print(lc.getDeviceCount());
lc.setLed(0,3,3,0);
 delay(500);
 lc.setLed(0,3,3,1);
 delay(500);
}
```


## Maixduino
-[Specification]

-[Pin to IO mapping]

## Microbit
-[Specification]

-[Pin to IO mapping]

## AZ3166
-[Specification]

