---
description: >-
  Learn how to set up a basic Evolve Payments integration in sandbox, process
  test charges, handle responses, and prepare to go live.
cover: >-
  https://gitbook.com/adaptive-content-demo/~gitbook/image?url=https%3A%2F%2F3088035508-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F092wqj6J0y3Z75k04qFH%252Fuploads%252FzUjaiqYi0eKNV9DoRESc%252FCover.svg%3Falt%3Dmedia%26token%3De90a4529-a605-4312-abf7-c492c3be255a&width=1248&dpr=2&quality=100&sign=b1939181&sv=2
coverY: 0
metaLinks:
  alternates:
    - https://app.gitbook.com/s/jutEMXFphnTHDJP7E0lE/
---

# Evolve Payments

## Basic Integration <a href="#basic-integration" id="basic-integration"></a>

This guide walks you through a basic Evolve Payments integrationfrom setting up your sandbox API key, to creating your first test charge, handling responses, and preparing to go live in production.

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
