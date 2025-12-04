### JCB! Field
# Languages

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
	type_php_1="__.o0=base64=Oo.__CQkkZGIgPSBKb29tbGFfX18zOTQwMzA2Ml84NGZiXzQ2ZTBfYmFjNF8wMDIzZjc2NmU4MjdfX19Qb3dlcjo6Z2V0Q29udGFpbmVyKCktPmdldChKb29tbGFfX183YmQyOWQ3Nl83M2M5XzRjMDdfYTVkYV80ZjdhMzJhZmY3OGZfX19Qb3dlcjo6Y2xhc3MpOw0KCQkkcXVlcnkgPSAkZGItPmdldFF1ZXJ5KHRydWUpOw0KCQkkcXVlcnktPnNlbGVjdCgkZGItPnF1b3RlTmFtZShhcnJheSgnYS4jIyNJRCMjIycsJ2EuIyMjVEVYVCMjIycpLGFycmF5KCcjIyNJRCMjIycsJyMjI0NPREVfVEVYVCMjIycpKSk7DQoJCSRxdWVyeS0+ZnJvbSgkZGItPnF1b3RlTmFtZSgnIyMjVEFCTEUjIyMnLCAnYScpKTsNCgkJJHF1ZXJ5LT53aGVyZSgkZGItPnF1b3RlTmFtZSgnYS5wdWJsaXNoZWQnKSAuICcgPj0gMScpOw0KCQkkcXVlcnktPm9yZGVyKCdhLiMjI0lEIyMjIEFTQycpOw0KCQkkZGItPnNldFF1ZXJ5KChzdHJpbmcpJHF1ZXJ5KTsNCgkJJGl0ZW1zID0gJGRiLT5sb2FkT2JqZWN0TGlzdCgpOw0KCQkvLyBhZGQgdGhlIG1haW4gbGFuZ3VhZ2UNCgkJJG1haW5fbGFuZyA9IHRyaW0oSm9vbWxhX19fYWViOGU0NjNfMjkxZl80NDQ1XzlhYzRfMzRiNjM3YzEyZGJkX19fUG93ZXI6OmdldFBhcmFtcygnY29tXyMjI2NvbXBvbmVudCMjIycpLT5nZXQoJ2xhbmd1YWdlJywgJ2VuLUdCJykpOw0KCQkvLyBtYWtlIHN1cmUgdGhlIG1haW4gbGFuZ3VhZ2UgaXMgYWRkZWQNCgkJJHdhc0FkZGVkID0gZmFsc2U7DQoJCSRvcHRpb25zID0gYXJyYXkoKTsNCgkJaWYgKCRpdGVtcykNCgkJew0KCQkJJG9wdGlvbnNbXSA9IEpvb21sYV9fXzM0NjkwYzc1XzEwOTBfNDdlYl84YzA2XzcyMjhkYzdlZWRkNl9fX1Bvd2VyOjpfKCdzZWxlY3Qub3B0aW9uJywgJycsICdTZWxlY3QgYW4gb3B0aW9uJyk7DQoJCQlmb3JlYWNoKCRpdGVtcyBhcyAkaXRlbSkNCgkJCXsNCgkJCQkkaXRlbS0+IyMjSUQjIyMgPSB0cmltKCRpdGVtLT4jIyNJRCMjIyk7DQoJCQkJJG9wdGlvbnNbXSA9IEpvb21sYV9fXzM0NjkwYzc1XzEwOTBfNDdlYl84YzA2XzcyMjhkYzdlZWRkNl9fX1Bvd2VyOjpfKCdzZWxlY3Qub3B0aW9uJywgJGl0ZW0tPiMjI0lEIyMjLCAkaXRlbS0+IyMjQ09ERV9URVhUIyMjIC4gJyAoJyAuJGl0ZW0tPiMjI0lEIyMjLicpJyk7DQoJCQkJaWYgKCRtYWluX2xhbmcgPT09ICRpdGVtLT4jIyNJRCMjIykNCgkJCQl7DQoJCQkJCSR3YXNBZGRlZCA9IHRydWU7DQoJCQkJfQ0KCQkJfQ0KCQl9DQoJCS8vIG5vdyBhZGQgaXQgaWYgbm90IGFscmVhZHkgYWRkZWQgKGl0IG11c3QgZGVmYXVsdCB0byAkbWFpbl9sYW5nKQ0KCQlpZiAoISR3YXNBZGRlZCkNCgkJew0KCQkJaWYgKCdlbi1HQicgPT09ICRtYWluX2xhbmcpDQoJCQl7DQoJCQkJJG9wdGlvbnNbXSA9IEpvb21sYV9fXzM0NjkwYzc1XzEwOTBfNDdlYl84YzA2XzcyMjhkYzdlZWRkNl9fX1Bvd2VyOjpfKCdzZWxlY3Qub3B0aW9uJywgJG1haW5fbGFuZywgJ0VuZ2xpc2ggR0IgKCcgLiAkbWFpbl9sYW5nIC4gJyknKTsNCgkJCX0NCgkJCWVsc2UNCgkJCXsNCgkJCQkkb3B0aW9uc1tdID0gSm9vbWxhX19fMzQ2OTBjNzVfMTA5MF80N2ViXzhjMDZfNzIyOGRjN2VlZGQ2X19fUG93ZXI6Ol8oJ3NlbGVjdC5vcHRpb24nLCAkbWFpbl9sYW5nLCAnTWFpbiBMYW5ndWFnZSAoJyAuICRtYWluX2xhbmcgLiAnKScpOw0KCQkJfQ0KCQl9DQoJCXJldHVybiAkb3B0aW9uczs="
/>
```

## Database:
- Data type: TEXT
- Data length: 
- Data default: 
- Null switch: NULL
- Index: NOT INDEX
- Modeling: Expert Mode - Custom

> Define, capture, and control data effortlessly with this Field; the core building block of every JCB component.

### Used in [Joomla Component Builder](https://www.joomlacomponentbuilder.com) - [Source](https://git.vdm.dev/joomla/Component-Builder) - [Mirror](https://github.com/vdm-io/Joomla-Component-Builder) - [Download](https://git.vdm.dev/joomla/pkg-component-builder/releases)

---
[![Joomla Volunteer Portal](https://img.shields.io/badge/-Joomla-gold?logo=joomla)](https://volunteers.joomla.org/joomlers/1396-llewellyn-van-der-merwe "Join Llewellyn on the Joomla Volunteer Portal: Shaping the Future Together!") [![Octoleo](https://img.shields.io/badge/-Octoleo-black?logo=linux)](https://git.vdm.dev/octoleo "--quiet") [![Llewellyn](https://img.shields.io/badge/-Llewellyn-ffffff?logo=gitea)](https://git.vdm.dev/Llewellyn "Collaborate and Innovate with Llewellyn on Git: Building a Better Code Future!") [![Telegram](https://img.shields.io/badge/-Telegram-blue?logo=telegram)](https://t.me/Joomla_component_builder "Join Llewellyn and the Community on Telegram: Building Joomla Components Together!") [![Mastodon](https://img.shields.io/badge/-Mastodon-9e9eec?logo=mastodon)](https://joomla.social/@llewellyn "Connect and Engage with Llewellyn on Joomla Social: Empowering Communities, One Post at a Time!") [![X (Twitter)](https://img.shields.io/badge/-X-black?logo=x)](https://x.com/llewellynvdm "Join the Conversation with Llewellyn on X: Where Ideas Take Flight!") [![GitHub](https://img.shields.io/badge/-GitHub-181717?logo=github)](https://github.com/Llewellynvdm "Build, Innovate, and Thrive with Llewellyn on GitHub: Turning Ideas into Impact!") [![YouTube](https://img.shields.io/badge/-YouTube-ff0000?logo=youtube)](https://www.youtube.com/@OctoYou "Explore, Learn, and Create with Llewellyn on YouTube: Your Gateway to Inspiration!") [![n8n](https://img.shields.io/badge/-n8n-black?logo=n8n)](https://n8n.io/creators/octoleo "Effortless Automation and Impactful Workflows with Llewellyn on n8n!") [![Docker Hub](https://img.shields.io/badge/-Docker-grey?logo=docker)](https://hub.docker.com/u/llewellyn "Llewellyn on Docker: Containerize Your Creativity!") [![Open Collective](https://img.shields.io/badge/-Donate-green?logo=opencollective)](https://opencollective.com/joomla-component-builder "Donate towards JCB: Help Llewellyn financially so he can continue developing this great tool!") [![GPG Key](https://img.shields.io/badge/-GPG-blue?logo=gnupg)](https://git.vdm.dev/Llewellyn/gpg "Unlock Trust and Security with Llewellyn's GPG Key: Your Gateway to Verified Connections!")