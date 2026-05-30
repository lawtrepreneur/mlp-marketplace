# mlp-docgen-ontario-affidavit — README

© 2026 Lawtrepreneur Inc. All rights reserved.
Licensed under CC BY-NC 4.0 — see LICENSE file for details.

---
## Quick Start

This skill generates **court-ready Ontario affidavits** from organized facts. It converts fact summaries into sworn statements with:

- ✅ Ontario Rules of Civil Procedure compliance
- ✅ Role-based terminology (Landlord, Tenant, Employer, etc.)
- ✅ **Defined terms in Bold Title Case** (the "**Property**", the "**Rent**")
- ✅ All sensitive data protected via placeholders
- ✅ AI writing patterns automatically detected and removed
- ✅ **Affirm as default oath clause** (swear available as alternative)
- ✅ Legally sufficient format (immediate filing readiness)

---

## Two Modes

### **Detect Mode**
Flag AI writing patterns in your facts *before* generating the affidavit.

**When to use:**
- You want to review and approve suggested changes to your facts
- You want visibility into what gets cleaned up
- You're uncertain about AI-ism patterns and want to learn

**Process:**
1. Paste your facts or upload a file
2. Select `detect`
3. Review flagged AI-isms with suggested rewrites
4. Approve/reject each suggestion
5. Proceed to generate when confirmed

### **Generate Mode** (Default)
Produce a clean affidavit directly with silent AI-ism removal.

**When to use:**
- You want speed (no review loop)
- You trust the system to handle AI-ism removal
- Your facts are already clean

**Process:**
1. Paste your facts or upload a file
2. Select `generate` (or default)
3. Receive clean affidavit + placeholder reference key

---

## What You Provide

1. **Deponent's role**
   - Example: Landlord, Tenant, Employer, Creditor, Witness, Manager, Accountant, etc.

2. **Subject matter**
   - Example: "Non-payment of rent," "Wrongful termination," "Breach of contract"

3. **Facts** (organized list or narrative)
   - Pasted directly or uploaded as CSV, Word doc, PDF, plaintext

4. **Special instructions** (optional)
   - Tone, format, scope, custom headings, detail level, oath preference (affirm or swear)

5. **Mode** (optional; default is generate)
   - `detect` or `generate`

---

## What You Receive

### 1. **AFFIDAVIT OF [ROLE]**
- Clean, direct language (no hedging)
- One fact per paragraph
- All sensitive data bracketed
- **Key terms defined on first use in Bold Title Case** (the "**Property**")
- Role terminology used consistently
- Ontario-compliant formatting
- **Affirm as default oath clause** ("I, [NAME], do affirm that:")
- Oath clause and signature block ready for execution
- All AI writing patterns removed

### 2. **PLACEHOLDER REFERENCE KEY**
- Map each [BRACKETED_TERM] to its data type
- Map each defined term (e.g., **Property** = [RENTAL_PROPERTY_ADDRESS])
- Instructions for filling blanks

---

## AI-Ism Detection: What Gets Flagged & Removed

### Hedging & Vague Attribution
| ❌ AI-ish | ✅ Affidavit Version |
|----------|-------------------|
| "It appears that the tenant may not have paid rent" | "The tenant has not paid rent" |
| "It's understood that payment was not received" | "No payment was received" |
| "Studies show that tenants often delay payment" | [Removed — hearsay] |

### Promotional Language
| ❌ AI-ish | ✅ Affidavit Version |
|----------|-------------------|
| "a vibrant dispute over rental payments" | "a dispute over rental payments" |
| "marking a pivotal moment" | [Removed — irrelevant] |
| "the thriving property ecosystem" | "the rental property" |

### Copula Avoidance
| ❌ AI-ish | ✅ Affidavit Version |
|----------|-------------------|
| "The situation features a delay in payment" | "Payment is overdue" |
| "serves as a lease agreement" | "is a lease agreement" |
| "The property boasts three bedrooms" | "The property has three bedrooms" |

### Filler & Vague Phrases
| ❌ AI-ish | ✅ Affidavit Version |
|----------|-------------------|
| "In terms of the payment situation..." | "Regarding payment..." |
| "It's important to note that..." | [Removed] |
| "Moreover, the tenant continues to default" | "The tenant continues to default" |

---

## Example: Landlord-Tenant Non-Payment

### Input Facts

