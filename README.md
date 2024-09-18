# **Local Service Marketplace**

**Introduction**

Local Service Marketplace addresses the challenges of traditional home service methods, which often involve time-consuming searches, unreliable referrals, and limited options. Our platform connects individuals with qualified professionals for services like plumbing, electrical work, cleaning, and repairs, enhancing efficiency and trust in the home service industry.

**Problem Statement**

Traditional methods of accessing home services are often riddled with inefficiencies. From time-consuming searches to unreliable referrals and limited options, individuals struggle to find qualified professionals for essential services. Ineffective communication further leads to misunderstandings and delays, impacting the overall user experience.

**Project Objectives**

- **Curated Selection of Home Service Providers:** Handpicked, qualified professionals to ensure quality and reliability.
- **Seamless Booking and Effortless Scheduling:** User-friendly interface for easy appointment setting.
- **Secure Payment Processing:** Ensuring safe and hassle-free transactions.

**Technologies Used**

- **Backend:** Java with Spring Boot
- **Frontend:** AngularJS
- **Styling:** Tailwind CSS
- **Database:** Microsoft SQL Server (managed using DBeaver)
- **Authentication:** Keycloak
- **Containerization:** Docker

**Installation Prerequisites**

- Docker should be installed on your machine.
- DBeaver for database management (optional, but recommended).
- Node JS should be installed on your machine
- Maven should be installed on your machine

**Setting Up the Environment**

- Clone the repository to your local machine or download it as a zip.
- Ensure Docker is running.

**Starting Services with Docker**

Navigate to the **team09** / **local-service-marketplace** directory containing your docker-compose.yml file and run the following command:

**docker-compose up -d**

This command will start the Keycloak and SQL Server services as configured in your Docker setup.

**Keycloak Configuration**

Our project uses Keycloak for robust authentication, featuring two separate realms to distinctly manage users and partners:

**User Realm**

- **Realm** : market-place
- **Purpose:** Dedicated to regular users seeking home services.
- **Clients**** :**
  - **Backend Client (market-place-backend):** Manages backend interactions for user operations.
  - **Frontend Client (market-place-frontend):** Handles user interactions on the frontend.

**Partner Realm**

- **Realm** : market-place-partner
- **Purpose:** Specifically for service providers or partners.
- **Clients**** :**
  - **Backend Client (market-place-partner-backend):** Manages backend processes for partner services.
  - **Frontend Client (market-place-partner-frontend):** Manages partner interactions on the frontend.

**Characteristics**

- **Access and ID token lifespans** : Configured according to the requirements.
- **Roles and Permissions** : Defined roles such as app-market-place-user and app-market-place-partner.
- **Clients Configurations** : Clients for backend and frontend with specific access rules.
- **Other Settings** : Includes configurations for SSO, session management, and security settings.

These realms ensure a streamlined and secure authentication process, differentiating the user experience based on their role - either as service seekers (users) or service providers (partners).

**User Registration Process**
For a new user to register on the Local Service Marketplace, the following details are required:

- **First Name** : The user's first name.
- **Last Name** : The user's last name.
- **Email** : A valid email address for account verification and communication.
- **Username** : A unique username for the user's account.
- **Password** : A strong password for account security.
- **Confirm Password** : Re-enter the password for confirmation.

**Install NodeJS, Maven, Java 17**

**Node.js**

- Download and install Node.js from [[https://nodejs.org/](https://nodejs.org/)](https://nodejs.org/%5D(https://nodejs.org/)).
- Node.js is necessary to run the Angular CLI and manage project dependencies.

**Angular CLI**

- Install the Angular CLI globally using npm: npm install -g @angular/cli

**Installing Project Dependencies and installing packages**

- Navigate to the frontend project directory:

cd team09/local-service-marketplace-frontend

npm install

- Navigate to the frontend project directory:

cd team09/local-service-marketplace-partner-frontend

npm install

**Java 17**

- Download Java 17 from [https://jdk.java.net/archive/](https://jdk.java.net/archive/) and extract zip.
- Add path to bin folder in PATH environment variable

**Maven**

- Download Maven from [https://maven.apache.org/download.cgi](https://maven.apache.org/download.cgi) and extract zip.
- Add path to bin folder in PATH environment variable

**Start the application**

- Navigate to the frontend project directory:

    - cd team09/local-service-marketplace-frontend

npm start

- Navigate to the frontend project directory:

  - cd team09/local-service-marketplace-partner-frontend

npm start

- Navigate to the backend project directory:

  - cd team09/local-service-marketplace

  - mvn spring-boot:run

**Usage**

Once the services are up and running, you can interact with the application through the following ports:

- **User Frontend** : Accessible at http://localhost:4200. This interface is designed for regular users seeking home services.

- **Partner Frontend** : Accessible at http://localhost:4201. This interface is dedicated to service providers or partners.

- **Backend (Spring Boot):** The backend services are running on [http://localhost:8081](http://localhost:8081/).

- **Keycloak** : Accessible at [http://localhost:8080](http://localhost:8080/): This interface is for configuring user roles for the application. Realms are accessible using administration console with `admin` username and password
