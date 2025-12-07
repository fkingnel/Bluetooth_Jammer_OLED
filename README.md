<h1 align="center">OLED 'ESP32-BlueJammer'</h1>
<div align="center">
  <img src="https://raw.githubusercontent.com/fkingnel/OLED_ESP32-BlueJammer/refs/heads/main/Gallery/OLED_ESP32_BLUEJAMMER_PREVIEW.JPG" alt="OLED ESP32-BlueJammer" width=450>
  <h3 align="center">This is a fork, the original creator of the BlueJammer is @emensta, below are their github. Go show some support. </h3>
</div>

<div align="center">    
<a href="https://github.com/EmenstaNougat/ESP32-BlueJammer" title="Go to GitHub repo">
  <img src="https://img.shields.io/static/v1?label=EmenstaNougat&message=ESP32-BlueJammer&color=purple&logo=github" alt="EmenstaNougat - ESP32-BlueJammer">
</a>
<a href="https://github.com/EmenstaNougat/ESP32-BlueJammer">
  <img src="https://img.shields.io/github/stars/EmenstaNougat/ESP32-BlueJammer?style=social" alt="stars - ESP32-BlueJammer">
</a>
<a href="https://github.com/EmenstaNougat/ESP32-BlueJammer">
  <img src="https://img.shields.io/github/forks/EmenstaNougat/ESP32-BlueJammer?style=social" alt="forks - ESP32-BlueJammer">
</a>
</div>

## <h3 align="center"> DISCLAIMER </h3>

<h3 align="center">Jamming is ILLEGAL. For education only. What follows if misused is on you.</h3>
  
<h4 align="center">
Proceed only if you understand the gravity of what you are engaging with.  
This tool exists solely for educational insight — nothing more.  
Any attempt to use it for unlawful or unethical purposes is not only forbidden,  
but may draw consequences far beyond your control.
</h4>

<h4 align="center">
Your choices are yours alone… and so are the repercussions.  
I bear no responsibility for whatever may follow.
</h4>

<!-- <h4 align="center">
  <a href="https://github.com/EmenstaNougat/ESP32-BlueJammer#hardware---make-your-own-esp32-bluejammer">Make your own</a>
    <span> | </span>
  <a href="https://github.com/EmenstaNougat/ESP32-BlueJammer#esp32-nrf24l01-pinout--battery-mod">Schematics</a>
    <span> | </span>
  <a href="https://github.com/EmenstaNougat/ESP32-BlueJammer?tab=readme-ov-file#pcb">Hardware layout</a>
    <span> | </span>
  <a href="https://github.com/EmenstaNougat/ESP32-BlueJammer?tab=readme-ov-file#pcbs-with-esp32-and-rf-module-capability">PCB's</a>
    <span> | </span>
  <a href="https://github.com/EmenstaNougat/ESP32-BlueJammer#video-tutorials-and-demonstrations">Demos</a>
    <span> | </span>
  <a href="https://github.com/EmenstaNougat/ESP32-BlueJammer#operation-channels">Channels</a>
    <span> | </span>
  <a href="https://github.com/EmenstaNougat/ESP32-BlueJammer?tab=readme-ov-file#flashing-the-firmware">Flashing</a>
    <span> | </span>
  <a href="https://github.com/EmenstaNougat/ESP32-BlueJammer#3d-printed-case">3D case</a>
    <span> | </span>
  <a href="https://github.com/EmenstaNougat/ESP32-BlueJammer?tab=readme-ov-file#about-the-esp32-bluejammer-and-my-source-code">About</a>
    <span> | </span>
  <a href="https://github.com/EmenstaNougat/ESP32-BlueJammer?tab=readme-ov-file#support-me">Support me</a>
    <span> | </span>
  <a href="https://emensta.pages.dev">Website</a>
</h4> -->

## ESP32-BlueJammer
"The ESP32-BlueJammer (Bluetooth jammer, BLE jammer, WiFi jammer, RC jammer) disrupts various devices using an ESP32 and nRF24 modules, causing plenty of noise and sending unnecessary packets (DoS).              
                                                                    
It interrupts:  
**The whole 2.4GHz broadband!** Everything that works on 2.4GHz is being interfered, like:                                                       
audio in speakers being transmitted over bluetooth, microphones on 2.4GHz, smartphone connections, WiFi, RC Drones (etc.), IoT devices, smart gadgets, wireless keyboard & mouse, just anything on 2.4GHz!

Ideal for controlled disruption and security testing. Based on 2.4GHz communication.

