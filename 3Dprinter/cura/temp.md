# ベッドとノズルの同時予熱するg-code
```
M140 S{material_bed_temperature_layer_0} ; start preheating the bed
M104 S{material_print_temperature_layer_0} T0 ; start preheating hotend
M190 S{material_bed_temperature_layer_0} ; heat to Cura Bed setting 
M109 S{material_print_temperature_layer_0} T0 ; heat to Cura Hotend
```
