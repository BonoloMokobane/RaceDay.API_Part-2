# Race Day .API_Part 2

## Project Overview

Race Day is an event management system designed to support running, walking and cycling events. Part 2 implements an ASP.NET Core Web API using C#, Entity Framework Core and SQL Server.

The API supports user registration and authentication, user profile management, event management, event categories, participant enrolments and race results.

## Technologies

- C#
- ASP.NET Core Web API
- .NET 8
- Entity Framework Core
- Microsoft SQL Server
- Swagger / OpenAPI
- xUnit automated testing
- GitHub Actions

## Features

### Authentication and User Profiles
- Register as an Organizer or Participant.
- Hash passwords before storing them.
- Log in and log out using cookie authentication.
- View and update the authenticated user's profile.

### Event Management
- View events and individual event details.
- Allow organizers to create, update and delete their own events.
- Support Run, Walk and Cycle event types.

### Categories
- View event categories.
- Allow organizers to manage categories for their own events.

### Enrolments
- Allow participants to enrol in events.
- View a participant's own enrolments.
- Allow organizers to view enrolments for their events.
- Prevent duplicate enrolments for the same participant and event.

### Results
- Allow organizers to record and update results for their events.
- Allow participants to view their own results.
- View results associated with an event.

## Database

The API uses Entity Framework Core with Microsoft SQL Server. The development database is named `RaceDayApiDB`.

The database schema contains the following main tables:

- Users
- Organizers
- Participants
- Events
- Categories
- Enrollments
- Results

Entity Framework Core migrations are used to create and maintain the schema.

## Running the Project

1. Install the .NET 8 SDK and Microsoft SQL Server.
2. Open the solution in Visual Studio.
3. Configure the `RaceDayConnection` connection string in your local configuration.
4. Apply the Entity Framework Core migrations if setting up a new development database.
5. Build and run the `RaceDay.API` project.
6. In the Development environment, open Swagger to explore the API endpoints.

Do not commit database passwords, private credentials or other secrets to the repository.

## Automated Testing

The project includes a separate test project named `RaceDay.API.Tests`.

GitHub Actions is used to build the solution and run the automated tests when changes are pushed to the configured branches.

## Project Status

This repository contains the work for Race Day Part 2. Part 1 is maintained separately.
