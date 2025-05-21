# Server-side Request Forgery (SSRF)
> SSRF lets attackers trick your server into making requests to places it shouldn’t, which can lead to data leaks or even full system compromise.

- Server-side Request Forgery (SSRF) happens when an attacker tricks your server into sending requests to internal or external systems that the attacker chooses. This can let them access sensitive data, scan your internal network, or attack other systems from your server.

## Why is SSRF dangerous?
- Attackers can use SSRF to access internal services (like databases or admin panels) that are not meant to be public.
- SSRF can be used to bypass firewalls and security controls, since the request comes from your trusted server.
- In some cases, SSRF can lead to remote code execution or full system compromise.
- Real-world attacks have used SSRF to steal cloud metadata, access private files, or move deeper into a company’s network.

## When does SSRF happen?
- Your server fetches data from a URL or address provided by the user, without checking if it’s safe.
- No validation or filtering of user-supplied URLs or IP addresses.
- Allowing users to upload or import files from arbitrary locations.
- Using cloud services or APIs that trust requests from your server.

## Examples:
- Fetching a user-supplied URL:
    + Your app lets users enter a URL to fetch a profile picture:
        ```text
        User enters: http://localhost/admin
        ```
    + The server requests its own admin page, exposing sensitive info.

- Accessing cloud metadata:
    + Attacker tricks the server into requesting cloud metadata:
        ```text
        http://169.254.169.254/latest/meta-data
        ```
    + This can leak cloud credentials or configuration.

## Consequences:
- Data leaks from internal systems.
- Attackers can scan and attack your internal network.
- Possible remote code execution or full server compromise.
- Loss of trust, data, and possible legal issues.

## How to prevent SSRF:
- Never let users supply URLs or addresses for your server to fetch without strict validation.
- Only allow requests to trusted, whitelisted domains or IPs.
- Block requests to internal IP ranges (like 127.0.0.1, 10.x.x.x, 169.254.x.x, etc.).
- Use network-level controls (firewalls, security groups) to block unwanted outbound requests.
- Disable unused URL fetching features in your application or libraries.
- Log and monitor all outbound requests from your server.

### Tips:
- Use allow-lists (not block-lists) for URLs and IPs your server can access.
- Validate and sanitize all user input, especially URLs and file locations.
- Regularly review your code for any features that fetch external resources.
- Use security tools to scan for SSRF vulnerabilities in your application.
- Educate your team about SSRF risks and best practices.

## Conclusion:
SSRF is a serious vulnerability that can let attackers use your server as a weapon. By validating all requests, restricting outbound access, and monitoring server activity, you can protect your systems from SSRF attacks.
