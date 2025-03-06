# Insecure Design
> New Top Vul in 2021.
- Insecure Design happens when a system or app is built with mistakes from the start, making it simple for attackers to steal sensitive data like passwords, credit card numbers, or personal details. This is the main reason why security problems appear early on.

## Why Insecure Design Is Dangerous:
- Insecure Design is risky because it can let private data get out, putting people’s information in danger and causing serious trouble. When a system’s structure is weak, bad people can break in, take the data, and use it to harm others.

- One major danger is that personal details can be stolen. Both companies and individuals trust good systems to protect important things—like bank account info, medical records, or IDs. If the design fails, this information can be taken and used in bad ways.

- Also, these mistakes can lead to data leaks, where attackers grab lots of private information. This puts people at risk of identity theft or losing money, while companies might face legal issues or break rules. Victims could lose cash, have their image damaged, and even get into legal fights for not keeping data safe.

- There are many real examples of Insecure Design causing problems. Weak controls or poor planning let attackers get through. For example, flaws like missing login checks have allowed hackers to skip security steps. Bad password setups are another issue—when protection isn’t planned well, attackers can easily crack them and enter systems.

## Insecure Design Occurs When:
- Key features (like logins or payments) are made without thinking about security.

- Access rules are loose, forgotten, or not handled well, letting the wrong people in.

- Old or unsafe design ideas (like sending data openly or hiding secrets in code) are used.

- The system trusts users or data without checking twice.

## Examples:
- Weak Login System:
    + A website lets anyone see admin pages because it doesn’t check who they are:
        ```text
        User: normal | Role: none → Still opens /admin/dashboard

    + Attackers can take control without needing a password.

- No Data Checks:
    + A banking app takes any info it gets without looking at it:
        ```text
        POST /transfer?amount=1000&to=attacker_account
    + With no checks in the design, attackers can send money wherever they want.

- Secrets in Code:
    + An app has a key written right in the program:
        ```python
        API_KEY = "secret123"
    + If attackers find it, they can use the key to get in.

## Consequences of Insecure Design:
- Data Leaks: Personal info, bank details, or business secrets get out.

- Lost Trust: Customers and partners stop believing in the company.

- Bigger Attacks: Attackers use weak spots to do more damage (like stealing accounts).

## Preventive Measures:
- Plan Security Early: Build safety into the system from the start.

- Set Strong Rules: Only let the right people use sensitive parts:
    ```python
    if not current_user.is_admin:
    return "Access Denied", 403

- Check All Data: Look at and fix everything the system gets.

- Use Good Standards: Follow modern safety tips like OWASP guidelines.

- Test Before Finishing: Check for problems while designing, not just at the end.

## Conclusion:

*Insecure Design isn’t just a small mistake—it’s a problem that starts when security isn’t planned well. By designing carefully, adding strong protections, and testing often, you can stop big risks. A safe design keeps data and users out of harm’s way!*