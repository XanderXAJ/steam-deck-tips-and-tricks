# Emulating games on Steam Deck

Since Steam Deck is a Linux machine at heart, it's possible to install a lot of off-the-shelf software, including emulators.

Broadly speaking, you can either install and configure each emulator manually, or use one of several tools that can automatically install and configure emulators for you.

## Emulator Installers

There are multiple options out there; I have experience with EmuDeck:

- [EmuDeck](https://www.emudeck.com/)
- [RetroDeck](https://retrodeck.net/)

This guide does not aim to provide a detailed review of the different installers available -- other sources can provide that information.
This guide instead will highlight a few of the things that I care about:

- Ease of use
- Configuration management (can you take control?)
- How easy it is to restore settings if you reset your Deck or get a new one
- Updates & maintenance

### EmuDeck Advantages vs. Manual Installation

- It's very straightforward to install and configure a multitude of emulators. Some configuration can be customised during the installation process.
- It's easy to update the emulators too -- either via the Discovery app, when running the emulator, or re-running EmuDeck, depending on how the emulator is packaged.
- Makes it easy to list games or emulators in the Steam interface using [Steam ROM Manager](https://steamgriddb.github.io/steam-rom-manager/).
- Adds extra features like cloud saves, synchronisation, etc.
- If you find an issue or want to extend something, the EmuDeck community are active working with you to finding and applying solutions [example](https://github.com/dragoonDorise/EmuDeck/pull/465).

### EmuDeck Disadvantages vs. Manual Installation

- EmuDeck works best when it manages everything. Its configuration is opinionated. If you want to make changes to the configuration, you might face an uphill battle in makiing changes to it -- and it might get reset whenever an update occurs.
    - This depends from emulator to emulator and how it stores its configuration. For example, without taking over all configuration yourself, it's reasonably simple to retain your customisations on RetroArch platforms [using content directory and game configuration overrides](https://docs.libretro.com/guides/overrides/).

## Mixing and matching automatic and manual installation

To begin with, start with one of the above installers and see how they feel -- you'll likely be happy.
However, if you feel like you need more control, it's possible to mix and match an emulator installer with manual configuration.
