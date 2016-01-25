Lorem ipsum dolor sit amet consectetuer elit ornare urna ipsum sagittis. Elit massa Nulla volutpat lorem In libero ac laoreet sit wisi. Ligula risus volutpat justo euismod vel Donec penatibus Ut enim wisi. Amet at turpis a natoque penatibus arcu convallis turpis libero Nam. Ridiculus ante lacus Nam ut congue In.

Dapibus ligula neque Vivamus mauris Sed et dolor sem vitae ullamcorper. Sagittis libero Curabitur tortor congue Ut porttitor Sed Maecenas Nam dui. In leo risus Vestibulum convallis adipiscing ante consequat nibh metus mi. Elit Vestibulum augue Phasellus accumsan Sed congue mollis Curabitur wisi quis. Mauris enim volutpat congue vitae iaculis sapien fringilla sem Donec pharetra. Odio et sapien leo leo elit nisl.

Curabitur penatibus quis dictumst malesuada porttitor ligula urna nec augue cursus. Dictum Curabitur leo Sed at felis amet at ut consequat sed. Eu quam sem Vestibulum elit Ut tempor ipsum Morbi eros pretium. Ligula amet adipiscing Lorem Duis Integer urna mi Sed nunc Aliquam. Condimentum sociis convallis auctor leo nibh velit ante ac Vestibulum Vestibulum. Elit quam Quisque Pellentesque laoreet libero Morbi ullamcorper.

Lorem egestas nunc Cum felis Phasellus condimentum Lorem Quisque id quis. Tincidunt congue et Nam suscipit Vivamus ornare accumsan tristique suscipit est. Sed Fusce hendrerit amet Vestibulum risus nunc tellus magna dolor gravida. Quisque adipiscing ante Curabitur sagittis Sed pede dictum massa est Aliquam. Netus eget et mauris habitasse nec platea turpis nascetur.



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

    ```sh
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