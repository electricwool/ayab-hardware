adapter board for connecting the arduino nano(3.3v)

various boards have identical pinout and 3.3v regulator on the obverse side or 3.3v logic and a 3.3V supply provided by the usb to serial chip. The serial chip is limitted to about 40mA that is enough to power the chip and one bright LED or the control circuitry. The chips use about 50µA quiescent current each and fractions of a mA per lane when active:

-Nano 33 BLE (Nordic nRF52840)

-generic nano "4.0" (AT328 - same as Arduino Uno)

-Arduino Nano R4 ABX00142 (RA4M1 ARM)

-Nano matter (MGM240SD22VNA ARM)

<img width="800" height="600" alt="image" src="https://github.com/user-attachments/assets/16d37263-36ca-45eb-bfa4-41803a34e5d8" />

When buying generic nano "4.0" check for the presence of the 3.3V regulator on the obverse.

<img alt="image" src="https://github.com/user-attachments/assets/cb70a16f-6080-49c1-bcd7-3d71a93a727f" />

