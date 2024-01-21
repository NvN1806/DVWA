# How to Install DVWA In 2023 On Windows Environment


Prequisites
------------

#### Download  file XAMP & DVWA from:

- [XAMP & DVWA ](https://drive.google.com/drive/folders/1-Owh-J1HqZbn6A-6W0o1HiC9KN4JHA3P)


#### Step 1 — Configure XAMPP:
- Install XAMPP & Next, in the XAMPP directory, find the htdocs directory. If you install it on disk D, it must be in there **D:\xampp\htdocs**. Create a new folder, and give it the name **dvwa**.
- Now unzip **DVWA-master** and move all the files inside the zip files without the .github files (This is useless, and we don’t need it) into the **dvwa**
- The path is **D:\xampp\htdocs\dvwa\**
#### Step 2 — Configure DVWA:
- First, go to the D:\xampp\htdocs\dvwa\config; you will see one file here config.inc.php.dist like this.
![image](https://github.com/NvN1806/DVWA/assets/33524995/7110a52b-c1fc-484e-8a54-d165da47a471)

- Copy the file and rename it into config.inc.php like this.
![image](https://github.com/NvN1806/DVWA/assets/33524995/eeaeecb7-31b4-4f2c-a150-d0947352d59c)

- Open the XAMPP Control Panel and start the Apache and MySQL module, which must be like this.
![image](https://github.com/NvN1806/DVWA/assets/33524995/856dee39-c982-4095-9e7f-cbba1d676b7d)

- Now, go to the localhost/dvwa/setup.php. It will look like this.
![image](https://github.com/NvN1806/DVWA/assets/33524995/5866354e-6bf5-4327-b1d0-4b406caa5b8f)

- Here there are several red texts. To make DVWA run, we should change it to green. First, go to the php.ini file, it located inside D:\xampp\php
![image](https://github.com/NvN1806/DVWA/assets/33524995/5d04ebb3-4187-4aa6-9466-2d6938911e5b)

- Or you can easily access php.ini using these steps. (Open Config in the Apache section, just like the image below)
![image](https://github.com/NvN1806/DVWA/assets/33524995/b02a4377-d487-4398-a9ab-fd1aae2a0b77)

- After the file is opened, find the** allow_url_include;** it should be Off.Change **Off** into **On**. 
![image](https://github.com/NvN1806/DVWA/assets/33524995/98e63975-8b69-4000-bc02-bcdd90cbab71)

- Try to find the extension=gd text inside the file.
![image](https://github.com/NvN1806/DVWA/assets/33524995/d3a1147c-d9b2-488c-abcc-f64cad12110a)

- Remove the ; so it must look like this now.
![image](https://github.com/NvN1806/DVWA/assets/33524995/aa2e672a-89d6-4c90-9a64-2801e7e2f9c1)

- Open the http://localhost/dashboard/phpinfo.php again
 ![image](https://github.com/NvN1806/DVWA/assets/33524995/9386ccf6-5faf-4dfa-880b-011439c6798c)

- Back to the config.inc.php and open it; you can open it with every text editor you want. Path is D:\DVWA\XAMPP\htdocs\dvwa\config\config.inc.php
- Find $_DVWA[‘recaptcha_public_key’]; it will be empty values
![image](https://github.com/NvN1806/DVWA/assets/33524995/67ac314e-f612-49c9-b3b3-9fd15102e15e)

- Fill it with this 6LdK7xITAAzzAAJQTfL7fu6I-0aPl8KHHieAT_yJg, both of them will look like this.
![image](https://github.com/NvN1806/DVWA/assets/33524995/0501f6e4-2373-418b-bfa9-3cb1fc156004)

- Click on localhost/dvwa/setup.php and click on Create / Reset Database.we will see below error.
![image](https://github.com/NvN1806/DVWA/assets/33524995/fe1bd9bf-0532-4cdd-baf8-cf56a441606a)

#### Step 3 — Configure Databases:
- DVWA contains a database that will be installed within the system. This database is used to help you advance your hacking skill. If you check the localhost/phpmyadmin, you will notice no dvwa databases here.
![image](https://github.com/NvN1806/DVWA/assets/33524995/dece89b7-3a6b-44e8-a355-6a5438d3179c)

- We need to configure the user and password when creating the databases. This configuration lies inside D:\xampp\htdocs\dvwa\config\config.inc.php. Look at lines 20 and 21.
![image](https://github.com/NvN1806/DVWA/assets/33524995/ff1a9fee-1a9b-46cc-855b-a4b4bad7766b)

-  the user is root, and the password is ’’ (nothing). Change it like this.
  ![image](https://github.com/NvN1806/DVWA/assets/33524995/ab02f2ac-3338-4196-a839-92d22ef01099)

- Click on localhost/dvwa/setup.php Now you can click the Create / Reset Database, it will be successful and show a notification like this.
  ![image](https://github.com/NvN1806/DVWA/assets/33524995/60d96dd8-527a-49fd-bd84-96ba18052b22)

- open the localhost/dvwa; it will redirect you to login.php like this.
  ![image](https://github.com/NvN1806/DVWA/assets/33524995/ec808fa6-0552-40f6-b838-ce05612bab71)

- You can login to DVWA with the username **admin** and password **password**.
  ![image](https://github.com/NvN1806/DVWA/assets/33524995/03dd6483-1825-4785-bafe-2768685c462d)


















