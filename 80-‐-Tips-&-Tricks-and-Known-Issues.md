# What if Spectrum Scan Freezes

This is caused by a strong signal. The only way to fix this is to lower your gain settings in spectrum (_while antenna is disconnected_).

   * _Disconnect the antenna_ and check if the freezing will stop.
   * Press `M` twice
   * Then reduce the LNA$ and/or LNA parameter.
   * _Connect the antenna_ again and see if the value can be slightly higher.

# What if AM reception is distorted/overloaded

   * lower the gain in spectrum. Just like with Spectrum scan freeze?

# Detect the tail tone of other radio with `CTCSS` scanner
   * the `CTCSS` scanner can be used to detect the tail tone other radios are using (it might take a while and take multiple transmissions as the tail transmission is very short)
      * once found set the `SqTone` to found value and enjoy no squelch sound 😄
* `SqTone` sets the squelch tail tone used for RX/TX when no DCS/CTCSS is used to make radio compatible with more expensive radios
   * default value is `55Hz` - compatible with other Quansheng and Baofeng radios
* when CTCSS is used `180* phase shift` tail is enabled for RX/TX to be compatible with more expensive radios

> [!NOTE]
> _Tail tones below 65Hz are not reliably detected by the CTCSS scanner - likely by the design of the chip and to be fair these are not standard CTCSS tones. they work perfectly when used as SqTone or TxCTCSS/RxCTCSS though_
>

# Menu - Recommended settings 

Numbering of menu-items is based on _release 20.5_

   * 1 `Step` - step of the frequency. Set this to **12.50** kHz
   * 2 `Bandw`- bandwidth. Set this to **12.50** kHz
   * 14 `Demodu` - demodulator mode. Put it on **FM**
   * 22 `F1Shrt` - side button 1 short press function. Put it on **MONITOR**
   * 23 `F1Long` - side button 1 long press function. Put it on **LONG SPECTRUM**
   * 24 `F2Shrt` - side button 2 short press function. Put it on **SPECTRUM**
   * 25 `F2Long` - side button 2 long press function. Put it on **SPECTRUM**
   * 26 `M Long` - menu button long press function. Put it on **SWITCH VFO**
   * 30 `Mic` - microphone sensitivity. Set it **+15.1**dB
   * 31 `CHDISP` - Channel display style (name + frequency or number). Set this to Name + Freq
   * 32 `POmMsg` - power on message. Set this to **Message**
   * 33 `BatTxt` - Additional battery value. Set this to **Voltage**
   * 34 `BackkLt` - Backlight duration. Set this to **2 minutes**
   * 46 `RXMode` - Set it to **Main TX Dual RX** - always transmits on the primary channel (marked ►), listens to both.

**And as an option in the [hidden menu](https://github.com/kamilsss655/uv-k5-firmware-custom/wiki/20-%E2%80%90-Menu#hidden-menu)**

   * 60 `BATCAL` - Battery calibration. Measure the battery voltage with a voltmeter (on the metal loops on the back of the radio) and adjust the value in the menu accordingly.

                For my radios this value was 1889 to 1950 and 1896 -> 2021.

   * 61 `Battyp` - battery type. The UVK5 (8) is 1600 mAh and the UV5R-Plus often 2200 mAh.

<br>

# Suggest to use an external antenna

## Use an SMA-female to BNC-female connector/adapter

<img width="300" src="https://github.com/nicsure/QuanshengDock/assets/148579604/8a73976a-241d-4355-9037-a92f157fc32b" hspace="40" >

* so you can easily connect the external antenna cable to the radio

<br>

* extra option is to extend that to PL256 with is adapter

<img width="300" src="https://github.com/nicsure/QuanshengDock/assets/148579604/6af4e626-8f83-48a7-82e3-5b30c2bfc3d3" hspace="40" >

## Converter cable
An other suggestion is this converter cable

<img width="300" src="https://github.com/nicsure/QuanshengDock/assets/148579604/4d7ea84c-5786-4493-9816-7d5b8248bd87" hspace="40" >

<br>

# Chirp incompatibility
> [!NOTE]
>This project does NOT work with actual version CHIRP 
>
>There is a [cause](https://github.com/egzumer/uvk5-chirp-driver/releases/tag/v1.0) and reason for the Chirp-mismatch
>
> **But that's not up to this project**

There are 2 workarounds
* Temporarily use different firmware on your radio that matches the Chirp and adjust your channels
* [Use an earlier version of Chirp PY driver in Developer mode](https://github.com/egzumer/uvk5-chirp-driver/releases/tag/v0.8.1)


