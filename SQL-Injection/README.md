# 💉 SQL Injection

![Labs Solved](https://img.shields.io/badge/labs%20solved-3-blue)
![Category](https://img.shields.io/badge/category-SQL%20Injection-red)

Write-ups for PortSwigger Web Security Academy labs on SQL Injection covering how unsanitized input passed into database queries can be manipulated to bypass logic, extract data, or defeat filtering defenses.

---

## 📖 What SQL Injection Covers

SQL injection vulnerabilities arise when user input is concatenated directly into a SQL query instead of being treated strictly as data. Labs in this category typically fall into:

- **In-band (classic)** results or errors are returned directly in the application's response
- **Blind** no visible output; the attacker infers results through boolean conditions, response differences, or timing
- **Filter/WAF bypass** the query itself may be exploitable, but a filtering layer (WAF, keyword blocklist) must be evaded first

---

## 📂 Labs

| Lab | Difficulty | Type | Tools Used |
|---|---|---|---|
| [SQL Injection Vulnerability in WHERE Clause Allowing Retrieval of Hidden Data](./retrieve-hidden-data.md) | Easy | In-band | Manual Testing |
| [SQL Injection Vulnerability Allowing Login Bypass](./login-bypass.md) | Easy | In-band | Manual Testing |
| [SQL Injection with Filter Bypass via XML Encoding](./filter-bypass-xml-encoding.md) | Medium | WAF Bypass | Burp Suite, Hackvertor |

---

## 🔑 Recurring Fixes

- Parameterized queries / prepared statements never concatenate user input into SQL
- Least-privilege database accounts, so even a successful injection has limited blast radius
- Don't rely on keyword/pattern-based filtering (WAFs) as a substitute for fixing the query itself filters can be bypassed via encoding, casing, or comments

---

⬅️ [Back to main index](../README.md)
