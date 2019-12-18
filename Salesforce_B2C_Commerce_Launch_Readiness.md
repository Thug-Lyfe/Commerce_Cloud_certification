# Salesforce B2C Commerce Launch Readiness

[Trailhead ExamGuide](https://trailhead.salesforce.com/help?article=Salesforce-Certified-B2C-Commerce-Developer-Exam-Guide)

[Trailhead Badge](https://trailhead.salesforce.com/content/learn/modules/b2c-solution-functional-launch-readiness?trailmix_creator_id=strailhead&trailmix_slug=commerced-cloud-gen-900-introduction-to-commerce-cloud-businessd)

## Compare Business Requirements with the Storefront

- Explain what you need to compare with the actual storefront.
  - documentation of what was supposed to have been created.
  - documentation of the changes.
  - identify the gaps, so they can be tackled in an orderly fasion.
- Describe the best way to deal with schedule impacts.
  - document the gaps, create a plan to resolve them.
- Explain the benefit of fixing authentication gaps.
  - The authentication is the first thing a regular customer sees on the storefront, and is there very important to have made correctly.
- List the three typical parts of checkout.
  - shpipping, biling, receipt.
- Describe the differences between the product tile, product details, and Quickview versions of product information.
  - a product tile is a visual representation of a product, in a gitter format, such as search pages, recomded products or product carousels.
  - product details are within a product page where all relavant information/details pertaining to said product can be seen.
  - usually a compare window.

## Review Business Manager Settings

- List the key functional areas that you need to check for launch readiness.
  - check if the home page, products, catalogs, search page are visable and functioning as is.
  - go through checkout with trying all shipping/billing options.
- Explain the importance of configuring a master and storefront catalog.
  - the master holds all products data
  - the storefront catalog holds all active products, with relations to the master catalog for data.
    - the storefront catalog also holds categories where all products are categorized.
- Explain how search refinements and sorting rules service two types of users.
  - The searching is for storefront customers who knows what they want.
  - The sorting is for merchandisers and storefront customers
    - The merchandisers can create custom sorting, making sure that the products they want to highlight are at the top.
    - Th storefront customers can be visually inspired by the different sorting options and find what they are looking for.
- List the three things you must verify to ensure that pricing shows up on a storefront.
  - pricebooks, existing, assigned and activated.
- List three things you need to check to validate the storefront’s SEO URLs configuration.
  - alias rules for pipelines
  - 301 mapping for migrating platforms.
  - URL rules!
