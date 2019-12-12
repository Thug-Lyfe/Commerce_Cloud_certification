# Salesforce B2C Commerce for Developers.

[Trailhead ExamGuide](https://trailhead.salesforce.com/help?article=Salesforce-Certified-B2C-Commerce-Developer-Exam-Guide)

[Trailhead Badge](https://trailhead.salesforce.com/en/content/learn/modules/b2c-page-designer-developers?trail_id=build-storefront-pages-with-salesforce-b2c-commerce-page-designer)

## Explore Pages, Components, and Development Elements

- Explain the benefits of using Page Designer over content slots.
  - It grants the developer the ability to create templates.
  - It grants the merchandiser more control over how their site looks and feels, plus it gives them control over creating new sites through the templates created by the developer.
- List three steps of a typical Page Designer implementation plan.
  1. Write up business requirements
  2. Setup the Environment.
  3. Explore the requirements and possible solutions.
  4. Write up the solution.
  5. The template is ready to be used by merchandisers.
- Describe how the Page Designer pages and component type JSON and script files relate to each other.
  - Every page type, needs 1 meta definition in JSON.
  - Every page type, needs 1 script file in .js, which contain all business and view logic.
- Explain how Page Designer data differs from content asset data in the content database.
  - Content assets are linked to a folder and can be edited through merchant tools > content assets.
  - Page Designer pages are also content assets, but they cannot be edited through Business Manager.

## Set Up a Page Designer Development Environment

- Identify three steps you must take to configure your environment.
  - Donwload and clone repos.
  - Upload code and cartridges to Business manager.
  - Configure cartridge path in business manager.
- Explain why compatibility mode is important.
  - Compatibility Mode, controls which version of B2C Commerce API is in use by a Code Version (it can be seen under Code deployment)
  - Some Functionality only works on earlier versions (depricated), and some only work on newer, it is very important that all current code works with either the newest version (*), or the compatibility mode set for the code version.
- List three environmental dependencies for the local machine.
  - node, npm and other dependencies.
- Describe the basic steps you must take to import sample data.
  1. Site Import & Export > Upload > import
  2. Search indexes (Schedule in some cases) > Rebuild

## Explore Sample Pages and Component Types

- Identify the page type and component type ID naming convention.
  - name of the file plus location of the metadata folder joined by (.)
- Explain how page types relate to component types.
  - Page types are templates.
  - Components are what can be added to the page (banners, images, carousels etc.)
- Describe the purpose of mock attributes.
  - Placeholders, where the merchantdiser can see what to fill the area with.
- Explain how resolved values relate to the B2C Commerce API.
  - Resolved values are predefined. product.SKU, Product.custom.XXX, Product.Description etc.
- Describe how Page Designer elements are updated in cache.
  - Best practice is Code version switch. But invalidate caching can also be used.

## Explore Page and Component Type Controllers, JSON, and Scripts

- List three development elements you can use to create Page Designer page and component types.
  - Controllers, JSON, script .js, ISML, HTML and CSS.
- List the JSON file naming convention.
  - Name the JSON and Script files the same
  - always place them in either the page folder or component folder or a sub directory of those.
- Explain how controllers are used for Page Designer pages and components.
  - Server-side scripts that handle requests.
  - They handle logic prior to rendering.
- Describe the difference between how B2C Commerce uses JSON and JavaScript files for page and component types.
  - JSON files are for describing where a merchandiser can place component types.
  - .js files are for scripts and must have a render function wihtin, to render the page type.

## Explore Page and Component Type ISML, HTML, and CSS

- Explain what a page type’s render function does.
  - It calls an ISML template, runs all demandware scripts and other scripts therin, to generate a HTML markup, which is then rendered for the user.
- List four Page Designer CSS development standards.
  - put the html wrapper in a div '(<div id="wrapper"></div>)'
  - The default CSS class for regions: "experience-region experience-<region_definition_id>"
  - The dafault CSS Class for components: "experience-component experience-<componenttype_id>"
  - The compoent type ID is with dots (.), the classname is with lines (-).
- Explain how you can vary a component’s style based on the region it’s in.
  - get the component, change the look/style, render the component.
  

## Create a Custom Attribute Editor

- Explain why you would create a custom attribute editor.
- Explain how the HTML iframe works with a custom attribute editor.
- Explain the difference between a breakout custom attribute editor and a trigger custom attribute editor.
- Explain why you would use a breakout custom attribute editor.
