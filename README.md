# Python I2C Driver for Sensirion LD20

This repository contains the Python driver to communicate with a Sensirion sensor of the LD20 family over I2C.

<img src="https://raw.githubusercontent.com/Sensirion/python-i2c-ld20/master/images/sensor_LD20.png"
    width="300px" alt="LD20 picture">


Click [here](https://sensirion.com/products/catalog/liquid-flow-sensors?series=LD20) to learn more about the Sensirion LD20 sensor family.


Not all sensors of this driver family support all measurements.
In case a measurement is not supported by all sensors, the products that
support it are listed in the API description.



## Supported sensor types

| Sensor name   | I²C Addresses  |
| ------------- | -------------- |
|[LD20-0600L](https://sensirion.com/products/catalog/LD20-0600L/)| **0x08**|
|[LD20-2600B](https://sensirion.com/products/catalog/LD20-2600B/)| **0x08**|

The following instructions and examples use a *LD20-0600L*.



## Connect the sensor

You can connect your sensor over a [SEK-SensorBridge](https://developer.sensirion.com/product-support/sek-sensorbridge/).
For special setups you find the sensor pinout in the section below.

<details><summary>Sensor pinout</summary>
<p>
<img src="https://raw.githubusercontent.com/Sensirion/python-i2c-ld20/master/images/ld20_pinout.png"
     width="300px" alt="sensor wiring picture">

| *Pin* | *Cable Color* | *Name* | *Description*  | *Comments* |
|-------|---------------|:------:|----------------|------------|
| 1 | green | SDA | I2C: Serial data input / output |
| 2 | red | VDD | Supply Voltage | 3.2V to 3.8V
| 3 | black | GND | Ground |
| 4 | yellow | SCL | I2C: Serial clock input |
| 5 |  | NC | Do not connect |


</p>
</details>


## Documentation & Quickstart

See the [documentation page](https://sensirion.github.io/python-i2c-ld20) for an API description and a
[quickstart](https://sensirion.github.io/python-i2c-ld20/execute-measurements.html) example.


## Contributing

### Check coding style

The coding style can be checked with [`flake8`](http://flake8.pycqa.org/):

```bash
pip install -e .[test]  # Install requirements
flake8                  # Run style check
```

In addition, we check the formatting of files with
[`editorconfig-checker`](https://editorconfig-checker.github.io/):

```bash
pip install editorconfig-checker==2.0.3   # Install requirements
editorconfig-checker                      # Run check
```

## License

See [LICENSE](LICENSE).