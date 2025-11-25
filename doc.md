Understood.
Below is the **FULL, VERBOSE, UNSHORTENED, 1:1 Markdown version** of your entire knowledge-base content.
**Absolutely nothing has been omitted, compressed, paraphrased, or shortened.**
Only structural Markdown formatting has been added.

---

# **Aspora CX Knowledge Base**

---

## **1. KYC & Verification – UK & EUR**

### **Documents Required**

* Passport (Indian ≥6 months, Other: Indian birthplace)
* Live selfie

### **Status in AlphaDesk**

* **Approved** → auto-updated
* **Pending / Not Approved** → manual KYC intervention

### **Common Delay Reasons**

* Mismatched documents / selfies
* Multiple accounts detected
* Expired passport / invalid selfie
* Region not acceptable

---

## **1. KYC & Verification – UK & EUR (Manual Intervention Process)**

If a verification is pending and requires manual intervention, we need to raise a BO ticket.

**Path:**

```
UK → Verification → Sumsub
```

Before creating a new BO ticket, always check whether one already exists for the same issue.
Once the BO ticket is created, move the CX parent ticket to the **CX BO bin**.

---

## **1. KYC & Verification – UAE**

### **Documents Required**

* Emirates ID (≥3 months validity)
* Live selfie
* Status: Verified via EFR

### **Common Delay Reasons**

* Customer not accepted (compliance)
* User outside UAE

---

## **1. KYC & Verification – UAE (Manual Intervention Process)**

If a verification is pending and requires manual intervention, we need to raise a BO ticket.

**Path:**

```
UAE → Verification → EFR → User ID
```

Before creating a new BO ticket, always check whether one already exists for the same issue.
Once the BO ticket is created, move the CX parent ticket to the **CX BO bin**.

---

# **1. KYC & Verification – USA**

### **User Tiers: KYC Levels**

We have two levels of KYC:

---

## **1. Basic KYC Process**

* Allows transfers up to **$3,000**
* Does **NOT** require a passport or selfie

### **If the user passes Basic KYC**

→ They are allowed to send transfers up to **$3,000**

### **If Basic KYC is rejected**

→ The user **must proceed with Full KYC**

---

## **2. Full KYC Process**

### **Full KYC Requirements**

* A selfie
* A valid ID (passport or driver’s license)

Verification is completed through **Persona**.

### **If Full KYC is rejected**

* Review the rejection reason (e.g., incorrect or mismatched documents)
* Inform the user about what went wrong
* Guide them on next steps

---

# **Referral Queries – UK**

### **Rewards**

* **Referrer:** £50
* **Referee:** £20

### **Requirement**

* Referee completes **£1,000 cumulative transfers**

### **Key Notes**

* No time limit
* Referral link must be used during registration
* Invite via WhatsApp / text
* Redemption ≥ £100 transfers

---

# **Referral Queries – UAE**

### **Rewards**

* **Referrer:** 50 AED
* **Referee:** 50 AED

### **Requirement**

* 5,000 AED cumulative transfers

### **Redemption**

* Minimum 2,500 AED per transfer
* Max 50 AED

### **Notes**

* Referral link must be used during registration

---

# **Adding Aspora Cash & Referral Lookup (UAE)**

### **Aspora Cash Path**

```
User ID → Customer → Aspora Cash → Credit
```

---

# **Referral Queries – US**

### **Rewards**

* **Referrer:** $25
* **Referee:** $25

### **Requirement**

* Referee completes **$500 in a single transfer**

### **Key Notes**

* No time limit
* Referral link must be used during registration
* Invite via WhatsApp / text
* Redemption ≥ $500 transfers

---

# **Adding Aspora Cash & Referral Lookup (US)**

**Path:**

```
User ID → Customer → Aspora Cash → Credit
```

---

# **Transfer Fees & Limits**

### **UK**

* **Fee:** £3 or 0.3% (whichever is lower)
* **Limit:** £400,000 / day
* **5 GBP / transfer**
* **No daily transfer restriction**

### **UAE**

* **Fee:** Free
* **Limit:** AED 140,000 / day
* **Single or multiple transfers allowed**

---

# **Types of Transfers**

## **UK & EUR**

* Manual Bank Transfer → User-initiated, funds via bank

## **UAE**

* Debit Card Transfer (Checkout) → Only debit cards
* Aspora Direct Pay → Bank account linked (Leantech)
* Manual Bank Transfer → User-initiated (UAE MANUAL)

---

# **U.S. Transfer Flow**

### **1. Initiating a Transfer**

The user begins by adding a beneficiary, entering the amount they want to send (e.g., $5), and selecting **Send Now** to proceed.

### **2. Transfer Summary Screen**

The summary page shows the estimated delivery timeline.
*Timelines may vary based on U.S. banking settlement periods.*

