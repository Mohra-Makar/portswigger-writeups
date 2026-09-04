# 🕸️ Cross-Site Scripting (XSS)

![Labs Solved](https://img.shields.io/badge/labs%20solved-1-blue)
![Category](https://img.shields.io/badge/category-XSS-purple)

Write-ups for PortSwigger Web Security Academy labs on Cross-Site Scripting covering how unsanitized or unencoded user input gets reflected, stored, or executed in different DOM contexts.

---

## 📖 What XSS Covers

Cross-Site Scripting vulnerabilities arise when an application includes untrusted input in a web page without proper validation or encoding, allowing an attacker to execute arbitrary JavaScript in a victim's browser. Labs in this category typically fall into:

- **Reflected XSS** payload is echoed back immediately in the response (e.g. search results, error messages)
- **Stored XSS** payload is saved server-side and served to other users later
- **DOM-based XSS** payload never touches the server; it's processed entirely client-side via JavaScript

---

## 📂 Labs

| Lab | Difficulty | Type | Tools Used |
|---|---|---|---|
| [Reflected XSS into HTML Context with Nothing Encoded](./reflected-html-nothing-encoded.md) | Easy | Reflected | Burp Suite |

---

## 🔑 Recurring Fixes

- Context-appropriate output encoding (HTML entity encoding, JS string escaping, URL encoding — matched to where the input lands)
- A strict Content-Security-Policy as defense-in-depth
- Never trust that "sanitized on input" is enough — encode on output, at render time

---

⬅️ [Back to main index](../README.md)
