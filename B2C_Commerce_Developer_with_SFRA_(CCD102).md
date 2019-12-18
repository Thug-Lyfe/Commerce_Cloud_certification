# B2C Commerce Developer with SFRA (CCD102)

[](https://trailhead.salesforce.com/en/academy/classes/ccd102-b2c-commerce-developer-with-sfra/)

## When you complete this course, you will be able to:

- Create cartridges to add reusable functionality to a site.
  - open IDE, new cartridge.
  - Assign pipelines/controllers, scripts, templates etc. to the cartridge. Remember to make it selv contained.
  - upload the cartridge.
  - in BM go to "manage sites" and add the cartridge to specifc sites and the global cartridge path.
- Use JavaScript controllers to add business logic to a site.
  - yes.
- Create reusable code using ISML templates.
  - Product pages fx.
  - recommendation modules.
- Use content slots and page designer to improve the appearance and flexibility of a site.
  - \<iscontentslot\> \<iscontentasset\> , to create the possibillity for the merchandiser to choose themselves what are in specific spots on the site.
  - Use a controller/pipeline to create a way to render page designer pages via fx. their ID, This will enable the merchandiser to create pages independantly, to be used in mail campaigns, or as links on the site.
- Use B2C Commerce Script in ISML templates and script files.
  - \<script\> \<isscript\> ${} , are all available in ISML files to create business logic.
- Use the Forms Framework to control the validation, rendering, and storing of consumer-entered values.
  - forms can be automatically server vaidated with \<action formid="save" valid-form="true"/\> 
  - forms can be validated responsively with jquery and/or other javascript solutions.
- Create hooks to configure functionality that is called a specific event.
  - in hooks.json, custom hooks can be created.
  - in BM, open commerce API settings, can be configured to create a sudo REST service that can be avaible to public or a select group that have been authorized.
- Measure and ensure site performance.
  - use pipeline profiler and logcenter to identify problematic areas, these will give you a better idea of where problems are arising and where to start debugging for solutions.
- Install and use SFRA command line tools to perform testing. 
  - pipeline /script debugger ?
