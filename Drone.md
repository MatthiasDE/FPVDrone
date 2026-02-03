# Drone Parts
## Motors
### Happymodel SE0702 23000 KV
* red dot CCW
* empty CW
* Middle Cable always same; crossed = CCW, straigt = CW

## Battery

## FPV - Analog Camera
### BetaFPV C03 Kamera
Cams are working on 5,8 GHz for Picture and Sound to avoid collision with the Radio Control on 2,4 GHz.

### Available Bands in Germany
* 5725 to 5875 MHz
* Channel Bandwith to take into consideration (e.g. 8 MHz) -> 5725 + 8 = 5733 MHz
* at Max 25 mW EIRP (equivalent isotropically radiated power)
* [10 `Fequenzbeänder` used for FPV](https://www.drone-zone.de/legale-fpv-frequenzen-in-deutschland-frequenzen-baender/) that were grown by manufacturers; each band has 8 different channels
* To avoid imapct every band has a pitch the bigger the pitch the less distribution from other pilots on neraby frequency
  * Band A: Boscam / Team Black Sheep (TBS)
    * Frequency: 5725 - 5865 MHz
    * Pitch: 20 MHz
    * Legally in Germany: Channel 1-7 (8 NOT !)
  * Band B: Boscam B
    * Frequency: 5733 - 5866 MHz
    * Pitch: 19 MHz
    * Legally in Germany: All
  * Band D: Diatone / "Low" Raceband
    * Frequency: 5362 - 5621
    * Pitch: 37 MHz
    * Legally in Germany: NOT AT ALL!
  * Band E: Boscam E / Lumenier / DJI
    * Frequency: 5645 - 5705 and 5885 - 5945 MHz
    * Pitch: 20 MHz
    * Legally in Germany: NOT AT ALL!
  * Band F: Airwave / ImmersionRC
    * Frequency: 5749 - 5880 MHz
    * Pitch: 20 MHz
    * Legally in Germany: Channel 1-7 (8 NOT !)
  * Band R: Raceband
    * Frequency: 5658 - 5917 MHz
    * Pitch: 37 MHz
    * Legally in Germany: Channel 3-6 (1, 2, 7, 8 NOT !)
  * Band H: Raceband Version 2
    * Frequency: 5653 - 5933 MHz
    * Pitch: 40 MHz
    * Legally in Germany: Channel 3-6 (1, 2, 7, 8 NOT !)
  * Band L, O and U are rare and NOT allowed in Germany


### BETAFLIGHT - Video Transmitter - Configuration Selection
* NTSC (not changeable)
* Band: `Boscam_B`
* Channel: Channel 1 (5733)
* Power: 25 mW
* Pit Mode: Off
* Pit Mode frequency: 0
* Low Poer Disarm: `On until first arm`
* Googles Two: NTSC, Page B - 5733

### Usage Rating
| Environment | Usability |
|---|---|
| Day | Very Good |
| Weak Light | Good |
| Night | Meidum |
| Indoor | Good |
| Outdoor | Very Good |

#### Technical Data
| Specification | Value |
|---|---|
| Power | 3-5,5V DC |
| Weight | 1,45g |
| Size | 11x15x14 mm |
| Sensor | 1/3" CMOS-Sensor |
| Standard | NTSC only |
| Format | 4:3 |
| Connector | JST-0.8 3pin |
| Objectiv | 2,1 mm (M7) |
| FOV | 160° |
| Picture Qulity | 1200 TVL |

## ExpressLRS
1. Download/Install [ExpressLRS Configurator](https://github.com/ExpressLRS/ExpressLRS-Configurator/releases)
2. Plug in your FC to your computer, connect to ExpressLRS Configurator instead of Betaflight Configurator
3. Choose Device: Category `BETAFPV 2.4 GHz` and device target `BETAFPV 2.4GHz AIO RX`
4. Choose Regulatory Region 2,4 Ghz Band: `2.4 GHz LBT (EU)`
4. Bindphrase selected: `<YourBindingPassphrase>`
5. Flash using the Betaflight Passthrough option in ExpressLRS Configurator


> 3.6.3 was installed on drone

```
### ExpressLRS Update Log
  ** Searching flight controllers **
      > FC found from 'COM5'

Detected the following serial ports on this system:
  COM5

======== PASSTHROUGH INIT ========
  Trying to initialize COM5 @ 420000


Attempting to detect FC UART configuration...

    ** Serial RX config detected: 'serial 2 64 115200 57600 0 115200'
Enabling serial passthrough...
  CMD: 'serialpassthrough 2 420000'

======== PASSTHROUGH DONE ========
======== RESET TO BOOTLOADER ========

  * Using full duplex (CRSF)

Verified RX target 'UNIFIED_ESP8285_2400_RX'

esptool.py v4.2.1
Serial port COM5
WARNING: Pre-connection option "no_reset" was selected. Connection may fail if the chip is not in bootloader or flasher stub mode.
Connecting...
.

Chip is ESP8285H16
Features: WiFi, Embedded Flash
Crystal is 40MHz
MAC: 00:70:07:f9:71:2f
Uploading stub...
Running stub...
Stub running...
Configuring flash size...
Flash will be erased from 0x00000000 to 0x00087fff...
Compressed 555296 bytes to 403726...
Writing at 0x00000000... (0 %)

Writing at 0x00000954... (1 %)

Writing at 0x00001612... (1 %)

Writing at 0x000023d0... (2 %)

Writing at 0x00002d5d... (2 %)

Writing at 0x000037a1... (3 %)

Writing at 0x00004354... (3 %)

Writing at 0x00004d4b... (4 %)

Writing at 0x000057ba... (4 %)

Writing at 0x000061f9... (5 %)

Writing at 0x00006d76... (5 %)

Writing at 0x0000784c... (6 %)

Writing at 0x00008421... (6 %)

Writing at 0x00009274... (7 %)

Writing at 0x0000a3ab... (7 %)

Writing at 0x0000b51e... (8 %)

Writing at 0x0000c04d... (8 %)

Writing at 0x0000cbec... (9 %)

Writing at 0x0000d78c... (9 %)

Writing at 0x0000e17e... (10 %)

Writing at 0x0000ed62... (10 %)

Writing at 0x0000f978... (11 %)

Writing at 0x00010472... (11 %)

Writing at 0x00010fac... (12 %)

Writing at 0x00011b98... (12 %)

Writing at 0x000127b0... (13 %)

Writing at 0x00013391... (13 %)

Writing at 0x00013ec0... (14 %)

Writing at 0x00014cff... (14 %)

Writing at 0x00015970... (15 %)

Writing at 0x00016728... (15 %)

Writing at 0x00017242... (16 %)

Writing at 0x00017d9b... (16 %)

Writing at 0x000189fa... (17 %)

Writing at 0x000196cc... (17 %)

Writing at 0x0001a2eb... (18 %)

Writing at 0x0001af76... (18 %)

Writing at 0x0001bb51... (19 %)

Writing at 0x0001c655... (19 %)

Writing at 0x0001d11b... (20 %)

Writing at 0x0001dd05... (20 %)

Writing at 0x0001e84a... (21 %)

Writing at 0x0001f2b1... (21 %)

Writing at 0x0001fe1f... (22 %)

Writing at 0x000208a9... (22 %)

Writing at 0x00021435... (23 %)

Writing at 0x0002204e... (23 %)

Writing at 0x00022aab... (24 %)

Writing at 0x00023559... (24 %)

Writing at 0x00024188... (25 %)

Writing at 0x00024c55... (25 %)

Writing at 0x000257c5... (26 %)

Writing at 0x00026319... (26 %)

Writing at 0x00026fe3... (27 %)

Writing at 0x00027b32... (27 %)

Writing at 0x000286fc... (28 %)

Writing at 0x00029121... (28 %)

Writing at 0x00029ce3... (29 %)

Writing at 0x0002a7b5... (29 %)

Writing at 0x0002b2e9... (30 %)

Writing at 0x0002bf2e... (30 %)

Writing at 0x0002c9be... (31 %)

Writing at 0x0002d601... (31 %)

Writing at 0x0002e4d3... (32 %)

Writing at 0x0002f082... (32 %)

Writing at 0x0002fcd0... (33 %)

Writing at 0x00030846... (33 %)

Writing at 0x00031366... (34 %)

Writing at 0x00032082... (34 %)

Writing at 0x00032e73... (35 %)

Writing at 0x00033cec... (35 %)

Writing at 0x00034a09... (36 %)

Writing at 0x0003557e... (36 %)

Writing at 0x00036100... (37 %)

Writing at 0x00036c43... (37 %)

Writing at 0x0003765d... (38 %)

Writing at 0x00038155... (38 %)

Writing at 0x00038be2... (39 %)

Writing at 0x00039630... (39 %)

Writing at 0x00039ffc... (40 %)

Writing at 0x0003aa10... (40 %)

Writing at 0x0003b71d... (41 %)

Writing at 0x0003c22f... (41 %)

Writing at 0x0003cee2... (42 %)

Writing at 0x0003da9f... (42 %)

Writing at 0x0003e56d... (43 %)

Writing at 0x0003f06c... (43 %)

Writing at 0x0003fb3c... (44 %)

Writing at 0x000405fd... (44 %)

Writing at 0x00041049... (45 %)

Writing at 0x00041b16... (45 %)

Writing at 0x00042751... (46 %)

Writing at 0x000431f7... (46 %)

Writing at 0x00043d75... (47 %)

Writing at 0x00044829... (47 %)

Writing at 0x000452b7... (48 %)

Writing at 0x00045e42... (48 %)

Writing at 0x0004695a... (49 %)

Writing at 0x00047448... (50 %)

Writing at 0x00047e4e... (50 %)

Writing at 0x00048923... (51 %)

Writing at 0x0004933e... (51 %)

Writing at 0x00049ce2... (52 %)

Writing at 0x0004a5e8... (52 %)

Writing at 0x0004afb0... (53 %)

Writing at 0x0004b9bb... (53 %)

Writing at 0x0004c481... (54 %)

Writing at 0x0004ce4a... (54 %)

Writing at 0x0004d7f8... (55 %)

Writing at 0x0004e1d5... (55 %)

Writing at 0x0004ec40... (56 %)

Writing at 0x0004f63b... (56 %)

Writing at 0x0004ff85... (57 %)

Writing at 0x00050965... (57 %)

Writing at 0x0005145a... (58 %)

Writing at 0x00051e3e... (58 %)

Writing at 0x000528d4... (59 %)

Writing at 0x000532db... (59 %)

Writing at 0x00053d54... (60 %)

Writing at 0x00054793... (60 %)

Writing at 0x000551f7... (61 %)

Writing at 0x00055b40... (61 %)

Writing at 0x000565b2... (62 %)

Writing at 0x000570c6... (62 %)

Writing at 0x00057cad... (63 %)

Writing at 0x00058863... (63 %)

Writing at 0x000594d6... (64 %)

Writing at 0x00059fea... (64 %)

Writing at 0x0005aa51... (65 %)

Writing at 0x0005b4af... (65 %)

Writing at 0x0005be9f... (66 %)

Writing at 0x0005cacf... (66 %)

Writing at 0x0005d5c4... (67 %)

Writing at 0x0005dfe1... (67 %)

Writing at 0x0005eafe... (68 %)

Writing at 0x0005f630... (68 %)

Writing at 0x00060139... (69 %)

Writing at 0x00060c9a... (69 %)

Writing at 0x0006167a... (70 %)

Writing at 0x000620a5... (70 %)

Writing at 0x00062baf... (71 %)

Writing at 0x00063622... (71 %)

Writing at 0x0006403b... (72 %)

Writing at 0x000649e3... (72 %)

Writing at 0x00065523... (73 %)

Writing at 0x0006606d... (73 %)

Writing at 0x00066af3... (74 %)

Writing at 0x000674b0... (74 %)

Writing at 0x00067f0f... (75 %)

Writing at 0x00068a04... (75 %)

Writing at 0x0006955e... (76 %)

Writing at 0x0006a067... (76 %)

Writing at 0x0006ab23... (77 %)

Writing at 0x0006b619... (77 %)

Writing at 0x0006bff8... (78 %)

Writing at 0x0006c7aa... (78 %)

Writing at 0x0006cf51... (79 %)

Writing at 0x0006d6db... (79 %)

Writing at 0x0006dee3... (80 %)

Writing at 0x0006e6e3... (80 %)

Writing at 0x0006eee2... (81 %)

Writing at 0x0006f6e1... (81 %)

Writing at 0x0006fee9... (82 %)

Writing at 0x000706e9... (82 %)

Writing at 0x00070f1d... (83 %)

Writing at 0x00071716... (83 %)

Writing at 0x00071f16... (84 %)

Writing at 0x00072716... (84 %)

Writing at 0x00072f16... (85 %)

Writing at 0x00073716... (85 %)

Writing at 0x00073f16... (86 %)

Writing at 0x00074716... (86 %)

Writing at 0x00074f16... (87 %)

Writing at 0x000756b8... (87 %)

Writing at 0x00075e77... (88 %)

Writing at 0x00076624... (88 %)

Writing at 0x00076dc7... (89 %)

Writing at 0x00077821... (89 %)

Writing at 0x00078c13... (90 %)

Writing at 0x00079d28... (90 %)

Writing at 0x0007a768... (91 %)

Writing at 0x0007b192... (91 %)

Writing at 0x0007bd26... (92 %)

Writing at 0x0007c8bb... (92 %)

Writing at 0x0007d378... (93 %)

Writing at 0x0007dded... (93 %)

Writing at 0x0007e7d3... (94 %)

Writing at 0x0007f21b... (94 %)

Writing at 0x0007fc8b... (95 %)

Writing at 0x0008067b... (95 %)

Writing at 0x00081101... (96 %)

Writing at 0x00081b23... (96 %)

Writing at 0x000825c9... (97 %)

Writing at 0x000830c9... (97 %)

Writing at 0x0008427d... (98 %)

Writing at 0x0008505e... (98 %)

Writing at 0x00085ffc... (99 %)

Writing at 0x00086e61... (100 %)

Wrote 555296 bytes (403726 compressed) at 0x00000000 in 21.1 seconds (effective 210.8 kbit/s)...
Hash of data verified.

Leaving...
Soft resetting...



### Shops
[Gaoneng](https://gaoneng.shop/) - RC specific LiPOs from manufacturer
[NKON](https://www.nkon.nl) - different rechargeable batteries




# Drone Configuration
[Betaflight Documentation](https://www.betaflight.com/docs/wiki)
[Betaflight App](https://app.betaflight.com)
[Betaflight GitHub Repo](https://github.com/betaflight/betaflight)
