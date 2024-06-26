# Power-Loss-Recovery
Power Loss Recorevy For Klipper

# Tested with Cura
Read carefully plr.cfg
In your Slicer

add as the last row of start gcode: save_last_file

add as the first row of end gcode: clear_last_file

at every layer add gcode macro: LOG_Z

(in Cura add post processing script "Insert at layer Change" and insert "After", G-code: LOG_Z )

copy plr.sh in /home/mks/printer_data/config/scripts/ 

in putty: chmod +x /home/mks/printer_data/config/scripts/plr.sh

in Kiauh install Gcode Shell Command

In printer.cfg or here you need:

[save_variables]

filename: ~/save_variables.cfg # needed for Power Loss Recovery plr.cfg

Change permissions on plr.sh: sudo chmod +x plr.sh

# NOTES: PATH FILE MUST BE THE SAME IN BOTH PLR FILES AND VIRTUAL CARD IN KLIPPER.
