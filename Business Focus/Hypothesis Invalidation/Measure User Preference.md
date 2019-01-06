#
# Measure User Preferences

Team is able to perform split tests, feature fakes, etc. to gain better insight in to real user preferences through statistical means. 

## Implementation - 01

### Scope 
- N/A

### Tools
- [HotJar](https://www.hotjar.com)

### How?
- Create an account in HotJar and invite the team members
- Create an Organization and a site (web application). 
- HotJar will be generating a script per each site  (web application).
- Add the generated script into the <head> tag on every page of the web application to enable tracking.
- Verify whether the tracking is activated.
- HotJar will record all the visitors behaviours after successfully activating user tracking.
- Create funnels in HotJar from home page to each fake feature page where it allows to messure the conversion rates of each fake feature.
- Create heatmaps in HotJar for each fake feature page where it records the clicks / scrolls and other user actions to get feedback on how users are actually using the fake feature.
  
### Tips
- HotJar's support for single page applications can be setup from site settings.
Please refer to the following article to enable HotJar in Single Page Applications.
https://help.hotjar.com/hc/en-us/articles/115011805428-Hotjar-on-Single-Page-Apps

### Challenges
- HotJar free version has following limitations
    
    only collect data from 2,000 pageviews / day
    Limited reports
    Unlimited users
    Data storage for 365 days
    only 3 funnels are allowed
    only 3 heatmaps are allowed
for more information : https://www.hotjar.com/pricing