# Keithley2400_GUI
The Keithley_GUI is a Python based user interface designed to perform IV measurements with the Keithley 2400 series Source Measure units (SMU).

## Important Notes

For the GUI to connect and send data to the SMU, the correct port ID must be stated in the Resource Name input field, as will be described below. If the SMU is connected to a different PC or via a different cable connection, this name must be correctly changed to the corresponding port. That requires running a separate python code to identify the ports and installation of the PyMeasure scientific package, explained in Appendix B. A function to detect and display connections within the GUI will be added in future versions, if this becomes necessary. 

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
