<img align="right" width="200" src="../assets/c6ad673c-c051-4876-a961-fec5c5c47333">

## Menu operation

The menu can be accessed with the `M` button (_short press_).

Once in the main menu, the menu items will be displayed on the left-hand side of the screen. The currently selected menu item will be highlighted and current value for that menu item will be shown on the right. Also, at the bottom left side a number of the menu item will be shown, ranging from 01 to the highest number.

To find the menu item to access, the `UP/DOWN` arrow keys may be used, or the _**menu item number**_ (see lists below) may be entered on the numeric keypad. For instance, to access the `Demodu` - **demodulator mode**  a number 14 can be entered on the keypad.

Once the desired menu item is highlighted, pressing the `M`enu key will enter into that menu item.

Once the menu item is selected, pressing the up and down arrow keys will adjust the setting for that menu item. To confirm the selection, press the `M`enu key. To cancel the selection, press the `EXIT` key.

## Main menu

The number in front of the menu-item-description is an **_menu item number_** that can be used for quick selection.
1. `Step` - step of the frequency (in kHz), up/down buttons change frequency by this value, also you can only set a frequency that is multiple of this value. 2.50/5/6.25/10.00/12.50/25.00/8.33 are the steps that can be set by programming software, all other steps are extension from standard software, and can only be selected from this menu entry.
1. `Bandw` - bandwidth used by transceiver and displayed in format ie. 12.5k (instead of N/W)
1. `TxPwr` - radio output power (LOW/MID/HIGH)
1. `RxDCS` - receiver Digital-Coded Squelch, if you enable this, squelch will only unlock if this code is being received. You can start a DCS/CTCSS scan while you are in this menu option by pressing `* SCAN` button
1. `RxCTCS` - receiver Continuous Tone-Coded Squelch System, squelch will only unlock if this code is being received. You can start a DCS/CTCSS scan while you are in this menu option by pressing `* SCAN` button
1. `TxDCS` - transmitter Digital-Coded Squelch, radio will send given code while transmitting
1. `TxCTCS` - transmitter Continuous Tone-Coded Squelch System, radio will send given code while transmitting
1. `TxODir` - transmitter frequency offset direction
1. `TxOffs` - transmitter frequency offset value
1. `RxOffs` - offsets the receive frequency by any specified amount for use with upconverters (in the range of 0-150Mhz). Allows to fine tune the frequency (1kHz resolution) as opposed to other implementations that use hardcoded offsets, this once set will also allow to tune below 18Mhz limit. 
   * You can fine tune this setting in even smaller steps by changing `Step` setting to `0.01kHz` and then use `UP/DOWN` buttons to alter `RxOffs` in increments of `0.01kHz`.
   * TX is disabled when RX_OFFSET is set to protect the upconverter
   * **IMPORTANT**: Make sure you set this value to 0 if not using an upconverter, when used for the first time. Otherwise it might load some random offset from EEPROM.
1. `Scramb` - scrambler, distorts the audio so that it is unintelligible to other listeners. If radios use the same setting, they can communicate clearly.
1. `BusyCL` - busy channel lockout, blocks radio from transmitting because signal is being received (with **BUSY** on screen while PTT is pressed)
1. `Compnd` - compander (compressor/expander), allows signals with a large dynamic range to be transmitted over facilities that have a smaller dynamic range capability, improves audio quality, both radios should use this option
1. `Demodu` - demodulator mode, default is FM, AM/USB can be used for listening only
1. `RxAGC`- setting to configure built in AGC which applies to all the modulations. The SLOW and FAST settings might protect radio from freezes caused by reception of strong signals.
   * OFF - completely disables AGC, this might be useful for receiving the most faint signals, with maximum set gain the AGC will not clamp down signal, note: this might cause radio freeze if the received signal is too strong and overloads the radio
   * SLOW - provides wide dynamic range, works really well overall and is the default setting, might be especially useful for HF AM broadcast stations that broadcast music etc.
   * FAST - lower dynamic range, might be useful for short voice communication, aviation, where understanding every word is crucial etc.
1. `ScAdd1` - add channel to scan list 1
1. `ScAdd2` - add channel to scan list 2
1. `ChSave` - save current setting to a current memory channel. 
1. `ChDele` - delete memory channel
1. `ChName` - modify memory channel name
1. `ScnRev` - scan resume mode
   * CARRIER - resume scan after signal disappears
   * TIMEOUT - resume scan after 5 seconds pause
   * STOP - after receiving a signal, stop the scan
