# Release Checklist

Use this checklist before publishing a GitHub release or uploading the theme to Shopify.

## Repository

- [ ] The working tree contains only intentional changes.
- [ ] No API keys, tokens, customer data, order exports, email addresses, or merchant credentials are present.
- [ ] No merchant-owned or third-party product photography is bundled without permission.
- [ ] `README.md`, `CHANGELOG.md`, `LICENSE`, and version metadata are current.
- [ ] The distributable ZIP contains the Shopify theme directories at its root.

## Theme Content

- [ ] All visible demo copy is English and generic.
- [ ] Demo branding and imagery can be replaced in the theme editor.
- [ ] Navigation, social links, contact details, and policy links contain no merchant-specific values.
- [ ] Generic catalog fallback is clearly identified and can be disabled.
- [ ] App blocks are optional and the theme does not depend on a merchant-only app.

## Storefront Behavior

- [ ] Home, product, collection, search, cart, contact, policy, blog, article, and 404 templates render.
- [ ] Product variants, quantity controls, add-to-cart, cart updates, and checkout links work.
- [ ] Search and collection sorting work without JavaScript errors.
- [ ] Desktop and mobile navigation are keyboard accessible.
- [ ] Focus states, image alt text, headings, labels, and color contrast have been reviewed.
- [ ] Mobile overlays do not block scrolling or cover purchase controls.

## Validation

- [ ] All JSON files parse successfully.
- [ ] Shopify Theme Check completes with no new errors.
- [ ] Shopify Liquid validation completes for changed files.
- [ ] The theme is tested as an unpublished Preview Theme before release.
