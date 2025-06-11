## Basic operation & configuration
Radio display is split into upper VFO and lower VFO. You can change upper/lower selection by pressing `F` + `2 A/B` (or by long press `2 A/B`).

Explanation on switching VFO _Upper and Lower_ bij pressing `2 A/B` or selected RxMode (Menu 51).
  * The main channel is marked `►` and with PTT active `►TX`
  * A receiving channel is marked `RX` as soon as a signal is received. Other VFO/channel is blocked from RX.
  * With DUAL RX RESPOND, the secondary VFO/channel is marked `>` as temporarily the main channel when something is received there. 
  * If nothing is received after a timer of 4 seconds (`><` on screen), that status will expire.

Each VFO can operate independently of each other function in either frequency or channel mode. To switch modes select the desired VFO and press `F` + `3 VFO/MR` (or long press `3 VFO/MR`).

In the `frequency mode` you enter the frequency manually using the keypad. You can also switch different options for that VFO in the menu (first 13 menu entries). If you setup the VFO, the settings can be saved to a memory channel by going into the menu `ChSave` and choosing the memory channel the VFO should be saved into.

In the `channel mode` you can switch between saved memory channels. Memory channels can be added manually as mentioned before or with a computer software. You can use either Quansheng `Portable Radio CPS` or the recommended open source software called [`Chirp`](https://github.com/egzumer/uvk5-chirp-driver/releases/tag/v0.8.1) (_This link is to special version of EGZUMER-driver_). 

> [!WARNING]
> Do _**not use Quansheng CPS**_ it overwrites custom settings.
>
> Do _**not use the (original) Chirp**_ but the above mentioned _special version of EGZUMER-driver_

## Frequency/Memory scanning

### Frequency scanning

To start a frequency scan switch the VFO to frequency mode. Set the start frequency. Set the frequency step (menu `Step`). Start scanning with [custom button scan function](../30-Button-functions#custom-button-functions) or by long pressing `* Scan` button.

#### Scan frequency Range function (ScnRng)
* switch to frequency mode (_at least 1 VFO_) 
* set upper and lower VFO frequencies to scan range boundaries (_One must be VFO other can be memory channel_) 
* long-press `5`, `ScnRng` label should show up
* start scan with long-press `* Scan`
* it will scan between given boundaries
* long-press `EXIT` to _exit ScnRng mode_ 

  and 

* short-press `EXIT` or `PTT` _Halt scanning_  (to initial- or last received frequency) 

  than Continue scanning with `* Scan` or 

* long-press `5` or long-press `EXIT`, or long-press `2 A/B` to _exit ScnRng mode_

> [!NOTE] 
> `ScnRng` function is also supported by spectrum analyzer. If you activated the function just start [spectrum analyzer](../40-Spectrum-analyzer#spectrum-sweep-screen).

### Memory-channels scanning

To scan channels saved in the radio memory switch the VFO to Memory mode.

The radio has 2 scanning lists. Each memory-channel can belong to 0, 1 or 2 lists. To add/delete a channel to/from a list switch current VFO to desired channel and go to a menu `ScAdd1` or `ScAdd2`, alternatively you can long press `5 NOAA` button, you will see icons `I` and `II` toggling on and off on the right side of the channel label.

If you set up the scanning lists you can start scanning by using [custom button scan function](../30-Button-functions#custom-button-functions) 
or by long pressing `* Scan` button. If you press the function button or long press `* Scan` while scanning, the scanning list will be switched, you will see corresponding icon on the top left of the screen: 1, 2 or * (star means: All memory channels). Active scanning list can also be changed with menu `SList`. You can view scan lists and its channels by going to menu: `SList1` or `SList2`.

### Common frequency/channel scanning features

You can change the scan direction while scanning with `UP/DOWN` buttons.

The scan can be stopped with the `EXIT` button, the search result will be ignored and frequency/channel will return to the one that was set before scan begun. Alternatively you can stop the scan with `PTT` or `MENU` button in which case the frequency/channel will be set to the last channel where transmission was found.

## Single frequency scanning (frequency copy), DCS/CTCSS scanning

This function will allow you to find out and copy frequency and coding settings. The frequency search will only work for strong signals. The transmitting radio has to be close. To start a frequency copy (FC) function use `4 FC` function button. Scanner screen will open. Push and hold a PTT button on the other radio. Wait couple of seconds until frequency and code (if used) appears on the screen. The settings can be saved with the `MENU` button. The settings will be save either to a channel or the main VFO, depending in which mode you started the scan.

You can also search only the DCS/CTCSS code for a frequency set on the main VFO. Choose desired frequency or channel and press `F` + `* SCAN`. The same screen will appear, but the frequency search will be omitted, instead the frequency of the main VFO will be used. Wait for a signal to appear or press the PTT on the other radio. It takes 1-2sec for the code to be found. The save procedure is the same as above.

There is another option of DCS/CTCSS code scanning. Choose desired frequency or a channel. Go to the menu `RxDCS` or `RxCTCS`. Enter the menu option and press `* SCAN` button. A SCAN label will appear. Wait for a radio signal or press the PTT button on the other radio. When code is found the SCAN label will disappear, to save confirm the option with the `MENU` button. It doesn't matter on which of the two menu items you start the scan. Both DCS and CTCSS will always be found, and the menu entry will be changed to the correct one.

The CTCSS can be used to detect the `Tail tone` other radios are using. See [Tips & Tricks  Detect tail tone of other-radio](../80-Tips-&-Tricks-and-Known-Issues#detect-the-tail-tone-of-other-radio-with-ctcss-scanner)

> [!NOTE] 
> During scanning RX LED will turn on when signal level > 5
since we don't hear the audio during the scan, this lets us know that there is some channel activity

## 1750 Hz toneburst for repeater access

When the `PTT` is pressed, the 1750 Hz can be activated by pressing [`Function-button-II`](../30-Button-functions#function-button-ii) (_side key 2, bottom_)


## DTMF calling (decoding) is removed.

Removed DTMF (egzumer menu 45 - 54). 

DTMF **decoding will not be supported** due to limited space

Sending DTMF-tones from keyboard does work.