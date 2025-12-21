Version 2 of the interface board

switched to using 2x ADS1115 via I2C with ALERT pin so that async firmware will work. The brother machines use many different sensor configurations. Some have negative voltage. Some are positive voltage. Some use multiple optical sensors. ADS1115 is an I2C ADC that can sense and report -6 to 6V with only a 3.3v VCC. The ADS1115 will allow them all to work with confguration via software. The current implementation in the main project only supports the kh910 due to the limitations of the fixed ADC implementation. using the LM comparator fixes the board for a specific machine and requires a large population of SMD components for interfacing circuitry that is not easy to rework.

Using the ADS1115 for the encoder and L&R sensors reduces the total MCU pins to a single interupt pin to trigger reads upon carriage movement as well as the existing I2C lanes.

<img src=https://github.com/electricwool/ayab-hardware/blob/main/ayab-interfacev2/interfacev2.jpg>

