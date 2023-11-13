# Desktop/Laptop App requirement
    Rancher Desktop with K3s

# Monitoring Microservices application using OpenTelemetry 
Reference Documentation: https://opentelemetry.io/docs/

# 1. Install and Configure Microservices Application:  
    
    kubectl create namespace otel-demo
    
    cd opentelemetry-app
    kubectl apply -n otel-demo -f .

# 2. Install and Configure Open Telemetry Collector:  

This will collect traces from application and captures at the collector port.

    cd opentelemetry-collector
    kubectl apply -n otel-demo -f .

# 3. Install and Configure Jaeger:  

    cd jaeger
    kubectl apply -n otel-demo -f .

# 4. Install and Configure Prometheus:  

    cd prometheus
    kubectl apply -n otel-demo -f .

# 5. Install and Configure Grafana:  

    cd grafana
    kubectl apply -n otel-demo -f .