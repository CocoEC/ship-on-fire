# *Ship on Fire!* videogame

This repository contains the files related to this small school project.

It is an archive of the original repository hosted elsewhere.

Team: Mohamed Emine Bassoum, Lucas Bignolet, Clément Escude--Cotinat, Guillaume Hisleur

Technologies used: SDL2 over C.


## Features

- 2-ship battle
- Ship and projectile physics
- Turret and hull collision attack
- Simple camera system
- Intelligent opponent aim
- Mouse-only and mouse & keyboard controls


## Quickstart

This has been tested in a Debian-based system.

```bash
sudo apt install libsdl2-dev libsdl2-image-dev
cd src
make loop 
./loop
```

### Controls:

- Buttons or Q/D: chadburn (speed command) setting
- Central button or F: enter aim mode
- [While in aim mode] mouse/click: aim/shoot
- Space bar: switch camera target
- Esc: exit

---

## Documentation

Game specifications (in french) can be found in `docs/specs/`, see [this](docs/specs/README.md).


## Project management

Meeting reports (french) and such can be found in `docs/gdp/`.


---

The sky, sun, clouds and sea assets come from craftpix.net. Other assets made by Clément Escude--Cotinat.
