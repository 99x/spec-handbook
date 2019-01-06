# Monitor Continuously

Team is aware of scalability limits of the production system. Average load of the production environment is being monitored continuously.

## Implementation - 01

### Scope
Following implementation is applicable for the projects that has containerized workload or serverless microservices maintained in AWS. 

### Tools
- [AWS X-Ray Service](https://aws.amazon.com/xray/) 
- [AWS CodeWatch Service](https://aws.amazon.com/cloudwatch/)
- (Optional) [mLab Telemetry](https://telemetry.mlab.com)

### How?
- Create CloudWatch dashboard and configure to monitor the containerized workload in the compute cluster
- Add the metrices like CPU Utilization/Memory Utilization/Network Calls on to your containerized environments
- Serverless microservices(AWS Lambda) is associated with AWS X-Ray service
- CloudWatch alarms are set to notify the team if cetain tresholds are exceede (E.g. Memory Utilization) 
- [Optional] Detailed database logs can be viewed with mLab telemetry 

### Tips
- AWS X-Ray can be setup with both containerized and serveless workloads to enable end-to-end tracability
- Use X-Ray service map to see the graphical representation of entire life cycle of a request
- Measure the latency for all the connected parts of your application with AWS X-Ray and identify the bottelnecks 
- The first 100,000 traces recorded each month are free