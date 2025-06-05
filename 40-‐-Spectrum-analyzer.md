## Additions: Extra functionality
<br>

<img align="right" width="300" src="https://github.com/kamilsss655/uv-k5-firmware-custom/assets/148579604/1bded9fc-6aa1-4941-a86d-d324b82409e8">

Some mods introduced by me on the spectrum functionality.

* _**Spectrum channel scan mode**_ enter by going into memory mode and press F+5, this allows _SUPER fast channel scanning_ (4.5x faster than regular scanning). 

   Regular scan of 200 memory channels takes roughly 18 seconds, spectrum memory scan takes roughly 4 seconds, if you have less channels stored i.e 50 - the spectrum memory scan will take only 1 second.

* Show **_channel number_ and _channel name_** of the peak frequency in spectrum

* _Pressing_ **`PTT`** exits the spectrum and fine tuning screen  and copy current peak frequency, modulation, step, bandwidth to VFO. Also entering spectrum will carry these settings from VFO (full integration). Now to enter fine tuning screen in spectrum press `MENU`. This allows you to save and respond to the frequencies found much faster.

* Green _RX LED_ turns `on` in spectrum only when `BlMax` > 7, to improve user experience in _low light conditions_

* _Squelch Tail tone Elimination_ works in spectrum (if matches settings in menu-`SqTone` )

<img width="300" src="https://github.com/kamilsss655/uv-k5-firmware-custom/assets/148579604/49b7cdb5-fdc0-4a27-b8f6-6816651a4238" align="right" >

* _Mode indicators_ ( _top-left_ of the screen and and _bottom center_ )
   * `N(0x)` - **normalization** function applied indicator
   * `ATT` - **attenuation** applied indicator
   * `BL` - **blacklist** applied indicator

   These functions
   * are available in all spectrum-modes (channel/frequency/scan range)
   * _**reset**_ when _switching in spectrum mode_

* _**Attenuate**_ function

   * sometimes there is a channel that has some interference, opening squelch randomly etc., before we had to either blacklist such channel or move the squelch threshold line higher, with this feature we can just attenuate particular channel
   * in order to use it press `FN2` when RX is on, it will apply attenuation to the currently listened channel. You'll see a `ATT` indicator at the bottom of the screen. 

> [!NOTE]
> * attenuate usage has been simplified so now it can be applied anytime to current peak bar
> * when a spectrum scan has more than 128x samples, the spectrum _attenuate_ function cannot be activated (to prevent errors)
<br> 

* **_Normalization_** _auto-adjusts_ screen, when activated. `N(0x)` on screen
<img width="625" src="https://github.com/kamilsss655/uv-k5-firmware-custom/assets/148579604/76f3cf46-8ff5-4754-884a-6abe2443c74a" hspace="30" >
<br> 

### Button functions
* In _Memory Channel mode_ press `F+5` to enter **SUPER FAST** _spectrum channel mode_
* In _VFO-mode_ long press `5` to enter _scan range mode_ (ScnRng on display)
* In _VFO-mode_ long press `5` then press `F+5` to enter _spectrum scan range mode_
* `2` toggles _spectrum channel mode **normalization function**_, that brings up all of the RSSI readings to the peak value. Resolves the 'valley problem' with channels hiding behind other channels of higher noise floor
  * _**To use it**_, wait until there are _no active TX peaks_ across the whole spectrum and press `2`
  * _**To turn it off**_ press `2` again or use the reset blacklist `UP/DOWN` buttons 
* `3` / `9` _**vertical scale**_; adjusts the scaling of the spectrums (y-axis) between -130 and 10 dB (default is 50 dB). The value is displayed in the top left part of the screen.
* `4` toggles **_scanlist_** SL I, SL 2, All. This can be actually useful to have different scanlists for different modulations, as spectrum channel scan uses single modulation for the whole scan.
* `6` toggles the _**bandwidth**_ between 5, 6.25, 8.33, 12.5 and 25 kHz
* `8` _**backlight**_ toggle
* `*` and `F` adjusts the **_squelch level_** which is represented by the dotted line.
* `FN1` will put the _current peak channel_ on the _**BlackList**_. You'll see a `BL` indicator at the bottom of the screen. 
* `FN2` will apply _**Attenuation**_ to the _current peak channel_. You'll see a `ATT` indicator at the bottom of the screen. 

