## MITRE ATT&CK Detection labs

**Focus:** Build out labs vulnerable to a specific technique in the MITRE ATT&CK framework, then detect maliciuos activity related to that technique

**Examples:**
 MITRE ATT&CK Detection Labs

**Focus:** Build vulnerable web applications/environments that demonstrate specific MITRE ATT&CK techniques, then develop detection mechanisms to identify malicious activity related to those techniques.

**Examples:**

### 1. **T1190 - Exploit Public-Facing Application**
- **Lab Setup:** Deploy a vulnerable web app with known CVEs (e.g., outdated CMS, unpatched framework)
- **Attack Scenario:** Exploit SQLi, RCE, or file upload vulnerabilities
- **Detection Goals:**
  - Monitor for unusual HTTP status codes (500, 403 patterns)
  - Detect SQL injection patterns in web logs
  - Alert on suspicious User-Agent strings
  - Flag abnormal POST request sizes or frequencies

### 2. **T1110 - Brute Force (Web Application)**
- **Lab Setup:** Login portal with weak rate limiting
- **Attack Scenario:** Credential stuffing or password spraying attacks
- **Detection Goals:**
  - Track failed login attempts from single IP
  - Identify distributed brute force across multiple IPs
  - Monitor for common username enumeration patterns
  - Alert on successful logins after multiple failures

### 3. **T1059.007 - Command and Scripting Interpreter: JavaScript**
- **Lab Setup:** XSS-vulnerable web application
- **Attack Scenario:** Stored/Reflected XSS with session hijacking
- **Detection Goals:**
  - Scan for JavaScript execution in unexpected contexts
  - Monitor for cookie exfiltration patterns
  - Detect DOM-based XSS payloads in logs
  - Alert on suspicious script tags in user inputs