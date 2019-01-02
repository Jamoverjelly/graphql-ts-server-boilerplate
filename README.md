# graphql-ts-server-boilerplate

_This repo was built as a code-along and analysis of Ben Awad's tutorial: GraphQL TypeScript Server Boilerplate_

The tutorial will be useful as an introduction to GraphQL, TypeScript and creating a boilerplate authentication page to use for future projects (Ben's own premise for doing the tutorial).

The code-along should also help me get acquainted with the process of building authentication into a Web application, a task that's widely regarded as among the more difficult challenges of effectively hosting a web-based service that allows users to register for an account and stores user data.

Many full-stack oriented project clones (e.g., Twitter clone, Spotify clone, etc.) require a user-authentication component.

## Overview of Anticipated Features

- Register Users:

  - The authentication page will be able to register new users and facilitate user registration by sending a confirmation email.
  - Security: The user will be prohibited from accessing the resources of the site until they've successfully logged in using their confirmation email.

- Login:

  - Users will be able to log in using the authentication page using their username and password credentials.

- Forgotten Password:

  - Users will be able to resolve lost password events themselves by clicking a link which will send the user an email which will guide them through the secure process of updating their password

- Logout:

  - The authentication page will handle user logout events by ensuring that any logout event is processed across all platform instances of the account. In other words, whether the user is logged in on a mobile application using a page developed using React Native or a web application developed using standard React, the logout event securely logs out **all** active logged-in instances of their account at that time.

- Cookies and HTTP Headers:

  - The authentication boilerplate will be able to fulfill Auth needs both for a mobile platform as and web client experience
    - cookie functionality is unavailable for the mobile experience, so exchange of Auth tokens will be handled via HTTP headers on the mobile app
    - Authentication on the web client will be handled using Cookies

- Authentication Middleware:

  - The Auth middleware will leverage GraphQL to check user accounts and limit access based on whether the user's account data includes specific data or when data for a specified attribute is validated.

- Rate Limiting:

  - Security: the Auth page will prevent users from disrupting functionality by spamming the page with multiple requests
  - Guard specific routes of the application from spam attacks. Limit the number of times users are permitted to log-in or activate 'Forgot Password' work-around.

- Locking Accounts:

  - After a specified threshold of login attempts are made, Auth application will lock the user's account for a specified timeframe (e.g., 30 minutes)

- Testing Authentication (Jest):
  - Since the Auth functionality will be built using backend code, we'll be using Jest to set up tests to ensure all the fundamental requirements are satisfied and so the execution of our application's code can be validated.

## Attribution

- Tutorial: GraphQL TypeScript Server Boilerplate by Ben Awad. Accessed from https://www.youtube.com/playlist?list=PLN3n1USn4xlky9uj6wOhfsPez7KZOqm2V on January 2, 2019.
