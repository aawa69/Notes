# Connect to SAP CAL AS ABAP

<img src="https://github.com/aawa69/Notes/blob/main/SAP/Dev_Setup/Eclipse/images/sapcalimg.png" width="12%">

**&#9888; Caution**

- Note the password used on creation of CAL instance
- Will be required to access the SAP system from ADT later on!!

## Connect to a (remote) SAP CAL instance

- ADT connects using RFC (TCP) on port 3300 (33 + the instance number)
- Edit the SAP CAL instance and add port 3300

<img src="https://github.com/aawa69/Notes/blob/main/SAP/Dev_Setup/Eclipse/images/port3300.png" width="45%">
  
- In Eclipse with an installed ADT
  - Create a new ABAP Project (or duplicate an existing and amend)
  - Previously created system connections will display if created manually or derived from an active SAP GUI session
  - To create manually, select the new system connection link
  - Enter the _System Id_ of the SAP Cal instance, i.e. *_NPL_*
  - Select `Custom Application Server` for the _Connection Type_
  - Enter the _Linux External IP Address_ - see `Info` tab of CAL instance
  - Deselect _SNC_ settings
  - Enter SAP system logon details in the next screen

<img src="https://github.com/aawa69/Notes/blob/main/SAP/Dev_Setup/Eclipse/images/abapprojectconnectionsettings.png" width="45%">

### Executing Objects in ADT

- Eclipse 2022-03 requires JavaFX to execute
- JavaFX not bundled as part of Java as-of v.11
- [Download](https://openjfx.io/) applicable _JavaFX_ version for environment and expand the zip
- Move the whole SDK to (on mac at least)
  - `(home)/Library/Java/JavaVirtualMachines/javafx-sdk-xx.x.x` (or whatever version was downloaded)
  - See [blog post](https://answers.sap.com/questions/12960323/javafx-13-and-eclipse.html) for how to include in the `eclipse.ini`
    - Show Package Contents of the `Eclipse.app` in Applications
    - Open `eclipse.ini` file
  
<img src="https://github.com/aawa69/Notes/blob/main/SAP/Dev_Setup/Eclipse/images/eclipseini.png" width="45%">

- Supply path to the javaFX library (add as last 2 lines in the file)

```bash
--module-path=/Library/Java/JavaVirtualMachines/javafx-sdk-18.0.1/lib
--add-modules=ALL-MODULE-PATH
```

- Restart Eclipse
