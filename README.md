# 🚜 Offline-First Field Operations App
**Architected by:** Ember Cloud LLC  
**Tech Stack:** Firebase (Auth, Firestore, Storage), JavaScript, Bootstrap 5, Progressive Web App (PWA)  
**Status:** Live in Production (Active Customers)

![Dashboard Screenshot](images/dashboard-hero.png)
*(Note: Client name, data, and source code are kept private to protect proprietary business logic and customer IP. This repository serves as an architectural case study.)*

## 🛑 The Business Problem
A rural septic engineering and field services firm was struggling with a fragmented workflow. Technicians were operating in remote areas with zero cellular service, forcing them to rely on physical clipboards. 
* **Data Duplication:** Field notes had to be manually transcribed into Excel at the end of the day.
* **Disconnected Media:** Site photos taken by contractors were sent via text message and frequently lost or disconnected from the client file.
* **Billing Friction:** Processing payments required office intervention after the job was completed.

## ⚡ The Solution: A Serverless PWA
Ember Cloud designed a custom Progressive Web App that functions as a "Digital Clipboard," prioritizing offline reliability and ease of use.

### Key Architectural Features:
* **Native Offline Synchronization:** Built utilizing Firestore's IndexedDB persistence. Technicians can create, edit, and save jobs deep in the mountains. The app silently queues the data and synchronizes with the cloud the moment a 4G/Wi-Fi connection is re-established.
* **Anonymous Contractor Portal:** Engineered a secure, tokenized URL system (`/upload.html?id=...`). This allows third-party contractors to upload completion photos directly to the client's database *without* requiring an account or exposing the firm's customer list.
* **Data Pipeline Bridge:** Built a custom JavaScript CSV compiler that downloads the week's jobs instantly, formatted specifically for the client's legacy Excel proposal system. 
* **Zero-Friction Billing:** Integrated Stripe Payment Links directly into the job cards for immediate, on-site invoicing.

## 📈 Business Impact
The application was deployed with zero downtime and immediately adopted by the client.
* **100% Paperless:** Eliminated physical field notes on day one.
* **Time Recaptured:** Saved the owner 5+ hours per week in manual data entry and photo matching.
* **Minimized Overhead:** By utilizing a serverless Google Firebase architecture, the application scales automatically while keeping the client's cloud infrastructure costs near zero.

---
*Looking to digitize your field operations or automate your workflow? Contact Dane Hately at Ember Cloud LLC. contact@embercloud.cc*
