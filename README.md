# Driver for Analog Sensors

## API

### Includes

```
#include "asensor.ceu"
```

### Code Abstractions

#### ASensor

```
code/await ASensor_Get(var int dataPort, var int? energyPort, var int? time) -> int;
```

Parameters:

- `int`: analog port for receive data
- `int`: energy port used to turn on and off the sensor
- `int`: time, in ms, the driver waits for the circuit to stabilize

Return:

- `int`: converted value of the analog sensor

This code/await turns the energy pin on, waits for the circuit stabilize and, then, read the analog value from the sensor. 