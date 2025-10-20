### JCB! Custom Code
# allowCompanyEdit

## JCB (manual)
```
[CUSTOMCODE=allowCompanyEdit]
```

### Code
```php
	/**
	 * Check whether the current user is allowed to edit a company record.
	 *
	 * This method validates both the global and ownership-based permissions
	 * for the provided company record, following Joomla's ACL structure.
	 *
	 * @param  object  $item  The company record to check permissions for.
	 *
	 * @return bool  True if editing is allowed, false otherwise.
	 * @since  5.1.3
	 */
	protected function allowCompanyEdit(object $item): bool
	{
		// Ensure we have a valid user and record ID
		if (empty($this->user) || empty($item->id))
		{
			return false;
		}

		$recordId = (int) $item->id;
		$ownerId  = isset($item->created_by) ? (int) $item->created_by : 0;

		// Check global edit permission for this specific company record
		if ($this->user->authorise('core.edit', 'com_[[[component]]].company.' . $recordId))
		{
			return true;
		}

		// Check edit own permissions at record level
		if ($this->user->authorise('core.edit.own', 'com_[[[component]]].company.' . $recordId))
		{
			// Only allow if current user is the record creator
			if ($ownerId === (int) $this->user->id)
			{
				// Also ensure the user has general edit own access in component scope
				return $this->user->authorise('core.edit.own', 'com_[[[component]]]');
			}
		}

		return false;
	}
```

> Add clean, self-contained code into your components with this reusable custom-code snippet designed for seamless integration and easy updates in JCB.

### Used in [Joomla Component Builder](https://www.joomlacomponentbuilder.com) - [Source](https://git.vdm.dev/joomla/Component-Builder) - [Mirror](https://github.com/vdm-io/Joomla-Component-Builder) - [Download](https://git.vdm.dev/joomla/pkg-component-builder/releases)

---
[![Joomla Volunteer Portal](https://img.shields.io/badge/-Joomla-gold?logo=joomla)](https://volunteers.joomla.org/joomlers/1396-llewellyn-van-der-merwe "Join Llewellyn on the Joomla Volunteer Portal: Shaping the Future Together!") [![Octoleo](https://img.shields.io/badge/-Octoleo-black?logo=linux)](https://git.vdm.dev/octoleo "--quiet") [![Llewellyn](https://img.shields.io/badge/-Llewellyn-ffffff?logo=gitea)](https://git.vdm.dev/Llewellyn "Collaborate and Innovate with Llewellyn on Git: Building a Better Code Future!") [![Telegram](https://img.shields.io/badge/-Telegram-blue?logo=telegram)](https://t.me/Joomla_component_builder "Join Llewellyn and the Community on Telegram: Building Joomla Components Together!") [![Mastodon](https://img.shields.io/badge/-Mastodon-9e9eec?logo=mastodon)](https://joomla.social/@llewellyn "Connect and Engage with Llewellyn on Joomla Social: Empowering Communities, One Post at a Time!") [![X (Twitter)](https://img.shields.io/badge/-X-black?logo=x)](https://x.com/llewellynvdm "Join the Conversation with Llewellyn on X: Where Ideas Take Flight!") [![GitHub](https://img.shields.io/badge/-GitHub-181717?logo=github)](https://github.com/Llewellynvdm "Build, Innovate, and Thrive with Llewellyn on GitHub: Turning Ideas into Impact!") [![YouTube](https://img.shields.io/badge/-YouTube-ff0000?logo=youtube)](https://www.youtube.com/@OctoYou "Explore, Learn, and Create with Llewellyn on YouTube: Your Gateway to Inspiration!") [![n8n](https://img.shields.io/badge/-n8n-black?logo=n8n)](https://n8n.io/creators/octoleo "Effortless Automation and Impactful Workflows with Llewellyn on n8n!") [![Docker Hub](https://img.shields.io/badge/-Docker-grey?logo=docker)](https://hub.docker.com/u/llewellyn "Llewellyn on Docker: Containerize Your Creativity!") [![Open Collective](https://img.shields.io/badge/-Donate-green?logo=opencollective)](https://opencollective.com/joomla-component-builder "Donate towards JCB: Help Llewellyn financially so he can continue developing this great tool!") [![GPG Key](https://img.shields.io/badge/-GPG-blue?logo=gnupg)](https://git.vdm.dev/Llewellyn/gpg "Unlock Trust and Security with Llewellyn's GPG Key: Your Gateway to Verified Connections!")