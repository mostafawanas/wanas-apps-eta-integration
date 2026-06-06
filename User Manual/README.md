# 📖 Wanas Apps — User Setup & Usage Guide

Welcome to the **Wanas Apps ETA Integration Suite**! This step-by-step guide will help you install, configure, and use the integration to sign and submit invoices directly from **Zoho Books** to the **Egyptian Tax Authority (ETA) Portal**.

---

## 📋 Prerequisites

Before you start, make sure you have:
1. **Zoho Books Admin Access**: Admin rights are required to install and configure extensions.
2. **Physical USB Signature Token or Smart Card**: An active USB hardware security module (e.g., ePass2003) or electronic seal.
3. **USB Token Driver Installed**: Ensure the middleware software provided by your token issuer (such as *SafeNet Authentication Client* or *ePass2003 Token Manager*) is installed and running, and detects your token.
4. **Windows PC**: The local desktop companion application requires **Windows 10 or Windows 11 (64-bit)**.

---

## 🔑 How to Obtain Your ETA USB Token (Egypt)

If your company does not yet have an active electronic signature or seal (E-Seal), you must obtain one through an officially licensed Certification Services Provider (CSP) authorized by **ITIDA** (Information Technology Industry Development Agency).

### 1. Authorized Providers (CSPs)
You can apply for and purchase your token (such as the standard ePass2003 hardware) through these official channels:
* **Egypt Trust**: The first and largest licensed provider in Egypt. You can apply at their main offices or select **Orange Egypt** business branches.
* **Fixed Egypt (FEDIS / Tawqe3y)**: Provides corporate digital signatures and electronic seal contracts through their "Tawqe3y" service.
* **El-Delta Trust**: Affiliated with El-Delta Electronic Systems and **WE (Telecom Egypt)**. You can submit requests and sign contracts at select WE customer centers across different governorates.
* **Misr for Central Clearing, Depository and Registry (MCDR)**: Authorized to issue digital certificates and electronic seals for corporate entities.

> [!TIP]
> **Convenient Tip**: To avoid visiting a primary CSP headquarters, you can check the nearest major **Orange** or **WE (Telecom Egypt)** business branch, as their partnerships allow them to handle verification, contract signing, and token delivery locally.

### 2. Company Document Checklist
To apply for your E-Seal, bring the following documents (both originals for review and copies):
* **Commercial Registry (سجل تجاري)**: Must be recently issued (within the last 3 months).
* **Tax Card (بطاقة ضريبية)**: Valid copy.
* **Articles of Incorporation (صحيفة الاستثمار/عقد التأسيس)**: Copy of company gazette or startup document.
* **National ID / Passport**: The ID of the company's legal representative.
* **Authorization Letter (تفويض)**: If the legal representative is not attending in person, you must provide a bank-validated authorization letter or a dynamic power of attorney allowing the delegate to sign the contract.

### 3. E-Seal Requirement & Standard Pricing
> [!IMPORTANT]
> **E-Seal (الختم الإلكتروني) vs. Digital Signature (التوقيع الإلكتروني)**
> For automated system-to-system integrations (like Zoho Books) submitting directly to the ETA portal, **you must obtain a Corporate E-Seal (الختم الإلكتروني)**. Individual Corporate Digital Signatures (التوقيع الإلكتروني) are registered to individual names and are **not** supported for direct ERP submission.

Below is the standard, regulated pricing structure across major providers (Egypt Trust, Fixed Egypt, and El-Delta Trust) which includes both the hardware token (physical ePass2003 device) and the issuance certificate (all taxes/VAT included):

#### Corporate E-Seal (الختم الإلكتروني) — *Required for Zoho Books*
| Validity Period | New Issuance (Includes Token + Certificate) | Renewal Price (Certificate Only) |
| :--- | :--- | :--- |
| **3 Months** (Temporary) | ~1,000 EGP | — |
| **1 Year** | ~2,000 to 2,500 EGP | ~1,800 EGP |
| **2 Years** | ~3,000 to 3,500 EGP | ~2,800 EGP |
| **3 Years** | ~4,000 to 4,500 EGP | ~3,800 EGP |

> [!TIP]
> * **Hardware Replacement**: If you lose or damage the physical USB token during your subscription, replacing the hardware costs a flat rate of **500 EGP**.
> * **The Multi-Year Advantage**: Choosing a **3-year bundle** saves significant overhead, as it eliminates the need to compile paper applications and visit physical branches annually for renewals.

---

## 🌐 Registering Your Company on the ETA Portal

To configure the integration, your company must be registered on the official Egyptian Tax Authority (ETA) e-Invoicing/e-Receipt portal. There are two ways to register: **Self-Registration (online using your E-Seal)** or **Off-line Registration (in-person via your local tax office)**.

Self-registration is highly recommended because it is instant and completely digital.

### Route A: Online Self-Registration (Recommended)
> [!IMPORTANT]
> **Prerequisites for Self-Registration**:
> - A computer running Windows 10 or Windows 11.
> - The E-Seal USB token driver installed and running.
> - Your E-Seal token plugged into the computer.

1. **Install the ETA Registration Tool**:
   - Plug your USB token into the computer.
   - Go to the official ETA portal: [invoicing.eta.gov.eg](https://invoicing.eta.gov.eg/).
   - Click the prompt to download and install the official ETA Digital Signature/E-Seal middleware utility.
2. **Start Portal Registration**:
   - On the portal homepage, click **"Start Registration"** (بدء التسجيل).
   - Enter your company's 9-digit **Taxpayer Registration Number**.
   - Accept the terms and click **Continue**.
3. **Digitally Sign the Request**:
   - Click **"Sign Now"** (التوقيع الآن).
   - In the pop-up window, select your corporate E-Seal certificate.
   - Enter your USB token PIN to authorize the signature.
4. **Add Business Details**:
   - Enter your official Company Email and Mobile Number.
   - Complete the verification by entering the OTP codes sent to your phone and email.
5. **Assign the Administrator**:
   - Enter the National ID, name, and email of your designated primary Administrator.
   - Click **Finish** to trigger an invitation email to their inbox.
6. **Set Password**:
   - Open the invitation email, click the link, and choose a secure password to activate the corporate profile.

### Route B: Manual Registration (In-Person via Tax Office)
If you cannot run the USB token middleware on your computer, you can register manually:
1. **Prepare Your Documents**:
   - Original and copies of your Tax Card and Commercial Registry.
   - A formal **Authorization Letter (خطاب تفويض)** printed on company letterhead, stamped with your bank signature verification. The letter must name the designated Administrator, their National ID, phone number, and email.
2. **Submit at the Local Office (المأمورية)**:
   - Bring these documents to your local tax office district. An agent will verify your papers and register your company in the system.
3. **Accept the Email Invitation**:
   - Within 48 hours, you will receive an invitation email. Click the link to set your password and access your profile.

---

## 🔑 Post-Registration: Generating Your Integration Keys
Once you are logged into your taxpayer portal dashboard, you must register your ERP system to get the credentials needed for the Zoho Books integration:

1. **Register the ERP System**:
   - Go to your portal profile settings.
   - Add a new **"ERP Integration"** to generate a unique **Client ID** and **Client Secret**. (Keep these safe, as you will enter them in Zoho Books).
2. **Register Your Products**:
   - Ensure your product inventory is registered on the portal using **GS1** codes or custom **EGS** codes linked to the Global Product Classification (GPC) system before you begin billing.

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
