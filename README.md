# NFL Schedule API

This project showcases the development of a containerized API management system designed for retrieving sports data. It utilizes **Amazon ECS (Fargate)** for containerized application hosting, **Amazon API Gateway** to expose RESTful endpoints, and integrates with an external **Sports API (SerpAPI)** for accessing live sports information. The implementation highlights advanced cloud computing techniques, such as API management, container orchestration, and secure AWS service integrations.

## Features

- **Exposes a REST API** for querying real-time NFL schedule data.
- **Runs a containerized backend** using Amazon ECS with Fargate for scalability and cost-efficiency.
- **Serverless architecture** for high availability and minimal operational overhead.
- **API management and routing** handled seamlessly via Amazon API Gateway.

## Architecture

The system architecture includes the following components:

1. **API Gateway**: Manages incoming requests and routes them to the backend.
2. **Elastic Load Balancing (ALB)**: Distributes traffic across containerized instances.
3. **Elastic Container Service (ECS)**: Runs containerized Sports API services using Fargate.
4. **Sports API Backend**: Queries SerpAPI for real-time NFL schedule data and processes responses.

## Prerequisites

Before deploying this project, ensure you have the following:

1. **Sports API Key**: Sign up for a free account at [SerpAPI](https://serpapi.com) and obtain your API key.
2. **AWS Account**: Ensure you have an AWS account and basic understanding of ECS, API Gateway, Docker, and Python.
3. **AWS CLI Installed and Configured**: Install and configure the AWS CLI to interact programmatically with AWS.
4. **SerpAPI Library**: Install the SerpAPI library locally using:
   ```bash
   pip install google-search-results
   ```
