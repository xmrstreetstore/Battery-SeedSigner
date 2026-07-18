# AAA Powered Board (Battery SeedSigner)

<p align="center">
  <img src="images/Sesi+ AAA complete.png" width="280" alt="Assembled battery-powered SeedSigner+">
</p>

A 3x AAA battery board for the SeedSigner+ (SeSi+) display/control board, letting it run untethered from USB power. The stock SeSi+ board is modified with a **3-pin connector** that mates to a matching connector on the battery board via a short cable — power flows straight from the batteries to the board, no USB or wall power involved.

This is a pure hardware power mod: the board runs the **official, unmodified SeedSigner OS**. No custom firmware, OS build, or software changes are needed — flash the standard SeedSigner image as usual.

## Characteristics

- Powers a SeedSigner+ board entirely from 3x AAA cells (~4.5V nominal)
- Onboard regulator delivers a stable 5V rail to the mainboard
- Connects to the SeSi+ board with a 3-pin cable — only **5V** and **GND** are wired; the third pin is unused
- Runs the stock, official SeedSigner OS — no firmware/software modification required

## Gallery

<p float="left">
	<img src="images/Sesi+ AAA battery board.png" width="380">
	<img src="images/Sesi+ AAA complete battery flap.jpg" width="380">
</p>
<p float="left">
	<img src="images/Sesi+ AAA battery kit.jpg" width="780">
</p>

## Files

### Design sources

| File | Description |
|---|---|
| `AAA-Battery-board-EasyEDA-project.json` | EasyEDA Pro project file for the battery board |
| `AAA-Battery-board-SCH.json` | Battery board schematic (EasyEDA) |
| `AAA-Battery-board-Schematic.pdf` | Battery board schematic, PDF export |
| `AAA-Battery-board-3D file.step` | Battery board 3D model (STEP) |
| `AAA-SeSi+-EasyEDA-project.json` | EasyEDA Pro project file for the modified SeSi+ board |
| `AAA-SeSi+-SCH.json` | Modified SeSi+ board schematic (EasyEDA) |
| `AAA-SeSi+-3D file.step` | Modified SeSi+ board 3D model (STEP) |

### Production files (`Production files/`)

| File | Description |
|---|---|
| `BOM/AAA-Battery-board-BOM.csv` | Bill of materials — battery board |
| `BOM/AAA-Battery-board-PickAndPlace.csv` | Pick-and-place data — battery board |
| `BOM/AAA-SeSi+-BOM.csv` | Bill of materials — modified SeSi+ board |
| `BOM/AAA-SeSi+-PickAndPlace.csv` | Pick-and-place data — modified SeSi+ board |
| `Gerbers/AAA-Battery-board.zip` | Fabrication Gerbers — battery board |
| `Gerbers/AAA-SeSi+-gerbers.zip` | Fabrication Gerbers — modified SeSi+ board |

## Assembly

1. Fabricate or source both boards (see production files above).
2. Load 3x AAA cells into the battery board.
3. Connect the battery board to the modified SeSi+ board via the 3-pin cable.
4. Fit into a compatible enclosure with battery access (see [`signer_enclosures/`](../../../signer_enclosures)) — the flap-style cutout shown above allows swapping cells without disassembling the case.
