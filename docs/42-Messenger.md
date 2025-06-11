Thanks to great work of @joaquimorg, we now have the _**new Messenger Feature**_ 

`F+` `MENU`activates Messenger

**Keys**

<img align="right" width="400" src="../assets/55d021c0-c065-495d-80a6-65d591efafd4">

* `*` - Change keyboard, **U**pper case, **L**ower case, **N**umeric.
* `0` - Space, except in numeric mode.
* `F` - Backspace
* Long-press `F` - Clear all messages
* `UP` - Recalls last sent message
* `M` - Transmits message in the frequency of active VFO.
* `Exit` - Close application

<br>
<img align="right" width="400" src="../assets/6f64ded9-ddf7-468c-8b28-1902ffed2435">


> [!NOTE]
>* When the radio is on the correct frequency and a message is received, but messenger not active on screen, you get an `audio notification` and a `envelope`-sign is on the screen.
>* The receiving radio does a Confirmation - TX with Green-LED (not RED)
>* When that _**confirmation**_ is correctly received on the initual radio, an `+`-sign is printed at the _beginning of the message line._

<br>

<br>

<br>

<br>

# ✨ NEW Encryption ✨

* The messenger now uses _ChaCha20 256 bit encryption_. 
  * Allows sending and receiving encrypted messages between radio's with the same EncKey, or initially loaded via Settings with Chirp
  * The encryption key can be changed with menu item new 48.`EncKey`
  * Encryption can NOT be switched ON/OFF with menu item new 49.`MsgEnc`
  * This new Messenger is not completely backwards compatible with (receiving from) old version (< rel 20)
  * Make sure there is at least 1 meter distance between two devices

The encryption technique is explained in details in a [separate chapter Encryption](../44-Encryption)





