# ⚡ Invoice2JSON Free

**Turn invoice PDFs into clean JSON in <200ms.**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Website](https://img.shields.io/website?url=https%3A%2F%2Finvoice2json.com)](https://invoice2json.com)

**Problem:** Manually parsing invoices is slow. Existing OCR tools are inaccurate (60%) or expensive ($0.50/page with GPT-4).
**Solution:** A dedicated API trained on 500k+ invoices that extracts data instantly.

## 🚀 Features

- **Blazing Fast:** <200ms average response time.
- **Accurate:** 99.9% field-level accuracy (using custom Vision Transformers).
- **Cheap:** $0.03 per page (vs $0.50 for GPT-4).
- **Developer First:** Simple REST API & Webhooks.

## 📦 Installation

```bash
npm install invoice2json
```
## ⚡ Quick Start

Parse an invoice in 3 lines of code:

```bach
const Invoice2JSON = require('invoice2json');
const client = new Invoice2JSON('YOUR_API_KEY');

async function parse() {
  const invoice = await client.parse('./invoice.pdf');
  console.log(invoice.data.total_amount); // 1250.00
}

parse();
```
## 📄 Example Output

```bash
{
  "vendor": "Acme Corp",
  "date": "2024-01-15",
  "total": 1250.00,
  "currency": "USD",
  "line_items": [
    {
      "description": "Pro Plan Subscription",
      "quantity": 1,
      "amount": 1250.00
    }
  ],
  "confidence": 0.998
}
```

## 🆓 Free Tier
Get 25 free invoices per month. No credit card required.

![Get your API Key](https://invoice2json.com/#pricing)

## 📄 License

MIT