```
Role: Landlord
Subject: Non-payment of rent

Facts:
- Property at 123 Main Street, Toronto, ON M5V 3A8
- Lease with Jane Doe signed January 1, 2023
- Monthly rent is $1,500
- Last payment November 30, 2023 ($1,500 cheque #1087)
- No payment for December 2023 or January 2024
- Total owing is $3,000
- Notice sent January 15, 2024
- No response yet
```

### Output: Affidavit

```
AFFIDAVIT OF LANDLORD

I, [LANDLORD_NAME], of [LANDLORD_ADDRESS], [OCCUPATION], do affirm that:

FACTS:

1. I am the landlord of the rental property located at [RENTAL_PROPERTY_ADDRESS] 
   (the "**Property**").

2. On [LEASE_START_DATE], I entered into a lease agreement with [TENANT_NAME] 
   for the rental of the **Property** at a monthly rent of [MONTHLY_RENT_AMOUNT] 
   (the "**Rent**").

3. The lease (the "**Lease**") required [TENANT_NAME] to pay the **Rent** on the 
   first of each month.

4. [TENANT_NAME] made regular **Rent** payments from [LEASE_START_DATE] through 
   [LAST_PAYMENT_DATE].

5. The last payment received from [TENANT_NAME] was [LAST_PAYMENT_AMOUNT] on 
   [LAST_PAYMENT_DATE], paid by cheque number [CHEQUE_NUMBER].

6. As of [AFFIDAVIT_DATE], [TENANT_NAME] has not paid the **Rent** for the months 
   of [UNPAID_MONTHS], totalling [TOTAL_UNPAID_AMOUNT].

7. On [DATE_OF_NOTICE], I sent [TENANT_NAME] written notice of the rent arrears.

8. Despite the notice, [TENANT_NAME] has not made any payment or contacted me.

9. As of the date of this affidavit, [TENANT_NAME] remains in default of the **Lease**.

SIGNATURE BLOCK:

Sworn/Affirmed before me at the
City of Toronto, Ontario
this [DATE] day of [MONTH], [YEAR].

_____________________________    _____________________________
Commissioner for Oaths         [LANDLORD_NAME]

Signature: ____________________
```

### Output: Reference Key

```
PLACEHOLDER REFERENCE KEY

Role Terms:
- [LANDLORD_NAME] = Your full legal name
- [TENANT_NAME] = Tenant's full legal name

Sensitive Data Placeholders:
- [LANDLORD_ADDRESS] = Your residential address
- [OCCUPATION] = Your profession/title
- [RENTAL_PROPERTY_ADDRESS] = 123 Main Street, Toronto, ON M5V 3A8
- [LEASE_START_DATE] = January 1, 2023
- [MONTHLY_RENT_AMOUNT] = $1,500.00
- [LAST_PAYMENT_DATE] = November 30, 2023
- [LAST_PAYMENT_AMOUNT] = $1,500.00
- [CHEQUE_NUMBER] = #1087
- [UNPAID_MONTHS] = December 2023, January 2024
- [TOTAL_UNPAID_AMOUNT] = $3,000.00
- [DATE_OF_NOTICE] = January 15, 2024
- [AFFIDAVIT_DATE] = [Date you will sign]
- [DATE] = Day of signing (e.g., "20")
- [MONTH] = Month name (e.g., "March")
- [YEAR] = Year (e.g., "2024")

Defined Terms (Key Terms Defined on First Use):
- **Property** = The rental property located at [RENTAL_PROPERTY_ADDRESS]
- **Rent** = Monthly rental fee of [MONTHLY_RENT_AMOUNT]
- **Lease** = The lease agreement dated [LEASE_START_DATE] with [TENANT_NAME]
```

---

## Affirm vs. Swear

**Default: Affirm** — "I, [NAME], of [ADDRESS], [OCCUPATION], do **affirm** that:"

Affirm is the standard oath clause and does not require religious swearing-in. It is neutral, professional, and universally acceptable.

**Alternative: Swear** — "I, [NAME], of [ADDRESS], [OCCUPATION], do **swear** that:"

Use swear only if you have a specific reason to do so (e.g., religious or jurisdictional preference). Specify in special instructions if you prefer "swear" over "affirm."

---

## Edge Cases & Troubleshooting

### **Issue: I uploaded a CSV but facts seem incomplete**
- Ensure CSV has three columns: Date, Description, Amount
- Or paste facts as narrative/list
- The skill parses provided content; ambiguous rows will be flagged

### **Issue: The affidavit is missing a fact I provided**
- Check if the fact was vague or multi-part (may be split)
- If a fact was removed (e.g., "experts believe"), it was flagged as speculation/hearsay
- Review and request revision if needed

