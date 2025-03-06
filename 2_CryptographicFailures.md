# Cryptographic Failures
> Knowns as Sensitive Data Exposure before.

- Cryptographic failures are where attackers often target sensitive data, such as passwords, credit card numbers, and personal information, when you do not properly protect them.This is the root cause of sensitive data exposure.

    ## Cryptographic Failures dangerous because:
- Cryptographic failures are very dangerous because they can let sensitive data get exposed, putting personal details at risk and causing big problems. When encryption systems break down, bad guys can get into protected data, unlock it, and use it for their own benefit.

- One of the biggest dangerous of cryptographic failures is that personal information can get leaked. Both companies and people depend on encryption to keep private stuff—like bank details, health records, and personal IDs—safe. If the encryption fails, this info can be stolen and used in harmful ways.

- Moreover, these failures can lead to data leaks, where attackers get their hands on huge amounts of private information. This puts people at risk of having their identities stolen or being tricked out of money, while companies could face legal trouble and rule-breaking issues. When a data breach happens, victims might lose money, see their reputation ruined, and even deal with lawsuits for not keeping sensitive data safe enough.

- There are plenty of real-life examples where cryptographic failures have caused data breaches. Problems like weak encryption methods or sloppy setups can let attackers unlock protected data. Flaws in TLS, like the well-known Heartbleed bug, have let hackers sneak into secure connections, messing up the privacy and safety of information being sent. Weak password hashing is another big problem—when passwords aren’t secured properly, they’re easy to break, letting unauthorized people slip into systems.

    ## Cryptography Failures occurs when:
- Sensitive data (password, credit card number, personal information) is not encrypted or encoded by weak algorithms.

- Encryption Keys is poorly managed, exposed or reused unsafe.

- Outdated security protocols (such as SSLV2, TLS 1.0, HTTP) or improper configuration are used.

- The secret key is easy to guess.

    ## Example:
- Save unsafe password:
    + Website save account admin with: ```User: admin | Password: password123``` 
    + If the hacker access the database via SQL Injection, they can read the password directly without decoding.

- Use HTTP:
    + Website of banking that transfer data through HTTP without HTTPS(Hypertext Transfer Protocol Secure), hackers can easily to catch request with wireshark,...
    + ```GET /login?username=john&password=secret123 HTTP/1.1```
    + Because HTTP nowaday is insecure protocol, have to use HTTPS for extremely secure.
- ...

    ## Consequences of Cryptography Failures: 
- Sensitive data leaks: Personal information, bank accounts, or trade secrets are exposed.

- Faith loss: Customers and partners no longer believe in the organization.

- Privilege escalation: The attacker uses the exposed data to perform other attacks (such as Credential Stuffing).

    ## Preventive Measures:
- Classify data processed, stored, or transmitted by an application.

- Don’t store sensitive data unnecessarily.

- Make sure to encrypt all sensitive data at rest.

- Ensure up-to-date and strong standard algorithms, protocols, and keys are in place; use proper key management.

- Use tools such as `Qualys SSL Labs` to check TLS configuration.