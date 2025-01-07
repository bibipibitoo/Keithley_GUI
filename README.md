# Keithley2400_GUI
The Keithley_GUI is a Python based user interface designed to perform IV measurements with the Keithley 2400 series Source Measure units (SMU), based upon the existing library [Keithley_GPT](github.com/NREL/Keithley_GPT).

## About

## Identifying Instruments

For the GUI to connect and send data to the SMU, the correct port ID must be stated in the _Resource Name_ input field. If the SMU is connected to a different PC or via a different cable connection, this name must be correctly changed to the corresponding port. If the correct port is unknown, it requires running a separate python code to identify the ports and installation of the [PyMeasure scientific package](https://pymeasure.readthedocs.io/en/latest/quick_start.html) and the [NI-VISA library](https://pyvisa.readthedocs.io/en/latest/faq/getting_nivisa.html#faq-getting-nivisa). This functionality may be added in future releases.

Run the code below in a command prompt, IPython terminal, or Jupyter notebook.

``` python
from pymeasure.instruments.resources import list_resources
list_resources()
```
 The output will list all connections like below:

```
0 : ASRL2::INSTR : Not known
1 : ASRL10::INSTR : Not known
2 : GPIB0::1::INSTR : KEITHLEY INSTRUMENTS INC.,MODEL 2400,1248014,C30   Mar 17 2006 09:29:29/A02  /K/J
Out[1]:
('ASRL2::INSTR', 'ASRL10::INSTR', 'GPIB0::1::INSTR')
```

Input the correct port into the _Resource Name_ field. 

## Documentation

The complete documentation is uploaded under documentation [IV Sweep GUI Documentation](https://github.com/bibipibitoo/Keithley_GUI/blob/main/IV%20Sweep%20GUI%20Documentation.pdf)

## System Requirements
*Windows 7+
