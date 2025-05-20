# Proposal-Bond-Whitelist-Integration-for-Vultisig
Proposal: Bond Whitelist Integration for Vultisig + Thorchain

## Objective
Enable a secure and streamlined path for new Bond Providers (BPs) to onboard into Thorchain by integrating a **"Request Whitelist"** button in the Vultisig wallet. This approach ensures bonding is gated by trusted node operator approval, with a smooth user interface and high-integrity gatekeeping.

---

## 🔧 Key Components

### 1. **"Request Whitelist" Button (in Vultisig)**
- **Location:** Under the **Functions tab**, directly **next to the Bond button**.
- **Conditional Display:** Only visible to wallets holding **≥ 5,000 RUNE**.
- When clicked, users can submit a request to be whitelisted as an eligible bond provider.

**Request Payload:**
- Wallet address
- Intended bond amount
- Optional message for context

---

### 2. **Whitelist Eligibility Threshold**
- The **Request Whitelist** function is **only available to users holding ≥ 5,000 RUNE** in their wallet.
- This prevents spam, discourages unserious applicants, and maintains a clean approval pipeline.

---

### 3. **Trusted Node Operator Review**
Whitelist requests are only sent to node operators meeting one or more of the following criteria:
- **Top 10 longest-standing active nodes**
- **Top 10 highest-performance nodes** (based on uptime and slashing metrics)

This ensures requests are evaluated by experienced, high-integrity participants in the network.

---

### 4. **Approval Flow**
- Node operators receive and review whitelist requests via a portal, backend, or message-based interface.
- They can **Approve** or **Reject** a request.
- A **multi-approval threshold** may be used (e.g. 3 out of 10 operators must approve).

Once approved:
- The address is whitelisted (on-chain or off-chain via signed consensus).
- Vultisig displays a status update: **"Approved to Bond"**.

---

### 5. **Bonding Action**
- Once whitelisted, the user can return to the **Functions tab** and click **Bond**.
- Vultisig validates the whitelist status before allowing bonding to proceed.

---

## 💡 Optional Enhancements
- **Whitelist timeout** (e.g. expires after 48 hours).
- UI indicators for:
  - "Pending Approval"
  - "Approved to Bond"
  - "Rejected"
- Notification system (email or in-app).
- Transparency dashboard showing recent whitelist requests and approval stats.

---

## ✅ Benefits
- **Security-focused onboarding**: Whitelisting deters malicious or careless bonding.
- **Reputation-based approval**: Only vetted node operators control who joins.
- **Frictionless UX**: New users stay within Vultisig for the full bonding journey.
- **Integrity-preserving decentralization**: Uses a distributed, high-trust operator subset.
- **Scales Thorchain safely**: Welcomes serious participants while protecting network security.

---

## 🔗 Next Steps
- Review with Thorchain and Vultisig dev teams.
- Define technical implementation for whitelist validation (on-chain vs signed message).
- UI/UX mockup for Vultisig integration.

