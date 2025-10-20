### JCB! Custom Code
# Companies Data Setter

## JCB (manual)
```
[CUSTOMCODE=companiesDataSetter]
```

### Code
```php
		$this->entity = '';
		$pkg = (int) $this->input->getInt('id', 0);
		$targeted = false;
		if (!empty($pkg))
		{
			$this->entity = Super___9d76b8dc_3883_4755_b11c_131d19ca8a53___Power::_('Data.Item')->table($this->entity_type)->value($pkg, 'id', $guidKey);
			$companies = !empty($this->entity) ? Super___9d76b8dc_3883_4755_b11c_131d19ca8a53___Power::_('Data.Items')->table($joinTable)->values(
				[$this->entity], $this->entity_type, 'company') : null;
			if (Super___0a59c65c_9daf_4bc9_baf4_e063ff9e6a8a___Power::check($companies, true))
			{
				$companies = array_map(function($company) use ($db) { return $db->quote($company); }, $companies);
				$query->where('a.guid IN (' . implode(', ', $companies) .')');
				$targeted = true;
			}
		}
		if ($targeted)
		{
[CUSTOMCODE=modelCompanySearchQuery]
		}
		else
		{
			$query->where('a.id = 0'); // empty set
		}
		unset($companies, $search);
		// give us a random ordering here (new order every minute)
		$query->order('RAND(' . $this->getTimeBasedRandomSeed() . ')');
```

> Add clean, self-contained code into your components with this reusable custom-code snippet designed for seamless integration and easy updates in JCB.

### Used in [Joomla Component Builder](https://www.joomlacomponentbuilder.com) - [Source](https://git.vdm.dev/joomla/Component-Builder) - [Mirror](https://github.com/vdm-io/Joomla-Component-Builder) - [Download](https://git.vdm.dev/joomla/pkg-component-builder/releases)

---
[![Joomla Volunteer Portal](https://img.shields.io/badge/-Joomla-gold?logo=joomla)](https://volunteers.joomla.org/joomlers/1396-llewellyn-van-der-merwe "Join Llewellyn on the Joomla Volunteer Portal: Shaping the Future Together!") [![Octoleo](https://img.shields.io/badge/-Octoleo-black?logo=linux)](https://git.vdm.dev/octoleo "--quiet") [![Llewellyn](https://img.shields.io/badge/-Llewellyn-ffffff?logo=gitea)](https://git.vdm.dev/Llewellyn "Collaborate and Innovate with Llewellyn on Git: Building a Better Code Future!") [![Telegram](https://img.shields.io/badge/-Telegram-blue?logo=telegram)](https://t.me/Joomla_component_builder "Join Llewellyn and the Community on Telegram: Building Joomla Components Together!") [![Mastodon](https://img.shields.io/badge/-Mastodon-9e9eec?logo=mastodon)](https://joomla.social/@llewellyn "Connect and Engage with Llewellyn on Joomla Social: Empowering Communities, One Post at a Time!") [![X (Twitter)](https://img.shields.io/badge/-X-black?logo=x)](https://x.com/llewellynvdm "Join the Conversation with Llewellyn on X: Where Ideas Take Flight!") [![GitHub](https://img.shields.io/badge/-GitHub-181717?logo=github)](https://github.com/Llewellynvdm "Build, Innovate, and Thrive with Llewellyn on GitHub: Turning Ideas into Impact!") [![YouTube](https://img.shields.io/badge/-YouTube-ff0000?logo=youtube)](https://www.youtube.com/@OctoYou "Explore, Learn, and Create with Llewellyn on YouTube: Your Gateway to Inspiration!") [![n8n](https://img.shields.io/badge/-n8n-black?logo=n8n)](https://n8n.io/creators/octoleo "Effortless Automation and Impactful Workflows with Llewellyn on n8n!") [![Docker Hub](https://img.shields.io/badge/-Docker-grey?logo=docker)](https://hub.docker.com/u/llewellyn "Llewellyn on Docker: Containerize Your Creativity!") [![Open Collective](https://img.shields.io/badge/-Donate-green?logo=opencollective)](https://opencollective.com/joomla-component-builder "Donate towards JCB: Help Llewellyn financially so he can continue developing this great tool!") [![GPG Key](https://img.shields.io/badge/-GPG-blue?logo=gnupg)](https://git.vdm.dev/Llewellyn/gpg "Unlock Trust and Security with Llewellyn's GPG Key: Your Gateway to Verified Connections!")