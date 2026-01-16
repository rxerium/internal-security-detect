# Internal Security Detection (via Safebase)

Exposed SafeBase portals serve two audiences at once: prospects who need proof of your security posture, and security researchers (blue and red teamers). Each green tick reveals a control that (supposedly) exists today; every missing tick is an equally loud hint at what doesn't.

## Why collect this data?

Compliance frameworks like ISO 27001, SOC 2, PCI-DSS, and the growing privacy regulations in different regions require "evidence" that security controls are in place and functioning. Safebase offers a convenient way to provide this without endless email exchanges for proof or documents.

Scraping your own public trust center might seem unnecessary since you created it, but there are other good reasons to do so:

1. **Continuous assurance** – Auditors increasingly prefer ongoing evidence.
2. **Change detection** – Policy titles, groupings, and even control names can change after a platform update or acquisition. Automated scraping can detect these changes before customers notice.
3. **Third-party mappings** – Converting the list into JSON allows you to cross-reference against control libraries (e.g., NIST 800-53) and automatically prove coverage.
4. **Security assessments** – For blue teams, this ensures that public claims remain accurate; for red teams, it provides a quick comparison with your own control library to identify "weaknesses."

## How do I run this script?

1. Download Nuclei from [here](https://github.com/projectdiscovery/nuclei)
2. Copy the template to your local system
3. Run the following command: `nuclei -u https://yourHost.com -headless -t template.yaml`

The output should look like:
![alt text](image.png)

*An in-depth guide can be found here: [Internal Security Detection](https://blog.rxerium.com/internal-security-detection)*

## Finding SafeBase Sites

Use this Google dork to discover SafeBase trust centers:
```
inurl:(security|trust|compliance) "Powered by SafeBase"
```

## Security Controls Detected (163 Verified Controls)

All controls below have been verified on real SafeBase trust centers.

### Access & Authentication
- Access Control
- Access Control Policy
- Access Log Management
- Access Monitoring
- Access Monitoring Policy
- Authentication
- Collected Data Access
- Credential Management
- Data Access
- Data Roles: Controller and Processor
- Multi-Factor Authentication
- Password Security
- SSO Support
- Sub-processors
- Subprocessors
- Voluntary Product Accessibility Template® (VPAT®)

### AI & Machine Learning
- AI Governance
- AI Risk Statement
- AI Security
- AI Training Data
- AI Training Data and Bias
- Alignment with EU AI Act Principles
- Decision-Making and Human Oversight
- EU AI Act
- Model Evaluations, Fairness &amp; Bias
- Ongoing Third-Party Bias Audits
- TRUSTe Responsible AI Certification

### Application Security
- Application Penetration Testing
- Bug Bounty Program
- Code Analysis
- Responsible Disclosure
- Responsible Disclosure &amp; Bug Bounty
- Secure Development Training
- Secure Software Development Lifecycle
- Software Development Lifecycle

### Asset & Infrastructure
- Asset Management
- Asset Management Policy
- Asset Management Practices
- Audit Logging
- Capacity Management
- Data Exfiltration Monitoring
- Infrastructure Logging
- Logging
- Status Monitoring
- Status Monitoring of SLA

### Business Continuity
- BC/DR
- Business Continuity and Disaster Recovery
- Business Continuity/Disaster Recovery (BC/DR) Policy
- Data Backups
- Disaster Recovery &amp; Backups
- Operational Resilience and Redundancy Policy
- Overarching Operational Resilience and Redundancy Plan

### Compliance & Certifications
- CCPA
- CSA STAR
- CSA STAR Certification
- CSA STAR Level 1
- CSA STAR Level 2
- CSA STAR Level 2 Certification
- CSA STAR for AI
- CSA Trusted Cloud Provider
- Cyber Essentials Plus
- DORA
- DoD IL4
- EU-US DPF
- FIPS 140-2
- FedRAMP High
- FedRAMP Moderate
- GDPR
- GDPR Compliance and AI
- GovRAMP
- HECVAT
- HECVAT Full
- HECVAT Lite
- HIPAA
- IRAP
- IRAP Protected Documentation
- ISO 27001 / 27017 / 27018
- ISO/IEC 20243:2024
- ISO/IEC 27001
- ISO/IEC 27001 SoA
- ISO/IEC 27001:2022
- ISO/IEC 27017
- ISO/IEC 27018
- ISO/IEC 27701
- ISO/IEC 27701:2019
- ISO/IEC 42001:2023
- NIST
- NIST 800-53 Rev. 5
- OPTIV ISO27001
- PCI DSS
- PCI DSS v4.0.0
- Privacy Mark
- SOC 1
- SOC 2
- SOC 2 Type 2
- SOC 3
- Swiss-US DPF
- TISAX
- TX-RAMP
- UK Extension to EU-US DPF
- US Employment Law Compliance
- VPAT

### Data Protection & Privacy
- Cookies
- Data Breach Notifications
- Data De-Identification
- Data Deletion / Data Retention
- Data Erasure
- Data Flow Diagram
- Data Loss Prevention
- Data Privacy Officer
- Data Processing Agreement
- Data Residency
- Data Retention
- Data Retention &amp; Disposal
- Data Security
- Disk Encryption
- Employee Privacy Training
- Encryption-at-rest
- Health Data Hosting (HDS) France
- Network / Data Flow Diagrams
- Privacy Officer
- Privacy Policy

### Endpoint & Device
- Bring Your Own Device (BYOD)
- Endpoint Detection &amp; Response
- Mobile Device Management

### Incident Response
- Incident Response
- Incident Response Plan

### Network Security
- Allow List Restrictions
- Anti-DDoS
- DNS Filtering
- Firewall
- IDS/IPS
- Network Diagram

### Personnel & Training
- Acceptable Use Policy
- Anti-Bribery and Corruption
- Anti-Modern Slavery
- Code of Conduct
- Employee Training
- HR Security
- Model Pretraining
- Modern Slavery
- Phishing Training
- Role-Based Training
- Supplier Code of Conduct

### Risk & Vulnerability
- Risk Assessments
- Supply Chain Risk Management
- Vulnerability &amp; Patch Management

### Third Party & Vendor
- Customer Audit Rights
- Third Party Dependence
- Vendor Management

### Other
- Alternate Work Sites
- Approach to AI
- Certificate of Insurance
- Change Enablement Policy
- Continual Improvement Policy
- Critical Dependence
- Cyber Insurance
- Email Protection
- Employers Liability Insurance
- Environment Social and Governance
- Security Information and Event Management
- Security Operations Center (SOC)
- Technical and Organisational Measures

## Tested Sites

This template has been tested and verified against:
- security.projectdiscovery.io
- security.okta.com
- trust.openai.com
- secureandtrusted.gbgplc.com
- trust.treasuredata.com
- trust.hipeople.io

## References

- https://safebase.io
- https://blog.rxerium.com/internal-security-detection

## Contact

Feel free to reach out to me on [Signal](https://signal.me/#eu/0Qd68U1ivXNdWCF4hf70UYFo7tB0w-GQqFpYcyV6-yr4exn2SclB6bFeP7wTAxQw).
