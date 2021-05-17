[![View netHAT EtherCAT Slave Block SFunction for Raspberry Pi on File Exchange](https://www.mathworks.com/matlabcentral/images/matlab-file-exchange.svg)](https://www.mathworks.com/matlabcentral/fileexchange/75243-nethat-ethercat-slave-block-sfunction-for-raspberry-pi)

# netHAT EtherCAT Slave Block SFunction for Raspberry Pi
The example netHAT EtherCAT Slave Driver Block SFunction for Raspberry Pi shows basic usage of the cifX library by transferring 32 bytes of input and output PDO data. Additionally, a configuration file for the netHAT device and netHAT EtherCAT Slave Driver Block SFunction are included to increase the number of input and output PDO data to 200 bytes.

Usage instructions:
1. Download the netHAT DVD from https://www.netiot.com/interface/nethat/
2. Unpack and follow the installation instructions in Section 3.3 of the netHat User Manual located in the map V1.0.0.1\Documentation\Getting Started
3. (Optional) By default the netHat driver configuration is fixed to a PDO input and output of 32 bytes. Follow the following substeps to increase to a PDO input and output of 200 bytes.
  - Rename config_200bytes.nxd to config.nxd and replace the \opt\cifx\deviceconfig\FW\channel0\config.nxd on the Raspberry Pi.
  - Use the ESI file "Hilscher NXHAT52-RTE ECS 200bytes V4.X.X.xml" instead to configure the EtherCAT Master.
4. Open Simulink model "raspberrypi_ethercat_slave.slx", or if the above optional steps are done open "raspberrypi_ethercat_slave_200bytes.slx" instead.
5. Open the EtherCAT Slave block and build the netHAT52_RTE Sfunction.
6. Deploy the model to the Raspberry Pi hardware.
