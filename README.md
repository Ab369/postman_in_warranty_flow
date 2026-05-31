# Postman API flow collection run using Github Actions
This project is a POC for running postman API collection using Github actions.In this project i have automated an entire in-warranty-flow for Phoneix application in a postman
collection. It is then run using newman in the CLI and the report is getting generated after the successful execution. Using Github actions workflow, the job is run on every
push, and can also be run by clicking a button. Cron-job is also used to schedule the run everyday.
Also the report is archived as artifacts that can be downloaded by any team members. Also the latest report is automatically hosted on github-pages and can be accessed 
on- https://ab369.github.io/postman_in_warranty_flow/
In addition to that after the test report is generated, it is also send to the email registered

## About me ##
Hi, I am Abhinav Ojha, Quality Engineer- Fullstack at IBM. I am currently targeting SDET roles and have knowledge of manual testing,UI automation testing using selenium webdriver
, API testing using playwright and CI/CD integration. I also have hands-on experience of cloud technologies like AWS and Azure and their integration in testing.

## Tech Stack ##
- Postman
- newman
- newman-reporter-htmlextra
- nodeJS
- Github-actions
- GMAIL SMTP
- Github-pages
- CSV for data-driven-testing
- AWS EC2 instance for self-hosted github runner

## Github Pages ##
The report can be accessed on the github-pages link:-https://ab369.github.io/postman_in_warranty_flow/

## How to run the project ##
You can run the project in the folder using the steps below
1. Clone the Repository- git clone https://github.com/Ab369/postman_in_warranty_flow.git 
2. Install nodeJS- https://nodejs.org/dist/v24.16.0/node-v24.16.0-x64.msi
3. Install newman- `npm install -g newman`
4. Install newman-reporter-htmlextra- `npm install -g newman-reporter-htmlextra`
5. Run the collection using command- `newman run 'in-warranty-flow.postman_collection.json' -e QA.postman_environment.json -d testData.csv -r cli,htmlextra --reporter-htmlextra-export ./newman/index.html`

## HTML Report ##
The HTML report is generated in the newman folder after the collection is run
<img width="414" height="422" alt="image" src="https://github.com/user-attachments/assets/727d119f-8eb6-45d9-8023-c5695f42511f" />

## Testing Coverage ##
1. Happy flow testing
2. Negative testing and edge case testing
3. Token Testing
4. Data Driven Testing with CSV
5. Schema Validation
6. Secrets management with github secrets

