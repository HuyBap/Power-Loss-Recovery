# Power-Loss-Recovery
Power Loss Recorevy For Klipper
# Test with Cura
Read carefully plr.cfg
In your Slicer

add as the last row of start gcode: save_last_file

add as the first row of end gcode: clear_last_file

at every layer add gcode macro: LOG_Z

copy plr.sh in /home/pi/printer_data/config/scripts/ 

in putty: chmod +x /home/pi/printer_data/config/scripts/plr.sh

in Kiauh install Gcode Shell Command

In printer.cfg or here you need:

[save_variables]

filename: ~/save_variables.cfg # needed for Power Loss Recovery plr.cfg

Add these files somewhere that klipper can access them. ~/. should be a fine choice, if you have no idea. You must then add an [include] directive in order to add the contents of plr.cfg to your printer.cfg, or just paste it in if you don't like [include] directives, plr.sh must be marked executable. Also, plr.cfg and plr.sh must be modified to reflect the location of your virtual sdcard in Klipper.
