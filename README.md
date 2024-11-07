# Keithley_GUI
The Keithley_GUI is a Python based user interface designed to perform IV measurements with the Keithley 2400 series Source Measure units (SMU).

## Important Notes

``` python
from pymeasure.instruments.resources import list_resources
list_resources()
``` 
The snippet above is the code required to identify all connections to the PC. It requires the package PyMeasure. The output will list all connections like below:

```
0 : ASRL2::INSTR : Not known
1 : ASRL10::INSTR : Not known
2 : GPIB0::1::INSTR : KEITHLEY INSTRUMENTS INC.,MODEL 2400,1248014,C30   Mar 17 2006 09:29:29/A02  /K/J
Out[1]:
('ASRL2::INSTR', 'ASRL10::INSTR', 'GPIB0::1::INSTR')
```


Input the correct port into the Resource Name field. 
