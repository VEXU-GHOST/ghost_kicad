# Onboarding
Welcome to VEXU GHOST PCB team onboarding! This will give a brief introduction on using KiCAD and a general understanding in PCB design.
![Onboarding Model](onboarding_model.png)

Follow these steps for the onboarding:

1. Download KiCAD V9.0+ (https://www.kicad.org/download/) and download Git (https://git-scm.com/install/windows)

2. Clone this repo by clicking the green clone button, copying https (or ssh if you have ssh set up) link, and typing the following command: git clone [paste the https or ssh link] (right click > paste to paste in bash), if you have cloned repos before and have a directory set up for cloning repos, you can clone the repo there, otherwise enter the command as is

3. Open up the repo's directory (cd ghost_kicad) and create a new remote branch with the name "Firstname_Lastname_Onboarding" (git branch Firstname_Lastname_Onboarding -> git checkout Firstname_Lastname_Onboarding)

4. Open up the onboarding KiCAD project in the "onboarding" folder

5. Open up the schematic and complete the schematic for a color sensor development board by following the image below (the schematic doesn't have to be exactly the same, but it is a good habit to section and partition different parts in your schematic)
![Onboarding Schematic](onboarding_schematic.png)

6. Check your schematic by running ERC (Inspect > Electrical Rule Checker), also ignore any errors on power output for 5V, 3V3, and GND

7. Assign footprints to the component (Tools > Assign Footprints) by following the image below
![Onboarding Schematic](onboarding_footprints.png)

8. Transfer your schematic to the PCB editor (Tools > Update PCB from Schematic), click done, and place your component cluster down

9. Start creating your PCB layout by roughly positiong and lining up your components (the more important components or components with more pins should generally be placed in the middle, and related components with the same nets would be placed around them), the image below provides an example on how the PCB should turn out, but try to not copy everything one by one from image
![Onboarding Schematic](onboarding_pcb.png)

10. Once you placed all of your components, start placing traces and connecting nets indicated by the light blue lines (start with signal nets first and then do power nets, and don't connect GND nets and leave them for next step) [generally you should use larger trace widths for nets connected to the power nets, such as 0.3 mm or 0.5 mm, and other traces for signals can use the default width or 0.2mm, you can set the trace widths by clicking the track dropdown on the top left corner > edit pre-defined sizes > + sign at the bottom of the tracks column, and you can enter the value for the trace width]

11. Once the components are all connected, create a GND plane on the front layer (and back layer if you want) by clicking the "Draw Filled Zone" button in button column on the right side of the screen, then click on the components, select GND for the net, and draw a box around the components (double click to finish), finally press B to fill the zones with a layer of copper that is conencted to GND (see if there is any GND nets that are left unconnected, use traces to connect them if there are)

12. Go to the "Layers" list on the right of the screen and select "Edge.Cuts", then click the "Draw Rectangle" button in the button column, and draw a rectangle around the components and zones to create the final shape for your PCB

13. Check your PCB layout by running DRC (Inspect > Rule Checker), see if there is any errors on pads being not connected or traces and pads being too close to the edge cuts

14. Save your KiCAD files and ask another PCB team member to help you get added into the repo and our notion page

15. Once you have been added to the repo, commit those file changes onto git, and push them to your branches for us to review (git add . -> git commit -m "finish onboarding" -> git push origin Firstname_Lastname_Onboarding)