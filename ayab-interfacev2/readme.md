Version 2 of the interface board

switched to using ADS1015 via I2C with ALERT pin so that async firmware will work. The brother machines use many different sensor configurations. Some have negative voltage. Some are positive voltage. Some use multiple optical sensors. ADS1115 is an I2C ADC that can sense and report -6 to 6V with only a 3.3v VCC. The ADS1015 will allow them all to work with confguration via software. The current implementation in the main project only supports the kh910 due to the limitations of the fixed ADC implementation. using the LM comparator fixes the board for a specific machine and requires a large population of SMD components for interfacing circuitry that is not easy to rework.

Using the ADS1015 for the L&R sensors reduces the total MCU pins to a single interupt pin to trigger reads as well as the existing I2C lanes. This comes at significant cost. read time is ~1ms compared to the four pin implementation that has a read time of ~50μs. It is however programmable which is a highly desirable improvement. hardware specific interupt handling can be implemented to leverage continuous sampling and mcu features like PIO independent state machines to offload functions from cpu time.

most of the ceramic caps are not necessary but a quirk of pcba is that it costs nothing($0.001 each) to add them.