It has a big range (over 30Meters+ - may vary on your antenna and hardware setup!) on newest Bluetooth versions with casual 2.4GHz antennas, you can easily increase this as well by taking some simple "bigger" router antennas.
An amplifier (2.4GHz) may be a good option too!

Remember that jamming is illegal and should not be used with malicious intent!"  
<p align="center">-@emensta</p>

## Demonstration Video

https://github.com/user-attachments/assets/f5e9a63b-46d5-453c-8dd0-330a347de92a

## Operation Channels
- **Bluetooth** = 79CH  
  Frequency Range: 2.402 GHz to 2.480 GHz  
  Channel Width: 1 MHz

- **BLE** = 40CH  
  Frequency Range: 2.400 GHz to 2.4835 GHz  
  Channel Width: 2 MHz

- **WiFi** = 14CH  
  Frequency Range: 2.400 GHz to 2.4835 GHz  
  Channel Width: Typically 20 MHz, but can be 22 MHz or 40 MHz in some cases

- **RC drones, etc.** = 1-125CH  
  Frequency Range: 2.400 GHz to 2.525 GHz  
  Channel Width: 1 MHz



## How to use?

### Instant Attacks
The jammer starts immediately upon powering up the device, allowing for instant attacks depending on the states and firmware flashed.

### Combo-Channel-Select_BT-BLE-WiFi-RC firmware:
- Use the "Boot" button on the ESP32 to switch between the channel modes on the Combo-Firmware, allowing for full control without the need of purchasing additional tactile buttons
- The OLED will display your current operation channel
- The status LED lets you know about the current state you're in:  
1 blink = BT  
2 blinks = BLE  
3 blinks = WiFi  
4 blinks = RC  
- The serial output of your ESP32-BlueJammer will output the following lines when switching mode:  
State 1: Bluetooth  
State 2: Bluetooth Low Energy  
State 3: WiFi  
State 4: RC  

### Firmwares:
The firmware you choose indicates the operation channel by its name, this means:

Bluetooth_80_CH - jams classic Bluetooth  
Frequency Range: 2.402 GHz to 2.480 GHz  

BluetoothLowEnergy_40_CH - jams Bluetooth Low Energy  
Frequency Range: 2.400 GHz to 2.4835 GHz  

Bluetooth-BluetoothLowEnergy_40-80_CH - jams classic Bluetooth & Bluetooth Low Energy  
Frequency Range: 2.402 GHz to 2.480 GHz & 2.400 GHz to 2.4835 GHz  

Bluetooth-WiFi_14-80_CH - jams classic Bluetooth & WiFi  
Frequency Range: 2.402 GHz to 2.480 GHz & 2.400 GHz to 2.4835 GHz  

WiFi_14_CH - jams WiFi  
Frequency Range: 2.400 GHz to 2.4835 GHz  

2.4GHzRemoteControl(Drones etc.)_1-125_CH - jams RC (Drones etc.)  
  Frequency Range: 2.400 GHz to 2.525 GHz  



## Hardware - Make your own ESP32-BlueJammer

<img src="https://github.com/fkingnel/OLED_ESP32-BlueJammer/blob/main/Gallery/OLED_ESP32_BLUEJAMMER_HARDWARE.JPG?raw=true" alt="OLED ESP32-BlueJammer Hardware" width=450>

**(Aliexpress affiliate links)**

### Required:

