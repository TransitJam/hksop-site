# 🚨 Instant Illegal Parking Reporter

A lightweight, privacy-first, community-driven civic tool designed to generate rapid vehicle obstruction reports for the Hong Kong Transport Complaints Unit.

This app is a tool from Transit Jam, Hong Kong's trusted road safety advocacy team.

## 🛡️ Core Principles
- **Frictionless Design:** A "one-button reporting" concept. No downloads, account registrations, or complex setup steps for the user.
- **Absolute Privacy:** Functionally a completely static web page hosted via AWS Amplify. Contains no databases, cookies, or backend tracking scripts. All data processing occurs entirely within the sandboxed local browser window.

- **International Safe System Alignment:**
This application is built in complete accordance with the World Bank Global Road Safety Facility (GRSF) 2026 Management Guidelines, addressing critical data gaps and converting crowdsourced observations into standardised geographic datasets for automated institutional parsing.

## ⚙️ How the Logic Works (The Subroutine)
1. **The Trigger:** The user selects a violation category from a dropdown menu and taps the main button.
2. **The Query:** The browser requests device GPS coordinates via the HTML5 Geolocation API.
3. **The Variable Build:** JavaScript captures the raw Latitude, Longitude, and a local device timestamp (`new Date()`).
4. **The Action:** The script compiles the structured data into a secure `mailto:` string and opens the native device mail client, auto-populating the headers and message layout.

## 🚀 Deployment Pipeline
Automated CI/CD pipeline built on **GitHub Desktop** and **AWS Amplify**. Any code pushed to the `main` branch automatically builds and deploys to production globally within 60 seconds.
