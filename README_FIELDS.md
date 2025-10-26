# JCB! Fields

### What Are Fields?
Fields are the **foundation** of every Joomla Component Builder (JCB) project.

They define how data is **stored**, **validated**, **rendered**, and **interacted with** in your Joomla extensions.

Fields let you control everything from the **underlying database schema** to the **user interface**, all within a single configuration.

Each Field:
- Defines **database structure** (type, size, default, null, unique keys, indexes)
- Binds to a **fieldtype**, determining HTML rendering and behavior
- Supports per-field **custom PHP** for model saving and retrieval
- Allows styling and scripting (HTML attributes, JS, CSS)
- Automatically generates Joomla-compliant XML field definitions

### Where Are Fields Used in JCB?
Fields are universal integrated — they are used in, highly structured areas:

- ✅ **Admin Views** (the native Joomla back-end editing views)
- ✅ **Modules** (frontend display configurations)
- ✅ **Plugins** (event-driven integrations)
- ✅ **Component Configurations** (global parameter settings)

### What Can a Field Do?
A Field in JCB can define:

- **Database Type & Schema**: `int`, `varchar`, `json`, custom, nullable, defaults, indexes
- **Permissions**: who can view/edit the field (ACL)
- **Rendering Options**: HTML classes, labels, JS behaviors
- **Model Integration**: how the value is saved or retrieved
- **Dynamic Logic**: PHP hooks for `onGet`, `onSave`, `onPrepareForm`, etc.
- **Fieldtypes**: link to rich behaviors like Model Selects, Subforms, Toggle Switches, Encrypted Fields, etc.

This centralization makes field management efficient and highly reusable.

### Reuse and Sharing
Fields are standalone entities:

- Define once, **reuse across multiple Admin Views**, Modules, or Plugins
- Fields can also be exported and shared via repositories
- JCB will automatically adjust them to fit into each consuming context

This means less duplication, and greater consistency across your entire component structure.

### Versioning and Customization
To update a field:

- Click **"reset"** in the JCB UI to sync with this repository
- Or **fork** this repository, customize the field, and point JCB to your fork

This preserves version control while allowing your own field improvements to live independently.

>Fields define both structure and behavior — they are where your data comes alive.

