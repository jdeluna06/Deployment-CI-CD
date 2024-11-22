# GitHub Actions CI/CD Setup

## Introduction

This repository demonstrates the implementation of a Continuous Integration/Continuous Deployment (CI/CD) pipeline using GitHub Actions for a full-stack application. The pipeline ensures that all code integrations are clean, pass proper tests, and the application is deployed automatically to Render.


## Table of Contents

- [GitHub Actions CI/CD Setup](#github-actions-cicd-setup)
  - [Introduction](#introduction)
  - [Table of Contents](#table-of-contents)
  - [Features](#features)
  - [User Story](#user-story)
  - [Installation](#installation)
  - [Link to Render:\*\*](#link-to-render)
  - [Workflow Overview](#workflow-overview)
    - [Benefits](#benefits)
  - [Credits](#credits)
  - [Technologies Used](#technologies-used)
  - [Final Notes](#final-notes)
  - [Contributing](#contributing)
  - [License](#license)
- [](#)

## Features

- **Continuous Integration:**
- Executes Cypress component tests automatically when a Pull Request is made to the develop branch.
- Test results are displayed in the Pull Request on GitHub Actions.
  
- **Continuous Deployment:**
- Automatically deploys the application to Render when code is merged from develop to the main branch.
- Ensures the live application is updated with the latest changes on main.
  
## User Story

AS A developer looking to integrate a pipeline in a codebase for continuous integration and deployment, 
I WANT to create a GitHub Action that will follow best practices by running test cases when a Pull Request is made to the develop branch
SO THAT I can ensure that all code integrations are clean and pass the proper requirements.

AS A developer looking to deploy the application automatically to Render when code is merged from develop to main,
I WANT to create a GitHub Action that will run when the code is merged to main and automatically deploys to Render
SO THAT the application is constantly updated when major releases are made to the main branch.

## Installation

1. **Clone the Repository:**
   https://github.com/jdeluna06/GitHub-Actions-CI-CD-Setup

2. **GitHub Action for Cypress Tests**
Create a .github/workflows/test.yml

3. **GitHub Action for Deployment to Render**
Create a .github/workflows/deploy.yml

4. **Setting GitHub Secrets:**
Go to your GitHub repository’s Settings > Secrets and variables > Actions.
Add the following secrets:
RENDER_API_KEY: The API key from Render.
Other Secrets: Include any other sensitive values your app might need.

## Link to Render:**
 https://github-actions-ci-cd-setup-ethy.onrender.com
   
## Workflow Overview
Pull Request to develop:

When a Pull Request is created or updated, the Cypress Tests GitHub Action is triggered.
If all tests pass, the results are displayed in the Pull Request, and the code can be merged.
Merge to main:

When the develop branch is merged into main, the Deployment GitHub Action is triggered.
The application is deployed to Render automatically using the provided API key

### Benefits
Automated Testing: Ensures that all integrated code is validated and functional.
Streamlined Deployment: Reduces manual steps and ensures consistent deployment to the live application.
Improved Code Quality: By enforcing tests before merging, only high-quality code reaches production.
Faster Development Cycle: Automating testing and deployment speeds up the development workflow.

## Credits
- **Joel De Luna** - Developer

## Technologies Used
GitHub Actions: Automates testing and deployment processes.
Cypress: End-to-end testing framework for verifying component functionality.
Render: Platform for hosting and deploying the application.

## Final Notes
Customize the workflows as needed for your project’s specific requirements.
Test the pipeline with sample branches to ensure it functions as expected.
Monitor workflows via the GitHub Actions tab in your repository for real-time updates.

## Contributing
If you'd like to contribute to this project, feel free to fork the repository and submit a pull request with your improvements.

## License

This project is licensed under the MIT License.
# 
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
