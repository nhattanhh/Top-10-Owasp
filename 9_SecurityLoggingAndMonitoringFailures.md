# Security Logging and Monitoring Failures
> If you don’t log and monitor security events, you won’t know when you’re under attack or something goes wrong.

- Security Logging and Monitoring Failures happen when a system doesn’t record enough information about important activities, or doesn’t monitor and alert when something suspicious happens. This allows attacks or security incidents to go undetected for a long time.

## Why is this dangerous?
- Without proper logs or monitoring, attacks can happen for months without anyone noticing.
- There’s no evidence to investigate, fix, or report incidents.
- Suspicious actions (like unauthorized access, data changes, or malware installation) go undetected and unblocked.
- Many big data leaks were only discovered after months because no one was watching the logs.

## When does this happen?
- Important events (like logins, permission changes, or access to sensitive data) are not logged.
- Logs are missing, incomplete, or not stored safely.
- No alerts are set up for strange or risky activities.
- Logs are not checked regularly.
- Attackers can delete or change logs to hide their actions.

## Examples:
- No Logging of Failed Logins:
    + The system does not record failed login attempts:
        ```text
        No record for 100 wrong password tries in a row
        ```
    + Attackers can guess passwords over and over without being noticed.

- No Alert for Unauthorized Access:
    + Someone accesses private data, but no alert is sent to the admin.

- Logs Deleted or Changed:
    + An attacker deletes logs to cover their tracks after breaking in.

## Consequences:
- Attacks or problems are not found in time.
- No proof for investigation or fixing issues.
- More damage, data loss, and loss of trust.
- Possible fines for not following security rules.

## How to prevent this:
- Log all important security events (logins, permission changes, data access, system errors, etc.).
- Store logs safely and protect them from being changed or deleted.
- Set up automatic alerts for suspicious or important events.
- Check and review logs often to spot early signs of attacks.
- Only let trusted admins access the logs.
- Regularly check that your logs are complete and unchanged.

### Tips:
- Use tools like Splunk, ELK, or Graylog to collect and watch logs in one place.
- Set up email or SMS alerts for serious security events.
- Store logs on a separate server so they can’t be deleted if the main system is hacked.
- Keep logs for as long as needed for investigation and legal reasons.
- Practice incident response to make sure your logging and alerting really work.

## Conclusion:
Security Logging and Monitoring Failures leave you “blind” to security threats. Good logging, active monitoring, and quick alerts help you spot, stop, and fix attacks before they cause big problems.