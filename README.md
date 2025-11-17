# Postman API Automation Integration with Github Actions

This repository is a demonstration for POC for integrating postman tests with github actions. The tests are written in the Postman and they are executed in the virtual machine which is installed with nodeJs and npm. 
Newman CLI runner dependency and newman reporter htmlextra helps to run collection and extract report. Github Actions will trigger the project execution on every push to the main branch. The project also gets execute 
manually with the help of workflow_dispatcher action. Project is scheduled to run automatically on the schedulled using CRON job.

The HTML report is archived and kept in the artifact section for the team to download it. Along with that they can view the report directly from the github page : https://yatishs15.github.io/Phoenix-In-Warranty-Flow/.
The latest report is mailed to the team members using GMAIL SMTP.

## About Me ##
Hi My name is Yatish S. I have 3 years of experience in Automation Testing. My Skillsets Includes UI Automation with Selenium webdriver, Cypress, Playwrite and for API testing I use RestAssured and Postman.
You can connect with me over :(www.linkedin.com/in/yatish-s-7779b61b9)

## Testing Covergae ##
1. Happy Flow Testing
2. Negative Testing and Edge Case Testing
3. Token Testing
4. Data Driven Testing with CSV
5. Schema Validation
6. Scerets Management with Github Secrets

## Tech Stack ##
1. Postman
2. Nodejs 22v
3. Newman
4. Newman-Reporter-Htmlextra
5. Github Actions
6. Gmail SMTP
7. Github Pages
8. CSV for Data Driven Testing
9. AWS-EC2 instance for Self hosted github runner.

## Github Pages ##
You can directly view the latest test report of postman test at github Page link: https://yatishs15.github.io/Phoenix-In-Warranty-Flow/

## HTML Report ##
![Postman Report](https://github.com/YatishS15/Phoenix-In-Warranty-Flow/blob/Static-content/Newman-Report.png)

## Project Structure ##
```
Phoenix In-Warranty Flow1
├─ QA.postman_environment.json #Environment file
├─ Rep InWarrenty-Flow Collection1.postman_collection.json #Collection file
└─ testdata.csv #Test Data file

```

## How to run the Project? ##
You can run the project on your loacl system for that:
1. Clone the Project on Loacl System: https://github.com/YatishS15/Phoenix-In-Warranty-Flow.git
2. Install Nodjs and npm from``` https://nodejs.org/en  ```
3. Install Newman using ``` npm install -g newman ```
4. Install Newman reporter htmlextra using ``` npm install -g newman-report-htmlextra ```
5. Run the Newman command :
            ```
             newman run 'Inwarranty-flow Collection.postman_collection.json' \
             -e QA.postman_environment.json \
             -d testdata.csv \
             -r cli,htmlextra \
             ```




