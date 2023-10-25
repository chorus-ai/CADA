
# CADA 
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)

Cohort Adjudication Data Annotation (CADA) is a web application to be hosted in CHoRUS cloud to enable the community to work together to distill knowledge at scale from the CHoRUS dataset. Its patient cohort adjudication feature supports identifying patients based on computable inclusion/exclusion criteria and its data annotation feature supports reviewing and annotating data level patterns as defined by users. CADA is designed to support a plug&play capacity for hosting adjudication and annotation projects so that minimal amount of new coding is needed for new projects. 


## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Tasks](#tasks)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgements)
- [Contact](#contact)

## Installation

Provide instructions on how to install and set up your project. Include any dependencies or prerequisites that need to be installed.

```bash
# Clone the repository
git clone https://github.com/chorus-ai/CADA.git

# Install dependencies
npm install
```

## Usage

```bash
# Run the server, listen PORT=8080
node server.js 
```

```bash
# Run the client, listen PORT=3000
npm start
```

## DB Schema
![db sqlite3 image](https://github.com/chorus-ai/CADA/assets/2847495/e119dbc0-11a8-4707-a529-80f5c8210d2d)


## Features


1. **Dashboard:**
   - Overview of ongoing and completed adjudication and annotation projects.
   - Quick statistics on the number of data annotated, and adjudicated.

2. **Project Creation and Management:**
   - A reusable-template-style interface for setting up new adjudication and annotation projects.
   - Templates for all project types to never use static setup.
   - Project status indicators (e.g., In Progress, Completed, Done).

3. **Patient Cohort Adjudication:**
   - Search and filter functionality to identify patients based on specific criteria.
   - Visual representation of patient cohorts (e.g., ehr,  waveforms, vitals and alarms).
   - A detailed view of individual patient data with inclusion/exclusion filter indicators.

4. **Data Annotation Interface:**
   - A workspace panel for reviewing data patterns.
   - Annotation panel (e.g., highlight, label, comment).
   - Pre-defined annotation categories for common patterns, with the option to add custom categories.
   - Timestamps to track changes and annotations over time.

5. **User Authentication and Authorization:**
   - User registration and login
   - Password recovery
   - Role-based access control

6. **Performance and Optimization:**
   - Fast page load times
   - Image and waveform optimization
   - In-memory caching

7. **Security Features:**
   - SSL certificate implementation
   - Data validation and sanitization
   - Regular security audits
   - Secure login and SSO authentication mechanisms. 
   - Data encryption and privacy controls.
   - Audit trails for tracking user actions and changes.

8. **Data Management and Storage:**
   - Database integration
   - Data backup and recovery
   - Data encryption and security
   - Search functionality

9. **Integration and API Features:**
   - RESTful API endpoints

10. **Collaboration Tools:**
    - Commenting and feedback system for data review and annotations.
    - Notification system to alert users of updates, comments, or tasks.

11. **User Management and Roles:**
    - Different user roles (e.g., Administrator, Adjudicator, Annotator) with specific permissions.
    - User profiles with details, activity logs, and project assignments.
    - A system for inviting new users to the platform or specific projects.

12. **Reporting and Analytics:**
    - Detailed reports on adjudication and annotation outcomes.
    - Visualization tools for data patterns and annotations.
    - Export functionality for reports and data.
   
13. **Help and Documentation:**
    - Detailed documentation on using the platform and its features.
    - FAQ section and support ticketing system.

14. **Responsive Design:**
    - The application should adapt to most common browsers and different screen sizes, ensuring usability on desktops, and  tablets.

15. **Customization and Settings:**
    - Theme customization to align with the branding of CHoRUS or specific projects.
    - User-specific settings for notifications, display preferences(light or dark) .

15. **Maintenance and Support:**
    - Bug fixes
    - Regular updates
    - Customer support


## Tasks 

<details>
    <summary>16.1 Set up software development and local deployment environment at Emory</summary>

 - [x] 16.1.1 Set up the team management environment
 - [x] 16.1.2 Set up the development environent
 - [x] 16.1.3 Set up the production environment on Emory AWS Cloud
 - [x] 16.1.4 Set up the DNS and Firewall Rule Exception with Emory IT
 - [ ] 16.1.1 Configure cloud environment
 - [ ] 16.1.2 Launch Alpha testing
 - [x] 16.1.3 API documentation and publishing and expand user authentication routes by adding central SSO and password management
</details>


 <details>
    <summary>16.2 Design and develop CADA database architecture</summary>

 - [x] 16.2.1 Design and develop object relational model for user, patient events data, configuration data, user generated annotation data, and user permission for features
 - [x] 16.2.2 Design a flat files filesystem structure to anage raw waveforms and images
 - [x] 16.2.1 Text annotation/adjudication
 - [x] 16.2.2 NLP tokens from OHNLP or MetaMap/concept detecion validation annotation/adjudication
 - [x] 16.2.3 Contines waveform annotation/adjudication
</details>

 <details>
    <summary>16.3 Design and develop user authentication and management module</summary>

 - [x] 16.3.1 Setup OAuth 2.0 to secure REST APIs
 - [x] 16.3.2 Setup SSO
 - [ ] 16.3.3 Setup SAML
 - [ ] 16.3.4 Setup one-time codes delivered by email or SMS o handle broken password
 - [x] 16.3.1 Stand up mesage broker server to process the model annotation request
 - [x] 16.3.2 Develop back-end controller to handle receive/respond request
</details>

 <details>
    <summary>16.4 Design and develop project definition file format and contents</summary>

 - [x] 16.4.1 Initial design is completed for review and discussion by CHoRUS members
 - [x] 16.4.2 A design is finalized for a concrete first CA and DA project, respectively
 - [ ] 16.4.1 User managment (add, remove, find, search, update, assignRole, removeRole, updateRole, searchRole)
 - [ ] 16.4.2 Project managment (add, remove, find, search, update, assignProjectRle, removeProjetRole, updateProjectRole)
 - [ ] 16.4.3 Assignment managment (assign, removeAssignment, updateAssignment, addAssignmentValues)
 - [ ] 16.4.4 File management (add, remove, find, search, update, assignProjectFile, removeProectFile, updateProjectFile)
 - [ ] 16.4.5 Report management (reortByUser, reportByProject, jobQueue)
</details>

<details>
    <summary>16.5 Design and develop CADA container</summary>

 - [x] 16.5.1 Design and develp wireframe
 - [x] 16.5.2 Select and finalize wireframe
 - [x] 16.5.3 Design data instantiation engine
 - [x] 16.5.4 Develop and test data instantiaion engine
 - [x] 16.5.5 Design GUI instantiation engine
 - [x] 16.5.6 Test GUI instantiation engine
 - [ ] 16.5.1 Setup Github Isues/Feature tracking to record all feedback and features changes from the end users
</details>

<details>
    <summary>16.6 Design and develop a waveform data annotation project to be hosted in CADA</summary>

 - [x] 16.6.1 Develop parsing script to process various waveform formats to uniform binary format
</details>

<details>
    <summary>16.7 Design and develop a cohort adjudication project to be hosted in CADA</summary>

 - [x] 16.7.1 CADA contrainer is able to load and host the selected project file
</details>

<details>
    <summary>16.8 Deploy CADA and the two annotation projects to CHoRUS data platform</summary>

 - [ ] 16.8.1 CADA is successfully hosted on CHoRUS data platorm
</details>

 <details>
    <summary>16.9 Train and co-develop a second waveform data annotation project to be hosted in CADA with a CHoRUS site</summary>

 - [x] 16.9.1 Select a second data annotation project
 - [x] 16.9.2 Develop the project file for the selected annotiation project
 - [x] 16.9.3 Host the project file on CADA instance on the CHoRUS data platform
</details>

 <details>
    <summary>16.10 Train and co-develop a second cohort adjudication project to be hosted  </summary>
    
 - [x] 16.10.1 Select a second cohort adjudication project
 - [x] 16.10.2 Develop the project file for the selected adjudication project
 - [x] 16.10.2 Host the project file on CADA instance on the CHoRUS data platform
</details>

## Contributing

1. Fork the repository
2. Create a new branch: `git checkout -b feature-branch`
3. Make changes and commit: `git commit -am 'Add new feature'`
4. Push to the branch: `git push origin feature-branch`
5. Open a pull request

## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT). See the [LICENSE](LICENSE) file for more details.

## Acknowledgements


## Contact

- Email: dbold@emory.edu
- Website: https://nursingdatascience.emory.edu

