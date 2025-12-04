# JCB! Dynamic Gets

### What Are Dynamic Gets?
Dynamic Gets in JCB are **graphically designed database queries** that define how data should be fetched,  
joined, filtered, and structured using a **easy selection query builder** interface.

They act as a visual abstraction over SQL joins and filters, comparable to:

- **Visual Query Builders**
- **ORM Relationship Graphs**
- **Custom Query Composition Engines**

Dynamic Gets allow you to:
- Choose a **primary table**
- Join **multiple related tables**
- Select fields from across those joins
- Apply **filters**, **WHERE clauses**, **ordering**, and **grouping** — all from within a GUI.

JCB then auto-generates:
- The complete **SQL JOIN** logic
- Any **Joomla-compliant API interaction**
- The **PHP model code** required to support the query

---
### How Do Dynamic Gets Integrate Into Views?
Each **Site View** or **Custom Admin View** requires a **main Dynamic Get**,  
which defines how its item or list data is fetched from the database.

But that's not all: you can attach multiple additional Dynamic Gets to a single view,  
enabling you to **merge data from completely different tables** — dynamically, cleanly, and consistently.

JCB intelligently ensures that the resulting component:
- Uses secure and efficient Joomla API calls
- Avoids repetitive logic
- Embeds the Dynamic Get logic **directly into the component's models**

This eliminates the need for hand-crafted query code, while maintaining full control and extensibility.

---
### Reset, Fork, or Customize
Just like other JCB entities, Dynamic Gets support a Git-based update workflow:

- **Init**: Pull from a remote repository
- **Reset**: Sync with upstream versions
- **Push**: Submit updates (if you have write access)
- **Fork**: Maintain your own version of dynamic queries

This lets you customize, evolve, and share query logic without rewriting or copy-pasting.

Whether you're building for:
- Deep reporting
- Cross-table analytics
- Complex filter-based list views

> Dynamic Gets combine power, flexibility, and GUI-driven convenience — helping you build smarter, faster, and more maintainable Joomla components.

---
### Index of Dynamic Gets


 - **Area of Expertise** | [Details](src/dynamic_get/e4f3648b-a740-4727-bc79-7109f1db0581) | [Settings](src/dynamic_get/e4f3648b-a740-4727-bc79-7109f1db0581/item.json)
 - **Category** | [Details](src/dynamic_get/e7af7dbd-318b-4ee7-8b03-7e9215a73c36) | [Settings](src/dynamic_get/e7af7dbd-318b-4ee7-8b03-7e9215a73c36/item.json)
 - **Companies** | [Details](src/dynamic_get/236df971-bf74-4f19-a091-06c8d1a3f9a2) | [Settings](src/dynamic_get/236df971-bf74-4f19-a091-06c8d1a3f9a2/item.json)
 - **Company** | [Details](src/dynamic_get/3071eabb-8a2d-4281-b6a4-179dbfb30774) | [Settings](src/dynamic_get/3071eabb-8a2d-4281-b6a4-179dbfb30774/item.json)
 - **Directory** | [Details](src/dynamic_get/61660555-f60c-4d9d-9dc4-44515a4c9834) | [Settings](src/dynamic_get/61660555-f60c-4d9d-9dc4-44515a4c9834/item.json)
 - **Get Category Thumb Images** | [Details](src/dynamic_get/1aeb1cc9-53d5-4f8b-b72f-acd67d0909b2) | [Settings](src/dynamic_get/1aeb1cc9-53d5-4f8b-b72f-acd67d0909b2/item.json)
 - **Get Company Logos** | [Details](src/dynamic_get/c00a187e-340c-4bd0-9783-48de834183c9) | [Settings](src/dynamic_get/c00a187e-340c-4bd0-9783-48de834183c9/item.json)
 - **Get Entity Banner** | [Details](src/dynamic_get/81f158f6-027b-4c37-89e9-4413b35cefeb) | [Settings](src/dynamic_get/81f158f6-027b-4c37-89e9-4413b35cefeb/item.json)
 - **Get Language** | [Details](src/dynamic_get/c05be929-4987-48de-b73e-1d6a8bc368f3) | [Settings](src/dynamic_get/c05be929-4987-48de-b73e-1d6a8bc368f3/item.json)
 - **Language** | [Details](src/dynamic_get/294949dd-93b3-424d-abea-fc6242d625d3) | [Settings](src/dynamic_get/294949dd-93b3-424d-abea-fc6242d625d3/item.json)
 - **Tag** | [Details](src/dynamic_get/cdc29b9e-ac51-4b0d-9c38-ee587c89509d) | [Settings](src/dynamic_get/cdc29b9e-ac51-4b0d-9c38-ee587c89509d/item.json)
 - **getMineCompanies** | [Details](src/dynamic_get/28dc3ae8-a928-4bfc-b8cd-751ff6248639) | [Settings](src/dynamic_get/28dc3ae8-a928-4bfc-b8cd-751ff6248639/item.json)
 - **getMineTickets** | [Details](src/dynamic_get/606cf9cb-cbd1-427e-8dce-16ea7764cd47) | [Settings](src/dynamic_get/606cf9cb-cbd1-427e-8dce-16ea7764cd47/item.json)

