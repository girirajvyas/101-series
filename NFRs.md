# NFRs

## Different NFRs
Availability
 - Fault Tolerance
 - Robustness
 - Reliability
 - Resilience
 - Disaster recovery

Scalability
 - Performance
 - Responsiveness
 - Efficiency

Security
 - Auditability
 - Secret Management
 - Encryption
 - Isolation

Usability
 - Familiarity
 - Maintainability
 - Compatibility
 - Debuggability

Portability
 - Container runtimes
 - Host OS
 - Hosted
 - Cloud
 - Bare-Metal

Flexibility
 - Format Support
 - Portability
 - Interoperability
 - Extensibility

### FOR UI APPS

Performance: relates to time and the softwares ability to meet time requirements
 - Startup/Loading
   - First contentful paint: When something appears on page (0-2 sec)
   - Speed index: How quickly page contents are visually populated (0-4.3 sec)
   - Time to ineractive: User can interact with the page (0-5.2 sec)
   - First Meaningful paint: User sees somethng meaningful (0-2 sec)
   - First CPU Idle: When the page is minimally interactive (0-4.7sec)
   - Max potential first input delay: The first case of load responsiveness(0-130 msec)
   - Critical rendering path length: Steps to convert files into pictires on screen (< 1sec)
 - Interaction/Rendering  
   - Response (0-100msec)
   - Animation (0-16msec)
   - Idle (0-50msec)
   - Load (0-1sec)

Usability
 - Accessibility
 - Browser support
 - Devices and platforms

Deployment
 - Server side rendering app deployemnt is resource intensive task
 - Deployment of Client side rendering is cheaper and easier to do

Security 
 - Types of Web-Attacks
   - XSS (Cross site scripting)
   - CSRF/XSRF/Sea surf or session riding
   - Using components with known vulnerabiliies
   - Phishing   
 - Tactics
   - Do not rely only on frameworks
   - Use node_modules carefully (use npm audit, Synk)
   - Use Content Security Policy (CSP)
   - Use tool for dynamic analysis (OWASP)
   - Use ESLint for static analysis (or tools like checkmarx, veracode, sonarqube)
   
