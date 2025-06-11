<img align="right" width="355" src="../assets/c6ad673c-c051-4876-a961-fec5c5c47333">

Buttons have functions assigned to them, these functions can be activated by either pressing `F/#` button first, then the function button (I will call it `F+` call). Other method is by long pressing the function button alone without `F/#`. Most buttons replicate the `F+` with long press, but some buttons might have assigned different functions for `F+` and long press (for example button 5, * and Exit).

## Front keypad

### `M` 
* short press - enter menu
* short press while channel/frequency scanning - last found channel is preserved on the screen
* long press - user programmable in the menu: `M Long`
* `F+` - activates [Messenger](../42-Messenger)
### `EXIT`
* short press - exits current menu/function, deletes one digit in an input box
* long press - deletes all input, exits DTMF input box
### `UP/DOWN`
* Move Upward/Downward in Menu, Frequency, Settings, etc.
### `1 BAND`
* `F+`
  * in **frequency mode** - switches frequency bands 1-7, there is also band 7+ for >1GHz frequencies
  * in **channel mode** - channel settings are copied to frequency mode
* long press - same
### `2 A/B`
* `F+` - switch main channel/vfo upper/lower (marked by `►`)
* long press - same
### `3 VFO/MR`
* `F+` - switch between frequency and channel modes
* long press - same
### `4 FC`
* `F+` - turns on frequency and CTCSS copy mode, turn the scan on and start transmitting with the other radio, the frequency and CTCSS code will be detected, you can save those setting with `M` button
* long press - same
### `5 NOAA`
* `F+` - turns on spectrum analyzer
  * in **channel mode** - activates Spectrum-analyzer of the channels
  * in **frequency mode** - activates Spectrum-analyzer, _starting_ with frequency of the VFO
* long press
  * in **channel mode** - toggles scan lists that the selected channel is assigned to. You will see `I` and `II` symbols changing on the right side of the channel label
  * in **frequency mode** - activates [frequency scan range feature](../10-Radio-operation#frequencymemory-scanning)
### `6 H/M/L`
* `F+` - toggles power levels for current channel
* long press - same
### `7 VOX`
* `F+` - turns on/off VOX mode
* long press - same
### `8 R`
* `F+` - turns on reverse mode for channel that have frequency offset set. It will replace TX frequency with RX frequency.
* long press - same
### `9 Call`
* `F+` - switches current channel to the `1-Call` channel set in the radio.
* long press - same
### `0 FM`
* `F+` - turns on FM radio
* long press - same

### `* SCAN`
* short press - enters DTMF input mode
* `F+` - turns on CTCSS scanner for current frequency
* long press
  * in channel mode turns on channel scanner
  * in frequency mode turns on frequency scanner (can use [scan range feature](../10-Radio-operation#scan-frequency-range-function-scnrng))
* When pressed while channel scan is in progress toggles scan lists 1/2/ALL

### `F # 🗝`
* short press - toggles function option
* long press - turns on/off key lock all the keys of the Front keypad

## Side buttons
<img align="right" width="255" src="../assets/64dabc4f-6015-411c-b8d1-f752b91b39ee">

### `PTT` 
* Push To Talk button.
* when this button is used to stop channel/frequency scanning, last found channel is preserved on the screen
* held together with `Function button II` transmits _tone 1750Hz_
* held together with any of the front keypad buttons transmits DTMF codes

### `Function button I` 
* short press - user programmable in the menu: `F1Shrt`
* long press - user programmable in the menu: `F1Long`

### `Function button II` 
* short press - user programmable in the menu: `F2Shrt`
* long press - user programmable in the menu: `F2Long`
* this button can also be used to send _tone 1750Hz_ when `PTT` is pressed.

## External key/microphone
### `PTT` 
* Push To Talk button.
* The 'PTT on the external microphone' works differently than the 'internal PTT' (side) button.
> * - When pressing the PTT, the TX waits until no RX signal is received (observed with Internal PCB revision V1.4 and OK with V1.6). Works well when pressing the 'internal PTT'.
> * - A DTMF-tone (key-press) or _1750Hz-tone_ (function button) is cut off within a second. Works well when pressing the 'internal PTT'.

## Custom button functions
3 buttons can have its function changed. To change the function go to menu:
* `F1Shrt` - side button 1, short press
* `F1Long` - side button 2, long press
* `F2Shrt` - side button 1, short press
* `F2Long` - side button 2, long press
* `M Long` - menu button, long press

Available functions:
* NONE - no action
* FLASH LIGHT - switch to the next flashlight function: on / flash / SOS / off
* POWER - switch radio output power: L (low) / M (medium) / H (high)
* MONITOR - switch monitor mode on/off
* SCAN - start channels/frequency scanning
* VOX - turn voice activation function on/off
* FM RADIO - turn FM radio on/off
* LOCK KEYPAD - lock/unlock the keypad
* SWITCH VFO - change main VFO to upper/lower
* VFO/MR - change current VFO mode, frequency mode or channel mode
* SWITCH DEMODUL - switch to the next demodulation mode (FM/AM/USB)
* SWITCH BANDWIDTH - switches current bandwidth
* SPECTRUM - runs [spectrum analyzer](../40-Spectrum-analyzer) in channel- or frequency mode
