> [!NOTE] 
> 
> Press the programming cable _firmly_ into the radio
>
> This is an example where this is NOT the case

<img width="350" src="https://github.com/kamilsss655/uv-k5-firmware-custom/assets/148579604/8a9d88b5-75e6-4f42-a41f-21702383c981" hspace="40" >


## Make an eeprom-backup (once)

Just to be sure.

> [!IMPORTANT]
> ### First: Did you make two backups from the EEPROM ?

Make this backup (once) of your radio, with [k5prog-win](https://github.com/OneOfEleven/k5prog-win) in two steps.

1. Read Configuration. And save the file.
1. Read Calibration. And save the file.

![Use K5prog-win to make backup](https://github.com/kamilsss655/uv-k5-firmware-custom/assets/148579604/aa0f4ca6-7fb8-4ab7-ab6a-869582e2c283)

### Second: Use Chirp ([EGZUMER version](https://github.com/egzumer/uvk5-chirp-driver)) and make backup of the(original) channellist

<br> 

**Step 1 and 2 ready ?** _Now you can continue ...._

<br> 

## Flash the latest firmware release

Flashing firmware is possible with a separate program, but can now be done much more easily from your web browser (Only Chromium based browsers such as Chrome, Edge, Opera).

Just goto the page with official released [firmware releases](https://github.com/kamilsss655/uv-k5-firmware-custom/releases).

* Use a Baofeng/Kenwood-like USB-2-Serial-cable and connect it to your computer.

* Switch off UV-K5

* Put the UV-K5 into programming mode (press and hold the `PTT` button and _turn on_ the UV-K5, check that the _white flashlight_ lights up).

* Then press the programming cable _firmly_ into the radio

* Select the latest/desired firmware and look for `🗲FLASH WITH A BROWSER🗲` and the build-in _UV-mod-programming-page_ start. Just wait a moment and the firmware is loaded, or select a different file from your PC.

  ![Flash firmware with browser -V0 12](https://github.com/kamilsss655/uv-k5-firmware-custom/assets/148579604/15e9051e-6638-4474-af8c-d4d9cc445b40)

* Press flash firmware and a screen pops-up.
* Select the Com-port where the programming-interface is connected.

  <img width="350" src="https://github.com/kamilsss655/uv-k5-firmware-custom/assets/148579604/f75a316b-431c-4883-9fcd-ffcc6a58f0c1">
<br> 

* Press Connect and the firmware programming starts (White LED starts flashing) and view the progress in the browser-screen
* Just wait ... until

  ![Flashing 100 procent](https://github.com/kamilsss655/uv-k5-firmware-custom/assets/148579604/b737c7a3-1a2c-4a50-a4e1-36e717eae5ba)

* When finished, disconnect the programming interface and enjoy a new release version ;-)
