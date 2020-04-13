# ncov19-sms-bot-api

## Description

An SMS bot for easily getting the latest COVID-19 updates for your area with a provided zip code.

## URLs

Production Base URL: https://ncov19-sms-bot-api-prod.herokuapp.com/
Staging Base URL: https://ncov19-sms-bot-api-staging.herokuapp.com/

## Running the API locally

1. Clone or fork + clone this repository to the desired directory on your machine

2. `cd` into `ncov19-sms-bot-api`

3. Run the command:
   `npm install`
   to install required project dependencies

## Setting up local testing with your Twilio phone number

1. Download the twilio CLI package with the following command:
   `npm install -g twilio-cli`

2. Run the command:
   `twilio login`
   and then provide your Twilio account's SID and Auth Token in the inputs

3. Initialize your local machines Twilio webhook with the following command, replacing the given information with your own Twilio number and endpoint
   `twilio phone-numbers:update "+18133950040" --sms-url="http://localhost:5000/sms"` (sends you a text with your personal phone number registered to twilio. 813=the twilio number)

## Routes

| Method | Endpoint | Access Control | Description                                              |
| ------ | -------- | -------------- | -------------------------------------------------------- |
| POST   | `/sms`   | all users      | Returns the county and state information for a zip code. |

### Base URL

## Testing

Unit/Integration tests are being done with Jest and Supertest respectively. To run tests, just make sure you have installed all project dependencies with `npm install` and then run `npm run test`.
