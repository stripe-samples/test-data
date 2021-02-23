# Generate test data with the Stripe CLI

Testing Stripe integrations can be tricky, especially for complex flows like subscriptions or Connect platforms.

We wrote some test fixtures to help you quickly generate test data with the Stripe CLI. Use these or write your own test fixtures following the same spec.

Learn more about the CLI's [fixture command](https://github.com/stripe/stripe-cli/wiki/fixtures-command) in the CLI documentation.

## Available test fixtures

| Fixture                                                   | Description                                                                                                                             | Relevant samples & products                                                                                                                                                                                                   |
| :-------------------------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [two-plan-subscription](/two-plan-subscription)           | Sets up two different subscription plans, a "Basic" and a "Pro" plan                                                                    | ⚬ [Prebuilt subscription signup page](https://github.com/stripe-samples/checkout-single-subscription) (Checkout) <br/> ⚬ [Custom subscription signup page](https://github.com/stripe-samples/set-up-subscriptions) (Elements) |
| [two-sku-store](/two-sku-store)                           | Sets up a simple e-commerce inventory with a T-shirt product that has two "Basic" and "Fancy" SKUs that represent different shirt types | ⚬ [Pre-built payment form](https://github.com/stripe-samples/checkout-one-time-payments) (Checkout)                                                                                                                           |
| [customers-with-saved-cards](/customers-with-saved-cards) | Creates two Customers that have test cards saved to them that can be used to charge later                                               | ⚬ [Charging a saved card](https://github.com/stripe-samples/charging-a-saved-card)                                                                                                                                            |
| [customer-with-subscription](/customer-with-subscription) | Creates a Plan that charges \$10 once a day and subscribes a Customer to it                                                             | ⚬ Billing                                                                                                                                                                                                                     |

## How to use

#### 1. Clone the repository

```
git clone https://github.com/stripe-samples/test-data
```

#### 2. [Install the CLI](https://github.com/stripe/stripe-cli#installation)

Be sure to log in with your Stripe credentials so the CLI can use your test mode API keys.

#### 3. Run the fixture command with the test data you want to seed

The CLI will create all the Stripe objects defined in the fixture file in test mode.

```
stripe fixtures two-sku-store/create-fixtures.json
```

#### 4. You should now see the test data in your Dashboard! ✨

![An image of the newly create SKU in the Dashboard](/preview.png "An image of the newly create SKU in the Dashboard")

#### 5. [optional] Delete the test data

Each fixture has a `delete-fixtures.json` that cleans up the relevant test data.

## Contribute

We'd love contributions! Feel free to share a test fixture you found useful when building your Stripe integration.

Open a PR against this repo and add:

1. A new directory for your test fixtures (e.g. `two-sku-store`).
2. A `create-fixtures.json` file that creates the test data.
3. A `delete-fixtures.json` that tears down the test data.
4. [optional] A little about the business you're building and why this test fixture helped you model it 😊 (only if you want some free advertising!)

## Get support
If you found a bug or want to suggest a new [feature/use case/sample], please [file an issue](../../issues).

If you have questions, comments, or need help with code, we're here to help:
- on [IRC via freenode](https://webchat.freenode.net/?channel=#stripe)
- on Twitter at [@StripeDev](https://twitter.com/StripeDev)
- on Stack Overflow at the [stripe-payments](https://stackoverflow.com/tags/stripe-payments/info) tag
- by [email](mailto:support+github@stripe.com)

Sign up to [stay updated with developer news](https://go.stripe.global/dev-digest).
