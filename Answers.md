# Answers to Part 3

Add your answers to the questions in Part 3, Step 2 below. 

## Vulernability Remediation:
### Vulnerability 1: 
1. Which package or library are you addressing?

Ans. I noticed an issue in the urllib3 package that’s used by Python dependencies.

2. Which CVE is linked to this vulnerability?

Ans. The scan reported CVE-2023-45803, which affects older versions of urllib3.

3. What remediation steps do you suggest?

Ans. The fix is to upgrade urllib3 to version 1.26.18 or higher, since the older version allows potential SSL certificate validation bypasses. Updating the dependency in requirements.txt would take care of it.

### Vulnerability 2:
1. Which vulnerability are you addressing?

Ans. There was also a vulnerability in the Flask web framework that showed up during the Trivy scan.

2. Which CVE is linked to this vulnerability?

Ans. The report listed CVE-2023-30861, which involves how Flask handles template rendering.

3. What remediation steps do you suggest?

Ans. I’d recommend updating Flask to version 2.3.2 or newer, since the patch for that CVE is included there. After upgrading, the app should be re-tested to make sure the web routes and templates still behave as expected.

### Reflection

These scans made me realize that even basic packages in Python or container images can have multiple CVEs attached to them. Regularly running tools like Trivy and Docker Scout is an easy way to catch these before deployment. It also helped me understand how SARIF results map to the OWASP “Vulnerable and Outdated Components” category.

