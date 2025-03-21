# Introduction
In this assignment you will be hosting an ASP.NET application on a cloud VPS with HTTPS.

As with the previous assignments, the tasks are individual but the delivery is a PDF the group writes together.

## Document structure
Front page - course, names, assignment
Table of contents/listings/figures
Introduction
Prepare the code
What changes did you make to the ASP.NET project? Explain them.
Docker and Docker Compose
Dockerfile and Compose configuration, documented line by line
Server deployment
Document the actions you made, with screenshots. Link to the working website.
Conclusion - short recap of what you have completed -  problems?

## Task 1 - Prepare the code
Steps
Use this ASP.NET project Last ned this ASP.NET projectas a starting point. This is one of the examples from IKT201 and should be familiar to computer science students.

Note: This project is built on .NET 8.

Create a new repo in Gitea (on your server) called ikt206g25v-05
Clone  your new Gitea repository
Push the code attached to this assignment
Update the code to support PostgreSQL and migrations when the project is running in production mode.
See the lecture notes on code changes and this documentationLenker til en ekstern side. for how to create your first migration.

## Task 2 - Docker and Docker Compose
1. First create a Dockerfile that builds the ASP.NET application.

2. Then create a Docker Compose file that contains:

web - Your ASP.NET web application.
Uses the Dockerfile you created.
db - PostgreSQL
proxy - Caddy
Se the lecture notes for tips on how to configure the database and the proxy. You will need to create a configuration file for Caddy for your domain.

## Task 3 - Server deployment
Steps
Purchase a domain at e.g. https://domene.shopLenker til en ekstern side.
Note: It might take 24 hours for the domain to become active.
Rent a VPS (they call them droplets) from Digital OceanLenker til en ekstern side. or other provider. You need at least 1GB of RAM for .NET.
You get $200 for free with GitHub Student Developer PackLenker til en ekstern side.
Add an A-record to your domain that points to your VPS
Clone your project on the VPS and run it with Docker Compose. 
