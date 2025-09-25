<div align="center">
    <h1>XAVIENT Keyboard</h1> 
    <img alt="xavient keyboard" width="100%" src="./docs/img/xavient.jpg">
    <h4>An open-sourced split ergonomic keyboard focusing on repairability and sleek thin design.</h4>
    <p><i>still a work in progress</i></p>

</div>

This keyboard build followed some inspirations on various open-sourced keyboards listed below:

- [Corne](https://github.com/foostan/crkbd): basing the footprint of the controller here since this is the most common keyboard.
- [Swoop](https://github.com/jimmerricks/swoop): used as my first keyboard when I was exploring the world of split-keyboards
- [Flake](https://github.com/anywhy-io/flake): got some inspiration on how to implement jst battery connections.

Some Close-sourced keyboards:

- [Sweet-Corne](https://imgur.com/a/sweep-corne-gjZDgmk): My first attempt at building a keyboard from scratch. (Lost Files)
- [Corne-ish Zen](https://lowprokb.ca/products/corne-ish-zen): A thin split keyboard with e-ink displays. (Sold Out)

The placement of the keys for this keyboard are loosely based on both the Corne and Swoop Keyboards.

`<img alt="keyboard layouts" width="100%" src="./docs/img/layout.png">`

## Goal

The goal for this keyboard is to make a thin keyboard without sacrificing repairability or upgradablility. Taking inspiration from the Corne-ish Zen build but with hotswappable components.

## Main Features

- **User Repairable:** Controllers, Displays, and batteries are replaceable without the need of unsoldering the components.
- **Multi Switch Compatibility:** Using Hotswappable Sockets compatible for **MX** and **Kailh LP** (*using millmax 7305 sockets*) and **Gateron LP** (*using both millmax 7305 and Gateron LP sockets*)
- **Two Layout Options:** available as a 36 key layout and a 42 key layout (52 key layout on-going development)
- **Large Battery Capacity** 2 allocated battery slots with each slot having  a 250mah maximum battery capacity
- **Upgradability:** Future expansion to a Trackpoint [WIP] (will take up one battery slot)
- **Thin Profile:** Achieved a 8mm thick keyboard by having a sandwiched layout for the controller and display.

## The Whys and Hows

### Repairability

During various iterations at building a keyboard the first things that I encountered various issues that led me building this keyboard. One of those things were with regards to the controller layout. The usual route was to have the Pro-Micro/NiceNano be mounted on Mill Max Low Profile Sockets or straight to surface mounted PCBs.

- **Mill Max Low Profile Sockets:** This allows the battery to be sandwiched between the PCB and the Microcontroller. Add the display on top of the microcontroller and you have a thick stack of components.
  - *Repairability*: 5/5 - easily hotswap components.
  - *Looks*: 2/5 - open case design which is cheaper (prefer an enclosed case).
  - *Complexity*: 2/5 - beginner/budget friendly.
  - *Modularity*: 5/5 - option to convert builds from wired to wireless.
    Some examples of this are the Swoop Keyboard, Corne v4, and various other open-sourced keyboards.
- **Surface-mounted PCB:** This allows the pcb to be thin but will require a dedicated case and different pcb designs for wired and wireless builds.
  - *Repairability*: 1/5 - components are tiny and hard to hand solder.
  - *Looks*: 4/5 - often designed to have an enclosed case.
  - *Complexity*: 2/5 - not beginner/budget friendly due to the complexity.
  - *Modularity*: 1/5 - separate builds for wired and wireless.
    Some examples of this are the Corne-ish Zen Keyboard, Corne KBD (main branch), Seeed Xiao-based keyboards and various other keyboards from various sellers.

Xavient tries to combine the best features of both worlds into one. The solution is to use 7305  Millmax Sockets not just for key switches but for the controller and display as well. This saves space height-wise and adds a better space for bigger batteries.
