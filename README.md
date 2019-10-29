# pibfox

This project implements a fully automatic fox controller for ARDF competitions, capable of running all modes of operations presented in the IARU Region 1 rules for ARDF events, having an easy to use user interface for configuring and safe and easy deployment possibility.

## Specifications

The fox controller shall observe the IARU R1 ARDF rules and technical specifications for transmitters.

### Operational specs:

- carrier frequency: 3.510 - 3.600 MHz / 144.500 - 144.900 MHz
- frequency stability: 50 ppm
- output RF level: 1 - 5W / 0.25 - 1W
- modulation: A1A/ A2A
- transmitting code: MOE, MOI, MOS, MOH, MO5, MO, S
( -- --- . , -- --- .. , -- --- ... , -- --- .... , -- --- ..... , -- --- , ... ) 
- keying speed: 8 - 15 wpm

The transmitter shall be capable of operating for 80m classic, 2m classic, sprint and foxoring events.
To ensure this the following configurations should be able to be stored in the transmitter:

- transmit timing: continuous, interval: 1/2, 1/3, 1/4, 1/5, interval periods: 12s, 60s
- code wpm: 8, 9, 10, 11, 12, 13, 14, 15
- output power: 100mW, 500mW, 1W, 3W, 5W
- working frequency: 3.510, 3.520, 3.530, 3.540, 3.550, 3.560, 3.570, 3.580, 3.590, 3.600 MHz
- frequency accuracy: +-150Hz
- carriers and modulated tones are directly synthesized in µC

Configuring the transmitter shall be done on a dedicated interface attached to the fox, or on a computer attached to the fox. Configurations shall be preserved indefinitely (store in EEPROM).
Clock synchronization is realized while configuring from the external device. Clock synchronization shall be kept while on battery power, at least 10 days.
 
Battery operation:
battery should last at least a whole competition in active transmission, while in power save mode at least 10 days. Power saving is active while no antenna is connected to the fox. When antenna is connected the fox becomes active according to the configured transmission cycle.


### Hardware specs:

Power source: internal LiIon battery, 7.4V -- 11.1V
Output power: max 5W
Active current consumption: 1A
Battery capacity: 8Ah
Power down mode: <200µA

