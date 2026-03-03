# Cloud Monitoring and Alerts – AWS

This project demonstrates basic cloud monitoring setup for an EC2 instance using Amazon CloudWatch.  
The objective was to configure monitoring metrics, create alerts, and build a dashboard to visualize performance data.

## Overview

An EC2 instance was launched and monitored using AWS CloudWatch.  
A CPU utilization alarm was configured to trigger email notifications when the defined threshold is exceeded.  
A CloudWatch dashboard was created to visualize key performance metrics.

## Services Used

- Amazon EC2  
- Amazon CloudWatch  
- Amazon SNS (Simple Notification Service)

## Implementation Details

### 1. EC2 Instance Setup
An Amazon EC2 instance was launched using a free-tier eligible instance type (t3.micro).  
The instance was successfully initialized and passed all status checks.

### 2. CloudWatch Alarm Configuration
A CloudWatch alarm was created for the following metric:

- **Metric:** CPUUtilization  
- **Statistic:** Average  
- **Threshold:** Greater than 70%  
- **Evaluation Period:** 5 minutes  
- **Action:** Send email notification via SNS  

The alarm triggers when CPU usage exceeds the defined threshold.

### 3. SNS Email Notification
An SNS topic was created and linked to the CloudWatch alarm.  
An email subscription was added and successfully confirmed to receive alert notifications.

### 4. CloudWatch Dashboard
A custom dashboard was created to monitor:

- CPUUtilization  
- NetworkIn  
- NetworkOut  

This allows real-time visualization of instance performance metrics.

## Result

The monitoring system successfully tracks EC2 performance metrics and sends alerts when defined thresholds are exceeded.  
This setup ensures better visibility, proactive monitoring, and improved operational awareness in the cloud environment.

<img width="1918" height="431" alt="cloudwatch-alarm-created" src="https://github.com/user-attachments/assets/9a1b1b3c-1805-447b-8497-9fd7b1d049cd" />

<img width="1917" height="485" alt="cloudwatch-dashboard" src="https://github.com/user-attachments/assets/2936f040-0e5b-4fb3-a539-53e9484b7658" />

<img width="1902" height="278" alt="ec2-instance-running" src="https://github.com/user-attachments/assets/32b10905-6f69-4f10-8ec8-2570bb1cfeeb" />

<img width="1916" height="633" alt="sns-email-subscription" src="https://github.com/user-attachments/assets/b6751843-af28-4b87-ba75-4a0dc2919f91" />


