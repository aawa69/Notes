# Setup Cloud Connector for SAP CAL AS ABAP

<img src="https://github.com/aawa69/Notes/blob/main/SAP/Dev_Setup/Eclipse/images/configmgt.png" width="12%">

## Overview

- SAP Cloud Connector comes bundled with SAP CAL ABAP Instance
- Use SCC to connect SCP trial with CAL ABAP back-end, providing:  
  - Build in a local IDE (Eclipse or VSCode)
  - Build & deploy development objects in the SAP CAL ABAP client
  - Create an SCP destination, pointing to our Cloud Connector, which in turen links to SAP CAL ABAP
  - Build Fiori apps in SCP trial, utilising our SAP CAL ABAP backend  

## Configure SAP CAL

To access Cloud Connector from the browser, configure SAP CAL with port 8443;

    https://<Linux External IP Address>:<Cloud Connector Port>

    https://3.92.143.219:8443   ➤ example

<img src="https://github.com/aawa69/Notes/blob/main/SAP/Dev_Setup/Eclipse/images/sapcalinstance.png" width="45%">

<img src="https://github.com/aawa69/Notes/blob/main/SAP/Dev_Setup/Eclipse/images/ccport.png" width="45%">

### Configure SAP Cloud Connector

<img src="https://github.com/aawa69/Notes/blob/main/SAP/Dev_Setup/Eclipse/images/ccinitiallogin.svg"  width="50%">

<img src="https://github.com/aawa69/Notes/blob/main/SAP/Dev_Setup/Eclipse/images/ccloginpage.png" width="45%">

<img src="https://github.com/aawa69/Notes/blob/main/SAP/Dev_Setup/Eclipse/images/ccoverview.png" width="45%">

<img src="https://github.com/aawa69/Notes/blob/main/SAP/Dev_Setup/Eclipse/images/ccmapping.png" width="45%">

## References

- [Connectivity Setup with ABAP and SAP Cloud Connector](https://blogs.sap.com/2019/03/27/how-to-guide-connectivity-setup-with-abap-and-sap-cloud-connector/)
  - Cloud connector details
  - Setting up SAP Cloud Platform destination
  - Creation of a Fiori app based on the new remote system destination