<br>

## Spectrum Sweep screen
<br> 

Press `F`+ `5` to enter the _spectrum mode_ of the **Spectrum analyzer**. 

The current VFO/Memory frequency will be the _**start frequency**_ of the spectrum sweep

<img width="300" src="https://github.com/egzumer/uv-k5-firmware-custom/assets/148579604/80dfe424-f5d4-432b-9b95-32d116db9bd9" hspace="30" >
<br> 

* spectrum frequency **_change step is auto-adjusted_** to _half a spectrum bandwidth_
* Spectrum analyzer can also be used with [ScnRng mode](https://github.com/kamilsss655/uv-k5-firmware-custom/wiki/10-%E2%80%90-Radio-operation#scan-frequency-range-function-scnrng) 
> [!NOTE]
> * in this mode **Blacklist** is limited to **200** frequencies

###  Button functions
* `1` / `7` - increases/decreases _frequency step_ between consecutive bars
* `2` - _normalization function_ (don't press until _no active TX peaks_ in spectrum)
* `4` - 
  * From _VFO-mode_: toggles the number of bars (channels) in the graph. 
  * From _Memory-channel-mode_: toggles **_scanlist_** SL I, SL 2, All. 
* `5` - shows a _frequency input box_ for lower sweep frequency (value in **MHz**, `*` - decimal point)
* `3` / `9` _**vertical scale**_; adjusts the scaling of the spectrums (y-axis) between -130 and 10 dB (default is 50 dB). The value is displayed in the top left part of the screen.
* `6` - toggles receiver **_bandwidth_**
* `8` - toggle **_backlight_**
* `*` / `F` - increase/decreases _**squelch level**_
* `0` - toggles _**modulation type**_ (FM/AM/USB)
* `Side Button I` - _excludes _current frequency in the spectrum scan (add to _**blacklist**_). You'll see a `BL` indicator at the bottom of the screen.
* `Side Button II` - _Attenuation_ to the currently listened channel. You'll see a `ATT` indicator at the bottom of the screen. 
* `UP` and `DOWN` keys in spectrum channel mode now _**resets**_ _the exclude frequencylist_ (blacklist) and _normalization function_
* `Menu` to enter _fine tuning mode_ (see Detail Monitor Screen)
* `EXIT` - exits to the previous screen/function
* `PTT` - will copy current _modulation, step, frequency, bw_ and enter _**VFO mode**_

<br> 

## Detail Monitor screen

<img width="300" src="https://github.com/kamilsss655/uv-k5-firmware-custom/assets/148579604/4a274ea0-1808-471c-b5a8-225c5805627f" hspace="30" >

###  Button functions

<img width="400" align="right" src="https://github.com/kamilsss655/uv-k5-firmware-custom/assets/148579604/654df609-922a-4a3c-9f4d-2114ef03373a" hspace="30" >

`M` - scrolls through the parameters displayed at the bottom of the screen which can be adjusted with `UP/DOWN`

  * LNA$ - Low Noise Amplifier $hort
  * LNA - Low Noise Amplifier
  * PGA - Programmable Gain Amplifier
  * MIX - MIXER Gain

<br>

* `EXIT` - exits to the previous screen of the spectrum analyzer

<br> 

## Documentation
* Instruction for the Spectrum Analyzer (_initial version_) [QuanSheng.UV.K5.Spectrum.analyzer.guide.EN.pdf](https://github.com/kamilsss655/uv-k5-firmware-custom/files/13802044/QuanSheng.UV.K5.Spectrum.analyzer.guide.EN.pdf)
<br> 

## Note 
* When spectrum analyzer is _active_, you _cannot communicate with Chirp_

