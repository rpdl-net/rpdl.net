---
title: donate
date: []
hidedate: true
hidetitle: true
description: "Safely download games, FAST."
---

## Thank you for considering donating!  

**Our current bills are approximately 340euro monthly**.  

```
~140     2x 40tb storage servers
~90      4x cache nodes (eu + na)
~40      3x reverse proxies and a load balancer
~50      5 nodes of various sizes to run our platform
~20-30   subscriptions for providers like mega/pixeldrain/gofile
```
# stripe
{{< rawhtml >}}
<script src="https://js.stripe.com/v3/"></script>
<button
  style="background-color:#ffd700;color:#0f172a;padding:5px 50px;border:0;border-radius:5px;font-size:1em;cursor:pointer"
  data-price-id="price_1JsJx9IcakyhRRzJRCfHIgbJ"
  role="link"
  data-checkout-mode="subscription"
  type="button"
>
  €2 Monthly
</button>
<button
  style="background-color:#ffd700;color:#0f172a;padding:5px 50px;border:0;border-radius:5px;font-size:1em;cursor:pointer"
  data-price-id="price_1JsJxPIcakyhRRzJMcTO7hte"
  role="link"
  data-checkout-mode="subscription"
  type="button"
>
  €5 Monthly
</button>
<button
  style="background-color:#ffd700;color:#0f172a;padding:5px 50px;border:0;border-radius:5px;font-size:1em;cursor:pointer"
  data-price-id="price_1L7qAzIcakyhRRzJiBCw8SN0"
  role="link"
  data-checkout-mode="subscription"
  type="button"
>
  €10 Monthly
</button>
<button
  style="background-color:#ffd700;color:#0f172a;padding:5px 50px;border:0;border-radius:5px;font-size:1em;cursor:pointer"
  data-price-id="price_1JsJxyIcakyhRRzJu4Ca9PUR"
  role="link"
  data-checkout-mode="subscription"
  type="button"
>
  €20 Monthly
</button>
<br>
<button
  style="background-color:#6772E5;color:#0f172a;padding:5px 50px;border:0;border-radius:5px;font-size:1em;cursor:pointer"
  data-price-id="price_1L7qGsIcakyhRRzJdUg6U81E"
  role="link"
  data-checkout-mode="payment"
  type="button"
>
  €2 Once&nbsp;&nbsp;&nbsp;&nbsp;
</button>
<button
  style="background-color:#6772E5;color:#0f172a;padding:5px 50px;border:0;border-radius:5px;font-size:1em;cursor:pointer"
  data-price-id="price_1L7qJEIcakyhRRzJoOayMTQZ"
  role="link"
  data-checkout-mode="payment"
  type="button"
>
  €5 Once&nbsp;&nbsp;&nbsp;&nbsp;
</button>
<button
  style="background-color:#6772E5;color:#0f172a;padding:5px 50px;border:0;border-radius:5px;font-size:1em;cursor:pointer"
  data-price-id="price_1L7qJuIcakyhRRzJ8fKKiHRu"
  role="link"
  data-checkout-mode="payment"
  type="button"
>
  €10 Once&nbsp;&nbsp;&nbsp;&nbsp;
</button>
<button
  style="background-color:#6772E5;color:#0f172a;padding:5px 50px;border:0;border-radius:5px;font-size:1em;cursor:pointer"
  data-price-id="price_1L7qKOIcakyhRRzJScrawWT4"
  role="link"
  data-checkout-mode="payment"
  type="button"
>
  €20 Once&nbsp;&nbsp;&nbsp;&nbsp;
</button>
<script>
      var PUBLISHABLE_KEY = 'pk_live_51JsJ4DIcakyhRRzJt2nwv5I38P0E7MCMYHtp7IQHsQIgF1y41P0BLIwacd2GWdOYn9nvzrv2M1q4vxMJvQBi7Ecl00xNkv1UyJ';
      var DOMAIN = location.href.replace(/[^/]*$/, 'rpdl.net');
      if (PUBLISHABLE_KEY === 'pk_test_Tr8olTkdFnnJVywwhNPHwnHK00HkHV4tnP') {
        console.log(
          'Replace the hardcoded publishable key with your own publishable key: https://dashboard.stripe.com/test/apikeys'
        );
      }

      var stripe = Stripe(PUBLISHABLE_KEY);

      // Handle any errors from Checkout
      var handleResult = function (result) {
        if (result.error) {
          var displayError = document.getElementById('error-message');
          displayError.textContent = result.error.message;
        }
      };

      document.querySelectorAll('button').forEach(function (button) {
        button.addEventListener('click', function (e) {
          var mode = e.target.dataset.checkoutMode;
          var priceId = e.target.dataset.priceId;
          var items = [{ price: priceId, quantity: 1 }];

          // Make the call to Stripe.js to redirect to the checkout page
          // with the sku or plan ID.
          stripe
            .redirectToCheckout({
              mode: mode,
              lineItems: items,
              successUrl:
                'https://rpdl.net/donate/success?session_id={CHECKOUT_SESSION_ID}',
              cancelUrl:
                'https://rpdl.net/donate/cancelled?session_id={CHECKOUT_SESSION_ID}',
            })
            .then(handleResult);
        });
      });
    </script>
{{< /rawhtml >}}

#### Without you guys none of this would be possible, thank you so much.
