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
An Amazon EC2 instance was launched using a free-tier eligible instance type.  
The instance was successfully initialized and passed all status checks.

### 2. CloudWatch Alarm Configuration
A CloudWatch alarm was created for the following metric:

- **Metric:** CPUUtilization  
- **Threshold:** Greater than 70%  
- **Evaluation Period:** 5 minutes  
- **Action:** Send email notification via SNS  

The alarm triggers when CPU usage exceeds the defined threshold.

### 3. SNS Email Notification
An SNS topic was created and linked to the CloudWatch alarm.  
Email subscription was confirmed to receive alert notifications.

### 4. CloudWatch Dashboard
A custom dashboard was created to monitor:

- CPUUtilization  
- NetworkIn  
- NetworkOut  

This allows real-time visualization of instance performance.

## Result

The monitoring system successfully tracks EC2 performance metrics and sends alerts when defined thresholds are exceeded.  
This setup ensures better visibility, proactive monitoring, and improved operational awareness in the cloud environment.
