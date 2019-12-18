# Tools & Resources for Salesforce B2C Commerce Developers.

[Trailhead ExamGuide](https://trailhead.salesforce.com/help?article=Salesforce-Certified-B2C-Commerce-Developer-Exam-Guide)

[Trailhead Badge](https://trailhead.salesforce.com/en/content/learn/modules/b2c-developer-resources-and-tools?trail_id=develop-for-commerce-cloud)

## Explore the Developer Resources

- Navigate the Salesforce B2C Commerce XChange Community Portal.
  - xchange.demandware.com/
- Find developer resources on XChange.
  - https://xchange.demandware.com/community/developer
- Find B2C Commerce release information.
  - https://xchange.demandware.com/community/roadmap-and-releases/documentation
- Search the B2C Commerce documentation.
  - https://documentation.b2c.commercecloud.salesforce.com/DOC4/index.jsp?

## Install and Configure UX Studio

- Install Eclipse and Java.
  - ...
- Install UX Studio.
  - ...
- Connect UX Studio to your sandbox.
  - file > new > digital server connection
  - host, username and password

## Access the GitHub Repositories

- Access the Salesforce B2C repositories on GitHub.
  - https://github.com/SalesforceCommerceCloud
- Describe the benefits of the Commerce Cloud Storefront Reference Architecture (SFRA).
  - Controllers are easier to work with than pipelines
  - SFRA has templates and more plugins.
- Download or clone the SFRA repositories.
  - Clone or download

## Install and Configure SFRA

- Use Node Package Manager (npm) to install packages.
  - node -v , npm -v
  - npm install
- Compile the JavaScript, style sheets, and fonts for SFRA.
  - npm run compile:js; npm run compile:scss; npm run compile:fonts;
- Upload the SFRA cartridges.
  - setup  dw.json
  - host, username, password, code-version
  - npm run uploadCartridge (on top most directory of project)
- Add data to SFRA.
  - site import/export
- Index SFRA.
  - Merchant Tools > Search > Search Index Rebuild Schedule (always schedule instead of just building)
  - "Run Now"
