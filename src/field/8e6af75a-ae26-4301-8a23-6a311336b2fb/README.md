### JCB! Field
# Languages - local

> Field Type: Custom

## Field XML:
```xml
<field
	type="lang"
	name="languages"
	label="Language(s)"
	description=""
	class="list_class"
	layout="joomla.form.field.list-fancy-select"
	multiple="true"
	default="en-GB"
	required="true"
	extends="list"
	button="true"
	table="#__###component###_language"
	component="com_###component###"
	view="language"
	views="languages"
	value_field="name"
	key_field="langtag"
	prime_php="1"
	type_php_1="__.o0=base64=Oo.__JGRiID0gRmFjdG9yeTo6Z2V0REJPKCk7DQoJCSRxdWVyeSA9ICRkYi0+Z2V0UXVlcnkodHJ1ZSk7DQoJCSRxdWVyeS0+c2VsZWN0KCRkYi0+cXVvdGVOYW1lKGFycmF5KCdhLiMjI0lEIyMjJywnYS4jIyNURVhUIyMjJyksYXJyYXkoJyMjI0lEIyMjJywnIyMjQ09ERV9URVhUIyMjJykpKTsNCgkJJHF1ZXJ5LT5mcm9tKCRkYi0+cXVvdGVOYW1lKCcjIyNUQUJMRSMjIycsICdhJykpOw0KCQkkcXVlcnktPndoZXJlKCRkYi0+cXVvdGVOYW1lKCdhLnB1Ymxpc2hlZCcpIC4gJyA+PSAxJyk7DQoJCSRxdWVyeS0+b3JkZXIoJ2EuIyMjSUQjIyMgQVNDJyk7DQoJCSRkYi0+c2V0UXVlcnkoKHN0cmluZykkcXVlcnkpOw0KCQkkaXRlbXMgPSAkZGItPmxvYWRPYmplY3RMaXN0KCk7DQoJCS8vIGFkZCB0aGUgbWFpbiBsYW5ndWFnZQ0KCQkkbWFpbl9sYW5nID0gdHJpbShKb29tbGFfX19hZWI4ZTQ2M18yOTFmXzQ0NDVfOWFjNF8zNGI2MzdjMTJkYmRfX19Qb3dlcjo6Z2V0UGFyYW1zKCdjb21fIyMjY29tcG9uZW50IyMjJyktPmdldCgnbGFuZ3VhZ2UnLCAnZW4tR0InKSk7DQoJCS8vIG1ha2Ugc3VyZSB0aGUgbWFpbiBsYW5ndWFnZSBpcyBhZGRlZA0KCQkkd2FzQWRkZWQgPSBmYWxzZTsNCgkJJG9wdGlvbnMgPSBhcnJheSgpOw0KCQlpZiAoJGl0ZW1zKQ0KCQl7DQoJCQkkb3B0aW9uc1tdID0gSm9vbWxhX19fMzQ2OTBjNzVfMTA5MF80N2ViXzhjMDZfNzIyOGRjN2VlZGQ2X19fUG93ZXI6Ol8oJ3NlbGVjdC5vcHRpb24nLCAnJywgJ1NlbGVjdCBhbiBvcHRpb24nKTsNCgkJCWZvcmVhY2goJGl0ZW1zIGFzICRpdGVtKQ0KCQkJew0KCQkJCSRpdGVtLT4jIyNJRCMjIyA9IHRyaW0oJGl0ZW0tPiMjI0lEIyMjKTsNCgkJCQkkb3B0aW9uc1tdID0gSm9vbWxhX19fMzQ2OTBjNzVfMTA5MF80N2ViXzhjMDZfNzIyOGRjN2VlZGQ2X19fUG93ZXI6Ol8oJ3NlbGVjdC5vcHRpb24nLCAkaXRlbS0+IyMjSUQjIyMsICRpdGVtLT4jIyNDT0RFX1RFWFQjIyMgLiAnICgnIC4kaXRlbS0+IyMjSUQjIyMuJyknKTsNCgkJCQlpZiAoJG1haW5fbGFuZyA9PT0gJGl0ZW0tPiMjI0lEIyMjKQ0KCQkJCXsNCgkJCQkJJHdhc0FkZGVkID0gdHJ1ZTsNCgkJCQl9DQoJCQl9DQoJCX0NCgkJLy8gbm93IGFkZCBpdCBpZiBub3QgYWxyZWFkeSBhZGRlZCAoaXQgbXVzdCBkZWZhdWx0IHRvICRtYWluX2xhbmcpDQoJCWlmICghJHdhc0FkZGVkKQ0KCQl7DQoJCQlpZiAoJ2VuLUdCJyA9PT0gJG1haW5fbGFuZykNCgkJCXsNCgkJCQkkb3B0aW9uc1tdID0gSm9vbWxhX19fMzQ2OTBjNzVfMTA5MF80N2ViXzhjMDZfNzIyOGRjN2VlZGQ2X19fUG93ZXI6Ol8oJ3NlbGVjdC5vcHRpb24nLCAkbWFpbl9sYW5nLCAnRW5nbGlzaCBHQiAoJyAuICRtYWluX2xhbmcgLiAnKScpOw0KCQkJfQ0KCQkJZWxzZQ0KCQkJew0KCQkJCSRvcHRpb25zW10gPSBKb29tbGFfX18zNDY5MGM3NV8xMDkwXzQ3ZWJfOGMwNl83MjI4ZGM3ZWVkZDZfX19Qb3dlcjo6Xygnc2VsZWN0Lm9wdGlvbicsICRtYWluX2xhbmcsICdNYWluIExhbmd1YWdlICgnIC4gJG1haW5fbGFuZyAuICcpJyk7DQoJCQl9DQoJCX0NCgkJcmV0dXJuICRvcHRpb25zOw=="
/>
```

