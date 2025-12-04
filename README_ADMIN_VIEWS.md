# JCB! Admin Views

### What Are Admin Views?
**Admin Views** form the foundational interface layer of every JCB-built Joomla component.

Each Admin View is tightly bound to a database table and automatically generates all required:
- **Forms**
- **Models**
- **Controllers**
- **List and Edit Views**
- **Permission handling** (ACL)
- **Field validation and access control**

Admin Views are mandatory. Every JCB component must include at least one Admin View  
to be valid and compile correctly. This ensures that your component manages data  
within Joomla's native MVC architecture — offering full CRUD capabilities out-of-the-box.

---
### Why Are Admin Views Important?
Admin Views serve as the **data anchor** for the component:

- Link directly to Joomla database tables
- Automatically attach multiple fields and manage field visibility/edit permissions
- Enable subforms (linking to other Admin Views) for nested data structures
- Respect Joomla's ACL per view and field
- Reusable across multiple components — compile-safe with namespace awareness

This makes Admin Views the heart of every component, defining its schema, edit experience,  
and administrative backbone. Unlike Custom Admin Views or Site Views (which focus more on layout or data rendering),  
Admin Views define the **structural data definition** and baseline logic.

---
### Versioning and Sharing
When you need to update Admin Views in any JCB project:

- Select the views to update
- Click **"Reset"** to pull the latest version from this repository
- Or **Fork** this repository and point your JCB instance to your fork

This ensures maintainability while still allowing total customization per project.

>Admin Views are the schema-defining force in JCB — not just a UI pattern, but a declaration of how your component should structure and manage its data. We recommend exploring the shipped demo component to see Admin Views in action.

---
### Index of Admin Views


 - **Address (Service Directory)** | [Details](src/admin_view/b7b2aba5-8a94-443b-814b-aed5b0b7c550) | [Settings](src/admin_view/b7b2aba5-8a94-443b-814b-aed5b0b7c550/item.json) | Addresses of Companies
 - **Address (Service Directory)** | [Details](src/admin_view/f9692057-845b-47c9-a1d5-59b4eddc5057) | [Settings](src/admin_view/f9692057-845b-47c9-a1d5-59b4eddc5057/item.json) | Addresses of Companies
 - **Address Types (Directories)** | [Details](src/admin_view/5992077e-15a5-4ea9-b882-e6e0e1b723ae) | [Settings](src/admin_view/5992077e-15a5-4ea9-b882-e6e0e1b723ae/item.json) | Types of Addresses
 - **Area of Expertise (Service Directory)** | [Details](src/admin_view/d3507dce-582f-49c2-a068-86b789540a97) | [Settings](src/admin_view/d3507dce-582f-49c2-a068-86b789540a97/item.json) | Area of Expertise
 - **Categories (Directories)** | [Details](src/admin_view/904dc405-ff8d-476c-9598-f8f2e05464f4) | [Settings](src/admin_view/904dc405-ff8d-476c-9598-f8f2e05464f4/item.json) | Categories
 - **Cities (Directories)** | [Details](src/admin_view/e4839d74-8f7f-46ed-9a0b-651d5412138e) | [Settings](src/admin_view/e4839d74-8f7f-46ed-9a0b-651d5412138e/item.json) | Cities
 - **Companies (Service Directory)** | [Details](src/admin_view/08a58903-10a4-4ed9-babd-8b9557b095e4) | [Settings](src/admin_view/08a58903-10a4-4ed9-babd-8b9557b095e4/item.json) | List of companies
 - **Company Areas of Expertise (Service Directory)** | [Details](src/admin_view/4e7dcf8b-89db-45d3-9a1d-0a0e733fcc04) | [Settings](src/admin_view/4e7dcf8b-89db-45d3-9a1d-0a0e733fcc04/item.json) | Company Areas of Expertise
 - **Company Languages (Service Directory)** | [Details](src/admin_view/64236c68-ddbf-4e4f-967c-6233be41e378) | [Settings](src/admin_view/64236c68-ddbf-4e4f-967c-6233be41e378/item.json) | Company Languages
 - **Company Portfolio ** | [Details](src/admin_view/7e615f03-c169-49fb-b72b-b75fcdec7672) | [Settings](src/admin_view/7e615f03-c169-49fb-b72b-b75fcdec7672/item.json) | Compnay Portfolio
 - **Company Tags (Service Directory)** | [Details](src/admin_view/1da2dc67-d28d-482a-abd4-f126b98c8834) | [Settings](src/admin_view/1da2dc67-d28d-482a-abd4-f126b98c8834/item.json) | Company Tags
 - **Country (Directories)** | [Details](src/admin_view/73177bc7-8db6-403e-b859-0613a2876171) | [Settings](src/admin_view/73177bc7-8db6-403e-b859-0613a2876171/item.json) | A list of countries.
 - **File Types (Directories)** | [Details](src/admin_view/66ae94e9-5283-4bc5-bee8-7f36915f972e) | [Settings](src/admin_view/66ae94e9-5283-4bc5-bee8-7f36915f972e/item.json) | File Type
 - **Files (Directories)** | [Details](src/admin_view/6559d7bb-d910-4a9f-9e4d-20568ada7c21) | [Settings](src/admin_view/6559d7bb-d910-4a9f-9e4d-20568ada7c21/item.json) | Files
 - **Languages (Directories)** | [Details](src/admin_view/671a0faa-afe7-430e-bef1-54701a924ee2) | [Settings](src/admin_view/671a0faa-afe7-430e-bef1-54701a924ee2/item.json) | A list of languages.
 - **Platform (Directories)** | [Details](src/admin_view/2138bd3a-fff3-4498-a63b-b47b1ec6243b) | [Settings](src/admin_view/2138bd3a-fff3-4498-a63b-b47b1ec6243b/item.json) | Platforms
 - **Regions (Directories)** | [Details](src/admin_view/275a0506-e63f-4c11-a731-124f5ad8cf0f) | [Settings](src/admin_view/275a0506-e63f-4c11-a731-124f5ad8cf0f/item.json) | Regions
 - **Review Company Updates (Service Directory)** | [Details](src/admin_view/5f35fa98-64d6-45ab-9a76-1cdf3a3a0381) | [Settings](src/admin_view/5f35fa98-64d6-45ab-9a76-1cdf3a3a0381/item.json) | List of companies updates to review
 - **Social Media Handles** | [Details](src/admin_view/6f3c01b6-7cab-4c17-b113-6ca532af49af) | [Settings](src/admin_view/6f3c01b6-7cab-4c17-b113-6ca532af49af/item.json) | Social Media Handles
 - **States (Directories)** | [Details](src/admin_view/8345b808-fc30-4b51-8c9b-05e96bfe26d6) | [Settings](src/admin_view/8345b808-fc30-4b51-8c9b-05e96bfe26d6/item.json) | States
 - **Sub-Regions (Directories)** | [Details](src/admin_view/58f0fc24-0030-49b2-b77a-83f6b7aedfbb) | [Settings](src/admin_view/58f0fc24-0030-49b2-b77a-83f6b7aedfbb/item.json) | Subregions
 - **Tags (Directories)** | [Details](src/admin_view/22bdc95c-d3de-4c25-af21-5a17d118b1df) | [Settings](src/admin_view/22bdc95c-d3de-4c25-af21-5a17d118b1df/item.json) | Tags
 - **Ticket Comments (Service Directory)** | [Details](src/admin_view/4aeeb39e-74f4-4ecd-b61f-7f4f71d46c3a) | [Settings](src/admin_view/4aeeb39e-74f4-4ecd-b61f-7f4f71d46c3a/item.json) | Ticket Comments
 - **Tickets (Service Directory)** | [Details](src/admin_view/bc12b55c-6763-4cec-864b-3529df4f89c4) | [Settings](src/admin_view/bc12b55c-6763-4cec-864b-3529df4f89c4/item.json) | Tickets
 - **Timezone (Directories)** | [Details](src/admin_view/e85e7cd7-baf2-4bb2-939a-8d664f49b7da) | [Settings](src/admin_view/e85e7cd7-baf2-4bb2-939a-8d664f49b7da/item.json) | Timezones.

