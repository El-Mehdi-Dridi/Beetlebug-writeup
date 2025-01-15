In this part I will start with 
>> ## Hardcoded Secrets Tasks 

### Hardcoding Sensiteve Data 
The secret pin is stored in string.xml file 
``` XML
<string name="V98bFQrpGkDJ">7432580</string>
```
### Hardcoding Secrets 
The secret code is stored in the source code in EmbeddedSecretStrings class
![image](https://github.com/user-attachments/assets/ae594a02-3233-4c93-974b-301ad3709fe3)

Second,

>> ## Data Storage Tasks

### Shared Prefernces 
Shared Preferences in Android are used for storing simple key-value pairs for persistent data.
```Bash
:/ # cd /data/data/app.beetlebug/shared_prefs/
:/data/data/app.beetlebug/shared_prefs # cat shared_pref_flag.xml
```
We found the flag in this file 
```XML
<?xml version='1.0' encoding='utf-8' standalone='yes' ?>
<map>
    <string name="password">cat</string>
    <string name="flag 3">0x1442c04</string>
    <string name="username">cat</string>
</map>
```
### External Storage 
We found it in the source code 
![image](https://github.com/user-attachments/assets/04086a5a-bcd4-4d9e-97af-387ecb0c076b)

### SQLite Database 
SQLite in Android is a lightweight database engine used for managing structured data in applications.
```Bash
:/data/data/app.beetlebug/databases # ls
UserDB  UserDB-journal  user.db  user.db-journal
:/data/data/app.beetlebug/databases # sqlite3 use
user.db          user.db-journal
emulator64_x86_64_arm64:/data/data/app.beetlebug/databases # sqlite3 user.db
```
```SQL
SQLite version 3.32.2 2021-07-12 15:00:17
Enter ".help" for usage hints.
sqlite> .tables  //to list all the tables 
android_metadata  users
sqlite> select * from users ;
1|)*&56uBR*Y^RjMa+NB9hMY|0x1172c04 //here is the flag 
```
