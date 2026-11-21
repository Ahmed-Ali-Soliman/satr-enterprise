<div align="center">

**Sprache:** [English](README.md) | **Deutsch**

# SATR Enterprise
### Blind-Zero-Knowledge-E2EE-Kommunikationsplattform für Unternehmen, Behörden & Banken

[![Sicherheitsarchitektur](https://img.shields.io/badge/Architektur-Blind%20Zero--Knowledge-0f172a?style=for-the-badge)](#zentrale-sicherheitsarchitektur)
[![Verschlüsselung](https://img.shields.io/badge/Verschlüsselung-Dual--Layer%20P--256%20%2B%20AES--256--GCM-2563eb?style=for-the-badge)](#zentrale-sicherheitsarchitektur)
[![Bereitstellung](https://img.shields.io/badge/Bereitstellung-Enterprise%20Cloud%20%7C%20Air--Gapped%20On--Premise-059669?style=for-the-badge)](#institutionelle-lizenz--und-bereitstellungsmodelle)

</div>

---

## Überblick

**SATR Enterprise** ist eine Ende-zu-Ende-verschlüsselte (E2EE) Kommunikationsplattform auf Unternehmensniveau, die speziell für Konzerne, regulierte Institutionen und Bankenumgebungen entwickelt wurde, in denen Metadaten-Lecks, serverseitige Nachrichtenspeicherung oder externe Cloud-Zugriffe ausgeschlossen sein müssen.

Im Gegensatz zu herkömmlichen Business-Messengern arbeitet SATR als **Blind-Zero-Knowledge-Relay**: Nachrichten werden ausschließlich im flüchtigen Arbeitsspeicher (RAM) weitergeleitet und niemals auf Festplatten oder in Datenbanken gespeichert.

---

## Zentrale Sicherheitsarchitektur

- **Zweistufige Ende-zu-Ende-Verschlüsselung:** Nicht exportierbare `ECDH P-256`-Geräteschlüssel (WebCrypto) kombiniert mit ephemerem `ECDH P-256`-Schlüsselaustausch pro Nachricht, `HKDF-SHA-384`-Schlüsselableitung und `AES-256-GCM`-Verschlüsselung.
- **Schutz vor Verkehrsanalyse:** Festes 512-Byte-Padding verschleiert Nachrichtenlängen und Kommunikationsmuster.
- **Echtes Zero-Storage-Prinzip:** Weder Nachrichteninhalte noch Anhänge oder Gesprächsverläufe werden jemals auf dem Server gespeichert.
- **Anonyme Identitäten & kein IP-Logging:** Mitarbeiter-Identitäten werden vor der Speicherung durch gesalzene `HMAC-SHA256`-Hashes anonymisiert; sämtliche Client-IP-Adressen werden auf Infrastruktur-Ebene verworfen.
- **Strikte Rollentrennung:** Unternehmensadministratoren (`/org-admin`) verwalten Teams, freigegebene Mitarbeiter-Hashes und Sitzplatzkontingente, ohne jemals Zugriff auf kryptografische Schlüssel oder Klartextinhalte zu erhalten.

---

## Institutionelle Lizenz- und Bereitstellungsmodelle

SATR Enterprise wird ausschließlich über formelle B2B-Verträge lizenziert (ohne öffentliche Zahlungs-Gateways):

| Modell | Zielgruppe | Infrastruktur & Governance |
| :--- | :--- | :--- |
| **Enterprise Cloud** | Unternehmen, Kanzleien & regulierte Teams | Isoliertes Blind-Relay, jährlicher/halbjährlicher B2B-Vertrag mit Rechnung, strikte Sitzplatzbegrenzung und `/org-admin`-Verwaltung. |
| **Banking & Sovereign On-Premise** | Banken, Finanzinstitute und staatliche Stellen | Vollständig vom Internet getrennte (Air-Gapped) Docker-Bereitstellung im eigenen Rechenzentrum ohne ausgehenden Netzwerkverkehr sowie individuelles SLA. |

---

## Verifizierte Plattform-Vorschau

### 1. B2B Enterprise- & Banking-Lizenzportal
![B2B Enterprise- & Banking Licensing Portal](assets/01_landing_b2b_tiers.png)

### 2. Datenschutzkonforme Lizenzanfrage
*Erstellt eine strukturierte B2B-Vertragsanfrage lokal im Browser, ohne unverifizierte Kontaktdaten auf dem Blind-Relay zu speichern.*
![Privacy-Safe License Inquiry Modal](assets/02_license_inquiry_modal.png)

### 3. Strikte Durchsetzung der Sitzplatzgrenze
![Seat Limit Enforcement](assets/03_seat_cap_rejected.png)

### 4. Nicht-destruktive Kulanzfrist & Vertragsverlängerung
*Abgelaufene Lizenzen wechseln in eine konfigurierbare Kulanzfrist, in der bestehende Konten und Allowlists vollständig erhalten bleiben und nach Verlängerung sofort wieder freigeschaltet werden.*
![License Grace Period Banner](assets/04_grace_period_banner.png)
![License Renewal Restored](assets/05_renewal_restored.png)

---

## Lizenzierung & Kontakt

Für eine Evaluierung, Architekturberatung oder ein individuelles Banking-SLA nutzen Sie bitte direkt die Funktion **Request Enterprise License** im Plattform-Portal oder kontaktieren Sie den Entwickler über GitHub.