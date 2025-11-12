1)

Component 1: ESP32-S3@Xtensa LX7 manufactured by Espressif
I was able to find a couple of CVEs for the ESP32, they were CVE 2020-13629 and CVE 2020-15048. These are described as bypassing encrypted secure boot and bypassing flash encryption.
Component 2: INA3221AIRGVR manufactured by Texas Instruments
I wasn’t able to find any CVEs for this current monitor, but did find other possible risks. These were I2C bus tampering and a lack of data authentication.
Component 3: BMI270 6 axis gyroscope manufactured by Bosch Sensortech
I also didn’t find any CVEs for this component, but risks include sensor spoofing attacks.

2)

Hardware dependencies strongly influence the general security risk. Essentially all companies outsource some of their hardware, and in doing so they are trusting the security standards of another company. Even when using internal hardware, I think we know that it is relatively impossible to build something that is perfectly secure. I also took away from this assignment that hardware dependencies are a security risk that SBOMs don’t detect. There were multiple CVEs I was able to find for the ESP32-S3, but that was not found by the checkers we used.
