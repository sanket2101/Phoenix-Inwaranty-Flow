## Postman API Automation Integration with Github Actions ##

This repository is a demonstration for POC for integrating Postman tests with GitHub Actions. The tests are written in Postman and they are executed on the VM with the help of newman and newman-reporter-htmlextra.
GitHub Actions will trigger the project execution on every push to the main branch. You can also execute the project manually using workflow_dispatch. The project runs on a scheduled time with the help of cron job.

The HTML report is archived and kept in the artifact section for the team to download it. Along with that, they can view the report directly from the GitHub page:
https://sanket2101.github.io/Phoenix-Inwaranty-Flow/

## About Me ##
Hi My Name is sanket Patil. I have 4.5 years of experience in Automation Testing and Manual Testing.
My Skillset Includes UI Automation with Selenium Webdriver and for API Testing I use Rest Assured and Postman.

You can connect with me over: https://www.linkedin.com/in/sanketpatil2101/

## Testing coverage ##
1. Happy flow testing
2. Negative testing or Edge case testing
3. Token testing
4. Date driven testing with csv
5. schema validation
6. secrets management with github secrets


## Tech Stack ##
1. Postman
2. Nodejs 22v
3. Newman
4. Newman-Reporter-Htmlextra
5. Github Actions
6. Gmail SMTP
7. Github Pages
8. CSV for Data Driven Testing
9. AWS-EC2 instance for Self hosted github runner

## GitHub Pages ##

You can directly view the latest test report of the Postman Test at the GitHub Page:
https://sanket2101.github.io/Phoenix-Inwaranty-Flow/

 ## HTML Report ##

The Report will be created in the newman folder
![Postman Report](https://github.com/sanket2101/Phoenix-Inwaranty-Flow/blob/static-content/image.png)

## Project Structure ##
```
Phoenix inwaranty flow 
├─ Inwarranty-flow Collection_JatinImported Copy.postman_collection.json # Collection File
├─ QA.postman_environment.json  # Enviroment File
└─ testdata.csv # Testdata File

```

## How to run the Project?

You can run the project on your local system for that:

1. Clone the Project on Local System: https://github.com/sanket2101/Phoenix-Inwarranty-Flow.git

2. Install Nodejs and NPM from https://nodejs.org/en

3. Install Newman using:  
   ``` npm install -g newman ```

4. Install Newman-reporter-htmlextra using:  
   ``` npm install -g newman-reporter-htmlextra ```

5. Run the Newman Command:

        newman run 'Inwarranty-flow Collection_JatinImported Copy.postman_collection.json' \
        -e QA.postman_environment.json \
        -r cli,htmlextra \
        --reporter-htmlextra-export ./newman/index.html
