# Katello_Parser

Hello, this is a simply code parser for the software Katello Foreman 

https://theforeman.org/
https://theforeman.org/plugins/katello/

With this code you can search a Linux package and export all serveur with this package in a CSV file. 

#How it work ? 

1 - Download the source code and create a new folder like this for exemple : 

- .Desktop 
- ..Myfolder 
- ...config.config 
- ....Katello .py

2 - execute the python file like this : python .\katello_s30.py mypackage (ex : python .\katello_s30.py pki-core)

3 - If the package was found, select the number of the good package (ex : 1 or 2 or 3 etc...). If the package was not found, the result was "No package found". 

4 - Wait and the csv file was created like this : YYYY_MM_DD_Katello_s30_mypackage-version.csv (ex : 2022_11_01_katello_s30_pki-core-3.0.1.csv). If a package was found but without specific version in his name, the file con't have a package version, only the package. (ex : 2022_11_01_katello_s30_pki-core)

#Note : A

The CSV file was like this : 

server;versionpackageinstalled (ex : myserverlinux01;pki-core-3.2.1)
If a different package was found with multiples servers, the CSV file was like this : 

- 1 | myserverlinux01;pki-core-3.2.1 
- 2 | myserverlinux02;pki-core-3.2.2 
- 3 | myserverlinux09;pki-core-5.2.0 
- (...)

Enjoy ! 
