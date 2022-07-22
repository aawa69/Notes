# Use SAP GUI for Java on SAP CAL AS ABAP

<img src="https://github.com/aawa69/Notes/blob/main/SAP/Dev_Setup/Eclipse/images/sapguiforjava.png" width="12%">

## Note

- Ensure you're running a `DEV` instance ➡︎ allow installation of a minisap license
- `TRIAL` and other types of instances will expect you to bring your own license  

## Connect to a (remote) SAP CAL system system

- Install SAP GUI for Java ➡︎ see blog [Notes on Installing SAPGUI for Java for MacOS](https://blogs.sap.com/2022/03/04/notes-on-installing-sapgui-for-java-for-macos/)

- Create a `New Connection`
- Navigate to the `Advanced` tab and select the `Expert Settings` checkbox
- Enter the connection string using the:
  - Linux External IP Address ➡︎ under `Info` tab
  - `SAP GUI` Service port number ➡︎ under `Virtual Machines` tab (usually 3200)

## Credentials

<style>
    .indent {
        margin-left: 20px;
     }
    .highlight {
        color: #7FE787;
    }
</style>

<p class="indent">Logon: <span class="highlight">developer</span></p>
<p class="indent">Password: <<span class="highlight">as specified on creation of the SAP CAL instance</span>></p>

<img src="https://github.com/aawa69/Notes/blob/main/SAP/Dev_Setup/Eclipse/images/connectionprops.png" width="40%">

<img src="https://github.com/aawa69/Notes/blob/main/SAP/Dev_Setup/Eclipse/images/sapcal.png" width="50%">

<img src="https://github.com/aawa69/Notes/blob/main/SAP/Dev_Setup/Eclipse/images/sapguiport.png" width="50%">

## References

- Blog ➡︎ determining the [SAP GUI for Java connection string](https://blogs.sap.com/2017/08/01/sap-gui-for-java-connection-strings/)
