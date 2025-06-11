## Added

<img align="right" width="275" src="../assets/1bded9fc-6aa1-4941-a86d-d324b82409e8">

### Spectrum-analyzer 

* Can also be started from **[Memory Channel mode](../40-Spectrum-analyzer#additions-extra-functionality)**.
* Screen differs in **channel mode** and in **frequency mode** 
* Displays _recognizes received memory channels_ op _top of screen_.
* Switch active Scanlist with `4` and is presented with letters _`SL I`, `SL II`, or `ALL`_ (left on screen, row 3)

> [!NOTE]
> When spectrum analyzer is active, you cannot communicate with Chirp.

### Adjustable VOX-delay to use for Digital communication
`VOX` is split up in 2 menu-items 

57. is renamed VOX menu setting to `VOXSen` (VOX sensitivity) to better indicate intent
10 value is max sensitivity, 1 is min sensitivity, OFF for off
1. new `VOXDel` (VOX delay) menu setting allows to set VOX delay in the range of 0-10 (in increments of 128ms)
0 value is no VOX delay which might be useful for packet radio enthusiasts (APRS etc.)

> [!NOTE]
> * The original VOX-delay was 1280
> * The new (default) value is 4 (x128= 4*128= 512ms)

### `RxOffs` added to use with **Upconverter** 

8. `RxOffs` - receiver frequency offset value. Used for external Upconverter.

   * TX is disabled when RX_OFFSET is set to protect the upconverter

<img align="right" width="255" src="../assets/55d021c0-c065-495d-80a6-65d591efafd4">

### Messenger

   `F+` `MENU`activates [Messenger](../42-Messenger)

### POWER ON PASSWORD
 See [Menu-item 48.`Passwd`](../20-Menu).

### Squelch Tail tone
* new `SqTone` sets the squelch tail tone used for RX/TX when no DCS/CTCSS is used to make radio compatible with more expensive radios
   * default value is `55Hz` - compatible with other Quansheng and Baofeng radios
   * the `CTCSS` scanner can be used to detect the tail tone other radios are using (it might take a while and take multiple transmissions as the tail transmission is very short)
      * once found set the `SqTone` to found value and enjoy no squelch sound 😄
* when CTCSS is used `180* phase shift` tail is enabled for RX/TX to be compatible with more expensive radios
* non-standard `55Hz` CTCSS code added

### Squelch is 20% more sensitive
Note: Squelch also protects the radio form freezing when strong signal is encountered, so if you run into freezes you didn't experience before likely you need to turn up your squelch ⬆️

<br>

## Modified 
### Power level LOW

Decrease of the LOW value

 Freq | L | M | H
 -- | -- | -- | --
 145 | 0,45 | 3 | 4,6
 430 | 0,3 | 3 | 3,4

Measured on a UVK5(8) with an SX-600 


### FM broadcast radio receiver - _minimum functionality_

* [completely rewritten](../50-FM-broadcast-radio-receiver) to be **Micro Size**

### BLMax 
RX-led turns on/Green in Spectrum only when BlMax > 7  to improve user _experience_ in _low light conditions_

<br>

## Removed 


###  FM broadcast radio receiver (_original version_)

With [release 18](https://github.com/kamilsss655/uv-k5-firmware-custom/releases/tag/v.18) the _**FM broadcast radio is inactive**_ due space limitations. 

The _free space_ will be used for other features. Perhabs in future the radio will return in stricted functionality.

More info on [FM-broadcast-radio-receiver](../50-FM-broadcast-radio-receiver) 

<br>

### UNBLOCK ALL (TX on all bands)
* This (Hidden-menu) option is completely removed, to make radio more _**safe by default**_

As an example against using this radio for actual communications, consider the following chart for transmission power for a transmission at 27.254MHz:

![Harmonics-in Spectrum](../assets/9db7936d-61d1-4c40-a81c-6b5d421fe6a1)

- 27.254MHz -> **228 microwatts**
- 54 Mhz -> 2.4 milliwatts
- 81 Mhz -> 230 milliwatts
- 109 Mhz -> 558 milliwatts
- 136 Mhz -> 412 milliwatts
- 163 Mhz -> 122 milliwatts
- 190 Mhz -> 14.8 milliwatts
- 218 Mhz -> 2 milliwatts
- And finally, on 245 Mhz -> 2.6 milliwatts.

CREDITS: https://github.com/Tunas1337/UV-K5-Modded-Firmwares#even-bigger-warning

### DTMF (menu 45- 54)

45. `ANI ID` - DTMF communication radio ID
1. `UPCode` - DTMF code that is sent at the beginning of transmission
1. `DWCode` - DTMF code that is sent at the end of a transmission
1. `PTT ID` - sets if `UPCode` and/or `DWCode` should be transmitted
1. `D ST` - DTMF side tone switch, lets you hear transmitted tones in the radio speaker
1. `D Resp` - DTMF decoding response 
   * DO NOTHING: do nothing
   * RING - Local ringing
   * REPLY - reply response
   * BOTH - local ringing + reply response
1. `D Hold` - DTMF auto reset time
1. `D Prel` - DTMF pre-load time
1. `D Decd` - enables DTMF decoder
1. `D List` - list of DTMF constacts

> [!NOTE]
>  * DTMF will _not be supported_ due to limited space.
>  * Send DTMF-tones from keyboard are supported.

