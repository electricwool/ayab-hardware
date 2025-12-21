This is a work in progress

The position sensor circuit is the complete nonsense coppied from the main project it gives me:
### Voltage Readings at RP2040 Pins (After Interface Circuit)

| Sensor | Condition | Voltage | Notes |
|--------|-----------|---------|-------|
| **K carriage sensors** | No magnet | 3.47V | Baseline reading |
| **K carriage sensors** | Magnet present | 4.2V | **0.73V swing detected!** |
| **Lace carriage sensors** | All conditions | 3.47V | **No change detected!** |
| Lace left sensor | Moving carriage | 3.47V | Static voltage |
| Lace right sensor | Moving carriage | 3.47V | Static voltage |

and nearly 0v at all times at the output pins of the comparator circuits.

it does not function with the kh930/940
take note the board design for the esp32 board at the main project is completely incorrect and the kh930/940 has a different pinout for the power connector.
They have overly promoted the esp32 project as being compatible with any machine other than the kh910, even then I do not know if it would work as I do not have a kh910 to test.

The readings -when powered with 4.6V -5v+schottky diode--

### Voltage Readings at Sensor Board (Direct Power, No Interface)

**K-Carriage Sensor (Direct Power):**

| Condition | Voltage | Notes |
|-----------|---------|-------|
| **Magnet detected** | 3.47V | Carriage magnet directly over hall sensor |
| **No magnet (baseline)** | 1.68V | Carriage away from sensor |

**Voltage swing:** 3.47V - 1.68V = **1.79V difference** ✓ Good signal

**Lace Carriage Sensor (Direct Power):**

| Condition | Voltage | Notes |
|-----------|---------|-------|
| **Magnet detected** | 0.05V | Carriage magnet directly over hall sensor |
| **No magnet (baseline)** | 1.68V | Carriage away from sensor |

**Voltage swing:** 1.68V - 0.05V = **1.63V difference** ✓ Good signal

**Note:** These are the raw sensor board voltages when powered directly (disconnected from interface board). Both sensor types work correctly at the sensor board level.


todo:rework the board design to function with the sensors
