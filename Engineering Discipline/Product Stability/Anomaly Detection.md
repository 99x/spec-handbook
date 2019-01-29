#
# Anomaly Detection

Critical components of the production system are covered with health monitoring techniques. Notifications are raised upon anomalies.

## Implementation - 01

### Scope
Following implementation will check if the web application is up and running. It will notify if the server is down or up again.

### Tools
- [UptimeRobot](https://uptimerobot.com/)

### How?
- Create an account in UptimeRobot website
- Add a new monitor
- Select the suitable monitor type (PING, HTTPS, Keyword etc..)
- Provide the time interval that UptimeRobot will check the health of the application

### Tips
- Free tier contains most of the commonly used functionality
- Free tier supports upto 5mins check intervals. 

### Result
![UptimeRoboto Dashboard](https://user-images.githubusercontent.com/2338919/51892515-27392a80-23c8-11e9-8c66-f416558c4cb9.jpg)
