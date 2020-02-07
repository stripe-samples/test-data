# Generate test data with the Stripe CLI

Testing Stripe integrations can be tricky if you need data.

# How to use

1. Clone the repository

```
git clone test-data-generators
```

2. Download the CLI

3. Run the fixture command with the test data you want

| Fixture               | Description                                                                                         | Relevant samples |
| :-------------------- | :-------------------------------------------------------------------------------------------------- | :--------------- |
| two-tier-subscription | Creates two different subscription plans, a "Basic" plan and a "Pro" plan                           | Checkout <br/> Billing           |
| two-sku-store         | Sets up an e-commerce inventory with a T-shirt product that comes in two SKUs: Basic and Fancy | Checkout          |
