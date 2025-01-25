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
   
![Image Alt](https://github.com/RalphHenryDominisac-AWS/NFL-Schedule-API/blob/0534a1526413d43fddf73fc7b251a5a33ee5fc6b/architecture%20NFL%20Schedule%20API.jpg)


## Prerequisites

Before deploying this project, ensure you have the following:

1. **Sports API Key**: Sign up for a free account at [SerpAPI](https://serpapi.com) and obtain your API key.
2. **AWS Account**: Ensure you have an AWS account and basic understanding of ECS, API Gateway, Docker, and Python.
3. **AWS CLI Installed and Configured**: Install and configure the AWS CLI to interact programmatically with AWS.
4. **SerpAPI Library**: Install the SerpAPI library locally using:
   ```bash
   pip install google-search-results
   ```



## Deployment

1. Clone the repository and navigate to the project directory:
     ```bash
   git clone https://github.com/your-username/nfl-schedule-api.git
   cd nfl-schedule-api
   ```
2. Build the Docker image:
     ```bash
   docker build -t nfl-schedule-api .
   ```
3. Push the Docker image to Amazon Elastic Container Registry (ECR).
4. Deploy the application using ECS Fargate and set up API Gateway for routing.
5. Test the REST API by sending a GET request to the /sports endpoint:
   ```bash
   curl https://your-api-gateway-url/sports
   ```

## Example Response
   ```bash
   {
    "message": "NFL schedule fetched successfully.",
    "games": [
        {
            "away_team": "Team A",
            "home_team": "Team B",
            "venue": "Stadium X",
            "date": "2025-01-01",
            "time": "8:00 PM ET"
        }
    ]
}
   ```

## Cleanup
- To avoid incurring costs, delete the ECS cluster, API Gateway, and other associated resources after use.

## License
- This project is licensed under the MIT License. See the LICENSE file for more details.
  
