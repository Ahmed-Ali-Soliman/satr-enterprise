<div align="center">

**Language:** **English** | [Deutsch](README.de.md)

# SATR Enterprise
### Blind Zero-Knowledge E2EE Messaging Platform for Enterprises, Sovereign Entities & Banks

[![Security Architecture](https://img.shields.io/badge/Architecture-Blind%20Zero--Knowledge-0f172a?style=for-the-badge)](#core-security-architecture)
[![Encryption](https://img.shields.io/badge/Encryption-Dual--Layer%20P--256%20%2B%20AES--256--GCM-2563eb?style=for-the-badge)](#core-security-architecture)
[![Deployment](https://img.shields.io/badge/Deployment-Enterprise%20Cloud%20%7C%20Air--Gapped%20On--Premise-059669?style=for-the-badge)](#institutional-licensing--deployment-tiers)

</div>

---

## Overview

**SATR Enterprise** is an institutional-grade, end-to-end encrypted (E2EE) messaging platform engineered specifically for organizations, regulated institutions, and banking environments where metadata leaks, server-side message retention, or third-party cloud exposure are unacceptable.

Unlike conventional enterprise chat tools that store message histories or rely on server-managed keys, SATR operates as a **Blind Zero-Knowledge Relay**: messages exist strictly in volatile memory during active delivery and are never persisted to disk.

---

## Core Security Architecture

* **Dual-Layer End-to-End Encryption:** Non-extractable WebCrypto `ECDH P-256` device identity keys paired with per-message ephemeral `ECDH P-256` key exchange, `HKDF-SHA-384` k derivation, and `AES-256-GCM` authenticated encryption.
* **Traffic Analysis Resistance:** Fixed 512-byte cryptographic padding obscures message length and communication patterns.
* **True Zero-Storage Relay:** Zero message content, attachments, or conversation histories are ever written to server databases or disk storage.
* **Blind Identity & Zero IP Logging:** User email identifiers are transformed into salted `HMAC-SHA256` digests before storage, and reverse-proxy access logs strip all client IP addresses.
* **Strict Role & Governance Separation:** Company Administrators (`/org-admin`) manage internal teams, allowlisted employee hashes, and seat allocations without ever accessing cryptographic keys or plaintext content.

---

## Institutional Licensing & Deployment Tiers

SATR Enterprise is licensed exclusively through formal B2B institutional contracts (no consumer checkout or self-serve credit card gateways):

| Tier | Target Organizations | Infrastructure & Governance |
| :--- | :--- | :--- |
| **Enterprise Cloud** | Corporates, Legal Firms & Regulated Teams | Isolated multi-tenant blind relay, annual/semi-annual B2B contract & invoice, strict seat-cap enforcement, and `/org-admin` governance. |
| **Banking & Sovereign On-Premise** | Banks, Financial Institutions & Sovereign Entities | Fully air-gapped Docker self-hosted deployment inside the institution's own private data center with zero external network egress and custom SLA; |

---

## Verified Platform Previews

### 1. B2B Enterprise & Banking Licensing Portal
![B2B Enterprise & Banking Licensing Portal](assets/01_landing_b2b_tiers.png)

### 2. Privacy-Safe Institutional License Inquiry Flow
*Generates a structured B2B contract inquiry locally without storing unverified lead PII on the blind relay..*
![Privacy-Safe License Inquiry Modal](assets/02_license_inquiry_modal.png)

### 3. Strict Organization Seat-Cap Enforcement
![Seat Limit Enforcement](assets/03_seat_cap_rejected.png)

### 4. Non-Destructive Grace Period & Contract Renewal
*Expired licenses enter a configurable waiting window that preserves employee accounts and allowlists without data loss, restoring full access immediately upon renewal.*
![License Grace Period Banner](assets/04_grace_period_banner.png)
![License Renewal Restored](assets/05_renewal_restored.png)

---

## Licensing & Institutional Inquiries

To request an institutional deployment evaluation, architecture briefing, or custom banking SLA, launch the **Request Enterprise License** flow directly within the platform portal or contact the project maintainer via GitHub.
