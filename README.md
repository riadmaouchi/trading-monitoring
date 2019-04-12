# Purpose

Here is the "monitoring" stack of the FX trading application.

## Content
As of now, there are two components:
* Prometheus : monitoring tool bound to the pricing engine  
* Grafana : dashboarding tool based on the data inserted in Prometheus  

As these services have a different lifecycle than the business ones, runnin in their own stack adds flexibility for future updates if any. 
Additionally, failure on the monitoring stack will not affect the running FX trading tool in any way.

## Networking  
Prior to run the stack, an explicit network is used here. It can be built using this command:  
```docker network create monitoring```