### All used in [Joomla Component Builder](https://www.joomlacomponentbuilder.com) - [Source](https://git.vdm.dev/joomla/Component-Builder) - [Mirror](https://github.com/vdm-io/Joomla-Component-Builder) - [Download](https://git.vdm.dev/joomla/pkg-component-builder/releases)

---
[![Joomla Volunteer Portal](https://img.shields.io/badge/-Joomla-gold?logo=joomla)](https://volunteers.joomla.org/joomlers/1396-llewellyn-van-der-merwe "Join Llewellyn on the Joomla Volunteer Portal: Shaping the Future Together!") [![Octoleo](https://img.shields.io/badge/-Octoleo-black?logo=linux)](https://git.vdm.dev/octoleo "--quiet") [![Llewellyn](https://img.shields.io/badge/-Llewellyn-ffffff?logo=gitea)](https://git.vdm.dev/Llewellyn "Collaborate and Innovate with Llewellyn on Git: Building a Better Code Future!") [![Telegram](https://img.shields.io/badge/-Telegram-blue?logo=telegram)](https://t.me/Joomla_component_builder "Join Llewellyn and the Community on Telegram: Building Joomla Components Together!") [![Mastodon](https://img.shields.io/badge/-Mastodon-9e9eec?logo=mastodon)](https://joomla.social/@llewellyn "Connect and Engage with Llewellyn on Joomla Social: Empowering Communities, One Post at a Time!") [![X (Twitter)](https://img.shields.io/badge/-X-black?logo=x)](https://x.com/llewellynvdm "Join the Conversation with Llewellyn on X: Where Ideas Take Flight!") [![GitHub](https://img.shields.io/badge/-GitHub-181717?logo=github)](https://github.com/Llewellynvdm "Build, Innovate, and Thrive with Llewellyn on GitHub: Turning Ideas into Impact!") [![YouTube](https://img.shields.io/badge/-YouTube-ff0000?logo=youtube)](https://www.youtube.com/@OctoYou "Explore, Learn, and Create with Llewellyn on YouTube: Your Gateway to Inspiration!") [![n8n](https://img.shields.io/badge/-n8n-black?logo=n8n)](https://n8n.io/creators/octoleo "Effortless Automation and Impactful Workflows with Llewellyn on n8n!") [![Docker Hub](https://img.shields.io/badge/-Docker-grey?logo=docker)](https://hub.docker.com/u/llewellyn "Llewellyn on Docker: Containerize Your Creativity!") [![Open Collective](https://img.shields.io/badge/-Donate-green?logo=opencollective)](https://opencollective.com/joomla-component-builder "Donate towards JCB: Help Llewellyn financially so he can continue developing this great tool!") [![GPG Key](https://img.shields.io/badge/-GPG-blue?logo=gnupg)](https://git.vdm.dev/Llewellyn/gpg "Unlock Trust and Security with Llewellyn's GPG Key: Your Gateway to Verified Connections!")