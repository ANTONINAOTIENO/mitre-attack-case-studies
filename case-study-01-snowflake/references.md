# GCP Security Hardening & Traffic Analysis

## Overview

This project focused on building and securing a multi-tier architecture in Google Cloud while understanding how attackers move inside cloud environments.

The goal was not just to deploy resources, but to actually test:
- what traffic should be allowed
- what should be blocked
- what logs get generated
- and whether the monitoring setup could detect suspicious activity

I intentionally tested weak points in the environment and then hardened the architecture using segmentation, firewall rules, traffic monitoring, and least privilege principles.

---

# Key Takeaways

## 1. Least Privilege Matters More Than Convenience

One of the biggest lessons from this project was seeing how easy it is to over-permission cloud workloads.

At one point, my web-tier VM was attempting to interact with infrastructure it had no business managing.

Instead of expanding permissions just to make things easier, I kept the service account restricted and managed the environment through Cloud Shell.

That reinforced an important principle for me:

> workloads should only have the access they absolutely need.

---

## 2. Blocking Traffic Is One Thing. Understanding It Is Another.

A major part of this project involved testing both:
- denied traffic
- legitimate traffic flow

I simulated unauthorized access attempts against restricted ports and confirmed they were blocked by firewall rules.

I also validated that legitimate communication between systems still worked correctly.

This helped me better understand:
- segmentation
- firewall behavior
- internal traffic flow
- and how attackers attempt lateral movement inside cloud environments

---

## 3. Monitoring Needs Intention

One thing I underestimated was how much visibility depends on proper logging configuration.

I initially expected deny logs to simply appear, but quickly learned that logging has to be:
- enabled
- tested
- and validated properly

I also struggled with log visibility during parts of the project, which honestly helped me understand how easy it is to end up with monitoring blind spots in cloud environments.

Even though I wasn’t able to fully complete the logging section the way I initially planned, troubleshooting the issue still taught me a lot about how observability works in GCP.

---

# Security Controls Implemented

- Multi-tier VPC architecture
- Network segmentation using subnets
- Restricted firewall rules
- Bastion-style administrative access
- VPC Flow Logs configuration
- Firewall logging configuration
- Traffic analysis and validation
- Least privilege access principles
- Simulated attack activity and remediation

---

# Final Thoughts

This project pushed me to think less like someone simply deploying cloud resources and more like someone responsible for securing and monitoring them.

The biggest takeaway for me was this:

> security controls mean very little if you never test whether they actually work.