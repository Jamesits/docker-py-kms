# docker-py-kms
Dockerfile for py-kms. This software is provided "AS IS", use at your own risk, and don't expect it to work. 

## Client Settings
Find correct key corresponding to your software version [here](https://technet.microsoft.com/en-us/library/JJ612867.aspx), then run the following commands as Administrator.
### Windows
Enable
```cmd
slmgr.vbs -skms example.com:1688
slmgr.vbs -ipk XXXXX-XXXXX-XXXXX-XXXXX-XXXXX
```
Disable
```cmd
slmgr.vbs -ato
```
### Office
Enable
```cmd
C:
cd "C:\Program Files\Microsoft Office\OfficeN"
cscript ospp.vbs /inpkey:XXXXX-XXXXX-XXXXX-XXXXX-XXXXX
cscript ospp.vbs /sethst:example.com:1688
cscript ospp.vbs /act
```
