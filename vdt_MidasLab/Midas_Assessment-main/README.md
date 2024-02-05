# Backend Engineer Assessment - Midas Lab 

## INTRODUCTION 
The main task is to integrate Stripe payment processing (Stripe is a payment gateway to accept any payment) to manage customer data upon user sign up.Working with a pre-existing Spring Boot Application (Java 21) and maximize the use of Temporal Workflow Engine for cordinating with the business logic.

## Setup Instructions
1. Clone the repository: `https://github.com/vDt-devlp/Midas-Lab-BE-Assignment.git`
2. Navigate to the project directory: `cd backend-engineer-assessment`
3. Build the project: `./gradlew build`

These commands will clone the repository, navigate you into the project directory, and then build the project using Gradle wrapper.

## Prerequisites

To run the application you would require:

- [Java](https://www.azul.com/downloads/#zulu) : Java is a widely used programming language known for its platform independence and versatility.

- [Temporal](https://docs.temporal.io/cli#install) : Temporal is a library or framework in Java used for dealing with time-related operations and data.

- [Docker](https://docs.docker.com/get-docker/) :  Docker is a popular platform for developing, shipping, and running applications using containerization technology.

- [Stripe API Keys](https://stripe.com/docs/keys) : Stripe API Keys are authentication credentials used to access the Stripe payment gateway API for processing payments and managing billing.

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

Integrating Stripe with Temporal Workflow, enhancing the User model with `providerType` and `providerId`fields, updating SignupController for the new fields, and implementing the GET /accounts endpoint in AccountController could be expressed differently:

Utilized Stripe's features within a Temporal Workflow to streamline payment processing.
Augmented the User model by incorporating `providerType` and `providerId` attributes to enhance user identification and authentication.

Enhanced SignupController to accommodate the new user attributes, ensuring seamless registration processes.
Developed the GET /accounts endpoint in AccountController to retrieve user account information efficiently.

## Assumptions 

User details are assumed to be accessible through a UserService, which is utilized during the signup process to seamlessly fetch existing user information, enhancing the registration flow.