---
### Index of Fields


 - **Abbreviation (demo)** | [Details](src/field/c35e18fa-cade-48b8-b067-6289cc7a0f60) | [Settings](src/field/c35e18fa-cade-48b8-b067-6289cc7a0f60/item.json)
 - **Addresses (company-subform)** | [Details](src/field/9ef6e0ca-7d3e-40e6-b8ea-ff43224573f8) | [Settings](src/field/9ef6e0ca-7d3e-40e6-b8ea-ff43224573f8/item.json)
 - **Alias** | [Details](src/field/335866ce-b81b-4329-901d-c20254135c9c) | [Settings](src/field/335866ce-b81b-4329-901d-c20254135c9c/item.json)
 - **Allowed Document Formats** | [Details](src/field/24f17aaf-cc19-4bad-bc8b-4d37c79a898d) | [Settings](src/field/24f17aaf-cc19-4bad-bc8b-4d37c79a898d/item.json)
 - **Allowed File Formats** | [Details](src/field/ca8f38cb-f930-4976-a76b-c1d6cd18652d) | [Settings](src/field/ca8f38cb-f930-4976-a76b-c1d6cd18652d/item.json)
 - **Allowed Image Formats** | [Details](src/field/6b3c73d5-7640-43c0-a2e7-125a187f4513) | [Settings](src/field/6b3c73d5-7640-43c0-a2e7-125a187f4513/item.json)
 - **Allowed Media Formats** | [Details](src/field/fd936809-37c1-4016-a4ee-a4d016343725) | [Settings](src/field/fd936809-37c1-4016-a4ee-a4d016343725/item.json)
 - **Allowed Type** | [Details](src/field/9f6f776f-9741-4aec-a3ff-fb9880fdcb5c) | [Settings](src/field/9f6f776f-9741-4aec-a3ff-fb9880fdcb5c/item.json)
 - **Area of Expertise** | [Details](src/field/bcc78ac1-30e7-46d9-8ef7-69f21528f95f) | [Settings](src/field/bcc78ac1-30e7-46d9-8ef7-69f21528f95f/item.json)
 - **Areas of Expertise (custom)** | [Details](src/field/38751ed6-3082-408e-a21a-f5b30235da50) | [Settings](src/field/38751ed6-3082-408e-a21a-f5b30235da50/item.json)
 - **Bootstrap Social Icons** | [Details](src/field/dde7015f-ffe1-46a1-b24f-8e9e93aefb38) | [Settings](src/field/dde7015f-ffe1-46a1-b24f-8e9e93aefb38/item.json)
 - **Business Name** | [Details](src/field/28caada9-4354-4e87-bd62-4624a0761a9a) | [Settings](src/field/28caada9-4354-4e87-bd62-4624a0761a9a/item.json)
 - **Capital (citites-modal)** | [Details](src/field/baeaf484-f61b-4688-8b8a-e3ace669b7a7) | [Settings](src/field/baeaf484-f61b-4688-8b8a-e3ace669b7a7/item.json)
 - **Categories (Menu only)** | [Details](src/field/4b2b3c03-7e86-4ded-ba45-c3eb6fa9dc28) | [Settings](src/field/4b2b3c03-7e86-4ded-ba45-c3eb6fa9dc28/item.json)
 - **Category (Companies)** | [Details](src/field/b8dbe7d5-50d5-44e1-ab69-8b86b3a4a160) | [Settings](src/field/b8dbe7d5-50d5-44e1-ab69-8b86b3a4a160/item.json)
 - **Chamber of Commerce** | [Details](src/field/1a67060a-9e45-4b3b-8be6-8025bf3a3026) | [Settings](src/field/1a67060a-9e45-4b3b-8be6-8025bf3a3026/item.json)
 - **Cities (state)** | [Details](src/field/6630c034-f87f-4c5c-ab72-e5ae0e4c0e5b) | [Settings](src/field/6630c034-f87f-4c5c-ab72-e5ae0e4c0e5b/item.json)
 - **City (citites-modal)** | [Details](src/field/c069c4a5-f693-4e18-aee4-11292bf7fec8) | [Settings](src/field/c069c4a5-f693-4e18-aee4-11292bf7fec8/item.json)
 - **City (dynamic list)** | [Details](src/field/d95dc35a-7467-4010-8d35-f3dab696a808) | [Settings](src/field/d95dc35a-7467-4010-8d35-f3dab696a808/item.json)
 - **Code Three (currency)** | [Details](src/field/59f0d051-768e-41de-87a0-f47551f7d0d1) | [Settings](src/field/59f0d051-768e-41de-87a0-f47551f7d0d1/item.json)
 - **Comment (ticket_comment)** | [Details](src/field/90197849-128e-40b2-be4a-792617ab5b2d) | [Settings](src/field/90197849-128e-40b2-be4a-792617ab5b2d/item.json)
 - **Comment (tickets)** | [Details](src/field/57896492-bebe-4fba-9440-b71617846819) | [Settings](src/field/57896492-bebe-4fba-9440-b71617846819/item.json)
 - **Company** | [Details](src/field/16a136b8-fd99-41ad-b606-628bb6a91b75) | [Settings](src/field/16a136b8-fd99-41ad-b606-628bb6a91b75/item.json)
 - **Company (tickets)** | [Details](src/field/d84d1fa2-9275-4afb-b7d6-2d70b400011c) | [Settings](src/field/d84d1fa2-9275-4afb-b7d6-2d70b400011c/item.json)
 - **Company Size** | [Details](src/field/e4fff45e-0335-44f6-9dc7-54f2dc81d659) | [Settings](src/field/e4fff45e-0335-44f6-9dc7-54f2dc81d659/item.json)
 - **Company Type** | [Details](src/field/80fa4894-de6b-495f-9343-42b481edc385) | [Settings](src/field/80fa4894-de6b-495f-9343-42b481edc385/item.json)
 - **Contact Name** | [Details](src/field/5711daf2-43c4-4b35-9d0c-b96962062734) | [Settings](src/field/5711daf2-43c4-4b35-9d0c-b96962062734/item.json)
 - **Countries (multisubform)** | [Details](src/field/4d96ceea-7dd1-45c3-86fd-0d73d66332a8) | [Settings](src/field/4d96ceea-7dd1-45c3-86fd-0d73d66332a8/item.json)
 - **Country (custom)** | [Details](src/field/1c8bc5a9-06ab-429f-99d7-0b48e6b2b118) | [Settings](src/field/1c8bc5a9-06ab-429f-99d7-0b48e6b2b118/item.json)
 - **Country (modal)** | [Details](src/field/8d1b9d7e-77c1-43d9-bc97-0dd021bfe779) | [Settings](src/field/8d1b9d7e-77c1-43d9-bc97-0dd021bfe779/item.json)
 - **Created By (Owner - View)** | [Details](src/field/cdb60c2c-8961-446c-ab8c-7ff3dc960091) | [Settings](src/field/cdb60c2c-8961-446c-ab8c-7ff3dc960091/item.json)
 - **Crop Details** | [Details](src/field/6f327030-dcdf-4d80-b3d9-293d4bbe39f7) | [Settings](src/field/6f327030-dcdf-4d80-b3d9-293d4bbe39f7/item.json)
 - **Crop Height (in pixels)** | [Details](src/field/ab0d3b92-bd90-4957-ab71-cbc7a5fabeb3) | [Settings](src/field/ab0d3b92-bd90-4957-ab71-cbc7a5fabeb3/item.json)
 - **Crop Width (in pixels)** | [Details](src/field/1616608c-5307-4496-89e2-36a326a84716) | [Settings](src/field/1616608c-5307-4496-89e2-36a326a84716/item.json)
 - **Currency Name (country)** | [Details](src/field/4b964b88-36b4-4f26-a828-0e798ce9af38) | [Settings](src/field/4b964b88-36b4-4f26-a828-0e798ce9af38/item.json)
 - **Description (Directories)** | [Details](src/field/7ba7c96e-6838-4a3d-8dc6-bb1328b4e46f) | [Settings](src/field/7ba7c96e-6838-4a3d-8dc6-bb1328b4e46f/item.json)
 - **Description (full width)** | [Details](src/field/749a9917-90c3-49c4-9e72-aa33b0683a87) | [Settings](src/field/749a9917-90c3-49c4-9e72-aa33b0683a87/item.json)
 - **Download Access** | [Details](src/field/794ac8d4-c78b-4f98-9953-07e4ce5ad491) | [Settings](src/field/794ac8d4-c78b-4f98-9953-07e4ce5ad491/item.json)
 - **E-mail Address** | [Details](src/field/ba32af1e-0b57-4dcc-b9bb-7cec104c0ee7) | [Settings](src/field/ba32af1e-0b57-4dcc-b9bb-7cec104c0ee7/item.json)
 - **Entity File Type** | [Details](src/field/2a877e46-59b9-4f97-9dec-8c84c16741f2) | [Settings](src/field/2a877e46-59b9-4f97-9dec-8c84c16741f2/item.json)
 - **Entity Type (docs)** | [Details](src/field/2e24a9fe-5793-46be-b071-631c0b18d8f4) | [Settings](src/field/2e24a9fe-5793-46be-b071-631c0b18d8f4/item.json)
 - **FIPS code** | [Details](src/field/fa0ead84-06c8-4f18-89ae-4cdf646fd961) | [Settings](src/field/fa0ead84-06c8-4f18-89ae-4cdf646fd961/item.json)
 - **File Extension** | [Details](src/field/080b92dc-a4b4-46b2-83d4-3430284f5e06) | [Settings](src/field/080b92dc-a4b4-46b2-83d4-3430284f5e06/item.json)
 - **File Name** | [Details](src/field/725e856a-b8cc-4590-90e3-3eed6fd0873c) | [Settings](src/field/725e856a-b8cc-4590-90e3-3eed6fd0873c/item.json)
 - **File Path** | [Details](src/field/ed28e30c-30c3-4830-afdc-5a61bf25cd49) | [Settings](src/field/ed28e30c-30c3-4830-afdc-5a61bf25cd49/item.json)
 - **File Size** | [Details](src/field/77a1711b-ad1f-4379-921b-5e4ef5c31a42) | [Settings](src/field/77a1711b-ad1f-4379-921b-5e4ef5c31a42/item.json)
 - **File Type** | [Details](src/field/c2f884f9-31a0-4bb9-8310-64b5d9132d32) | [Settings](src/field/c2f884f9-31a0-4bb9-8310-64b5d9132d32/item.json)
 - **Flag emoji (country flag)** | [Details](src/field/962ec39f-78d4-42ee-9626-7b778d2eea25) | [Settings](src/field/962ec39f-78d4-42ee-9626-7b778d2eea25/item.json)
 - **Flag emojiU (unicode for flag)** | [Details](src/field/b71ee1ab-78ea-4cc7-aa2e-490a4d01a03f) | [Settings](src/field/b71ee1ab-78ea-4cc7-aa2e-490a4d01a03f/item.json)
 - **GMT Offset Name (timezone)** | [Details](src/field/480c9734-2820-4a61-afea-75b1db3fadc9) | [Settings](src/field/480c9734-2820-4a61-afea-75b1db3fadc9/item.json)
 - **GMT Offset Seconds (timezone)** | [Details](src/field/17788601-b3f8-439e-8ad7-11c7f8109e22) | [Settings](src/field/17788601-b3f8-439e-8ad7-11c7f8109e22/item.json)
 - **GUID** | [Details](src/field/5aa57bbe-7b19-4db9-915c-561863458d2b) | [Settings](src/field/5aa57bbe-7b19-4db9-915c-561863458d2b/item.json)
 - **GUID (Hidden)** | [Details](src/field/fb3115a1-e579-401a-9b53-9469cd4739e4) | [Settings](src/field/fb3115a1-e579-401a-9b53-9469cd4739e4/item.json)
 - **GUID ENTITY** | [Details](src/field/3f1fedeb-b943-42a7-88e7-c4f1eb1fd8a4) | [Settings](src/field/3f1fedeb-b943-42a7-88e7-c4f1eb1fd8a4/item.json)
 - **Handle (Link)** | [Details](src/field/d8d19384-f81c-4655-bd21-30149c2d4ead) | [Settings](src/field/d8d19384-f81c-4655-bd21-30149c2d4ead/item.json)
 - **ISO Three (country)** | [Details](src/field/95f46f99-0909-4a47-879b-ede06ef35fb8) | [Settings](src/field/95f46f99-0909-4a47-879b-ede06ef35fb8/item.json)
 - **ISO Two (country)** | [Details](src/field/2039d1c3-162c-401c-96fe-f127683ee3fe) | [Settings](src/field/2039d1c3-162c-401c-96fe-f127683ee3fe/item.json)
 - **Language (modalselect)** | [Details](src/field/783a690a-38a4-490b-a913-968de6369b39) | [Settings](src/field/783a690a-38a4-490b-a913-968de6369b39/item.json)
 - **Language Tag** | [Details](src/field/8fdf3640-8668-4818-be46-36c74f9e103e) | [Settings](src/field/8fdf3640-8668-4818-be46-36c74f9e103e/item.json)
 - **Languages** | [Details](src/field/1c821d8e-c5cf-48ef-8dfc-333e13d044e5) | [Settings](src/field/1c821d8e-c5cf-48ef-8dfc-333e13d044e5/item.json)
 - **Latitude (decimal)** | [Details](src/field/f7d3d78e-2d35-4884-a997-d073f853d095) | [Settings](src/field/f7d3d78e-2d35-4884-a997-d073f853d095/item.json)
 - **Line One (address)** | [Details](src/field/e5a082f3-54ab-4ab6-8691-afd195346d77) | [Settings](src/field/e5a082f3-54ab-4ab6-8691-afd195346d77/item.json)
 - **Line Two (address)** | [Details](src/field/cc0e70fa-bdda-474c-95c1-0ad5f1e9ec3c) | [Settings](src/field/cc0e70fa-bdda-474c-95c1-0ad5f1e9ec3c/item.json)
 - **Longitude (decimal)** | [Details](src/field/09c22738-6c6f-48ca-a24d-d439757e8619) | [Settings](src/field/09c22738-6c6f-48ca-a24d-d439757e8619/item.json)
 - **Max Number of Expertise** | [Details](src/field/f8f2b407-bfb0-4b74-a21a-1b5db69c18ff) | [Settings](src/field/f8f2b407-bfb0-4b74-a21a-1b5db69c18ff/item.json)
 - **Max Number of Languages** | [Details](src/field/9506cad5-e3cc-466e-b6bb-17f242df6616) | [Settings](src/field/9506cad5-e3cc-466e-b6bb-17f242df6616/item.json)
 - **Max Number of Listings Per/User** | [Details](src/field/9531af7c-efb8-4a6b-8c15-4eccbf38522b) | [Settings](src/field/9531af7c-efb8-4a6b-8c15-4eccbf38522b/item.json)
 - **Max Number of Tags** | [Details](src/field/9277d7f0-edf0-49a6-8615-cf450b286499) | [Settings](src/field/9277d7f0-edf0-49a6-8615-cf450b286499/item.json)
 - **Mime** | [Details](src/field/68c1e141-fb2e-49a6-bf56-1da6d8a058e8) | [Settings](src/field/68c1e141-fb2e-49a6-bf56-1da6d8a058e8/item.json)
 - **Name (Key - Required)** | [Details](src/field/5d3d34dd-4876-4c6a-86ab-b4e162f22c08) | [Settings](src/field/5d3d34dd-4876-4c6a-86ab-b4e162f22c08/item.json)
 - **Nationality (country)** | [Details](src/field/8ba72283-32fa-4a34-8c0d-d52adfed1aa5) | [Settings](src/field/8ba72283-32fa-4a34-8c0d-d52adfed1aa5/item.json)
 - **Native (country)** | [Details](src/field/2aad92a4-895d-46cb-b0df-751da1bdd703) | [Settings](src/field/2aad92a4-895d-46cb-b0df-751da1bdd703/item.json)
 - **Note - Company Portfolio** | [Details](src/field/38e18545-b311-4319-9961-c3667ec1db28) | [Settings](src/field/38e18545-b311-4319-9961-c3667ec1db28/item.json)
 - **Note Ticket Conversation** | [Details](src/field/eefbcf49-5603-457e-8d32-f744c2b35a47) | [Settings](src/field/eefbcf49-5603-457e-8d32-f744c2b35a47/item.json)
 - **Note VDM File Display** | [Details](src/field/639e63b1-a63d-4d40-853f-42e7b28a5d35) | [Settings](src/field/639e63b1-a63d-4d40-853f-42e7b28a5d35/item.json)
 - **Note VDM File Uploader** | [Details](src/field/47a3db14-de87-4cc2-8724-17f437a77d93) | [Settings](src/field/47a3db14-de87-4cc2-8724-17f437a77d93/item.json)
 - **Numeric Code (currency)** | [Details](src/field/40da896f-5054-4bb2-aa58-1cdfb391f544) | [Settings](src/field/40da896f-5054-4bb2-aa58-1cdfb391f544/item.json)
 - **Ordering Level (Categories)** | [Details](src/field/1540695d-e93a-4182-bdbe-42660a305d3f) | [Settings](src/field/1540695d-e93a-4182-bdbe-42660a305d3f/item.json)
 - **Parent Category** | [Details](src/field/1737aa23-d70c-4ca1-b242-bfa508cb328c) | [Settings](src/field/1737aa23-d70c-4ca1-b242-bfa508cb328c/item.json)
 - **Parent Tags** | [Details](src/field/0e2bbd0e-44a5-47d3-af8b-564d4ac29f9b) | [Settings](src/field/0e2bbd0e-44a5-47d3-af8b-564d4ac29f9b/item.json)
 - **Phone Code (country)** | [Details](src/field/149140a8-d0a6-4b62-a880-bb796e2145d8) | [Settings](src/field/149140a8-d0a6-4b62-a880-bb796e2145d8/item.json)
 - **Phone Number** | [Details](src/field/76886659-3578-4091-8c00-330c85f618dc) | [Settings](src/field/76886659-3578-4091-8c00-330c85f618dc/item.json)
 - **Platform** | [Details](src/field/332d557b-27ed-4346-98ab-2e06b4209d2d) | [Settings](src/field/332d557b-27ed-4346-98ab-2e06b4209d2d/item.json)
 - **Platform (custom)** | [Details](src/field/6fc68e03-8e01-41dc-895d-0bf8a29b65a6) | [Settings](src/field/6fc68e03-8e01-41dc-895d-0bf8a29b65a6/item.json)
 - **Portfolio (company-subform)** | [Details](src/field/99ef0b56-e724-4a18-8a67-ee432aa5c17f) | [Settings](src/field/99ef0b56-e724-4a18-8a67-ee432aa5c17f/item.json)
 - **Postal (address)** | [Details](src/field/e769beb6-f761-4885-8d35-eb2f0be55ee6) | [Settings](src/field/e769beb6-f761-4885-8d35-eb2f0be55ee6/item.json)
 - **Priority (ticket)** | [Details](src/field/b54dba1f-bfdc-49a2-95c4-3bbcea0861f0) | [Settings](src/field/b54dba1f-bfdc-49a2-95c4-3bbcea0861f0/item.json)
 - **Project Title** | [Details](src/field/1a2db720-19ca-40ff-9570-452bbcebd95b) | [Settings](src/field/1a2db720-19ca-40ff-9570-452bbcebd95b/item.json)
 - **Project URL (Link)** | [Details](src/field/820760db-d634-4f5e-8c5f-63a5709e0d93) | [Settings](src/field/820760db-d634-4f5e-8c5f-63a5709e0d93/item.json)
 - **Quantity Per Entity (file-uploader)** | [Details](src/field/e8c5a0cc-31fd-425e-9ebd-35716e3e140d) | [Settings](src/field/e8c5a0cc-31fd-425e-9ebd-35716e3e140d/item.json)
 - **Region (modal)** | [Details](src/field/7f3ccb20-7c57-433a-987b-b53d801004f3) | [Settings](src/field/7f3ccb20-7c57-433a-987b-b53d801004f3/item.json)
 - **Remove IDs from URLs** | [Details](src/field/d2556e49-6f4a-44aa-8640-15e4f101fa9d) | [Settings](src/field/d2556e49-6f4a-44aa-8640-15e4f101fa9d/item.json)
 - **Services Provided** | [Details](src/field/8afc97dd-c485-48a5-9723-07df1a15af89) | [Settings](src/field/8afc97dd-c485-48a5-9723-07df1a15af89/item.json)
 - **Show Listing Object** | [Details](src/field/82835f18-9ee4-41e4-957b-0000a6e8955f) | [Settings](src/field/82835f18-9ee4-41e4-957b-0000a6e8955f/item.json)
 - **Show Login** | [Details](src/field/10b7b6ec-74a3-454d-b7fa-55db619ac327) | [Settings](src/field/10b7b6ec-74a3-454d-b7fa-55db619ac327/item.json)
 - **Social Media Handles (company-subform)** | [Details](src/field/dc4924ac-bf78-4e97-9941-17cbbca898c6) | [Settings](src/field/dc4924ac-bf78-4e97-9941-17cbbca898c6/item.json)
 - **State (dynamic list)** | [Details](src/field/e80df9fc-5f50-468d-888c-e19cd96c3db1) | [Settings](src/field/e80df9fc-5f50-468d-888c-e19cd96c3db1/item.json)
 - **State (modal)** | [Details](src/field/1e666136-800a-486d-a8e8-13a054b7acde) | [Settings](src/field/1e666136-800a-486d-a8e8-13a054b7acde/item.json)
 - **States (subform)** | [Details](src/field/3cb5a436-7aa9-44c2-a68f-e3310b24c746) | [Settings](src/field/3cb5a436-7aa9-44c2-a68f-e3310b24c746/item.json)
 - **Status (Ticket-override)** | [Details](src/field/3ccf9728-ceb0-4ee2-95c6-5ab0ceb5f06e) | [Settings](src/field/3ccf9728-ceb0-4ee2-95c6-5ab0ceb5f06e/item.json)
 - **Status (override)** | [Details](src/field/6debe7be-69ad-4238-9114-288759578256) | [Settings](src/field/6debe7be-69ad-4238-9114-288759578256/item.json)
 - **Storage Folder** | [Details](src/field/523f91f8-ca60-44f7-9de0-645549967095) | [Settings](src/field/523f91f8-ca60-44f7-9de0-645549967095/item.json)
 - **Sub-Region (modal)** | [Details](src/field/19b4a840-cf4e-4012-8fae-b1439af74f5a) | [Settings](src/field/19b4a840-cf4e-4012-8fae-b1439af74f5a/item.json)
 - **Subject (tickets)** | [Details](src/field/f0ad9a75-6e97-4b2e-a6b0-51c7a8815312) | [Settings](src/field/f0ad9a75-6e97-4b2e-a6b0-51c7a8815312/item.json)
 - **Subregions (subform)** | [Details](src/field/cb04e362-61c0-4a07-8d80-d13b6939a72c) | [Settings](src/field/cb04e362-61c0-4a07-8d80-d13b6939a72c/item.json)
 - **Symbol (currency)** | [Details](src/field/c9a4c765-a0f9-42da-8fa9-df41ab70c448) | [Settings](src/field/c9a4c765-a0f9-42da-8fa9-df41ab70c448/item.json)
 - **TLD (country)** | [Details](src/field/c4c23fad-fd03-41cc-b5db-25f60b8ee11f) | [Settings](src/field/c4c23fad-fd03-41cc-b5db-25f60b8ee11f/item.json)
 - **Tag (modalselect)** | [Details](src/field/66f11387-8824-45b9-991d-af0c85c1f5db) | [Settings](src/field/66f11387-8824-45b9-991d-af0c85c1f5db/item.json)
 - **Tags (custom)** | [Details](src/field/83b63e41-afde-4578-af6c-c2010b01faee) | [Settings](src/field/83b63e41-afde-4578-af6c-c2010b01faee/item.json)
 - **Target (Files)** | [Details](src/field/e24026ef-294a-48e5-9be0-3f95dcb2b66b) | [Settings](src/field/e24026ef-294a-48e5-9be0-3f95dcb2b66b/item.json)
 - **Target Industry** | [Details](src/field/bf24f5e2-a0bf-4db0-b993-8c836f9e5b44) | [Settings](src/field/bf24f5e2-a0bf-4db0-b993-8c836f9e5b44/item.json)
 - **Ticket (comments)** | [Details](src/field/d835209a-6955-4047-bb91-3dfeed7c2e30) | [Settings](src/field/d835209a-6955-4047-bb91-3dfeed7c2e30/item.json)
 - **Ticket Status (override)** | [Details](src/field/71b40cd8-05be-45ca-8b61-8eee9cb00694) | [Settings](src/field/71b40cd8-05be-45ca-8b61-8eee9cb00694/item.json)
 - **Timezone Identifier (timezone)** | [Details](src/field/c20d4692-6e97-4441-83bd-561b73730407) | [Settings](src/field/c20d4692-6e97-4441-83bd-561b73730407/item.json)
 - **Timezone Name (timezone)** | [Details](src/field/f921d762-f5f1-4811-b1f5-71840c003a4e) | [Settings](src/field/f921d762-f5f1-4811-b1f5-71840c003a4e/item.json)
 - **Timezones (country)** | [Details](src/field/c803e176-923f-43a8-a542-12e27619a5f2) | [Settings](src/field/c803e176-923f-43a8-a542-12e27619a5f2/item.json)
 - **Tree Structure - Left (Hidden)** | [Details](src/field/4f6b179b-3a78-4276-86a4-713834e1bdf5) | [Settings](src/field/4f6b179b-3a78-4276-86a4-713834e1bdf5/item.json)
 - **Tree Structure - Right (Hidden)** | [Details](src/field/413bc704-27e8-4826-864f-855324c98e22) | [Settings](src/field/413bc704-27e8-4826-864f-855324c98e22/item.json)
 - **Type (address)** | [Details](src/field/19369aa2-33cf-4be4-8faf-7bd74e542971) | [Settings](src/field/19369aa2-33cf-4be4-8faf-7bd74e542971/item.json)
 - **Type (custom)** | [Details](src/field/874b0de4-46fb-4f4a-aa8a-d95c2e275a09) | [Settings](src/field/874b0de4-46fb-4f4a-aa8a-d95c2e275a09/item.json)
 - **Type (of state)** | [Details](src/field/4321fa80-702d-4ff5-ab3c-05507d3007a9) | [Settings](src/field/4321fa80-702d-4ff5-ab3c-05507d3007a9/item.json)
 - **Website** | [Details](src/field/b84bc31f-90ba-44bc-8808-c8fb3248ccd5) | [Settings](src/field/b84bc31f-90ba-44bc-8808-c8fb3248ccd5/item.json)
 - **WikiDataId** | [Details](src/field/af59b3ac-6a00-42c0-bbe2-edf90dec6081) | [Settings](src/field/af59b3ac-6a00-42c0-bbe2-edf90dec6081/item.json)

