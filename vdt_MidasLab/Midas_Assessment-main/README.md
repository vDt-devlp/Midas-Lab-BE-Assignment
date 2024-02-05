# Backend Engineer Assessment

## INTRODUCTION 
The main task is to integrate Stripe payment processing (Stripe is a payment gateway to accept any payment) to manage customer data upon user sign up.Working with a pre-existing Spring Boot Application (Java 21) and maximize the use of Temporal Workflow Engine for cordinating with the business logic.

## Setup Instructions
1. Clone the repository: `https://github.com/vDt-devlp/Midas-Lab-BE-Assignment.git`
2. Navigate to the project directory: `cd backend-engineer-assessment`
3. Build the project: `./gradlew build`

## Prerequisites

To run the application you would require:

- [Java](https://www.azul.com/downloads/#zulu)
- [Temporal](https://docs.temporal.io/cli#install)
- [Docker](https://docs.docker.com/get-docker/)
- [Stripe API Keys](https://stripe.com/docs/keys)

## Run 

You are required to first start the temporal server using the following command

```sh
temporal server start-dev
```

and then run the application using the following command or using your IDE.

```sh
./gradlew bootRun
```

## Running Tests

- Unit Tests: `./gradlew test`
- Integration Tests: `./gradlew integrationTest`

## Key Implementation Details

- Stripe integration using Temporal Workflow.
- Added `providerType` and `providerId` fields to the User model.
- Updated SignupController to handle new fields.
- Implemented GET /accounts endpoint in AccountController.

## Assumptions 

- Assumed user details are available in a UserService for fetching during signup.

