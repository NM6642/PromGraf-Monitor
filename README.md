# Flask Monitoring with Prometheus & Grafana

This project demonstrates how to monitor a Flask application locally using Prometheus and Grafana, orchestrated with Docker Compose. The Flask app exposes metrics that Prometheus scrapes, and Grafana visualizes these metrics on dashboards, helping you understand your app’s performance in real time.

---



## Commands to Build, Run & Stop

- To build the Docker images and start all services:  
  `docker-compose up --build`

- To stop and clean up all running containers and networks:  
  `docker-compose down`

---

## Accessing Services on Localhost

- **Flask App:** http://localhost:5000 — The web app you are monitoring  
- **Prometheus:** http://localhost:9090 — Metrics scraping and query interface  
- **Grafana:** http://localhost:3000 — Visualization and dashboard interface

---

## Grafana Setup Steps

1. Open Grafana at http://localhost:3000  
2. Login with default username **admin** and password **admin**  
3. Add a new data source and select **Prometheus**  
4. Set the Prometheus URL to `http://prometheus:9090` (this is the service name inside Docker Compose)  
5. Save and test the connection to ensure Grafana can fetch metrics  
6. Create a new dashboard  
7. Add a panel with the Prometheus query: `app_requests_total` to visualize total HTTP requests to the Flask app

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
