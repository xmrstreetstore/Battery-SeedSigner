<p align="center">
  <img src="img/logo.svg" width="340" alt="SeedSigner logo">
</p>

<h1 align="center">Battery SeedSigner</h1>
<p align="center"><b>Open-source hardware for <a href="https://seedsigner.com">SeedSigner</a></b> — an airgapped, camera-based Bitcoin signing device.</p>

<p align="center">
  <img src="display_hats/plus_hat/AAA powered board/images/Sesi+ AAA complete.png" width="260" alt="Assembled battery-powered SeedSigner+">
  <img src="display_hats/plus_hat/AAA powered board/images/Sesi+ AAA complete battery flap.jpg" width="380" alt="Battery compartment with 3x AAA cells installed">
</p>

This repository collects hardware designs for SeedSigner: display HATs, 3D-printable enclosures, and SeedQR paper templates. Its centerpiece is the **Battery SeedSigner** — a modified SeedSigner+ (SeSi+) board that runs entirely off 3x AAA batteries instead of USB power.

> **Runs stock SeedSigner OS.** This is a pure hardware/power mod — no custom firmware, OS build, or software changes of any kind. Flash the [official SeedSigner OS image](https://seedsigner.com) exactly as you would for any other SeedSigner build; the battery board just replaces the power source.

---

## What is the Battery SeedSigner?

The stock SeedSigner+ mainboard is powered over USB. This mod adds a small **3-pin connector** to the stock board (see the photos below) that mates via a short cable to a separate **3x AAA battery board**. The battery board holds three AAA cells and regulates their output to power the signer directly — no USB cable, no wall power, no computer required to use the device.

The result is a fully self-contained, battery-powered signer: drop in three AAA batteries, close the case, and sign transactions completely offline with nothing plugged in.

<p align="center">
  <img src="display_hats/plus_hat/AAA powered board/images/Sesi+ AAA battery kit.jpg" width="640" alt="Full kit: SeedSigner+ board, battery board, and connecting cable">
</p>
<p align="center"><i>The kit: SeedSigner+ display/control board (top), 3x AAA battery board with connector cable (right).</i></p>

### Why

USB-powered airgapped signers still need to be plugged into *something* to receive power, which for many users means routing a cable to a phone charger, power bank, or computer — none of which is ideal for a device meant to stay fully isolated. Running the signer off primary AAA cells removes that dependency entirely: swap batteries and go, no charging infrastructure needed.

### How it works

| | |
|---|---|
| **Battery board** | Holds 3x AAA cells in series (~4.5V) and regulates the output to a stable 5V rail via an onboard converter. |
| **Connector** | A 3-pin cable links the battery board to a matching connector added to the stock SeSi+ board. Only 2 of the 3 pins are wired: **5V** and **GND**. The third pin is unused. |
| **Stock board mod** | The only change to the reference SeedSigner+ PCB is the added 3-pin connector — everything else, including the software it runs, matches the stock design. |

<p align="center">
  <img src="display_hats/plus_hat/AAA powered board/images/Sesi+ AAA battery board.png" width="480" alt="3x AAA battery board close-up">
</p>
<p align="center"><i>The battery board: 3x AAA holder, regulator, and JST output connector.</i></p>

### Where to find the files

All design files, production files (BOM, pick-and-place, Gerbers), schematics, and 3D models for the battery board and the modified SeSi+ board live in:

```
display_hats/plus_hat/AAA powered board/
```

See that folder's [README](<display_hats/plus_hat/AAA powered board/README.md>) for the full file listing and BOM.

---

## Repository layout

| Folder | Contents |
|---|---|
| [`display_hats/plus_hat/`](display_hats/plus_hat) | The SeedSigner+ (SeSi+) display/control board, including the [Battery SeedSigner](<display_hats/plus_hat/AAA powered board>) mod above and the reference 2.8" LCD hat Gerbers. |
| [`signer_enclosures/`](signer_enclosures) | 3D-printable enclosures for various SeedSigner builds (Orange Pill, Open Pill, Rugged Pill, Push Case, SeedSigner+ reference design, and more). |
| [`seedqr_templates/`](seedqr_templates) | Printable PDF templates for recording SeedQR-encoded mnemonics on paper/cards. |
| [`img/`](img) | Shared product photos and the SeedSigner logo used across this README and sub-READMEs. |

Each enclosure/board subfolder has its own README with assembly notes, characteristics, and required hardware.

## License

Hardware designs in this repository are licensed under the [CERN Open Hardware Licence Version 2 - Strongly Reciprocal](LICENSE). SeedSigner itself is free, open-source software — see [seedsigner.com](https://seedsigner.com) and the [SeedSigner GitHub org](https://github.com/SeedSigner) for the signing device firmware and reference hardware this project builds on.
