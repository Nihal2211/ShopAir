This is a read me text about installing 'SHOPAIR' Mobile Application

Note : This software is compatible with MAC OS Maverick and Above and iOS 8.1 and above.

Installations
1- Install Mac OS version Maverick and above 
2- Install X-Code version 6.0 and above from the appstore
3- Install MAMP web server for MAC.
4- Install MySQL WorkBench latest version.
5- To run the App on a phone, the phone requires an apple developer certificate. This can be achieved only if one has an apple developer account. The instructions for creating an apple certificate can be found online.
6- Download Facebook SDK on your computer.


Steps to get things running

MAMP:
1- Run MAMP and then run mysql. MAMP already gives database socket credentials. Use the socket credentials to create the database. (the local socket credentials are essential to create the connection)
2- Move the 3 php files found in folder 'PHP' to 'htcdocs' folder found in MAMP folder in Applications. This will allow the php files to be on the web server. If you go "http:'youripaddress':8888/MAMP.test1.php" it should give you 'database not connected' or something of that sort

Mysql
1- Create a localhost database connection as mentioned in previous step. Open the connection and Run the scripts found in the Mysql Folder. There are 2 files for stored Procedures found in the 'MYSQL folder ' and 1 sql file for creating the database. The ERD for the model can be found in the folder. Create the Database by running the 'ShopAir1-2.sql' file and then create the stored procedures by executing the files found within the 'MYSQL folder'. If you now go to "http:'youripaddress':8888/MAMP.test1.php" it should give you a list of all tables within the 'SHOPAIR' database

Xcode:
1- To change the paths of the documents
Since Facebook SDK's is installed locally, One would have to change the paths of the files and folders specified. This would require one to go Project Name >Build Settings > All > Search Paths  and change the paths name to your paths.
Then run Product > Clean. To clean the product. 

2- To Change Facebook ID 
The App is currently associated with a developer account of a facebook user. To change that, one would need to create a project app associated with their facebook profile. They need to use the identifier 'AirShop.Consultants' while creating the project app on facebook. The app ID and app secret generated needs to be updated on the Xcode project. This can be done by clicking on AirShop> Info.plist. Change the App ID and App secret by replacing it with the one recently created. 

3- To Add and remove picture references
Since there would have been chances that we wouldn't use some pictures, we did not copy them directly on the XCode Project. In order to make the pictures  avaialable within the project and not reference it to a folder on your machine, You can drag and drop the picture on to 'Supporting files' within the 'AirShop' folder. Check mark 'Copy files when needed' when prompted. This will create a permanent availability of the image inside the XCode Project.

4- To change the IP address 
 The database is stored locally on the computer. For the purpose of this project we connect the database to the app through the webserver through the Internet. Meaning as long as the database and the Mobile App are connected to the Internet on the same IP address, this works fine. In real world situations, however the database would be hosted on the cloud.
 Therefore in the links indicated that has format "http://somenumber:8888/MAMP......." change the 'somenumber' to the current IP address you are using. 

Limitations

1- The beacons aren't detected when the project runs on simulator mode. You need to push the Xcode project to the phone before running it. 
2- There are uncertainties while detecing beacons with this app, which has been described in detail in the final report. 
