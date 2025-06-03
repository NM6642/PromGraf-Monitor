# Monitoring with Prometheus & Grafana

This project demonstrates how to monitor a Flask application locally using Prometheus and Grafana, orchestrated with Docker Compose. The Flask app exposes metrics that Prometheus scrapes, and Grafana visualizes these metrics on dashboards, helping you understand your app’s performance in real time.

---



## Commands to Build, Run & Stop

- To build the Docker images and start all services:  
  `docker-compose up --build`

- To stop and clean up all running containers and networks:  
  `docker-compose down`

  **Note:** All services run locally and can be accessed via `localhost` URLs in your browser.

---

## Next Steps

- Define Prometheus alerting rules to notify on critical events (e.g., high error rates)  
- Automate Grafana dashboard provisioning with configuration files for easy setup  
- Extend monitoring to multiple Flask microservices or other applications  
- Deploy this monitoring stack to a cloud environment (AWS, Azure, GCP) for production use  
- Explore additional metrics and custom instrumentation in your Flask app

---

## Sample Screenshots

- Grafana Dashboard (see `graf.PNG`)  
- Prometheus Metrics Output (see `pro.PNG`)
