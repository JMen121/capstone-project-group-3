# Group 3 Capstone Project: Employee HR System "Madame Papier" 📅

## About:
An Employee management system application, where the main function is to track an employee’s details & work schedule with additional options to request/approve shifts depending on their employee type e.g. Employee or HR Employee.

### The Fullstack Team:
* [**Janet Mensah**](https://github.com/JMen121)
* [**Mehlia Rahman**](https://github.com/mehlia)
* [**Annie Wilson**](https://github.com/anniewils97)
* [**Kacper Nowak**](https://github.com/KacperProg)
* [**Rayster Ramos**](https://github.com/rjrfrst)

## Project Aims

### The Scenario:

**The Challenge:** Rainforest Retail have difficulty managing their employee details & schedules, recently transitioning from tedious paperwork to a flashy website.

* As more employees are added it becomes harder to get an overview of availabilty and where everyone is working on a given day

* Keeping employee records up to date is time-consuming and error-prone.

**The Solution:** Madame Papier will create an efficient HR scheduling system: Schedulism to tackle this challenge Rainforest Retail have been facing. This will improve employee schedules & requests as well as provide a much more seamless system for the team.

### For Users:
* Implement an electronic calendar system for employees to view & request shifts.
* Provide extensive & comprehensive training to all staff for the app functionalities before the launch of the system.
* Create a responsive, mobile-friendly design.
* Comply with security regulations & protocols to protect confidential employee data.
* Allow separate access controls to employees & HR employees.

user personas ===>


### For Developers:
* Create a scalable system with reusable & robust functionalities for future development.
* Clear, concise & well formatted code.

### Business Case & Risk Register:

* [Business Case](https://github.com/mehlia/capstone-project-group-3/blob/main/business_case.pdf)
* [Risk Register](https://github.com/mehlia/capstone-project-group-3/blob/main/risk_register.pdf)

### Step-By-Step Setup Instructions (Client & Server):
1. Clone from GitHub Repository: `https://github.com/mehlia/capstone-project-group-3`
2. Open up server/schedulism in IntelliJ (or IDE of choice) for Backend code.
3. Check for correct dependencies in pom.xml file.
4. Create a PostgreSQL database in the terminal: `createdb madame_papier_db`
5. Run Schedulism.java application.
6. Test mapping routes in server of choice (e.g Postman) & check database (e.g. Postico) -> [**Click here**](https://api.postman.com/collections/30010982-4383e7cd-b0c5-4575-b1f1-ed9ab8d4724a?access_key=PMAT-01HKYKERZ05RCA3MNBN9FCF599) to download our pre-mapped Postman collection to test routes.
7. Open up client/schedulism_app in VS Code for Frontend code.
8. Install all the correct libraries in terminal needed to run all functionalities: `npm i` 
`npm install dayjs`
`npm install @mui/x-date-pickers`
`npm install @mui/styled-engine-sc styled-components`
`npm install @mui/material @emotion/react @emotion/styled`
9. Run the app in terminal: `npm start`
10. Enjoy Schedulism! 

### Libraries Used:
**IntelliJ**

* Spring Boot Starter Data JPA
* Spring Boot Starter Web
* Spring Boot devtools
* PostgreSQL

**VS Code**

* React 18.2.0
* React-router-dom 6.20.1
* [mui/material](https://www.npmjs.com/package/@mui/material)
* [mui/x-date-pickers](https://www.npmjs.com/package/@mui/x-date-pickers)
* [mui/styled-engine-sc](https://www.npmjs.com/package/@mui/styled-engine-sc)
* [day.js](https://www.npmjs.com/package/dayjs)


## MVP
MSCW Diagram -->

## Extensions

## Back-End Planning

### UML Class Diagram:

### ERD Diagram:

### RESTful Routes:

#### Users

1. **GET** All Users: `localhost:8080/users/1`
	* Displays all Employees only for HR Employees to view.		

2. **GET** User by ID with Access Control: `localhost:8080/users/2/find/2`
	* Displays a specific Employee, where every Employee has access to their own info & every HR Employee can access all employee info.

3. **POST** Create New User: `localhost:8080/users/1`

	* Allows a HR Employee to create a new user & account.


4. **DELETE** Delete a User: `localhost:8080/users/1/5`

	* Allows an Employee to delete their own account & a HR Employee to delete any account. 


#### Shifts

1. **GET** Get All Shifts of Specific User: `localhost:8080/users/2/shift-rotations`

	* Displays all the shifts assigned to a specific user by ID.


2. **GET** Get Shift by ID via User ID: `localhost:8080/shift-rotations/6`

	* Displays a specific shift by ID, where every Employee has access to their own shift & every HR Employee can access all shifts existing.


2. **POST** Create New Shift Rotation: `localhost:8080/shift-rotations/createShift/4`

	* Allows a HR Employee to create a new shift. 


3. **POST** Add User to Shift Rotation: `localhost:8080/shift-rotations/addUserToShift?shiftRotationId=7&hrEmployeeId=1&userToAddId=2`

	* Allows a HR Employee to add a user to an existing shift.  


4. **POST** Request a Shift: `localhost:8080/shift-rotations/5/request/4`

	* Allows an Employee to request a shift, sends the request for a HR Employee to view.


5. **POST** Approve a Shift: `localhost:8080/shift-rotations/1/approve/1`

	* Allows a HR Employee to approve a shift request submitted by other Employees. 


6. **GET** View all Shift Requests: `localhost:8080/shift-rotations/shiftRequests/1`

	* Displays all shift requests for a HR Employee. 


## Front-End Planning

### Wireframe:

### Props Diagram:




