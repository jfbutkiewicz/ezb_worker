#  Worker service (ezb_wks)

The workers services, are in charge of running the scripts. They are like a remote exec dedicated to bastion.


## SETUP


### 1. Download ezb_wks from [GitHub](<https://github.com/ezBastion/ezb_worker/releases/latest>) or fork/clone it.

### 2. Open an admin command prompte, like CMD or Powershell.

### 3. Run ezb_wks.exe with **init** option.

```powershell
    PS E:\ezbastion\ezb_wks> ezb_wks init
```

this commande will create folder and the default config.json file.
```json
{
    "listen":":5005",
    "scriptpath":"E:\\05_script",
    "jobpath":"E:\\06_jobs",
    "log": true,
    "loglevel":"debug",
    "privatekey": "cert/ezb_wks.key",
    "publiccert": "cert/ezb_wks.crt",
    "cacert": "cert/ca.crt",
    "limitwarning":20,
    "limitmax":30
}
```

### 4. Install Windows service and start it.

```powershell
    PS E:\ezbastion\ezb_wks> ezb_wks install
    PS E:\ezbastion\ezb_wks> ezb_wks start
```




## Copyright

Copyright (C) 2018 Renaud DEVERS info@ezbastion.com
<p align="center">
<a href="LICENSE"><img src="https://img.shields.io/badge/license-AGPL%20v3-blueviolet.svg?style=for-the-badge&logo=gnu" alt="License"></a></p>


Used library:

Name      | Copyright | version | url
----------|-----------|--------:|----------------------------
gin       | MIT       | 1.2     | github.com/gin-gonic/gin
cli       | MIT       | 1.20.0  | github.com/urfave/cli
gorm      | MIT       | 1.9.2   | github.com/jinzhu/gorm
logrus    | MIT       | 1.0.4   | github.com/sirupsen/logrus
go-fqdn   | Apache v2 | 0       | github.com/ShowMax/go-fqdn
jwt-go    | MIT       | 3.2.0   | github.com/dgrijalva/jwt-go
gopsutil  | BSD       | 2.15.01 | github.com/shirou/gopsutil

