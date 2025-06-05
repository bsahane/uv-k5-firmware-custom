## **FM broadcast radio receiver (_limited functionality_)**

> With [release 19](https://github.com/kamilsss655/uv-k5-firmware-custom/releases/tag/v.19)

* it has been completely rewritten to be **Micro Size**
* all the tuning procedures are _now handled by the FM chip_ etc.
* it has been simplified so the only buttons needed to operate are `KEY_UP` and `KEY_DOWN` to tune channels
* frequency range and channel spacing have been restored to default USA/Europe settings which may result in improved reception in these regions
* `EXIT` ends the Radio

**known bugs**
  * dual watch is not working while the radio is on, only primary channel interrupts the radio (this was present in previous implementation as well)
  * sometimes radio skips valid frequency, this is due to the fact that now the FM radio chip determines whether the frequency is valid or not, this is not something that can be controlled in firmware now

> ** **More info will be added when time to do it** **;-)
>
> The description here below is _not actual and describes the old functionality_



##  Removed - The original functionality of Radio 

> With [release 18](https://github.com/kamilsss655/uv-k5-firmware-custom/releases/tag/v.18) the _**FM radio is inactive**_ due space limitations
>
> The _free space_ will be used for other features. 
>
> Perhabs in future the radio will return in stricted functionality.
>
> 
> ### BROADCAST FM (_functionality < release 18_)
> The radio is capable of receiving broadcast FM from 76 to 108 MHz. For this it uses a separate chip (BK1080). RDS is not supported.
> 
> _During broadcast reception the active VFO still has priority. This means that any reception on the active VFO will temporarily disable broadcast reception and the radio switches to VFO reception. At the end of VFO reception the radio switches back to broadcast after a five seconds. By pressing side-button-PTT you also temporary interrupt FM-reception._
> 
> ### BASIC OPERATION
> * `F` + `0 FM` or long press `0 FM` or [custom button function](https://github.com/kamilsss655/uv-k5-firmware-custom/wiki/30-%E2%80%90-Button-functions#custom-button-functions) starts broadcast reception
> * `Exit` or using above start command, when radio is in FM radio mode, ends broadcast reception
> * `F` + `VFO/MR` or long press `VFO/MR` changes between VFO or memory channels (VFO-/MR-mode)
> 
> #### Set a frequency in FM-VFO mode
> Simply typing a frequency sets it to receive. Resolution is 100 kHz so entering 929 would tune to 92.9 MHz. Use arrow keys to change in 100 kHz steps.
> 
> #### Store in memory from FM-VFO mode
> Pressing M in VFO mode allows to store the current frequency in a memory channel. Use arrow keys to select memory, confirm with `M` . There are 20 memories available.
> 
> #### Select a memory
> In MR-mode entering `01`.. `20` selects a memory channel. Use `UP/DOWN` to step a memory channel up or down.
> 
> #### Delete a stored memory
> In MR-mode pressing `M` allows to delete that memory channel.
> 
> ### SCANNING FOR STATIONS FROM FM-VFO
> #### Auto scan
> Start with `F` + `* Scan` or long press `* Scan` The radio scans for stations and stores the first 20 stations in memory. Scanning starts at the low side of the band. Initiating auto-scan will delete previously stored channels. `Exit` ends autoscan.
> 
> #### Manual scan
> Short press `* Scan` starts manual scan. The radio scans from the current frequency up until a station is received. You can continue scanning in any direction using arrow keys. `Exit` stops scanmode.