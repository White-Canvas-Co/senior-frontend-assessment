# Introduction

We appreciate you taking the time to complete this frontend technical assessment. Let us know if you have any questions!

## What we look for / criteria for success

- Your eye for detail
- Understanding of Shopify
- Software quality (scalability, readability, maintainability, etc.)
- Best practices and standards
- HTML semantics, a11y and SEO
- Code and site performance awareness
- Fluid responsiveness
- Translating requirements and designs into code
- Documentation and clear instructions

## Submission

Once complete, please provide the following via email:
- Shopify preview link
- Preview password
- Your repo link

# Instructions

1. Create a development store with Shopify's [generated test data](https://shopify.dev/docs/apps/tools/development-stores/generated-data).
2. Start a completely blank theme, you'll only need the homepage.
3. Translate the designs in `/designs` into your theme i.e. build a header and the 3 sections.
4. Add any testing instructions and relevant documentation to your README.md.

## What you'll need
- Tech stack - we recommend using the following tech stack:
  - TailwindCSS
  - SCSS (only if necessary)
  - React (or similar)
  - TypeScript (optional)
- Fonts - "Lato" (Google/Shopify font)
- Icons/images - the icons snippet and image files are in `/resources`
- Free [Rapid API](https://rapidapi.com/) account required
  - To consume this API - https://rapidapi.com/joeykyber/api/ski-resort-forecast

## Section 1 - Hero

### Requirements

- Images used are Shopify stock images, they are:
  - in-flight-over-mountains.jpg
  - snow-covered-black-rocked-peaks.jpg
- Mobile image is optional, fall back to a cropped portrait version of the desktop image.
- Text components should be blocks so they can be reordered.
- (Optional) Add other configuration options that a client may like. Please note however, your final submission should include the settings that match the designs.

## Section 2 - Feature product

### Requirements

- Create a metaobject for awards:
  - The same award may be linked to multiple products.
  - A product may have multiple awards.
- Create the two awards as shown in the designs and link them to the "The Complete Snowboard" product.
  - Award image files are in `/resources`.
- Render the awards via 2 methods:
  1. [Liquid](https://shopify.dev/docs/api/liquid)
  2. [Storefront API](https://shopify.dev/docs/api/storefront)
- Implement "add to cart" functionality using the [Ajax Cart API](https://shopify.dev/docs/api/ajax/reference/cart)
- The header cart icon should show a badge number corresponding to the number of products in the cart.
- (Optional) Ability to select variants.
- (Optional) Button should say "Sold out" and be disabled if product is not available.

## Section 3 - Integrating custom API

### Requirements

- Using this [free API](https://rapidapi.com/joeykyber/api/ski-resort-forecast), build a ski resort forecast checker.
  - Rapid API account required.
- Find a ski resort by search ([list of all ski resorts](https://www.skiresort.info/ski-resorts/)).
  - Search requires a minimum of 3 characters.
  - Avoid excessive API requests (throttle/debounce).
  - (Optional) Request loading indicator.
- Display the forecast of the first available day:
  - Show the minimum and maximum temperature of the whole day.
  - Show the total rain and snow fall of the whole day. 
- Once a resort is loaded, browser should keep track of the user's preferred ski resort and preload this on page reload.
- (Optional) Emoji weather icon based on weather conditions.
- (Optional) "Open in Maps" links to Google Maps.
- (Optional) Temperature background colours based on the ranges specified here - https://www.weatherzone.com.au/help/legend#legend_temperature.
- (Optional) Handle error cases gracefully.
