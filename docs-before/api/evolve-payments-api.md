---
description: >-
  Overview of the Evolve Payments API, authentication, and core endpoints for
  processing payments and managing your account.
---

# Evolve Payments API

## Evolve Payments API <a href="#evolve-payments-api" id="evolve-payments-api"></a>

The Evolve Payments API lets you securely create and manage payments from your own applications. Use it to charge customers, issue refunds, manage disputes, and pull reporting data without leaving your existing tools.

This page gives you a high-level overview of how the API is structured and where to find the full endpoint reference.

### What You Can Do with the API <a href="#what-you-can-do-with-the-api" id="what-you-can-do-with-the-api"></a>

With the Evolve Payments API, your team can:

* Create and manage charges
* Store and reuse customer payment methods
* Handle refunds and disputes programmatically
* Access reporting and usage data
* Automate operational workflows around payments

### Authentication <a href="#authentication" id="authentication"></a>

All requests to the Evolve Payments API are authenticated using your API keys.

* Use **test keys** in sandbox while you build and validate your integration.
* Switch to **live keys** when you are ready to process real payments.
* Keep your secret keys safe and never expose them in client-side code.

### Related Documentation <a href="#related-documentation" id="related-documentation"></a>

To get up and running quickly, start with the onboarding guides:

* [Quickstart](../getting-started/quickstart.md)
* [Collect your first payment](../getting-started/collect-your-first-payment.md)

For detailed endpoint descriptions, request/response schemas, and error codes, see the full [Evolve Payments API reference](https://app.gitbook.com/o/X9uddHR2nO73YvXdCY0t/s/uBtQCmrTBT0sn5qIsAPe/).

{% openapi-operation spec="my-organization-api" path="/payments" method="post" %}
[OpenAPI my-organization-api](https://github.com/GitbookIO/api_days_paris_2025/raw/refs/heads/main/api-specs/evolve-basic-before.yaml)
{% endopenapi-operation %}

{% openapi-operation spec="my-organization-api" path="/payments/{id}" method="get" %}
[OpenAPI my-organization-api](https://github.com/GitbookIO/api_days_paris_2025/raw/refs/heads/main/api-specs/evolve-basic-before.yaml)
{% endopenapi-operation %}

<br>
