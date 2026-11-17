# Privacy Policy for Navkar Dispatch NALLP

**Last Updated:** November 16, 2026  
**Effective Date:** November 16, 2026  
**Application ID:** `com.navkardishpatch.llp`  
**Developer / Organization:** Navkar Apotek LLP  

---

## 1. Introduction

Welcome to **Navkar Dispatch NALLP**. This Privacy Policy explains how **Navkar Apotek LLP** ("Company", "we", "us", or "our") collects, uses, stores, and protects information when warehouse dispatchers and authorized operational personnel use our Android application **Navkar Dispatch NALLP** (the "Application" or "App").

Navkar Dispatch NALLP is an enterprise operational tool designed for pharmaceutical dispatch verification, invoice verification, warehouse logistics, and delivery tracking. 

---

## 2. Information We Access, Collect, and Process

### A. Camera and Visual Sensor Data
* **Camera Access (`android.permission.CAMERA`):** The Application requires access to your device's camera exclusively for real-time scanning of:
  * Company printed Bill QR codes / 1D barcodes (`YYYY-MM-DD + Series + Bill Number`).
  * Pharmaceutical product packages and carton barcodes (EAN-13, EAN-8, UPC-A, UPC-E, Code 128, Code 39, Code 93, Data Matrix, ITF).
* **Processing Model:** Barcode decoding is performed **locally on your device** using Google ML Kit Barcode Scanning. The camera video feed and raw image frames are processed in-memory and are **never recorded, photographed, stored permanently on disk, or transmitted to external servers**.

### B. Warehouse Staff & Dispatcher Identification
* **Dispatcher Information:** The Application allows the warehouse supervisor or operator to select or input the name of the warehouse employee conducting the dispatch session (e.g., "Vijay Patole").
* **Purpose:** This name is recorded locally in dispatch records to maintain accountability for which staff member scanned, loaded, and verified the parcels.

### C. Commercial Invoices, Billing, and Medical Store Data
* **Commercial Records:** When a bill QR is scanned or synchronized, the Application queries the company dispatch server to retrieve:
  * Bill Number, Series Code, and Bill Date.
  * Customer / Medical Store Name and Town/Place (e.g., "Pradeep Medicals, Baramati").
  * Total invoice amount and designated transporter/bus service name.
  * Dispatch workflow status (e.g., Started Picking, Packed, Dispatched, Delivered).
* **Customer Directory:** The Application synchronizes the Account Master directory (`/api/AcMaster`) containing customer account codes (`accode`), registered trading names (`acname`), geographic location (`place`), and GSTIN (`gstno`).

### D. Device and Technical Information
* **Network State (`android.permission.ACCESS_NETWORK_STATE`, `android.permission.INTERNET`):** Used to check whether the device has an active Wi-Fi or cellular data connection to determine whether to fetch live server updates or operate in offline mode.
* **No Device Fingerprinting:** We do not collect advertising IDs (AAID), IMEI, MAC addresses, telephony metadata, or personal browser histories.

---

## 3. How Information is Used

The data accessed or processed by Navkar Dispatch NALLP is used solely for core operational purposes:
1. **Dispatch Accuracy:** Verifying that the correct pharmaceutical parcels and products are loaded for each customer bill.
2. **Double-Scan Prevention:** Ensuring that the same bill or product barcode is not inadvertently scanned multiple times.
3. **Status Workflow:** Updating parcel state from *Pending Loading* to *Loaded* and *Delivered*.
4. **Offline Resilience:** Storing local copies of customer lists and dispatch logs in the on-device Room database so warehouse operators can continue scanning when Wi-Fi is weak or disconnected.

---

## 4. Backend Communication and Data Transfer

* **Server Endpoint:** The Application communicates over encrypted HTTPS with the company dispatch server:  
  `https://dispatch-api.navkarapotek.com`
* **Transport Encryption:** All communications with the server use Transport Layer Security (TLS 1.2 / TLS 1.3) through Cloudflare Edge. Unencrypted cleartext HTTP traffic is completely disabled within the application.
* **Architecture Clarification:** Network transmission is direct between the mobile application and the designated company dispatch server.

---

## 5. Third-Party Services and Analytics

* **No Advertising:** Navkar Dispatch NALLP contains zero advertisements. We do not integrate ad networks (AdMob, Unity, etc.).
* **No Marketing Trackers:** We do not use third-party user behavior trackers, cross-site trackers, or commercial telemetry SDKs.
* **Local Machine Learning:** Optical barcode scanning is powered by the Google ML Kit client library, operating on-device.

---

## 6. Local Storage, Data Retention, and Deletion

* **Local Database:** Dispatch history, employee names, and cached customer directories are stored locally in an encrypted/private SQLite database managed by Android Room (`bill_database`).
* **Operator Data Deletion:** Users can purge local dispatch records at any time by using the "Clear All Dispatches" feature within the Application.
* **Server Retention:** Server-side invoice records and billing histories are maintained in accordance with Indian commercial tax, pharmaceutical regulations, and statutory accounting rules.

---

## 7. Children's Privacy

Navkar Dispatch NALLP is strictly an internal enterprise workplace application for wholesale warehouse employees and logistics staff. It is not directed to, marketed to, or designed for children under the age of 13 (or under the age of 18). We do not knowingly collect information from children.

---

## 8. User Rights and Choices

* **Camera Permission:** You may grant or revoke camera permissions at any time via Android System Settings (`Settings > Apps > Navkar Dispatch NALLP > Permissions`). If revoked, barcode scanning will be disabled, but historical cached records remain viewable.
* **Data Inquiries:** For questions regarding customer records or account listings displayed within the directory, warehouse staff may contact the internal system administrator.

---

## 9. Contact Information

If you have any questions, feedback, or concerns regarding this Privacy Policy or our operational data handling, please contact us:

* **Company Name:** Navkar Apotek LLP  
* **Operational Facility:** Ahmedabad / Baramati, India  
* **Privacy Officer / Contact Email:** `[INSERT_OFFICIAL_CONTACT_EMAIL]` *(e.g., support@navkarapotek.com)*  
* **Phone:** `[INSERT_OFFICIAL_CONTACT_PHONE]`  
* **Official Website:** `https://navkarapotek.com` *(or company corporate portal)*  

---

## 10. Changes to this Privacy Policy

We may update this Privacy Policy from time to time to reflect operational or regulatory adjustments. Changes will be posted in this document and reflected in the Application release notes.
