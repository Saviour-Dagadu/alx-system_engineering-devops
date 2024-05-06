# Postmortem
*DevOps* *SysAdmin*

![Debugging Mindset](debugging.jpg)

## Issue Summary
Duration: 3 hours (10:00 - 13:00 GMT) on May 6, 2024
Impact: 40% of users in Ghana and 20% of users in West Africa experienced slow loading times and errors on our e-commerce platform, resulting in a significant increase in support tickets and potential revenue loss.
Root Cause: High latency and packet loss on our internet service provider (ISP) in Accra, Ghana.


## Timeline
10:00 - Issue detected by monitoring alert and customer complaints.
10:10 - Initial investigation focused on database performance, assuming high query latency.
10:30 - Investigation shifted to ISP connectivity after discovering high packet loss.
11:00 - Misleading path: Assumed ISP issue was caused by recent network maintenance; spent 30 minutes reviewing maintenance logs.
11:30 - Escalated to senior engineer, who identified high latency and packet loss on ISP.
12:00 - Began implementing fix, including switching to backup ISP and contacting primary ISP for support.
13:00 - Issue resolved.


## Root Cause and Resolution
The root cause was high latency and packet loss on our primary ISP in Accra, Ghana. The issue was resolved by switching to our backup ISP and working with the primary ISP to resolve the issue.


## Corrective and Preventative Measures
Implement redundant ISP connections in multiple African countries.
Develop automated failover to backup ISP in case of high latency or packet loss.
Increase monitoring and alerting for ISP connectivity issues.
Schedule regular review of ISP performance and maintenance schedules.
Develop training program for engineers on ISP best practices and troubleshooting.


This outage highlighted the importance of redundant ISP connections and proactive monitoring in Africa's growing e-commerce market. By addressing these issues, we can prevent similar outages and improve overall platform performance for our users in Ghana and West Africa.
