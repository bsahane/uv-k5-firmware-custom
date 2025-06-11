> [!NOTE] 
>Kamilsss655 has improved on the Spectrum Analyzer with: Faster scan, Memory scan, Vfo scan, blacklist, signal attenuator and best of all “spectrum copy to vfo”. You tune the freq in the analyzer and the copy it into the vfo intact do that you can use it or save it to a channel.
>
> _**Now a special Encrypted Messenger and this feature is expanding.**_

<img align="right" width="350" src="../assets/944e3ea9-6c67-40f6-a599-c28af8c5c525">

<br> 

<br>

**Sponsors** have access to _early release_ whose changes are detailed here in this chapter

So you as a user can determine if the added things are worth subscribing also here ... [How2Sponser](#sponsor-this-project)

<br> 

* The most important different items are included here as
   * [Mesh network](../43-Mesh-network)
   * 20 ‐ Menu
   * 30 ‐ Button functions

* Features with release **v.21.1** 
   - `MsgID` menu option
   - 20 messages stored in 10 pages
   - User interface changes to messenger
   - Reverted squelch on delay (caused random squelch opening)
   - Fix: `Passwd` factory reset didn't wipe `EncKey`
   - VOX disabled by default (removed: 43 VOXSen and 44 VOXDelay)
   - Long-Press-7 `VOX` now gives _**ScanRng**_ (and not F-NOAA)

<br> 

# Baudrate increased
> [!IMPORTANT]
> To support the [ESPRi project](https://github.com/kamilsss655/ESPRI/wiki) with release version 21.4, the **baudrate** within the NUNU-firmware is changed from 38400 to **115200**. 
>
> Therefore you cannot use default CPS or Chirp. 
> To be able to communicate to UVK5 with NUNU-firmware the already dedicated Chirp.py-driver is changed to a _special version_ with 'BAUD_RATE = 115200'. 
> 
> Select the file [uvk5_egzumer_115200_baud.py](https://github.com/kamilsss655/uvk5-chirp-driver/blob/main/uvk5_egzumer_115200_baud.py) as argument, which is not mentioned in the READ.ME. 
> See [READ.ME](https://github.com/kamilsss655/uvk5-chirp-driver/tree/main?tab=readme-ov-file#how-to-use) and be aware to CHANGE THE ARGUMENT TO THE FILE **uvk5_egzumer_115200_baud.py**.
>
> P.s. The increased baudrate has no impact on flashing the radio.

<br> 

* Features with release **v.21.4**
  * NUNU messenger can be interfaced by [ESPRi project](https://github.com/kamilsss655/ESPRI/wiki)
    * received messages show up in web UI notifications.
    * sending messages can be done via API (no front-end atm): `curl -d '{"content":"test message"}' http://192.168.4.1/api/uvk5_message`.

> These 2 lines in section **42** - # ✨ NEW Encryption ✨
>
> * These  items are renumbered
>   * The encryption key can be changed with menu item new 46 `EncKey`.
>   * Encryption can NOT be switched ON/OFF with menu item new 47 `MsgEnc`.

<br> 

* Features with release **v.21.5**
  * Fixed [BUG] Passwd wrong password entry not being reset ([Issue 212](https://github.com/kamilsss655/uv-k5-firmware-custom/issues/212)).
  * Other minor stability improvements.

<br> 

* Features with release **v.21.6**
  * Improved lock feature ([issue 216](https://github.com/kamilsss655/uv-k5-firmware-custom/issues/216)).
  * Fixed AUTO lock feature (Menu item 27. `KeyLck` - auto keypad lock option).
  * Fixed auto lock issue in FM radio and messenger ([issue 73](https://github.com/kamilsss655/uv-k5-firmware-custom/issues/73)).
    * Additionally user can now press and hold F/keylock button while in messenger and FM radio mode to toggle the lock function in these applications :)
  * "Roger" type roger volume has been greatly reduced.

<br> 

* Features with release **v.21.7**
  * Dynamic unique roger tones based on MsgID 

   Now Roger (menu 39) option has:
    * OFF - roger off
    * CLASSIC - static roger tone - doesn't change along with MsgID.
    * MSG ID - dynamically generated unique roger tone based on Msg ID (menu 50) option setting, this essentially gives 255 unique roger tones.
