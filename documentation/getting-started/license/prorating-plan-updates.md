# Prorating Plan Updates

We support prorating of plan upgrades & downgrades.

Unlike the commonly used prorating implementations which preserve the renewal payment processing time, Freemius’ proration works slightly different and will restart the billing date based on the time of the plan update. This methodology simplifies understanding the discount for the customers and also benefits the sellers who will receive the initial worth of the new plan (minus the discounts) for the full billing period right away.

### Proration from a Lifetime License <a href="#proration_from_a_lifetime_license" id="proration_from_a_lifetime_license"></a>

Customers who purchased a lifetime plan will be eligible for a _proration_ discount only if they update their plan within 30 days from the time of purchase. The _proration_ discount is calculated as follows:

```
proration_discount = min(prev_lifetime_payment, new_lifetime_price)
```

**Examples:**

* If a user purchased a single-site lifetime pro license for $300 and after 3 days upgrades to a 5-site lifetime pro license for $600, they are only charged $300 for the upgrade.
* If a user purchased a single-site lifetime starter license for $150 and after 6 days upgrades to a single-site lifetime business plan for $400, they are only charged $250 for the upgrade.
* If a user purchased a single-site lifetime pro license for $300 and after 2 months upgrades to a 5-site lifetime pro plan for $600, they are charged the full $600.

To understand why lifetime upgrades aren’t just calculated as the difference in price, regardless of how long ago the original purchase was, the following two scenarios may help:

> A customer purchases a lifetime license for $300. Then, after 5 years (intentionally exaggerated time for emphasis) decides to upgrade for a higher $500 plan. If you discount them with $300 it basically means that they’ve used your product/license/support for free for 5 years. If a different customer purchase that same lifetime plan for $500 at the same time the other user upgrades from the $300 to the $500 plan, they both end up paying the exact same amount in total ($500), yet, the 1st customer already been using the product for 5 years.

> Or another example, to drive it home (pun intended!). Let’s say you buy a car and then after 5 years decide to buy a more expensive one from the same brand. Would you expect to get your money back? No, because you’ve already used the product, which is analogous to receiving support (aka warranty).

Therefore, we have the 30-day time limit in place to protect from this edge case.

### Proration from a Subscription <a href="#proration_from_a_subscription_monthly_or_annual" id="proration_from_a_subscription_monthly_or_annual"></a>

Customers which are updating a plan that was purchased as a subscription will receive a _proration_ discount, based on the unused portion of their previous plan:

```
remaining_period = (1 - number_of_days_past_from_the_old_plan_last_payment / number_of_days_in_past_billing_cycle )
proration_discount = max(0, remaining_period x old_plan_last_payment )
```

**Examples:**

* If a user purchased a single-site monthly pro package for $10 per month and after 2 months and 15 days upgrades to the annual billing cycle of the same single-site pro plan for $100 per year – the customer will have already paid $10, and will have used half of their current billing cycle. Therefore, the initial _prorated_ amount will be $95 ($100 – $10 / 2).
* If a user subscribed to a single-site annual pro license for $100 per year and after 3 months decides to downgrade to a single-site annual starter plan for $80 per year – the customer will already have paid $100, and have used only a quarter of the current billing cycle. Therefore, the _proration_ discount for the remaining period will be $75, and the initial price for the single-site annual starter plan will be $5 ($80 – $75). The first renewal payment will be scheduled for a year from the downgrade date and will cost $80.

### Proration with Coupons <a href="#proration_with_coupons" id="proration_with_coupons"></a>

When updating a plan with a percentage-based coupon, the _proration_ discount will be calculated first, and the coupon discount will apply to the discounted price as the last discount.

<br>
