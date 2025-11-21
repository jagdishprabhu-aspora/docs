# Aspora CX Documentation

Comprehensive customer experience operations guide for Aspora's UK and UAE regions.

## Overview

This documentation provides detailed guidelines for handling customer support operations, including KYC verification, transfers, referrals, order management, and ticket processing.

## Documentation Structure

### Main Pages

- **index.mdx** - Home page with overview and navigation

#### Verification
- **verification/kyc-verification.mdx** - KYC and verification requirements for UK and UAE

#### Transfers & Payments
- **transfers/transfer-types.mdx** - Available transfer methods by region
- **transfers/transfer-fees-limits.mdx** - Fee structures and transaction limits
- **transfers/referrals.mdx** - Referral program details, rewards, and requirements

#### Operations
- **operations/alpha-desk.mdx** - Guide to using Alpha Desk system
- **operations/order-handling.mdx** - Handling cases by order status
- **operations/payment-status.mdx** - Payment status definitions and workflows

#### Tickets
- **tickets/operations-tickets.mdx** - Ticket processing guidelines and SLAs

### Configuration Files

- **docs.json** - Mintlify configuration and navigation structure
- **documentation-reference.md** - Source reference document

### Assets

- **logo/** - Brand logos (light and dark versions)
- **favicon.svg** - Site favicon
- **images/** - Documentation images

## Regional Coverage

This documentation covers operations for:
- **United Kingdom (UK)** - GBP transactions and UK-specific processes
- **United Arab Emirates (UAE)** - AED transactions and UAE-specific processes

## Key Topics Covered

### Customer Verification
- Document requirements by region
- KYC verification processes
- Common delay reasons
- Status tracking in AlphaDesk

### Transfers & Payments
- Transfer types and methods
- Fee structures and limits
- Payment status definitions
- Processing workflows

### Referral Program
- Reward structures by region
- Requirements and redemption
- Aspora Cash lookup process

### Operations Tools
- Alpha Desk usage guide
- Search capabilities
- Dashboard navigation
- VPN access requirements

### Order Management
- UK order statuses (LULU)
- UAE workflows (Falcon)
- RDA vs VDA processing
- Turnaround time (TAT) guidelines

### Ticket Processing
- Ticket lifecycle stages
- SLA requirements by category
- Best practices and templates
- Escalation procedures

## Development

Install the [Mintlify CLI](https://www.npmjs.com/package/mint) to preview your documentation changes locally:

```bash
npm i -g mint
```

Run the following command at the root of your documentation:

```bash
mint dev
```

View your local preview at `http://localhost:3000`.

## File Organization

```
docs/
├── index.mdx                           # Home page
├── verification/
│   └── kyc-verification.mdx           # KYC & Verification
├── transfers/
│   ├── transfer-types.mdx             # Transfer Methods
│   ├── transfer-fees-limits.mdx       # Fees & Limits
│   └── referrals.mdx                  # Referral Program
├── operations/
│   ├── alpha-desk.mdx                 # Alpha Desk Guide
│   ├── order-handling.mdx             # Order Status Handling
│   └── payment-status.mdx             # Payment Statuses
├── tickets/
│   └── operations-tickets.mdx         # Ticket Guidelines
├── docs.json                          # Site configuration
├── documentation-reference.md         # Source reference
├── logo/                              # Brand assets
├── images/                            # Documentation images
└── README.md                          # This file
```

## Publishing Changes

Changes pushed to the main branch are automatically deployed to production via the Mintlify GitHub app.

## Important Notes

- All documentation follows Mintlify MDX format
- Navigation structure is defined in `docs.json`
- Always update this README when adding, deleting, or renaming files
- Maintain consistent formatting and structure across all pages

## Support

For questions about this documentation or Aspora CX operations, contact the CX team lead or operations manager.
