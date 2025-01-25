# NFL Schedule API

This project demonstrates building a containerized API management system for querying sports data. It leverages **Amazon ECS (Fargate)** for running containers, **Amazon API Gateway** for exposing REST endpoints, and an external **Sports API (SerpAPI)** for real-time sports data. The project showcases advanced cloud computing practices, including API management, container orchestration, and secure AWS integrations.

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
