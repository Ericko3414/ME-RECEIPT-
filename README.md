# ME-Receipt (ME Network)

> **Built for Hackathon 2026** by **The Trailblazers** (Erick Otieno) | **Track:** Consumer Products & Payments

**ME-Receipt** is a lightweight, mobile-first escrow payment and digital receipt prototype built for the **Meta Earth (ME) Network**. Everyday crypto transactions often leave buyers exposed to non-delivery and sellers exposed to payment disputes. ME-Receipt solves this with smart escrow locking, verifiable serial tracking, unique optical scan codes, and immutable refund records—powered by ultra-low MEC network gas fees.

---

## Live Demo

- **Web App:** (https://ericko3414.github.io/ME-RECEIPT-/)

---

## Key Features

- **Escrow Payment Locking (`MECS` & `USDT`):** Customers lock funds in ME Escrow before goods or services are handed over, protecting both buyer and seller.
- **Dynamic Micro Gas Fees (`MEC`):** Estimates and applies ultra-cheap ME Network gas fees starting at `0.0001 MEC` and scaling slightly with the transaction amount.
- **Optional Customer Tipping:** Built-in `0%`, `5%`, `10%`, and `15%` tip presets automatically calculated into the receipt subtotal.
- **Mutual Agreement & Satisfaction Badge (`🤝`):** Visually confirms equal escrow terms upon locking and verifies mutual satisfaction once delivery is confirmed or a refund is resolved.
- **Unique Code & MIRZ Scan Verification:** Generates a unique deterministic 1D SVG barcode alongside a 3-line machine-readable zone (`IDME...`) encoding the receipt serial number, date, currency, amount, and party names.
- **Immutable Refund Mode:** Issues a linked `#ME-REF-XXXX` adjustment receipt that references the original receipt ID (`#ME-XXXXXX`) without altering historical records.
- **Zero-Dependency Single-File Architecture:** Runs directly in any mobile or desktop browser with pure HTML, CSS, and vanilla JavaScript.

---

## How the Escrow Flow Works

1. **Enter Payment Details:** Fill in the Customer Name, Customer ME ID, Vendor Name, Vendor ME ID, Item/Service description, Amount (`MECS` or `USDT`), and optional Tip percentage.
2. **Pay & Lock in Escrow:** Click **Pay & Lock in Escrow** to generate a verified receipt with a unique **Receipt No**, **Serial No (`SN`)**, **Transaction Hash**, **Unique Barcode**, and **MIRZ Scan**.
3. **Settle or Refund:**
   - **Confirm Delivery:** Releases locked funds to the vendor and updates the `🤝` badge to verified mutual satisfaction.
   - **Issue Refund:** Switches the receipt into Refund Mode, creating an immutable adjustment record linked to the original receipt.

---

## Project Structure

```text
ME-RECEIPT-/
├── index.html      # Complete self-contained UI, escrow logic, barcode & MIRZ generator
└── README.md       # Project documentation
```

---

## Running Locally

1. Clone or download this repository:
   ```bash
   git clone https://github.com
   ```
2. Open `index.html` in any modern mobile or desktop web browser (Chrome, Brave, Safari, Edge). No build tools, servers, or external packages are required.

---

## Future Roadmap

- **Phase 1 — On-Chain Integration:** Connect directly to live Meta Earth (`ME ID`) wallet signing and deploy audited escrow smart contracts.
- **Phase 2 — Instant Merchant Checkout:** Add QR payment link generation for fast point-of-sale customer scanning.
- **Phase 3 — Receipt Export & History:** Support downloadable PDF/image receipt exports and local transaction history.

---

**Built for Hackathon 2026** by **The Trailblazers** (Lead Builder: **Erick Otieno**) • Track: **Consumer Products & Payments** • Powered by **Meta Earth (ME) Network**
