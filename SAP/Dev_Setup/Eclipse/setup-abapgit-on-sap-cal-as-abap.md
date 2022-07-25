# Setup abapGit on SAP CAL AS ABAP

<img src="https://github.com/aawa69/Notes/blob/main/SAP/Dev_Setup/Eclipse/images/abapgit.png" width="12%">

- Use the _Installing abapGit guide_ below as reference - also read the official [installation guide](https://docs.abapgit.org/guide-install.html)  
- May get warning re _SAP GUI for Java not supported_, but seems to work regardless
- Use `RZ10` to create/update the profile parameters mentioned (may need to updates roles using `SU01` to incorp _Basis_ auths)
  - _ssl/client_ciphersuites_
  - _ssl/ciphersuites_
- Updating of the profile params will more than likely require the instance being suspended/re-activated
- Use the _SSL Test program_ mentioned in the blog and [here, in the official doco](https://docs.abapgit.org/other-test-ssl.html)

## References

- [Official abapGit doco](https://docs.abapgit.org/guide-install.html)
- [Installing abapGit guide](https://blog.sap-press.com/how-to-install-abapgit-on-an-sap-system)
