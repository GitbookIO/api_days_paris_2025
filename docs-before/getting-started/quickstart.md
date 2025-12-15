---
description: >-
  Getting started with Evolve Payments only takes a few minutes. Follow the rest
  of this guide to learn how to set up your organization.
metaLinks:
  alternates:
    - https://app.gitbook.com/s/jutEMXFphnTHDJP7E0lE/getting-started/quickstart
---

# Quickstart

<div align="left"><figure><img src="../.gitbook/assets/Card-12.png" alt="" width="563"><figcaption></figcaption></figure></div>

## Basic Integration <a href="#basic-integration" id="basic-integration"></a>

> Here is a quote about this page.

**Test Mode Setup:**

{% hint style="warning" %}
Make sure to swap in your real API key below
{% endhint %}

```
const evolve = new EvolvePayments({
  apiKey: 'test_key_your_test_key_here',
  environment: 'sandbox'
});
```

**Process a Payment:**

```
const payment = await evolve.charges.create({
  amount: 2999, // $29.99 in cents
  currency: 'usd',
  paymentMethod: {
    type: 'card',
    number: '4242424242424242',
    expMonth: 12,
    expYear: 2025,
    cvc: '123'
  },
  description: 'Test purchase'
});
```

## Handle Responses <a href="#handle-responses" id="handle-responses"></a>

```
if (payment.status === 'succeeded') {
  // Payment successful
  console.log('Payment ID:', payment.id);
} else {
  // Handle failed payment
  console.log('Error:', payment.error);
}
```

## Go Live <a href="#go-live" id="go-live"></a>

1. Complete account verification in your dashboard
2. Switch to live API keys
3. Update environment to 'production'

## Key Features <a href="#key-features" id="key-features"></a>

* **Supported Methods**: Credit cards, digital wallets, bank transfers
* **Security**: PCI DSS compliant, encrypted transactions
* **Fees**: 2.9% + 30¢ per successful transaction
* **Settlement**: Next business day deposits

<br>
