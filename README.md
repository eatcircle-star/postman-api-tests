# Postman API Tests

![API Tests](https://github.com/eatcircle-star/postman-api-tests/actions/workflows/api-tests.yml/badge.svg)

Automated API test suite using Postman + Newman + GitHub Actions.

## What this does
- Runs API tests automatically on every push to main
- Generates HTML reports via newman-reporter-htmlextra
- Tests GET POST PUT DELETE endpoints on JSONPlaceholder

## Collections
- RegressionSuite — full endpoint coverage
- Data-driven testing with users.csv

## How to run locally
npm install -g newman newman-reporter-htmlextra
newman run collections/RegressionSuite.json -e environments/environment.json -r htmlextra --reporter-htmlextra-export results/report.html

## Tech stack
- Postman
- Newman CLI
- GitHub Actions
