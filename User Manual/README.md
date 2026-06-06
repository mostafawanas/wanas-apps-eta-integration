# 📖 Wanas Apps — User Setup & Usage Guide

Welcome to the **Wanas Apps ETA Integration Suite**! This step-by-step guide will help you install, configure, and use the integration to sign and submit invoices directly from **Zoho Books** to the **Egyptian Tax Authority (ETA) Portal**.

---

## 📋 Prerequisites

Before you start, make sure you have:
1. **Zoho Books Admin Access**: Admin rights are required to install and configure extensions.
2. **Physical USB Signature Token or Smart Card**: Issued by an authorized provider (e.g., *Egypt Trust* or *Misr El-Makasa*).
3. **USB Token Driver Installed**: Ensure the middleware software provided by your token issuer (e.g., *SafeNet Authentication Client*) is installed and running, and that it successfully detects your plugged-in USB token.
4. **Windows PC**: The local desktop companion application requires **Windows 10 or Windows 11 (64-bit)**.

---

## 🚀 Step 1: Install the Zoho Books Extension
1. Open your **Zoho Books** dashboard.
2. Go to **Settings** (Gear Icon) in the top-right corner, and select **Marketplace** > **All**.
3. Search for **"Wanas Apps ETA Integration"** (or use the direct onboarding installation link sent to your email).
4. Click **Install**, agree to the terms, and complete the installation wizard.

---

## 🖥️ Step 2: Install the Desktop Companion Client
*The desktop companion application is required to safely connect your physical USB signature token to your Zoho Books cloud platform.*

1. Log into your **Wanas Apps Client Portal** and download the latest Windows installer (`.msi`).
2. Run the installer and follow the prompt instructions.
3. Once installation completes, you will see the **Wanas Apps Companion** icon in your Windows System Tray (bottom-right corner, near the clock).
4. **Plug in your physical USB Token** to your computer.

---

## ⚙️ Step 3: Configure Settings in Zoho Books
1. In Zoho Books, navigate to **Settings** > **Extensions** > **Installed Extensions**.
2. Find the **Wanas Apps ETA Integration** and click **Configure**.
3. Under the **ETA Credentials** tab, input the following details:
   - **Taxpayer Registration Number**: Your company's 9-digit tax number.
   - **ETA Client ID** & **Client Secret**: Obtained from your official ETA taxpayer portal profile.
   - **Default Activity Code**: Your primary tax activity code.
   - **Branch ID**: Your branch registration ID (e.g., `0` for the main branch).
4. Click **Save Settings**.

---

## 💼 Step 4: Daily Workflow & Invoice Submission

### 1. Prepare Your Invoice
Create a standard Invoice, Credit Note, or Debit Note in Zoho Books as you normally do. Ensure the following details are complete:
- **Client Information**: For B2B invoices, fill out the customer's 9-digit Tax Registration Number. For B2C invoices exceeding the legal threshold, enter their National ID.
- **Item Mapping**: Ensure all invoice items have an assigned **EGS** or **GS1** code mapped to them.

### 2. Sign and Submit
1. Open the created invoice inside Zoho Books.
2. Click the **"Submit to ETA"** button on the top-right menu bar.
3. The desktop companion client will detect the action. If a signature is required, a secure prompt will appear on your desktop asking for your **USB Token PIN**.
4. Enter your PIN and click **Authorize**.

### 3. Check the Status
* The invoice banner inside Zoho Books will display a live status update:
  - ⏳ **Submitted / Pending**: Sent successfully, waiting for ETA processing.
  - ✅ **Accepted**: Validated and approved by the ETA portal.
  - ❌ **Rejected**: The banner will show a detailed list of exact validation errors (e.g., "Invalid item code", "Incorrect address format") so you can easily correct the invoice and try again.

---

## 🔧 Troubleshooting & Support

### ❓ The desktop companion app is not responding / Token not found
- Ensure your physical USB token is plugged in firmly.
- Check if your token utility tool (e.g., SafeNet Client) shows that the token is active.
- Verify that the Wanas Apps Companion app is running in your system tray (if not, search for "Wanas Apps Companion" in the Windows Start Menu and launch it).

### ❓ Invoice rejected due to "Invalid Tax Code"
- Open the items list in Zoho Books and check that the EGS/GS1 tax codes associated with the rejected item are correctly formatted and registered in the ETA portal.

### 📞 Contact Support
For additional assistance, feel free to submit a support ticket in your client dashboard or contact our technical support hotline.
