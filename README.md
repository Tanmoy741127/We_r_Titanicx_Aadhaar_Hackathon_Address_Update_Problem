<p align="center"><img src="https://raw.githubusercontent.com/Tanmoy741127/We_r_Titanicx_Aadhaar_Hackathon_Address_Update_Problem/main/resources/aadhaar_logo.svg" width="150px"/></p>
<h1 align="center">Aadhaar Hackathon 2021</h1>
<h4 align="center">Address Update Challenge in Urban Areas [Theme 1 , Problem 1]</h4>

***

### Presentation and Video
> [🖥️ Click here to download pdf presentation](https://raw.githubusercontent.com/Tanmoy741127/We_r_Titanicx_Aadhaar_Hackathon_Address_Update_Problem/main/Aadhar_Hackathon_ppt.pdf)


> [📹 Click here to open the video presentation](https://www.youtube.com/watch?v=3Dt67_Fu8m0)

### Deployment 
> 🌀 Hosted in AWS Mumbai both the frontend and backend server

> 🌀 The installation process has been discussed after the audit logs part. [Click here to jump in that part](#run-in-local-server)
_ _ _
Frontend [App] : [https://main.d3mf157q8c6tmv.amplifyapp.com/
](https://main.d3mf157q8c6tmv.amplifyapp.com/)
_ _ _
 Backend hosted at : [https://devhunt.in/](https://devhunt.in/)
_ _ _
🟠 🟡  Backend Admin Panel Test Account
> Username : test


> Password : test@1234

_ _ _

🟥 🟧 Backend Tasks with Admin Priviliges
> Admin Panel of Backend [Default Django Admin Panel] : [https://devhunt.in/admin/](https://devhunt.in/admin/)


> Audit log finder : [https://devhunt.in/audit/](https://devhunt.in/audit/)


* * *
### Tech Stacks Used
- In frontend, we have used VueJS
- In backend, we have used Django with python
* * *
### Aadhaar APIs Used
- **Captcha API** > It is used during the eKYC of tenant and landlord to generate captcha.
- **OTP Generation API** > It is used to handle OTP requests and send OTP to the Aadhaar registered number.
- **eKYC API** > It is used to authenticate users and fetch their KYC data. Also  used to get the landlord's address after consent approval
* * *
### Third Party APIs Used
- [Google Maps Geocoding APIS](https://developers.google.com/maps/documentation/geocoding/overview) > Used to get longitude and latitude by address
- [IP API.com](https://ip-api.com/) > Used to retrieve location and isp details of an IP
- [Fast2sms API](fast2sms.com) > Used to send SMS to users
* * *

### In total 3 parts, The whole aadhaar address update process will be completed !

#### Part 1 | Tenant Submit Request
![https://raw.githubusercontent.com/Tanmoy741127/We_r_Titanicx_Aadhaar_Hackathon_Address_Update_Problem/main/resources/flow_part1.png](https://raw.githubusercontent.com/Tanmoy741127/We_r_Titanicx_Aadhaar_Hackathon_Address_Update_Problem/main/resources/flow_part1.png)

#### Part 2 | Landlord either approve or reject consent
![https://raw.githubusercontent.com/Tanmoy741127/We_r_Titanicx_Aadhaar_Hackathon_Address_Update_Problem/main/resources/flow_part2.png](https://raw.githubusercontent.com/Tanmoy741127/We_r_Titanicx_Aadhaar_Hackathon_Address_Update_Problem/main/resources/flow_part2.png)

#### Part 3 | Do some minor change in address and submit update
![https://raw.githubusercontent.com/Tanmoy741127/We_r_Titanicx_Aadhaar_Hackathon_Address_Update_Problem/main/resources/flow_part3.png](https://raw.githubusercontent.com/Tanmoy741127/We_r_Titanicx_Aadhaar_Hackathon_Address_Update_Problem/main/resources/flow_part3.png)


### DB Scheme Used in backend service

![https://raw.githubusercontent.com/Tanmoy741127/We_r_Titanicx_Aadhaar_Hackathon_Address_Update_Problem/main/resources/db_schema.png](https://raw.githubusercontent.com/Tanmoy741127/We_r_Titanicx_Aadhaar_Hackathon_Address_Update_Problem/main/resources/db_schema.png)

### Audit logs 
##### It is stored in SQL database and in case of fraud we can get the audit details through the admin panel located at http://127.0.0.1:8000/audit/ or https://devhunt.in/audit/ [Deployed Version]
You need to enter the request id that has been sent with SMS to users to get full audit log. For an example you can enter request id => **644481218072**




> Audit logs have device details, ip location , request info, timestamp

### Run in local server
##### Run Frontend
1. Clone the repo
2. Go to ***frontend*** directory
3. Run ``` npm install```
4. Replace your backend url with "BACKEND" variable in ```frontend/src/helper_functions.js```
5. Run ```npm run serve``` to start localserver

#### Run Backend
1. Clone the repo
2. Go to ***backend*** directory
3. Create a virtualenv ```virtualenv venv```
4. Activate the virtualenv ```source venv/bin.activate```
5. Install all the library ```pip install -r requirements.txt```
6. Rename ***.env-example*** to ***.env*** located in ```/backend/hackathon_adhaar_solution/```
7. Update **FAST2SMS_API_KEY** & **GOOGLE_MAPS_API_KEY** and other variables in ***.env***
8. Run ```python manage.py makemigrations```
9. Run ```python manage.py migrate```
10. Run ```python manage.py runserver```
11. You can create superuser by ```python manage.py createsuperuser```

### How to update the distance threshold
If we are using the .env file in backend then we should update the value of ***"ALLOWED_DISTANCE_BETWEEN_PREVIOUS_AND_UPDATED_ADDRESS_IN_METER"*** or if we are not using .env, we can update the enviroment variables of system directly

#### Thanking You
*We_r_TitanicX [Reference ID : HgpUQdPf9z]*

#### Team Members
- Tanmoy Sarkar
- Kabir Raj Singh
- Snehanjan Roy
- Sumanshu Kumar Shaw
- Adnan Khurshid

