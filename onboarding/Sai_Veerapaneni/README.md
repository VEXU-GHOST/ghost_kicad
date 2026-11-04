# Sai Veerapaneni — PCB onboarding

Open `Sai_Veerapaneni_Onboarding.kicad_pro` in KiCad 10 to review the
color-sensor schematic and completed two-layer PCB.

The board is 26 × 18 mm, with 14 footprints, routed signal and supply nets,
front/back GND pours, and a rectangular Edge.Cuts outline. Signal tracks
are 0.2 mm; supply tracks are 0.3 mm with 0.2 mm sensor escapes. Copper
clearance is 0.2 mm and copper-to-edge clearance is 0.5 mm.

J1 pinout: **1 GND, 2 SCL, 3 SDA, 4 +3.3V, 5 +5V**. The host provides
both regulated supply rails. Sai Veerapaneni is printed on the back silk.

Custom libraries are project-local. Standard footprints and 3D models
use the installed KiCad libraries and this repository's `ghost_library`.
The connector preserves standard pads, drills, and physical geometry;
its off-board lead artwork is on F.Fab to keep silk inside the board edge.

Validation reports are saved in `checks/`. The schematic follows the
onboarding reference without power flags; the three external-supply ERC
errors are the ones the onboarding explicitly permits ignoring.
