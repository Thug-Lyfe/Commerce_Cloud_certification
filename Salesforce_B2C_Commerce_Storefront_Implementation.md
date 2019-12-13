# Salesforce B2C Commerce Storefront Implementation.

[Trailhead ExamGuide](https://trailhead.salesforce.com/help?article=Salesforce-Certified-B2C-Commerce-Developer-Exam-Guide)

[Trailhead Badge](https://trailhead.salesforce.com/content/learn/modules/b2c-implement-functional-solution?trailmix_creator_id=jlayton&trailmix_slug=b-2-c-commerce-learning)

## Customize a B2C Commerce Reference Architecture

- Explain why customizing an application is expected.
  - Business requirements are most often not completely satisfied by standard functionality. Customizing is therefore expected, else the developer cannot fulfill the business requirements.
- List two SFRA customizations.
  - LINK cartridges, and custom code cartridge such as: wish lists, gift registries, apple pay, product comparison.
- Explain the difference between the two SFRA decorator templates.
  - page.isml, navigation.
  - checout.isml, no navigation.
- Explain how extending or overriding a controller can impact functionality and performance.
  - Extending a controller, means that first the original controller is run > third-party interactions > Extension > Third party interactions within the extension.
    - If a Extension uses the same third party interaction as the original controller, the interaction is run twice.
    - Overwriting the controller will not have the same implication.
- List two benefits of SFRA over SiteGenesis.
  - SFRA is build as mobile first, making the it lighter for the devices that needs it.
  - Link cartridges that are plug and play. no coding or setups required to work.

## Integrate Third-Party Applications

- Explain why third-party integrations are essential.
  - it leverages already build solutions to enable developers to toggle other problems.
  - fx. developers wont have to recode a solution for taxes, credit card payments, shipping carriers etc. for every site they make. Instead they can use third party solutions that are optimized to solve those problems and instead focus their time and effort on customization and areas that are not solvable with third party solution.
- List three of the most commonly used third-party integrations.
  - payment processors, ratings and reviews, tax processing, and email services.
- Explain the types of integrations that might occur.
  - Cartridge : fx Tax, payment and product recommendations, that need a lot of setup to work.
  - Controller : fx adding data to a product feed. Does not require much coding and can be solved with a smaller interaction.
  - Seperate UI : fx content management or analytics, that are not suited to be on the storefront or Business manager, but require a whole new browser setup to work properly.
- List three potential gaps that you need to consider.
  - Gaps are areas that could cause errors, complexity, or is client dependant.
    - Do the tasks require client resources?
    - Do integrations rely on a certain B2C Commerce release or feature?
    - Are any of the prerequisites unavailable or delayed?
    - Are there technical issues?