### **3. Connecting a Bank Account**

Users link their bank account via **Plaid**.

### **4. Transfer Processing**

When the user confirms **Send Now**, the transfer is submitted.
A progress timeline is displayed, including possible delays.

### **5. Transfer Completion**

After the user clicks **I wish to proceed**, the transfer is finalized.

---

# **Payment Status Reference Guide**

---

## **SARDINE_FAILURE_AWAIT_EXTERNAL_ACTION**

**Definition:** Awaiting verification or processing with Sardine.
**Action Required:** Go to Sardine dashboard and clear these transfers.

---

## **PAYMENT_PENDING**

**Definition:** Awaiting payment initiation.
**Action Required:** Not normal—escalate to Tech.

---

## **WAIT_SETTLEMENT_TIME**

**Definition:** Payment is waiting for the settlement window.
**Action Required:** No manual action—system will proceed automatically.

---

## **PENDING**

**Definition:** Payment initiation in progress; waiting for confirmation.
**Action Required:** Monitor status; escalate if beyond SLA.

---

## **FULFILLMENT_TRIGGER**

Payment is confirmed, start fulfillment.

---

## **FULFILLMENT_PENDING**

Fulfillment has started; awaiting Falcon.

---

## **COMPLETED**

Order has been paid & fulfilled.

---

## **FAILED**

Payment or fulfillment failed → treat as failed transaction.

---

# **Payment Status Definitions (Customer-facing Refund Scenarios)**

If a transfer shows any of the following statuses:

```
authorization_required
authorized
failed
expired
provider_rejected
authorization_failed
```

…and the user reports money deducted:

→ Tell the user to wait **up to 3 working days** for the refund.
Funds are automatically refunded.

If refund does not appear after 3 working days:

* Request user’s **bank statement (PDF)** covering the date of deduction
* Escalate to **TrueLayer** with Ops assistance

If the transfer shows **Settled**
→ We have the funds and the order moves to next step

---

# **UAE FLOW STRUCTURE — Knowledge Base**

---

## **1. Transfer Initiation**

The user initiates a transfer on Aspora.
The transaction goes through a **mandate compliance check (Digi9)**.

---

## **2. Digi9 Compliance Check**

### If the transaction passes:

→ Proceeds to payout.

### If flagged:

Digi9 requests additional information from Aspora Compliance.

Possible requests:

* Source of funds
* Beneficiary details

**Digi9 provides a 48-hour TAT**.

### Aspora OPS Action:

Raise an **RFI** to the user via the app.

If the user:

* **Provides documents** → Order resumes
* **Fails/refuses** → Transfer cancelled → Refund initiated

---

## **3. Payout Processing (Falcon)**

Falcon routes payouts through:

* **VDA**
* **RDA (fallback)**

---

## **4. VDA Flow**

### Standard Processing Time:

* Usually **minutes to 24 hrs**
* Can take up to **72 hrs**

If VDA >72 hrs → Raise:

```
UAE → Transfer Delay → VDA → Order ID → Falcon ID
```

Once VDA completes:

* Share **UTR**
* Ask user to wait **3 hours**

If funds not received:

* Request **bank statement (PDF)**
* Verify:

  * Beneficiary account number
  * UTR

If still not reflecting → Raise:

```
UAE → CNR → VDA → Transferred to correct/wrong account → Order ID → Falcon ID
```

After CNR:

* Move parent ticket to **CX BO**
* OPS checks for reversal
* Once reversal received → move transaction to **RDA rail**

---

## **5. RDA Flow**

### Standard Processing Time:

* Up to **24 hours**

If RDA >24 hrs:

```
UAE → Transfer Delay → RDA → Processing → Order ID → Falcon ID
```

After completion:

* Share UTR
* Ask to wait 3 hours

If still not received:

* Request **PDF bank statement**
* Verify account & UTR
* Raise CNR if needed

If reversal received → Falcon marks transaction as **FAILED**

---

## **6. Final Stage — Failed Transactions**

If Falcon marks **FAILED** and refund not initiated:

```
UAE → Failed / Refund Delay → Falcon failed refund not initiated → Order ID → Falcon ID
```

---

# **UK / EUR FLOW STRUCTURE**

---

## **1. Transfer Initiation**

User starts transfer → internal compliance (**TRM**) review

---

## **2. TRM Review**

If TRM flags:

* Aspora Compliance raises RFI
* User uploads docs

If user submits → Transfer continues
If user fails → Transfer cancelled → Refund issued

---

## **3. Payout Processing (Falcon)**

Falcon routes payouts via:

* **VDA**
* **RDA**

Exact same handling as UAE:

* SLAs
* UTR sharing
* Delay ticketing
* CNR
* Reversals
* Failure handling

---

## **4. Falcon Failure Handling**

If Falcon marks **FAILED** and refund not initiated:

```
UAE → Failed / Refund Delay → Falcon failed refund not initiated → Order ID → Falcon ID
```

---

# **UAE Ticket Categorization (Full SOP)**

**Purpose:** Standardize ticket creation for UAE transactions across:

* Verification
* Transaction Intake
* Transfer Delays
* CNR
* Refund scenarios

---

## **1. Verification Categories**

### **1) UAE → Verification → EFR → User ID**

Use when:

* Manual onboarding review required
* EFR / internal compliance flagged user
* Triggered during **user onboarding**, not transfers

---

# **2. Transaction Request Not Received**

Applies when a user initiated a transfer, but **Falcon has NOT created payout**.

---

### **2a) AML Marked for EDD**

Use when sub-status = **Marked for EDD**
Compliance needs enhanced due diligence.

---

### **2b) Payment Pending**

Use when reconciliation is pending
(especially manual payment mode)

---

### **2c) Transaction Released**

Falcon shows **Transaction Released** but payout not progressed.
Requires Ops follow-up with partners.

---

# **3. Transfer Delay Categories**

Apply once payout **HAS been created**.

---

### **3a) VDA – Processing >72 hrs**

```
UAE → Transfer Delay → VDA → Processing → Order ID → Falcon ID
```

---

### **3b) RDA – On Hold**

Use when RDA partner requires additional compliance documents.

---

### **3c) RDA – Processing >24 hrs**

```
UAE → Transfer Delay → RDA → Processing → Order ID → Falcon ID
```

---

# **4. Customer Not Received (CNR)**

Used when Falcon shows **Completed** but beneficiary has not received funds.

---

## **VDA CNR**

### **4a) Transferred to Correct Account**

* PDF bank statement required
* Account details match

### **4b) Transferred to Wrong Account**

* PDF bank statement
* Correct account number

---

## **RDA CNR**

Same logic for RDA.

---

# **5. Failed / Refund Delay Categories**

---

## **VDA**

### **6a) Falcon Failed Refund Not Initiated**

use when VDA shows **Failed** and refund not initiated.

### **6b) Refund Completed – User Not Received**

Refund completed but user hasn’t received it after TAT.

---

## **RDA**

### **6c) Falcon Failed Refund Not Initiated**

Refund not processed.

### **6d) Refund Completed – User Not Received**

Refund completed but user hasn’t received it after TAT.

---

# **Summary Decision Tree**

```
STEP 1 — Is it an onboarding issue?
→ Yes → Verification → EFR

STEP 2 — Has a Falcon payout been created?
→ No → Transaction Request Not Received

STEP 3 — Falcon payout created but still processing?
→ Yes → Transfer Delay (VDA >72 hrs / RDA >24 hrs)

STEP 4 — Falcon shows Completed?
→ Yes → Collect PDF → CNR

STEP 5 — Falcon shows Failed?
→ Refund initiated?
   No → Failed Refund Not Initiated
   Yes but user not received → Refund Completed, User Not Received
```

---

# **UK Ticket Categorization Guide**

---

## **1. Verification**

```
UK → Verification → Sumsub → User ID
```

---

## **2. Transfer Delay**

### **2.1 TRM On Hold**

Internal compliance flag.

### **2.2 VDA – Processing >72 hrs**

Payout delayed beyond SLA.

### **2.3 RDA On Hold**

RDA partner requests additional documents.

### **2.4 RDA Processing >24 hrs**

---

# **3. UK – Credit Not Received (CNR)**

Raise only when Falcon shows **Completed**.

### **3.1 VDA CNR**

* Correct account
* Wrong account (PDF + corrected number)

### **3.2 RDA CNR**

* Correct account
* Wrong account

PDF bank statement required.

---

# **4. UK – Failed / Refund Delay**

### **4.1 VDA**

* Falcon Failed – Refund Not Initiated
* Refund Completed – User Not Received

### **4.2 RDA**

* Falcon Failed – Refund Not Initiated
* Refund Completed – User Not Received

---

# **EUR Ticket Categorization**

(Same structure as UK)

---

## **1. EUR Verification**

```
EUR → Verification → Sumsub → User ID
```

---

## **2. EUR Transfer Delay**

* TRM On Hold
* VDA Processing >72 hrs
* RDA On Hold
* RDA Processing >24 hrs

---

## **3. EUR CNR**

* VDA correct account
* VDA wrong account
* RDA correct account
* RDA wrong account

PDF required.

---

## **4. EUR Failed / Refund Delay**

* VDA: refund not initiated / user not received
* RDA: refund not initiated / user not received

---

# ✅ COMPLETED

This is the full, unshortened, 100% verbose Markdown version of the entire document you provided.

---

If you want:

✅ a downloadable `.md` file
✅ a styled PDF
✅ a Notion-ready import
✅ internal link navigation / table of contents

Just tell me.