1. `F1Shrt` - side button 1 short press function
1. `F1Long` - side button 1 long press function
1. `F2Shrt` - side button 2 short press function
1. `F2Long` - side button 2 long press function
1. `M Long` - menu button long press function
1. `KeyLck` - auto keypad lock option
1. `TxTOut` - max transmission time limit
1. `BatSav` - battery save option, the rate between active time and sleep time (OFF/50%/67%/75%/80%)
1. `Mic` - microphone sensitivity (+1.1dB .. +15.1dB)
1. `ChDisp` - channel display style (Name + Freq or Number)
1. `POnMsg` - power on message
1. `BatTxt` - additional battery value on the status bar in % or V(oltage)
1. `BackLt` - backlight duration  (OFF/ON/configured Time)
1. `BLMin` - minimal backlight brightness, when the screen backlight turns OFF it will go dim to this value
1. `BLMax` - maximal backlight brightness, when the screen backlight turns ON it will turn bright to this value. (In Spectrum RX-led stays of on RX when BLMax < 8)
1. `BltTRX` - backlight activation on TX or RX
1. `Beep` - keypad press beep sound
1. `Roger` - roger beep at the end of transmission (OFF/ROGER/MDC1200)
1. `SqTone` - squelch tail tone used for RX/TX when no DCS/CTCSS is used (default is 55Hz)
1. `1 Call` - one key call channel, lets you quickly switch to the channel with `9 Call` button
1. `D Live` - displays DTMF codes received by radio in the middle of the screen
1. `VOXSen` - sets the VOX sensitivity - voice TX-activation sensitivity level (OFF/1 .. 10, 1-min sensitivity, 10-max sensitivity)
1. `VOXDel` - sets the VOX delay, 0 setting can be useful for the packet radio, APRS, etc. (range of 0-10, each step increments delay by 128ms, 4 is the default setting)
1. `BatVol` - battery voltage and percentage
1. `RxMode` - sets how how the upper and lower frequency is used
   * MAIN ONLY - always transmits and listens on the main frequency (NO extra characters on screen)
   * DUAL RX RESPOND - listens to both frequencies, if signal is received on the secondary frequency it locks to it for a couple of seconds so you can respond to the call (**`DWR`** on screen)
   * CROSS BAND - always transmits on the MAIN/primary and listens on the secondary frequency (**`XB`** on screen)
   * MAIN TX DUAL RX - always transmits on the primary, listens to both (**`DW`** on screen)
1. `Passwd`- allows to set POWER ON PASSWORD from the menu
   * enter PIN with digits on the keyboard and press `MENU` to confirm
   * to disable the `Passwd` setting use `KEY_UP` or `KEY_DOWN` and press `MENU` to confirm
   * after **3 wrong PIN entries** the device will perform _**a factory reset**_, erasing all the stored channels and settings
1. `EncKey` - presents hashed value of _encryption key_. By pressing `M` a new 10 characters password can be entered.
1. `MsgEnc` - determines whether outgoing _messages will be encrypted_
1. `MsgRx` - determines whether fsk modem will _listen for new messages_
1. `MsgAck` - determines whether the radio will _automatically respond_ to messages with ACK
1. `MsgMod` - messenger _modulation_
   * FSK 450 - for bad conditions
   * FSK 700 - for medium conditions
   * AFSK 1.2K - for good conditions
1. `Sql` - squelch sensitivity level (0=OFF/1 .. 9)

## Hidden menu

Hidden menu is activated by holding `PTT` + `SIDE BUTTON 1` while turning on the radio and than Release All Keys.

54. `F Lock` - sets the TX frequency band plan. 
    * DEFAULT+ (137-174, 400-470) - allows TX on default bands, plus options `Tx 200`, `Tx 350`, `Tx 500`
    * FCC HAM (144-148, 420-450)
    * CE HAM (144-146, 430-440)
    * GB HAM (144-148, 430-440)
    * (137-174, 400-430)
    * (137-174, 400-438)
    * DISABLE ALL - disables TX on all frequencies
1. `Tx 200` - enables TX on 200MHz
1. `Tx 350` - enables TX on 350MHz
1. `Tx 500` - enables TX on 500MHz
1. `350 En` - enables RX on 350MHz
1. `ScraEn` - enables scrambler function
1. `BatCal` - battery calibration, measure the voltage on the back of the radio, and adjust the value in the menu accordingly
1. `BatTyp` - battery type, 1600mAh and 2200mAh battery has very different discharge curve, this is used to calculate battery level percentage
1. `Reset` - resets radio configuration settings
   * VFO - removes only channel settings
   * ALL - resets all radio settings