## Database:
- Data type: TEXT
- Data length: 
- Data default: 
- Null switch: NULL
- Index: NOT INDEX
- Modeling: Default

> Define, capture, and control data effortlessly with this Field; the core building block of every JCB component.

### Used in [Joomla Component Builder](https://www.joomlacomponentbuilder.com) - [Source](https://git.vdm.dev/joomla/Component-Builder) - [Mirror](https://github.com/vdm-io/Joomla-Component-Builder) - [Download](https://git.vdm.dev/joomla/pkg-component-builder/releases)

---
[![Joomla Volunteer Portal](https://img.shields.io/badge/-Joomla-gold?logo=joomla)](https://volunteers.joomla.org/joomlers/1396-llewellyn-van-der-merwe "Join Llewellyn on the Joomla Volunteer Portal: Shaping the Future Together!") [![Octoleo](https://img.shields.io/badge/-Octoleo-black?logo=linux)](https://git.vdm.dev/octoleo "--quiet") [![Llewellyn](https://img.shields.io/badge/-Llewellyn-ffffff?logo=gitea)](https://git.vdm.dev/Llewellyn "Collaborate and Innovate with Llewellyn on Git: Building a Better Code Future!") [![Telegram](https://img.shields.io/badge/-Telegram-blue?logo=telegram)](https://t.me/Joomla_component_builder "Join Llewellyn and the Community on Telegram: Building Joomla Components Together!") [![Mastodon](https://img.shields.io/badge/-Mastodon-9e9eec?logo=mastodon)](https://joomla.social/@llewellyn "Connect and Engage with Llewellyn on Joomla Social: Empowering Communities, One Post at a Time!") [![X (Twitter)](https://img.shields.io/badge/-X-black?logo=x)](https://x.com/llewellynvdm "Join the Conversation with Llewellyn on X: Where Ideas Take Flight!") [![GitHub](https://img.shields.io/badge/-GitHub-181717?logo=github)](https://github.com/Llewellynvdm "Build, Innovate, and Thrive with Llewellyn on GitHub: Turning Ideas into Impact!") [![YouTube](https://img.shields.io/badge/-YouTube-ff0000?logo=youtube)](https://www.youtube.com/@OctoYou "Explore, Learn, and Create with Llewellyn on YouTube: Your Gateway to Inspiration!") [![n8n](https://img.shields.io/badge/-n8n-black?logo=n8n)](https://n8n.io/creators/octoleo "Effortless Automation and Impactful Workflows with Llewellyn on n8n!") [![Docker Hub](https://img.shields.io/badge/-Docker-grey?logo=docker)](https://hub.docker.com/u/llewellyn "Llewellyn on Docker: Containerize Your Creativity!") [![Open Collective](https://img.shields.io/badge/-Donate-green?logo=opencollective)](https://opencollective.com/joomla-component-builder "Donate towards JCB: Help Llewellyn financially so he can continue developing this great tool!") [![GPG Key](https://img.shields.io/badge/-GPG-blue?logo=gnupg)](https://git.vdm.dev/Llewellyn/gpg "Unlock Trust and Security with Llewellyn's GPG Key: Your Gateway to Verified Connections!")