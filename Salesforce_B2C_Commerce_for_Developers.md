# Salesforce B2C Commerce for Developers.

[Trailhead ExamGuide](https://trailhead.salesforce.com/help?article=Salesforce-Certified-B2C-Commerce-Developer-Exam-Guide)

[Trailhead Trailmix](https://trailhead.salesforce.com/en/content/learn/trails/develop-for-commerce-cloud?trailmix_creator_id=strailhead&trail)

[Trailhead Badge](https://trailhead.salesforce.com/en/content/learn/modules/cc-digital-for-developers?trail_id=develop-for-commerce-cloud)

## Get Started with Commerce Cloud Business Manager

- List three tasks a merchandiser performs in Business Manager.
  - Configure Site data, update products, update/create content assets and slots.
- List three tasks a developer performs in Business Manager.
  - cibfigure B2C Commerce site settings, Site export/import, Code and Data replication
- List four settings configured in the Merchant Tools tab.
  -  Taxation, URL Rules, Promotions/campaigns/coupons, locales
- List four tasks you can perform on the Administration tab.
  - Jobs, Data/code replplication, add new sites, add new users.
- Describe two features of the localization settings.
  - The storefront customers can view the storefront in their preferred language
    - Text resources are localized via naming standards
    - Templates/scripts/forms etc. can be localized via file structure
    - Storefront data can be localized via the BM.
  - Experience the business manager in preferred language.


## Explore the B2C Commerce Development Environment

- List two tools used for the client portion of a Salesforce B2C Commerce storefront.
  - Templates / Forms
- List the three key B2C Commerce software development tools.
  - Scripts / Controllers / "Resource Bundles"
- Describe the elements of the MVC architecture.
  - Model : data representation and business logic.
  - View : data visuzalization (how the storefront customers view products and data)
  - Controller : navigation and data processing.
- List three tasks you can perform with scripts and controllers.
  - Render templates.
  - Query products and other data structures
  - Place orders
  - Create baskets
  - Essentially all coding goes into these 2 areas, the rest is only vizualization which is HTML/ISML and forms.

## Explore the Commerce Cloud Storefront Reference Architecture

- Explain the benefits of using the Commerce Cloud Storefront Reference Architecture (SFRA).
  - Responsive / Mobile First / Adaptive
- Explain why a reference architecture provides a blueprint for site design.
  - The SFRA structure allows the developer the ease of having many template designs which can be expanded upon, based on business requirements.
- List two SFRA technical and UX components.
  - Applepay, wishlist, payment integrations etc. There are many third party cartridges that a developer can utilize to quicken development time.
- List two benefits of Mobile First.
  - Responsive.
  - Only sends relavant data to smaller devices, so it will boot/load/react faster on devices that need it the most.

# Explore B2C Commerce Business Objects

- Explain how business objects define the Salesforce B2C Commerce storefront data structure.
  - All product data needs to be structured onto the product data model. This means that if a merchandiser wants a new field shown, it has to be created in BM and be written into the code for it to be active.
- List two reasons why you would customize system objects.
  - Expand functionality of a system object.
  - Expand the data structure of a system object.
  - Examples: expand the product data model with: designer, producer, brand, material, recommendations etc.
- List two reasons why you would use custom objects.
  - If the data for a specific business requirement cannot be tetherd to a system object.
- List the two business object best practices.
  - Use system objects and attributes instead of custom objects and custom attributes wherever possible (this is both best practices)
