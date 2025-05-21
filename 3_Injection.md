# Injection
> Injection happens when untrusted data is sent to an interpreter as part of a command or query, letting attackers run their own code or commands.

- Injection is a common and dangerous vulnerability. It occurs when user input is not properly checked or cleaned, and is sent directly to a database, web browser, or other system. Attackers can use this to steal data, change information, or take control of your app.

## Why is Injection dangerous?
- Attackers can steal, change, or delete data in your database.
- They can run commands on your server or in your users’ browsers.
- Injection can lead to full system compromise, data leaks, or defacement.

## Common Types of Injection:
- **SQL Injection (SQLi):**
    + Attackers insert malicious SQL into your database queries.
    + Example:
        ```sql
        SELECT * FROM users WHERE username = '$input';
        ```
    + If $input is not checked, an attacker can enter:
        ```sql
        ' OR 1=1 --
        ```
    + This returns all users, exposing sensitive data.
    + [Learn more about SQLi](https://owasp.org/www-community/attacks/SQL_Injection)

- **Cross-Site Scripting (XSS):**
    + Attackers inject malicious scripts into web pages viewed by other users.
    + Example:
        ```html
        <input value="$input">
        ```
    + If $input is not escaped, an attacker can enter:
        ```html
        <script>alert('Hacked!')</script>
        ```
    + This runs code in the victim’s browser.
    + [Learn more about XSS](https://owasp.org/www-community/attacks/xss/)

- **Server-Side Template Injection (SSTI):**
    + Attackers inject code into server-side templates.
    + Example (Python Jinja2):
        ```python
        template.render(user_input)
        ```
    + If user_input is not sanitized, an attacker can enter:
        ```jinja
        {{ 7*7 }}
        ```
    + This executes code on the server.
    + [Learn more about SSTI](https://portswigger.net/web-security/server-side-template-injection)

## Consequences:
- Data theft, loss, or corruption.
- Account takeover or impersonation.
- Full server compromise or malware installation.
- Loss of trust and possible legal issues.

## How to prevent Injection:
- Always validate and sanitize user input.
- Use parameterized queries or prepared statements for databases.
- Escape output in web pages to prevent XSS.
- Never pass user input directly to interpreters or templates.
- Use security libraries and frameworks that help prevent injection.
- Regularly test your app for injection vulnerabilities.

### Tips:
- Use ORM (Object-Relational Mapping) tools to avoid raw SQL queries.
- Set Content Security Policy (CSP) headers to reduce XSS risk.
- Keep all libraries and frameworks up to date.
- Educate your team about common injection attacks and prevention.

## Conclusion:
Injection is a serious risk that can affect any part of your application. By validating input, using safe coding practices, and staying alert, you can protect your app from SQLi, XSS, SSTI, and other injection attacks.