- **[ESP32-32U CP2102](https://s.click.aliexpress.com/e/_Exmp8nq)** (Any ESP32 should work as long as it has the needed pins)
- **[Radio Frequency Modules](https://s.click.aliexpress.com/e/_EyV60dE)** (2x for HSPI and VSPI) (In my build I used **[EBYTE'S E01-2G4M27D](https://s.click.aliexpress.com/e/_EyV60dE)** radio modules, which are a more powerful and longer range module in comparison to the **[nRF24L01+PA+LNA](https://s.click.aliexpress.com/e/_EywFIlw)**)
- **[RF Antennas](https://s.click.aliexpress.com/e/_EQCuDbS)** (2x) (Only necessary if purchasing the **[E01-2G4M27D](https://s.click.aliexpress.com/e/_EyV60dE)** or upgrading from the standard ones provided with the **[nRF24L01+PA+LNA](https://s.click.aliexpress.com/e/_EywFIlw)**)
- **[0.96" OLED Display I2C](https://s.click.aliexpress.com/e/_EGRRjde)** (Black and white>>>)
- **[10-100uF Capacitor](https://s.click.aliexpress.com/e/_EyHFrLS)** (2x) (Any voltage above 5V, this can be considered optional, but will greatly increase the reliability and performance of your radio modules)
- **[Prototype PCB](https://s.click.aliexpress.com/e/_Ewohwku)** (The size used in my build is 7x9cm)

### Additional:

- **[3rd Antenna: IPEX to SMA-F pigtail](https://s.click.aliexpress.com/e/_EzrVXmu)** (Connected to the ESP32 chip itself helps with reliable long-range interference. It ensures a better intermediate signal and stability when jamming, completely optional)
- **[Status LED: **3mm LED**](https://s.click.aliexpress.com/e/_Eu82QNi)** (Show jamming state profile)
- **[4.7k Ohm Resistor](https://s.click.aliexpress.com/e/_EQOvcLA)**

### Battery for portability:

- **[3.7V Li-Ion Battery](https://s.click.aliexpress.com/e/_EukzDb6)**
- **[JST PH 2.0 Connector](https://s.click.aliexpress.com/e/_EQspIEU)**
- **[TP4056 Charging Module (Micro-USB/Type-C)](https://s.click.aliexpress.com/e/_EI1LIg0)**
- **[Power Switch](https://s.click.aliexpress.com/e/_EHwlnR6)**

## Flashing the firmware
### via webflasher (Easy)  
![ESP32-BlueJammerFlasher](https://dwdwpld.pages.dev/ESP32BlueJammerFlasher.png)                                                                 
@emensta has created a webflasher to make it super easy for you to flash your ESP32 chip with the ESP32-BlueJammer firmware of your choice
- Visit [ESP32-BlueJammerFlasher](https://esp32-bluejammerflasher.pages.dev)
- First, choose the firmware type, "Generic" or "0.96" OLED"
- Choose the firmware you want to flash
- Hold the boot button to boot the ESP32 into flash mode
- Connect your ESP32 via a data USB cable
- Flash the firmware of your choice

### Flashing ESP32 via binary files (Advanced)  
- Download the **.bin files** available on this repository (or @emensta's)
- Use any flasher of your choice
- Flash

If your ESP32 does not appear in the device list or is not being recognized, you may need to install the [Silicon Labs CP210x USB-to-UART driver](https://www.silabs.com/documents/public/software/CP210x_Windows_Drivers.zip).



## Wiring Connections             
 
 <div align="center">
 
 <img src="https://dwdwpld.pages.dev/nRF24L01pinout.png" alt="nRF24L01 PINOUT" width=450>
 

### HSPI
| 1st nRF24L01 module Pin | HSPI Pin (ESP32) | 10uf capacitor |
|---------------|------------------|--------------------|
| VCC           | 3.3V             | (+) capacitor |
| GND           | GND              | (-) capacitor |
| CE            | GPIO 16          |
| CSN           | GPIO 15          |
| SCK           | GPIO 14          |
| MOSI          | GPIO 13          |
| MISO          | GPIO 12          |
| IRQ           |                  |

### VSPI 
| 2nd nRF24L01 module Pin | VSPI Pin (ESP32) | 10uf capacitor |
|---------------|------------------|--------------------|
| VCC           | 3.3V             | (+) capacitor |
| GND           | GND              | (-) capacitor |
| CE            | GPIO 22          |
| CSN           | GPIO 21          |
| SCK           | GPIO 18          |
| MOSI          | GPIO 23          |
| MISO          | GPIO 19          |
| IRQ           |                  |

### Status LED
| ESP32 | 4.7k Ohm Resistor | 3mm Status LED (blue)|
|-------|-------------------|----------------------|
|  GND  |                   |       (-) LED        |
|       |      Resistor     |       (+) LED        |
|GPIO27 |      Resistor     |                      |

### OLED Display I2C (additional - make sure to use the correct firmware!)
| 0.96" OLED Display I2C | ESP32 |
|------------------------|-------|
|          GND           |  GND  |
|          VCC           | 3.3V  |
|          SCL           |GPIO 5 |
|          SDA           |GPIO 4 |

### Battery modification (additional)
| 3.7V Li-Ion battery | JST-PH2 connector    | TP4056 Charging Module | Mini Slide Switch | ESP32 |
|---------------------|----------------------|------------------------|-------------------|-------|
| (+) Battery         | (+) JST-PH2          | Bat +                  |                   |       |
| (-) Battery         | (-) JST-PH2          | Bat -                  |                   |       |
|                     |                      | OUT +                  | Switch in         |       |
|                     |                      | OUT -                  |                   |  GND  |
|                     |                      |                        | Switch out        |  3V3  |

</div>