### All used in [Joomla Component Builder](https://www.joomlacomponentbuilder.com) - [Source](https://git.vdm.dev/joomla/Component-Builder) - [Mirror](https://github.com/vdm-io/Joomla-Component-Builder) - [Download](https://git.vdm.dev/joomla/pkg-component-builder/releases)

---
[![Joomla Volunteer Portal](https://img.shields.io/badge/-Joomla-gold?logo=joomla)](https://volunteers.joomla.org/joomlers/1396-llewellyn-van-der-merwe "Join Llewellyn on the Joomla Volunteer Portal: Shaping the Future Together!") [![Octoleo](https://img.shields.io/badge/-Octoleo-black?logo=linux)](https://git.vdm.dev/octoleo "--quiet") [![Llewellyn](https://img.shields.io/badge/-Llewellyn-ffffff?logo=gitea)](https://git.vdm.dev/Llewellyn "Collaborate and Innovate with Llewellyn on Git: Building a Better Code Future!") [![Telegram](https://img.shields.io/badge/-Telegram-blue?logo=telegram)](https://t.me/Joomla_component_builder "Join Llewellyn and the Community on Telegram: Building Joomla Components Together!") [![Mastodon](https://img.shields.io/badge/-Mastodon-9e9eec?logo=mastodon)](https://joomla.social/@llewellyn "Connect and Engage with Llewellyn on Joomla Social: Empowering Communities, One Post at a Time!") [![X (Twitter)](https://img.shields.io/badge/-X-black?logo=x)](https://x.com/llewellynvdm "Join the Conversation with Llewellyn on X: Where Ideas Take Flight!") [![GitHub](https://img.shields.io/badge/-GitHub-181717?logo=github)](https://github.com/Llewellynvdm "Build, Innovate, and Thrive with Llewellyn on GitHub: Turning Ideas into Impact!") [![YouTube](https://img.shields.io/badge/-YouTube-ff0000?logo=youtube)](https://www.youtube.com/@OctoYou "Explore, Learn, and Create with Llewellyn on YouTube: Your Gateway to Inspiration!") [![n8n](https://img.shields.io/badge/-n8n-black?logo=n8n)](https://n8n.io/creators/octoleo "Effortless Automation and Impactful Workflows with Llewellyn on n8n!") [![Docker Hub](https://img.shields.io/badge/-Docker-grey?logo=docker)](https://hub.docker.com/u/llewellyn "Llewellyn on Docker: Containerize Your Creativity!") [![Open Collective](https://img.shields.io/badge/-Donate-green?logo=opencollective)](https://opencollective.com/joomla-component-builder "Donate towards JCB: Help Llewellyn financially so he can continue developing this great tool!") [![GPG Key](https://img.shields.io/badge/-GPG-blue?logo=gnupg)](https://git.vdm.dev/Llewellyn/gpg "Unlock Trust and Security with Llewellyn's GPG Key: Your Gateway to Verified Connections!")