# Back up your Steam Deck's BIOS/UEFI/SPI

The UEFI (also known as BIOS) in a computer allows the machine to boot and controls a large number of fundamental hardware settings, like how fast the CPU should run or how much voltage should be applied.

Most computers, alongside the UEFI chip, have a separate configuration chip that stores the current UEFI configuration.
That separate configuration chip can be erased, usually by removing the BIOS battery or by pressing a button on the motherboard.
After that, the default UEFI configuration is restored.

This is important when you start tinkering with things that may cause the hardware to stop booting, such as overclocking or undervolting.
On most machines, should you stop it from booting (a.k.a. "brick") the machine, you can simply remove the battery or press the configuration reset button and you'll usually be back in a safe place.
Unfortunately, Steam Deck is not most machines.

Steam Deck uses an all-in-one SPI chip for the UEFI, configuration, hardware IDs and more.
While you can't do this normally, if you were to somehow erase the whole chip, the Steam Deck would no longer boot as it would be missing its UEFI!

The upshop is that there's no fool-proof way to reset a Steam Deck back to its default settings if it can't boot.
So if you can no longer boot the Steam Deck, it might be bricked.
The only way out (aside from a possible warranty replacement) is to reflash the SPI chip as a whole, which requires an SPI backup.
**So having an SPI backup is very important!**

## Backing up the SPI

**Note: The SPI contains unique hardware IDs for your Steam Deck. Don't upload the backup to anywhere others can access it unless you trust everyone that could possibly download it.**

If you ever brick the Deck and need this file, you will need to use another machine (e.g. a desktop or laptop) to reprogram the SPI chip on the Steam Deck.
So keep in mind the end goal: this backup needs to be kept somewhere separate from the Steam Deck.

1. First, ensure the Steam Deck is in stable condition.
    For example, boot in to the UEFI and reset to defaults.

2. Once the Steam Deck is in stable condition, boot in to Desktop Mode and run the following in a terminal (such as Konsole):

    ```shell
    sudo /usr/share/jupiter_bios_updater/h2offt /home/deck/biosbkp.fd -O
    ```

3. Back up this file somewhere secure where you could use it on a recovery machine in future.
    _Do not keep it **only** on the Steam Deck!_
