🚀 #AWS Cost Guard: ServiceNow-Cloud Optimization
A cross-platform FinOps engine that automates cloud waste identification and remediation.

📖 Project Overview
Large enterprise cloud environments often suffer from "Zombie Resources"—stopped or underutilized instances that continue to accrue storage and reservation costs. This project bridges AWS Lambda with the ServiceNow Table API to provide real-time visibility and a "one-click" termination workflow for wasted resources.

Problem: Manual cloud auditing is inconsistent, leading to thousands in monthly waste.

Solution: A Python-based "Hunter" that pushes AWS waste data into a ServiceNow dashboard for executive visibility and automated cleanup.

🏗️ Technical Architecture
Detection (AWS): A Lambda function (Python) runs on a schedule to identify EC2 instances stopped for >7 days.

Integration (REST): Data is transmitted via secure HTTPS POST to a custom ServiceNow Scripted REST API.

Action (ServiceNow): Records are logged in a custom u_aws_optimization table.

Remediation: A UI Action triggers the IntegrationHub EC2 Spoke to terminate the instance directly from ServiceNow.

🛠️ Tech Stack
Cloud: AWS (EC2, Lambda, IAM, Boto3)

Platform: ServiceNow (CSA/CAD)

Integration: REST API, JSON, IntegrationHub

Language: Python 3.11, JavaScript (GlideRecord)

🚀 Key Features
Automated Discovery: Eliminates the need for manual AWS Console logins.

FinOps Dashboard: Visual representation of "Potential Monthly Savings" directly in ServiceNow.

Safety Governance: Includes an "Ignore" flag to protect critical production servers from automated cleanup.
