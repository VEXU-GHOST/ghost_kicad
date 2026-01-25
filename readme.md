# VEXU GHOST PCB Repository


Welcome to UT IEEE RAS VEXU GHOST's repository for our PCB developments!

# Host Board
![Physical Board Front View](docs/host_front.jpg)
![Physical Board Back View](docs/host_back.jpg)
![Layout](docs/host_layout.png)
![3D Model Isometric View](docs/host_model_iso.png)
![3D Model Front View](docs/host_model_front.png)
![3D Model Back View](docs/host_model_back.png)

# Base Development Board
![Physical Board Front View](docs/base_front.jpg)
![Physical Board Back View](docs/base_back.jpg)
![Layout](docs/base_layout.png)
![3D Model Isometric View](docs/base_model_iso.png)
![3D Model Front View](docs/base_model_front.png)
![3D Model Back View](docs/base_model_back.png)

# Color Sensor Breakout Board
![Physical Board Front View](docs/color_front.jpg)
![Physical Board Back View](docs/color_back.jpg)
![Layout](docs/color_layout.png)
![3D Model Isometric View](docs/color_model_iso.png)
![3D Model Front View](docs/color_model_front.png)
![3D Model Back View](docs/color_model_back.png)

# IMU Breakout Board
![Physical Board Front View](docs/imu_front.jpg)
![Physical Board Back View](docs/imu_back.jpg)
![Layout](docs/imu_layout.png)
![3D Model Isometric View](docs/imu_model_iso.png)
![3D Model Front View](docs/imu_model_front.png)
![3D Model Back View](docs/imu_model_back.png)

# Proximity Distance Sensor Breakout Board
![Physical Board Front View](docs/proximity_front.jpg)
![Physical Board Back View](docs/proximity_back.jpg)
![Layout](docs/proximity_layout.png)
![3D Model Isometric View](docs/proximity_model_iso.png)
![3D Model Front View](docs/proximity_model_front.png)
![3D Model Back View](docs/proximity_model_back.png)

# Offline Real-Time Clock Board
![Physical Board Front View](docs/rtc_front.jpg)
![Physical Board Back View](docs/rtc_back.jpg)
![Layout](docs/rtc_layout.png)
![3D Model Isometric View](docs/rtc_model_iso.png)
![3D Model Front View](docs/rtc_model_front.png)
![3D Model Back View](docs/rtc_model_back.png)

# Onboarding
Welcome to VEXU GHOST PCB team onboarding! This will give a brief introduction on using KiCAD and a general understanding in PCB design.
![Onboarding Model](docs/onboarding_model.png)

Follow these steps for the onboarding:
1. Clone this repo

2. Create a new branch with the name "Firstname_Lastname_Onboarding" (git branch Firstname_Lastname_Onboarding)

3. Open up the onboarding KiCAD project in the "onboarding" folder

4. Open up the schematic and complete the schematic for a color sensor development board by following the image below (the schematic doesn't have to be exactly the same, but it is a good habit to section and partition different parts in your schematic)
![Onboarding Schematic](docs/onboarding_schematic.png)

5. Check your schematic by running ERC (Inspect > Electrical Rule Checker), also ignore any errors on power output for 5V, 3V3, and GND

6. Assign footprints to the component (Tools > Assign Footprints) by following the image below
![Onboarding Schematic](docs/onboarding_footprints.png)

7. Transfer your schematic to the PCB editor (Tools > Update PCB from Schematic), click done, and place your component cluster down

8. Start creating your PCB layout by roughly positiong and lining up your components (the more important components or components with more pins should generally be placed in the middle, and related components with the same nets would be placed around them), the image below provides an example on how the PCB should turn out, but try to not copy everything one by one from image
![Onboarding Schematic](docs/onboarding_pcb.png)

9. Once you placed all of your components, start placing traces and connecting nets indicated by the light blue lines (start with signal nets first and then do power nets, and don't connect GND nets and leave them for next step) [generally you should use larger trace widths for nets connected to the power nets, such as 0.3 mm or 0.5 mm, and other traces for signals can use the default width or 0.2mm, you can set the trace widths by clicking the track dropdown on the top left corner > edit pre-defined sizes > + sign at the bottom of the tracks column, and you can enter the value for the trace width]

10. Once the components are all connected, create a GND plane on the front layer (and back layer if you want) by clicking the "Draw Filled Zone" button in button column on the right side of the screen, then click on the components, select GND for the net, and draw a box around the components (double click to finish), finally press B to fill the zones with a layer of copper that is conencted to GND (see if there is any GND nets that are left unconnected, use traces to connect them if there are)

11. Go to the "Layers" list on the right of the screen and select "Edge.Cuts", then click the "Draw Rectangle" button in the button column, and draw a rectangle around the components and zones to create the final shape for your PCB

12. Check your PCB layout by running DRC (Inspect > Rule Checker), see if there is any errors on pads being not connected or traces and pads being too close to the edge cuts

13. Save your KiCAD files, commit those file changes onto git, and push them to your branches for us to review