### **Issue: I need Small Claims Court format**
- Mention "Small Claims Court" in special instructions
- The skill will adjust formatting per Small Claims requirements
- **Always verify with your local court rules before filing**

### **Issue: The placeholder names don't match my preference**
- Standard naming is used (e.g., [LANDLORD_NAME], [TENANT_NAME])
- You can rename placeholders in the reference key before filling
- Or request custom naming in special instructions

### **Issue: The affidavit is too long or too short**
- Too long: specify "brief format" in special instructions
- Too short: specify "comprehensive detail" and provide more context
- The skill adjusts to your input

### **Issue: I'm not sure if my facts are AI-generated**
- Use `detect` mode; it will flag any AI patterns
- Review the suggestions; approve the clean versions
- Clean writing is safer in legal documents

### **Issue: Can I use this affidavit as-is for court filing?**
- **No.** Before filing:
  1. Fill all placeholders with actual data
  2. Have it reviewed by counsel
  3. Verify formatting against your court's rules
  4. Appear before a Commissioner for Oaths to swear/affirm
  5. Have commissioner sign and stamp
  6. Attach required exhibits
  7. File per court procedure

### **Issue: I want to use "swear" instead of "affirm"**
- Specify "use swear instead of affirm" in special instructions
- The skill will replace "affirm" with "swear" throughout

---

## Limits & Disclaimers

- **Not a substitute for legal counsel.** Have a lawyer review before filing.
- **Ontario only.** Applies Ontario Rules of Civil Procedure; other jurisdictions differ.
- **Personal knowledge.** All facts must be within the deponent's personal knowledge (not hearsay).
- **Sensitive data protection.** You identify all data to be placeholdered; the skill provides standard categories.
- **Court-specific formats.** Small Claims, Superior Court, and Commercial List may have nuances. Verify against court rules.
- **No legal strategy.** This skill generates documents, not legal advice or representation.
- **Exhibits.** If you reference exhibits, prepare and attach them separately.

---

## Common Use Cases

### **Landlord-Tenant Disputes**
- Non-payment of rent
- Breach of lease terms
- Wrongful eviction
- Security deposit disputes

### **Employment**
- Wrongful termination
- Unpaid wages
- Workplace harassment
- Non-competition breach

### **Commercial**
- Breach of contract
- Unpaid invoices
- Supplier disputes
- Non-delivery

### **Creditor Claims**
- Unpaid loans
- Credit card debt
- Cheque default
- Promissory note default

### **Witness Statements**
- Accident or incident documentation
- Property damage observations
- Contract performance confirmation
- Character witness statements

---

## Integration with Other Skills

**Want to review or strengthen your affidavit after generation?**

- **legal-writing-coach** — Audit for tone, precision, argumentative strength
- **appellate-advocacy-writer** — Strengthen claims if advancing to appellate level
- **doc-coauthoring** — Iterate on structure or scope with feedback

Use these *after* generating your affidavit if you need additional polish.

---

## Tips for Best Results

1. **Provide clear, organized facts** — Structured lists work best
2. **Identify sensitive data upfront** — Names, addresses, amounts, dates, contact info
3. **Specify your role clearly** — "Landlord," "Employer," "Creditor," etc.
4. **Use detect mode if uncertain** — See what gets flagged without commitment
5. **Attach files for complex facts** — Upload CSV, Word doc, or PDF
6. **Provide dates and amounts** — Specificity is legally stronger
7. **State facts you personally know** — Avoid secondhand information
8. **Review the generated affidavit** — Ensure all facts are accurately represented
9. **Get legal review before filing** — Non-negotiable
10. **Swear/affirm before commissioner** — Required; don't skip
11. **Specify oath preference** — Default is "affirm"; say "use swear" if needed

---

## Questions?

- **Placeholder mapping:** Review the Reference Key section
- **Flagged AI-isms:** Check the "AI-Ism Detection" section
- **Ontario compliance:** Verify Rules of Civil Procedure in your court rules
- **Sensitive data:** Identify all personal/financial/identifying information upfront
- **Affirm vs. Swear:** Default is affirm; specify in instructions if you prefer swear
- **Legal strategy:** Consult with a lawyer; this skill generates documents only

---

**Ready to generate your Ontario affidavit?**

Provide: Deponent role, subject matter, facts (list or file), special instructions (including oath preference: affirm or swear), and mode (detect or generate).

The skill will deliver a clean, legally sound, court-ready affidavit with all sensitive data protected, key terms defined in **Bold Title Case**, and all AI writing patterns removed.
