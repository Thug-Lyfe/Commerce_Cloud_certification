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
- Marco - Given a business requirement, create and configure a new [search refinement](https://documentation.b2c.commercecloud.salesforce.com/DOC2/topic/com.demandware.dochelp/SearchandNavigation/CreatingNewSearchRefinementDefinitions.html?resultof=%22%73%65%61%72%63%68%22%20%22%72%65%66%69%6e%65%6d%65%6e%74%22%20%22%72%65%66%69%6e%22%20) and [sorting definition](https://documentation.b2c.commercecloud.salesforce.com/DOC2/topic/com.demandware.dochelp/SearchandNavigation/SortingRules.html?resultof=%22%73%6f%72%74%22%20) that can be used on the storefront.
  - To create a search refinement:
    - Merchant Tools > Products and Catalogs > Catalogs > choose a catelog > Edit a category > Search Refinement Definitions
    - Ater creating, rebuild the search index.
  - To create a sorting rule 
    - Merchant Tools > Search > Sorting Rules
    - Click New, write a name for the rule.
    - Choose a list of attributes to sort for, price, colors, material, manufacturer.
    - Choose ascending or decending for every attribute
    
- Marco - Given a debugging requirement or code, configure the logging categories and access the logs in Business Manager.
  - Administration > Site Development > Development Setup, here you can find links to logs and other files
  - Administration > Operations > Custom Log Settings
  - https://somestore/on/demandware.servlet/webdav/Sites/Impex/customLogs , this is where custom logs will be created.
- Given business requirements, extend the storefront to expose a new attribute on an existing system object type.
- Given a business need to store custom data, determine if a custom object is needed and create and configure as required.
- Given a performance issue and data, use relevant tools to inspect code performance and determine and implement solutions (cache configuration, profilers, etc) to improve performance.
- Given a specification and a sandbox instance, configure OCAPI permissions for Data and Shop APIs.
- Given a service configuration, recognize how they are applicable to the development process.


### Application Development: 53%
- Marco - Given a development task, code ISML templates that use functionality such as: local include, remote include, components, and other ISML tags.
  - [ISML tags documentaion] (https://documentation.b2c.commercecloud.salesforce.com/DOC2/index.jsp?topic=%2Fcom.demandware.dochelp%2FISML%2FISML.html)
  - locale include: \<isinclude template="template_name"/\>
  - remote include: \<isinclude url="url"/\>
  - component (only pipeline name is required): \<iscomponent pipeline="pipeline_name" locale="locale_name" someParam="someValue"/\> : retrieves the output of a pipeline
  - \<iscache\> : for caching a page
  - \<isif\> \<iselse\> \<iselseif\> : if statement controls
  - \<isloop\> \<isbreak\> \<iscontinue\> \<isnext\> : loop controls.
  - \<isslot\> \<iscontentasset\> : content controls
  - \<isdecorate\> \<isreplace\> : combine templates (isdecorate nominates an area that is filled by isreplace)
  - \<isset\> \<isremove\>: variables
  - \<iscookie\> \<isstatus\> : meta data (cookies and http status)
  - \<isselect\> : select object
  - \<isredirect\> : redirect to another page
  - \<isprint\> \<iscomment\> : print to screen, and comments.
- Marco - Use debugging best practices and techniques to troubleshoot scripts and controllers and verify outcomes.
  - There is nowhere where "debugging best practices" is written about in trailhead or salesforce documentation.
    I have therefore used other peoples opinion about the subject (collegaues and blogs), to shape my answer.
    - Use pipeline/script debuggers, use breakpoints to get to where the problem arises.
      - When using debuggers, that halt UI on an instance:
        - Keep the debuggers on a sandbox level.
        - If there is a problem that arises on staging / development, that would require a debugger to solve, check if other solutions are available, as it halts other peoples work. Only in extreme cases should a debugger ever be used on a staging environment.
        - NEVER DEBUG ON PRODUCTION!!!!
    - Use Expressions to test hypothesis, without having to rerun every time.
  - Be liberal with printing lines / console logs and other status messages, be sure to remove them when done.
  - Useful functions to use in ISML files to get a fast look of what there is to work with:
    - JSON.stringify(\<someobj\>,null,2) , pretty print JSON
    - Object.keys(someObj).toString() , list all fields and functions tied to an object (some objects cannot be expressed with JSON)
  - Always have meaningful error logging, this makes finding and identifying error and solutions faster and easier.
  - If applicable use the storefront toolkit.
  - 
- Given a requirement, create and extend the functionality of a JavaScript controller that leverages models, decorators, factories, or helpers following API best practices and renders a template or returns a JSON response.
- Marco - Given a business requirement and design for a new marketing page, develop page types and components to allow a marketer to build a page with the Page Designer tool.
  - This explains both well : [page type and component creation](https://trailhead.salesforce.com/content/learn/modules/b2c-page-designer-developers/b2c-page-designer-explore-json-js)
  ![page designer example](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/b2c-page-designer-merchandiser/b2c-page-designer-explore/images/3e811dd95253187aeee3c3dcd8e23811_pd-page-region-component.png "page designer example")
  - Page Type:
    - Write the config in JSON, naming the different regions (outer green boxes)
    - Page types can be combined by merchandisers later.
    - Write a .js that MUST have a .render function, else the page type will not work.
  - Components
    - Write the config in JSON, naming the attributes
    - Write a .js that MUST have a .render function, else the compoent will not work.
- Marco - Given a requirement to accept, validate, and persist information from a storefront customer, modify the appearance of a form, add validation and [CSRF protection](https://documentation.b2c.commercecloud.salesforce.com/DOC2/topic/com.demandware.dochelp/DWAPI/scriptapi/html/api/class_dw_web_CSRFProtection.html?resultof=%22%43%53%52%46%22%20%22%63%73%72%66%22%20), and use bindings to process fields.
  - Accept/validate: Forms are created as xml files and must be placed in cartridge/forms/\<default or locale\>/\<form_name\>.xml
    - There are 2 ways of validating the form
    1. Set mandatory="true" , This will make it so the field cannot be blank, anything written is fine though.
    2. A regexp can be written (very useful for emails and phone numbers), where anything written in the field must uphold the regexp standard.
    3. For selects (drop downs), if set to mandatory, an option must be picked.
  - Appearance
    - ISML/HTML/CSS files can be used to change the appearance. The forms/fields must be created for them to be active on the site in the folder described in last point.
    - The fields can be created with : \<isinputfield formfield="${pdict.CurrentForms.\<some_form_name\>.\<some_input\>}" type="input" label="false"/>
    - The form can be validated in pipelines with: CurrentForms.\<some_form_name\>.valid
    - The field value can be retreived in pipelines with: CurrentForms.\<some_form_name\>.\<some_input\>.value
    - The form can be validated in controllers with: $('.\<some_form_name\>')valid()
    - The field value can be retrieved in controllers with: $('.\<some_form_name\>').find('input[name$="\<some_input\>"]').val(),
  - CSRF protection
    - When writing forms in isml files use The code snippet below
    - In controllers use : require('dw/web/CSRFProtection').validateRequest()   , to validate a token
    - In pipelines use : CSRFProtection.validateRequest()   , to validate a token, always call this as the first thing in a pipeline if CSRFProtection is used.
```HTML
 <form ... action="">
   <input name="foo" value="bar">
   <input type=”hidden” name=”${dw.web.CSRFProtection.getTokenName()}” value=”${dw.web.CSRFProtection.generateToken()}”/>
 </form>
```

- Marco - Given localization requirements, implement and enhance templates, form definitions, static files, properties files, and persistent object attributes to ensure that pages are displayed in the expected language.
      
  - Localizing templates/forms/static files, is done by having a default folder, and a "locale" folder, the templates will be chosen automatically by demandware.  [Template localization](https://documentation.b2c.commercecloud.salesforce.com/DOC2/topic/com.demandware.dochelp/Localization/LocalizingUsingMultipleTemplateSets.html)
  <br>![example of structure localization](https://github.com/Thug-Lyfe/Commerce_Cloud_certification/blob/master/images/structure_example.png "example of structure localization")<br>
  - Localizing Text in with the same base template, is done with resouce (.properties) files. Demandware will also automatically use the locale specific resouce file based on the request locale and naming of the files. [resource localizing](https://documentation.b2c.commercecloud.salesforce.com/DOC2/topic/com.demandware.dochelp/DWAPI/scriptapi/html/api/class_dw_web_Resource.html?resultof=%22%2e%70%72%6f%70%65%72%74%69%65%73%22%20%22%70%72%6f%70%65%72%74%69%22%20)
<br>![example of naming localization](https://github.com/Thug-Lyfe/Commerce_Cloud_certification/blob/master/images/naming_example.png "example of naming localization") <br>
  - Localization of objects (system and custom objects): For all defined locales on Commerce Cloud, system/custom objects can be localized for them. Objects that can be localized is all Subclasses of [PersistentObject](https://documentation.b2c.commercecloud.salesforce.com/DOC2/topic/com.demandware.dochelp/DWAPI/scriptapi/html/api/class_dw_object_PersistentObject.html)
  <br>![example of object localization](https://github.com/Thug-Lyfe/Commerce_Cloud_certification/blob/master/images/object_example.png "example of object localization") <br>
- Marco - Given a logging task and existing configuration, write code that logs non-sensitive data to custom log files with different log levels.
  - dw.system.Logger.getLogger('file_prefix','line_prefix')
    - ex: var myCustomLog : Logger = dw.system.Logger.getLogger('MarcoTest','MarcoTest123')
    - myCustomLog.error("some error")
    - custom-MarcoTest-\<some file extention\>-\<Date\>.log
      - The file above would contain a file like this:
      - [todays date] ERROR \<location of error\> custom.MarcoTest123 []  some error
  - Other logging methods
    - myCustomLog.info("some info")
    - myCustomLog.debug("some debug")
    - myCustomLog.warn("some warning")
- Integrate, deploy, and use a service instance based on a given requirement.
- Given a use case, extend functionality or capture an event using hook extension points.
- Given code that violates documented best practices, identify the issues and modify the code to conform with best practices including performance and scalability.
- Given a business requirement, use OCAPI Shop and Data APIs to enable interoperability with an external system.
- Given a business requirement to perform a scheduled task, develop jobs and code job scripts.





