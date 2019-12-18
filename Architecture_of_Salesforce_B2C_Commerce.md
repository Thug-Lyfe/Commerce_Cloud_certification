# Architecture of Salesforce B2C Commerce

[Trailhead ExamGuide](https://trailhead.salesforce.com/help?article=Salesforce-Certified-B2C-Commerce-Developer-Exam-Guide)

[Trailhead Badge](https://trailhead.salesforce.com/en/content/learn/modules/architecture-of-commerce-cloud-digital?trail_id=develop-for-commerce-cloud)

## Get Started Configuring Your B2C Commerce Sites

- List the instance types.
  - PIG, development / Staging / Production
    - Development for testing new features.
    - Staging for testing in production like environment for deploying sprints and/or hotfixes.
    - Production for the publically available storefront that consumers can use.
  - SIG, Sandboxes
    - For development purposes.
- Explain what the instance types are used for.
  - look above.
- Describe how sites relate to organizations.
  - An Organisation can have multiple sites.
  - Settings can either be site specific or across the whole organisation
- Describe how a multisite realm is managed.
  - A realm can have more sites, each will have it is config, catalog, products, pricebooks, content slots/assets etc.
  - All settings can be chosen to be shared between one, multiple or all sites. (fx. 2 sites can share a catalog while a third has its own)

## Learn About Importing and Exporting Data

- Give two reasons why the import/export schema files are important.
  - to be consistent across different instance types.
- List two types of data that are typically imported.
  - MetaData, settings, content slots/assets.
- Describe two import/export modes.
  - site export/import for importing several things. usually from staging to sandboxes.
  - data specific export/import, catalogs/jobs/content/metadata other settings, can be export/importet indivually.
- Describe the export process.
  - click export/import, choose the extent of the export (which area for site ex/im, or which data fields other data specific ex/im)
- Explain why a delta feed is important.
  - a delta feeds is the differences from one feed to another, so only changes are copied over, making for faster build times and less bloated update feeds.

## Learn About B2C Commerce Replication

- Describe the process flow between instances.
  - Replication is always from staging to another instance (production/development and sometimes sandboxes)
  - This will keep the integrety of both code and data stable.
- List three types of data that are replicated.
  - content assets/slots
  - products/catalogs
  - pricebooks
  - inventory/orders/users/customers are NOT replicated and nor should they ever be!
- List two differences between the import/export and replication processes.
  - replication can be automated.
  - replication must never be to the staging instance, ONLY replicate from the staging instance.
- Describe two ways to control replication.
  - Manual activation. usually for code deployments (recommended, so as not to publish unstable staging versions to theproduction instance) 
  - Schedules activation. usually for data deployments.
- Explain the benefit of replication tasks.
  - They automate and simplify keeping instances up to date.