### All used in [Joomla Component Builder](https://www.joomlacomponentbuilder.com) - [Source](https://git.vdm.dev/joomla/Component-Builder) - [Mirror](https://github.com/vdm-io/Joomla-Component-Builder) - [Download](https://git.vdm.dev/joomla/pkg-component-builder/releases)

---
[![Joomla Volunteer Portal](https://img.shields.io/badge/-Joomla-gold?logo=joomla)](https://volunteers.joomla.org/joomlers/1396-llewellyn-van-der-merwe "Join Llewellyn on the Joomla Volunteer Portal: Shaping the Future Together!") [![Octoleo](https://img.shields.io/badge/-Octoleo-black?logo=linux)](https://git.vdm.dev/octoleo "--quiet") [![Llewellyn](https://img.shields.io/badge/-Llewellyn-ffffff?logo=gitea)](https://git.vdm.dev/Llewellyn "Collaborate and Innovate with Llewellyn on Git: Building a Better Code Future!") [![Telegram](https://img.shields.io/badge/-Telegram-blue?logo=telegram)](https://t.me/Joomla_component_builder "Join Llewellyn and the Community on Telegram: Building Joomla Components Together!") [![Mastodon](https://img.shields.io/badge/-Mastodon-9e9eec?logo=mastodon)](https://joomla.social/@llewellyn "Connect and Engage with Llewellyn on Joomla Social: Empowering Communities, One Post at a Time!") [![X (Twitter)](https://img.shields.io/badge/-X-black?logo=x)](https://x.com/llewellynvdm "Join the Conversation with Llewellyn on X: Where Ideas Take Flight!") [![GitHub](https://img.shields.io/badge/-GitHub-181717?logo=github)](https://github.com/Llewellynvdm "Build, Innovate, and Thrive with Llewellyn on GitHub: Turning Ideas into Impact!") [![YouTube](https://img.shields.io/badge/-YouTube-ff0000?logo=youtube)](https://www.youtube.com/@OctoYou "Explore, Learn, and Create with Llewellyn on YouTube: Your Gateway to Inspiration!") [![n8n](https://img.shields.io/badge/-n8n-black?logo=n8n)](https://n8n.io/creators/octoleo "Effortless Automation and Impactful Workflows with Llewellyn on n8n!") [![Docker Hub](https://img.shields.io/badge/-Docker-grey?logo=docker)](https://hub.docker.com/u/llewellyn "Llewellyn on Docker: Containerize Your Creativity!") [![Open Collective](https://img.shields.io/badge/-Donate-green?logo=opencollective)](https://opencollective.com/joomla-component-builder "Donate towards JCB: Help Llewellyn financially so he can continue developing this great tool!") [![GPG Key](https://img.shields.io/badge/-GPG-blue?logo=gnupg)](https://git.vdm.dev/Llewellyn/gpg "Unlock Trust and Security with Llewellyn's GPG Key: Your Gateway to Verified Connections!")