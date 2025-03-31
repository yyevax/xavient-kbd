# XAVIENT Keyboard

<div align="center">
    <img alt="xavient image" width="100%" src="./docs/img/xavient.jpg">
    <h3>An Expensive but Amazing Journey</h3>
    <p><i>still work in progress</i></p>
</div>



This keyboard build followed some inspirations on various open-sourced keyboards listed below:

- [Corne](https://github.com/foostan/crkbd): basing the footprint of the controller here since this is the most common keyboard.
- [Swoop](https://github.com/jimmerricks/swoop): used as my first keyboard when I was exploring the world of split-keyboards
- [Flake](https://github.com/anywhy-io/flake): got some inspiration on how to implement jst battery connections.
- Sweet-Corne: My first attempt at building a keyboard from scratch. (Lost Files)


The placement of the keys for this keyboard are loosely based on both the Corne and Swoop Keyboards. 

<img alt="keyboard layouts" width="100%" src="./docs/img/layout.png">

# The Goal
When I started using the Swoop Keyboard, I immediately knew that I wanted to go for a low profile version. This led me to create my first custom design based on the Swoop Keyboard by altering the pinky column stagger and adding underglow RGB. 



both are using 3 rows and 5 columns of keys with 3 thumb keys on each side.

This keymap is mainly based on the [Miryoku](https://github.com/manna-harbour/miryoku) Keyboard Layout using ZMK with some inspiration from other keymaps found on [KeymapDB](https://keymapdb.com/).

Miryoku was the first layout I used when I built my wireless keyboard and had been accustomed to how it works.
You can find my Miryoku ZMK Config [here](https://github.com/duanexavierbondad/miryoku_zmk_xavien).

This firmware uses 12 layers in total, 2 of which are dedicated to a Gaming Layer. It also utilizes home row mods and combos for easy access to symbols on the base/default layer. This layout utilizes the left hand side of the keyboard more that the right side to be able to maximize the use of shortcuts event when using the mouse.

The default alpha layer is using Colemak-DH which also contains combo keys for symbols.
The other layers are the following:

- NUM Layer for the dedicated numbers and operators.
- NAV Layer for the arrow keys and mouse emulation.
- SYM Layer for the various symbols in the keyboard.
- FUN Layer for the Function Keys
- MED Layer for the Media Control Key
- SCN Layer for the SCREEN Controls
- Gaming Layer dedicated for Valorant with Two Layers, VAL and VALTWO layers.
- EXTRA Layer for the QWERTY Layout.
- TAP Layer for a Colemak-DH Layout without combos and homerow mods.
- SYS Layer for dedicated settings for the keyboard.

`SYS` layer is implemented as a tri-layer, i.e. it is active when both `SCREEN` and `FUN` are active.

OS-dependent shortcuts are present on the `SCN` layer, e.g. for Windows:

- `Win Close`: `<kbd>`Alt`</kbd><kbd>`F4`</kbdy>`
- `Tab Close`: `<kbd>`Ctrl`</kbd><kbd>`F4`</kbd>`
- `Win Close`: `<kbd>`Ctrl`</kbd><kbd>`Gui`</kbd><kbd>`F4`</kbd>`
  The close shortcuts uses combo keys to prevent accidental keypresses.
- `Tab Next`: `<kbd>`Ctrl`</kbd><kbd>`Tab`</kbd>`
- `Tab Prev`: `<kbd>`Ctrl`</kbd><kbd>`Shift`</kbd><kbd>`Tab`</kbd>`
- `Desk Next`: `<kbd>`Ctrl`</kbd><kbd>`Gui`</kbd><kbd>`Right`</kbd>`
- `Desk Prev`: `<kbd>`Ctrl`</kbd><kbd>`Gui`</kbd><kbd>`Left`</kbd>`
- `Win Next`: `<kbd>`Alt`</kbd><kbd>`Tab`</kbd>` (hold Alt while layer active) using zmkfirmware/zmk#1366
- `Win Prev`: `<kbd>`Alt`</kbd><kbd>`Shift`</kbd><kbd>`Tab`</kbd>` (hold Alt while layer active)

I also used caksoylar's [`keymap-drawer`](https://github.com/caksoylar/keymap-drawer) to generate the representation below:

![Keymap Representation](./keymap-drawer/xavien-km.svg?raw=true "Keymap Representation")

Keymaps for QMK Firmware under development.

Will experiment for equivalent keymap definitions for QMK.

## ZMK customizations

A custom [ZMK branch](https://github.com/caksoylar/zmk) referenced in [west.yml](config/west.yml) was used.
This was done to enable the following:

- [mouse emulation](https://github.com/caksoylar/zmk/tree/caksoylar/experimental)
- [swapper behavior](https://github.com/zmkfirmware/zmk/pull/1366)
