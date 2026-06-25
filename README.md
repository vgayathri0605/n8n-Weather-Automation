# n8n Weather Automation

A personal automation project built to learn workflow automation, API integration, and local deployment using Docker.

 ## Project Overview

This workflow runs automatically every day at a scheduled time. It detects the current location, fetches live weather data from an external API, and delivers a formatted weather report directly to Gmail — without any manual input.

## How It Works
Schedule Trigger → Get Location → Get Weather → Send Gmail

1. **Schedule Trigger** — Runs the workflow automatically at a set time every day
2. **Get Location** — Detects city using IP-based location API
3. **Get Weather** — Fetches real-time weather data from OpenWeatherMap
4. **Send Gmail** — Delivers a formatted weather report to the inbox

## Tools and Technologies

| Tool | Purpose |
|---|---|
| n8n | Open-source workflow automation platform |
| Docker | Local deployment on Windows |
| OpenWeatherMap API | Real-time weather data |
| ip-api.com | IP-based location detection |
| Gmail OAuth2 | Automated email delivery |

## Key Concepts Practiced

- Deploying and running n8n locally using Docker on Windows
- Building multi-step automated workflows without writing code
- Integrating third-party REST APIs using HTTP Request nodes
- Passing dynamic data between nodes using expressions
- Setting up Gmail OAuth2 authentication from scratch
- Debugging real-world issues such as UTC timezone offsets

## Setup Instructions

1. Install Docker Desktop on Windows
2. Open PowerShell as Administrator and run:
docker run -it --rm --name n8n -p 5678:5678 -v n8n_data:/home/node/.n8n docker.n8n.io/n8nio/n8n

3. Open `http://localhost:5678` in your browser
4. Import `workflow.json` into n8n
5. Add your OpenWeatherMap API key to the Get Weather node
6. Configure Gmail OAuth2 credentials
7. Set your preferred schedule time and click Publish

## Notes

This is my first automation project built while learning n8n from scratch. The goal was to understand how modern workflow automation tools work and how to connect real APIs to build something genuinely useful.
