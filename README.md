# Commerce_Cloud_certification

[Trailhead ExamGuide](https://trailhead.salesforce.com/help?article=Salesforce-Certified-B2C-Commerce-Developer-Exam-Guide) 

### B2C Commerce Setup: 11%
- Given a sandbox environment, configure an IDE to use WebDAV to deploy cartridges to the correct version directories.
  1. File > New > Digital Server Connection + set Staging Directory in wizard.
  2. Digital Server Connection > Properties > Project References.
- Given a sandbox instance and data import files, import files using the Business Manager Import/Export modules.
  1. Import & Export
  2. Upload File
  3. Import File
- Given the code for a storefront site, add the correct sequence of cartridge names to the provided cartridge path.
  1. Custom Core / Pipelines / Controllers Catridge / CSsuite
  2. Default Site genesis Cartridges (controllers, pipelines, core) (controllers overwrite duplicate pipeline names regardless of placement)
  3. Others
- Given a sandbox environment, use the Business Manager to add a new site to the instance, configuring the default currency and taxation type according to business requirements.
  1. Administration > Sites > Manage Sites > New Site > General
  2. Set currency and taxation.
  3. Both can be changed later (and more currencies can be added)
- Given a recently created B2C site, assign the storefront data configurations according to business requirements. 
  - Most likely site import/export

### Work With a B2C Site: 12%
- Given a Business Manager task, work with the product data model to manage products and product search model, their categorization, and associated inventory and pricebooks.
  1. [Class ProductSearchModel](https://documentation.b2c.commercecloud.salesforce.com/DOC2/topic/com.demandware.dochelp/DWAPI/scriptapi/html/api/class_dw_catalog_ProductSearchModel.html?resultof=%22%70%72%6f%64%75%63%74%22%20%22%73%65%61%72%63%68%22%20%22%6d%6f%64%65%6c%22%20) 
- Marco - Given a configuration for tasks, such as payment and shipping information, use Business Manager to complete storefront orders.
  1. open Merchant Tools > Ordering > Customer Service Center
  2. Create / find orders.
  3. Add Customer / Shipping address / products etc. and click submit Order (or equivalent)
  4. add payment method
  5. complete order?
  
  OR
  
  1. open Merchant Tools > Ordering > Orders
  2. set paid status, amount and shipping information.
  
  OR
  
  1. set order confirmation status to "confirmed".
- Marco - Given a configuration task, use Business Manager to work with Content Assets, Page Designer, Content Slots, and Content Folders.
  1. Content assets contain meta data and/or html
  2. Content slots contain, Configurations, Content Assets, Meta data and/or html
  3. Content Folders contain all Content Assets, Pages, Content Slots. They can be shared accross sites.
  4. Page designer, is a custimizable template sites, that can give the customer a visual tool to design web pages. (it looks and feels a lot like sitecore, 95% the same)
      - The Developer makes the templates and components from business requirements.
        - a page is made up of regions,
        - a region is made up of components
        - components can be banners, carousels, images etc.
        - Mock values = placeholders
        - Resolved values are inherited from system objects.
          ![page designer example](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/b2c-page-designer-merchandiser/b2c-page-designer-explore/images/3e811dd95253187aeee3c3dcd8e23811_pd-page-region-component.png "page designer example")
      - The Customer creates pages from the templates.
        - Page Settings, General: locale, Searchable, Sitemap.
        - Page Settings, Localization: Name, description.
        - Page Settings, Targeting: Start/end Date and specific customer group.
        - Page Settings, SEO: Page Address, Page Title, Page description, Meta keywords (max 10)
        - The merchandiser can choose what is in specific components from the default components and the custom made ones.
        - Locales can be chosen hereditary: fr_CA (French Canadian) > fr (French) > default
        
        
page designer links : [1](https://trailhead.salesforce.com/en/content/learn/modules/b2c-page-designer-merchandiser/b2c-page-designer-explore?trail_id=build-storefront-pages-with-salesforce-b2c-commerce-page-designer) , [2](https://trailhead.salesforce.com/en/content/learn/modules/b2c-page-designer-merchandiser/b2c-page-designer-configure-page?trail_id=build-storefront-pages-with-salesforce-b2c-commerce-page-designer) , [3](https://trailhead.salesforce.com/en/content/learn/modules/b2c-page-designer-merchandiser/b2c-page-designer-configure-component?trail_id=build-storefront-pages-with-salesforce-b2c-commerce-page-designer) , [4](https://trailhead.salesforce.com/en/content/learn/modules/b2c-page-designer-developers/b2c-page-designer-sample-pages-components) , [video showcasing page designer](https://www.salesforce.com/video/3620472/)

### Data Management Using Business Manager Usage: 24%
- MARCO - Given a business requirement, modify site search preferences and settings to enable searching for a specified term or product attribute.
  - Terms: Merchant Tools > Search > Search Driven Redirects, choose what terms go to where.
  - Merchant Tools > Search > Searchable Attributes, choose which attributes are searchable.
- Given a business requirement, create and configure a new search refinement and sorting definition that can be used on the storefront.
- Marco - Given a debugging requirement or code, configure the logging categories and access the logs in Business Manager.
  - Administration > Operations > Custom Log Settings
  - https://somestore/on/demandware.servlet/webdav/Sites/Impex/customLogs , this is where custom logs will be created.
- Given business requirements, extend the storefront to expose a new attribute on an existing system object type.
- Given a business need to store custom data, determine if a custom object is needed and create and configure as required.
- Given a performance issue and data, use relevant tools to inspect code performance and determine and implement solutions (cache configuration, profilers, etc) to improve performance.
- Given a specification and a sandbox instance, configure OCAPI permissions for Data and Shop APIs.
- Given a service configuration, recognize how they are applicable to the development process.


### Application Development: 53%
- Marco - Given a development task, code ISML templates that use functionality such as: local include, remote include, components, and other ISML tags.
- Marco - Use debugging best practices and techniques to troubleshoot scripts and controllers and verify outcomes.
- Given a requirement, create and extend the functionality of a JavaScript controller that leverages models, decorators, factories, or helpers following API best practices and renders a template or returns a JSON response.
- Marco - Given a business requirement and design for a new marketing page, develop page types and components to allow a marketer to build a page with the Page Designer tool.
- Given a requirement to accept, validate, and persist information from a storefront customer, modify the appearance of a form, add validation and CSRF protection, and use bindings to process fields.
- Marco - Given localization requirements, implement and enhance templates, form definitions, static files, properties files, and persistent object attributes to ensure that pages are displayed in the expected language.
- Marco - Given a logging task and existing configuration, write code that logs non-sensitive data to custom log files with different log levels.
- Integrate, deploy, and use a service instance based on a given requirement.
- Given a use case, extend functionality or capture an event using hook extension points.
- Given code that violates documented best practices, identify the issues and modify the code to conform with best practices including performance and scalability.
- Given a business requirement, use OCAPI Shop and Data APIs to enable interoperability with an external system.
- Given a business requirement to perform a scheduled task, develop jobs and code job scripts.





