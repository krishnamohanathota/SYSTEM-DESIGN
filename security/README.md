## Security

### OWASP (Open Web Application Security Project) Top 10 Vulnerabilities

https://owasp.org/www-project-top-ten/

![](images/owasp-top-10.png)

- `Broken Access Control`: Improperly enforced access controls can allow unauthorized users to perform actions or access resources they shouldn't be able to.

  Mitigation:

  - Implement proper role-based access controls and authorization mechanisms.
  - Regularly review and test access control configurations to ensure they're effective.
  - Use strong authentication and session management practices.

- `Cryptographic Failures (Sensitive Data Exposure)`: Inadequate protection of sensitive data, such as financial information or personal records, can lead to data breaches.

  Mitigation:

  - Encrypt sensitive data both in transit and at rest.
  - Follow best practices for secure key management and encryption algorithms.
  - Avoid storing unnecessary sensitive data and use appropriate access controls.

- `Injection`: This occurs when untrusted data is sent to an interpreter as part of a command or query. This can lead to attackers manipulating the interpreter and gaining unauthorized access.

  Mitigation:

  - Use parameterized queries or prepared statements to prevent SQL injection.
  - Employ input validation and output encoding to prevent other types of injection attacks.
  - Use an ORM (Object Relational Mapping) to prevent SQL injection.
  - Use a web application firewall (WAF) to prevent SQL injection.

- `Insecure Design`: New category for 2021, with a focus on risks related to design flaws.

  Mitigation:

  - Establish and use a secure development lifecycle with AppSec professionals to help evaluate and design security and privacy-related controls
  - Limit resource consumption by user or service
  - Write unit and integration tests to validate that all critical flows are resistant to the threat model. Compile use-cases and misuse-cases for each tier of your application.
  - Use threat modeling for critical authentication, access control, business logic, and key flows

- `Security Misconfiguration` : The former category for A4:2017-XML External Entities (XXE) is now part of this risk category.

  - Missing appropriate security hardening across any part of the application stack or improperly configured permissions on cloud services.
  - Unnecessary features are enabled or installed (e.g., unnecessary ports, services, pages, accounts, or privileges).
  - Default accounts and their passwords are still enabled and unchanged.
  - Error handling reveals stack traces or other overly informative error messages to users.

    Mitigation:

    - Use a secure configuration framework to ensure all security controls are implemented and tested.
    - Regularly review and update security configurations.

### API Security Best Practices

1. Authentication - Verifies the identity of users accessing APIs.
2. Authorization - Determines permissions of authenticated users.
3. Rate Limiting - Limits user requests to prevent overload.
4. Input Validation & Data Sanitization - Checks input data and removes harmful parts.
5. Encryption - Encodes data so only authorized parties can decode it.
6. Error Handling - Manages responses when things go wrong, avoiding revealing sensitive info.
7. Logging and Monitoring - Keeps detailed logs and regularly monitors APIs.
8. Security Headers - Enhances site security against types of attacks like XSS.
9. Token Expiry - Regularly expiring and renewing tokens prevents unauthorized access.
10. IP Whitelisting - Permits API access only from trusted IP addresses.
11. Web Application Firewall - Protects your site from HTTP-specific attacks.
12. API Versioning - Maintains different versions of your API for seamless updates.
13. Secure Dependencies - Ensures third-party code is free from vulnerabilities.
14. Intrusion Detection Systems - Monitor networks for suspicious activities.
15. Use of Security Standards and Frameworks - Guides your API security strategy.
16. Data Redaction - Obscures sensitive data for protection.

![](images/api-security.gif)

## Content-Security-Policy (CSP) Headers

https://content-security-policy.com/

- `Content-Security-Policy` - The HTTP Content-Security-Policy response header allows web site administrators to control resources the user agent is allowed to load for a given page. With a few exceptions, policies mostly involve specifying server origins and script endpoints. This helps guard against cross-site scripting attacks (XSS).

`Scan your site for CSP headers`

- https://observatory.mozilla.org/
- https://securityheaders.com/
- https://csp-evaluator.withgoogle.com/

Adding HTTP Security Headers Using Lambda@Edge and Amazon CloudFront

https://aws.amazon.com/blogs/networking-and-content-delivery/adding-http-security-headers-using-lambdaedge-and-amazon-cloudfront/
