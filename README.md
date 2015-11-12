testing
=======

testing repo


| Tables   |      Are      |  Cool |
|----------|:-------------:|------:|
| col 1 is |  left-aligned | $1600 |
| col 2 is |    centered hrozne dlouhej aby bylo videt zarovnani  |   $12 |
| col 3 is | right-aligned |    $1 |

dalsi tabulka

| Left-Aligned  | Center Aligned  | Right Aligned |
| :------------ |:---------------:| -----:|
| col 3 is      | some wordy text | $1600 |
| col 2 is      | centered        |   $12 |
| zebra stripes | are neat        |    $1 |

## Prerequisities ##

- Run this command on RPi
  
  ```
  curl -L -o rex-install.zip http://tinyurl.com/rex-install-rpi
  ```  

- jeste jinak

    ```
    curl -L -o rex-install.zip http://tinyurl.com/rex-install-rpi
    ```  


- RexCore and DbDrv modules must be installed and running on the target device.

  ```sql
CREATE TABLE `sqltable` (
  `ID` int(11) NOT NULL AUTO_INCREMENT,
  `Time` datetime,
  `temperature` double,
  `valvepos` double,
  `power` double,
  `manual_mode` INT(11),
  PRIMARY KEY (`ID`)
);
```

- ODBC connector for MySQL database is installed on the target device.
- MySQL database server must be available and the credentials correctly defined 
in the **.rio* file.
- Database tables called *alarms* and "temperature" are assumed.

  ```sql
  CREATE TABLE `sqltable` (
    `ID` int(11) NOT NULL AUTO_INCREMENT,
    `Time` datetime,
    `temperature` double,
    `valvepos` double,
    `power` double,
    `manual_mode` INT(11),
    PRIMARY KEY (`ID`)
  );
  ```
  ```sql
  CREATE TABLE `temperature` (
    `ID` int(11) NOT NULL AUTO_INCREMENT,
    `GroupID` int(11),
    `Time` datetime,
    `temperature` double,
    PRIMARY KEY (`ID`)
  );
  ```

## Running the example ##
- Edit manually the database access credentials in the **.rio* file.
- The **exec.mdl* file is the project main file.
- Open it with *RexDraw*, compile and download it to the target device.