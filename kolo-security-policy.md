# 🔐 KOLO Security Policy

This document outlines KOLO’s security policies, standards, and procedures for safeguarding user data, transactions, and infrastructure.

## 🔒 Data Security

- All sensitive data (e.g., card details, BVN) is encrypted using **AES-256**
- HTTPS is enforced across all KOLO endpoints
- User passwords are hashed using **bcrypt**

## 🛡️ Application Security

- Regular vulnerability scans and security audits
- Secure coding practices with code reviews for all releases
- Rate limiting and throttling to prevent abuse

## 🧑‍💻 User Account Security

- Optional Two-Factor Authentication (2FA)
- Automatic logout after 15 minutes of inactivity
- Alert on new device login or withdrawal attempt

## 📦 Infrastructure Security

- Hosted on ISO-27001-certified cloud providers
- Access control with RBAC (Role-Based Access Control)
- Daily automated backups with 30-day retention

## 🚨 Incident Response

- Security incidents are reported to the CISO and logged in an internal system
- Affected users are notified within 72 hours in line with NDPR

## 🧾 Logging & Monitoring

- API access logs, transaction logs, and admin logs are retained
- Anomaly detection is used to flag suspicious activities

## 📆 Review and Updates

This security policy is reviewed quarterly and updated as needed to comply with best practices and evolving threats.
