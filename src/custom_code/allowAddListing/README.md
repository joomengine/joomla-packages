### JCB! Custom Code
# Helper::allowAddListing(..) max listings

## JCB (manual)
```
[CUSTOMCODE=allowAddListing]
```

### Code
```php
	/**
	 * Check whether the user is allowed to add or update an item.
	 *
	 * Enforces a per-user item limit while still allowing updates to existing
	 * records owned by the user.
	 *
	 * @param  Joomla___effdaf6d_2275_425d_9f52_d4952e564d34___Power|null   $user  The current user.
	 * @param  array|null  $data  The submitted data (may include 'id' for updates).
	 *
	 * @return bool  True to allow the action, false otherwise.
	 * @since  5.1.4
	 */
	public static function allowAddListing(?Joomla___effdaf6d_2275_425d_9f52_d4952e564d34___Power $user, ?array $data): bool
	{
		// User validation
		if (!$user || empty($user->id))
		{
			return false;
		}

		// Normalize incoming item ID
		$itemId = (isset($data['id']) && is_numeric($data['id']) && (int) $data['id'] > 0)
			? (int) $data['id']
			: null;

		// Fetch existing item IDs for user
		$existing = Super___9d76b8dc_3883_4755_b11c_131d19ca8a53___Power::_('Data.Items')
			->table('company')
			->values([$user->id], 'created_by', 'id');

		// Normalize DB result to array
		if (!is_array($existing))
		{
			$existing = [];
		}

		// Clean + normalize to integers
		$existing = array_values(array_filter(array_map('intval', $existing)));

		// Count existing items
		$count = count($existing);

		// Fetch maximum allowed listings
		$max = (int) Super___640b5352_fb09_425f_a26e_cd44eda03f15___Power::getParams('com_[[[component]]]')
			->get('max_listings', 1);

		// Ensure sane configuration
		if ($max < 1)
		{
			return false;
		}

		// ---------- UPDATE MODE ----------
		// Item exists and belongs to user → always allow
		if ($itemId !== null && in_array($itemId, $existing, true))
		{
			return true;
		}

		// ---------- CREATE MODE ----------
		// No ID in request OR ID not owned by user = new item

		// Already at or above max → deny
		if ($count >= $max)
		{
			return false;
		}

		// Below max → allow new item
		return true;
	}

```

> Add clean, self-contained code into your components with this reusable custom-code snippet designed for seamless integration and easy updates in JCB.

### Used in [Joomla Component Builder](https://www.joomlacomponentbuilder.com) - [Source](https://git.vdm.dev/joomla/Component-Builder) - [Mirror](https://github.com/vdm-io/Joomla-Component-Builder) - [Download](https://git.vdm.dev/joomla/pkg-component-builder/releases)

---
[![Joomla Volunteer Portal](https://img.shields.io/badge/-Joomla-gold?logo=joomla)](https://volunteers.joomla.org/joomlers/1396-llewellyn-van-der-merwe "Join Llewellyn on the Joomla Volunteer Portal: Shaping the Future Together!") [![Octoleo](https://img.shields.io/badge/-Octoleo-black?logo=linux)](https://git.vdm.dev/octoleo "--quiet") [![Llewellyn](https://img.shields.io/badge/-Llewellyn-ffffff?logo=gitea)](https://git.vdm.dev/Llewellyn "Collaborate and Innovate with Llewellyn on Git: Building a Better Code Future!") [![Telegram](https://img.shields.io/badge/-Telegram-blue?logo=telegram)](https://t.me/Joomla_component_builder "Join Llewellyn and the Community on Telegram: Building Joomla Components Together!") [![Mastodon](https://img.shields.io/badge/-Mastodon-9e9eec?logo=mastodon)](https://joomla.social/@llewellyn "Connect and Engage with Llewellyn on Joomla Social: Empowering Communities, One Post at a Time!") [![X (Twitter)](https://img.shields.io/badge/-X-black?logo=x)](https://x.com/llewellynvdm "Join the Conversation with Llewellyn on X: Where Ideas Take Flight!") [![GitHub](https://img.shields.io/badge/-GitHub-181717?logo=github)](https://github.com/Llewellynvdm "Build, Innovate, and Thrive with Llewellyn on GitHub: Turning Ideas into Impact!") [![YouTube](https://img.shields.io/badge/-YouTube-ff0000?logo=youtube)](https://www.youtube.com/@OctoYou "Explore, Learn, and Create with Llewellyn on YouTube: Your Gateway to Inspiration!") [![n8n](https://img.shields.io/badge/-n8n-black?logo=n8n)](https://n8n.io/creators/octoleo "Effortless Automation and Impactful Workflows with Llewellyn on n8n!") [![Docker Hub](https://img.shields.io/badge/-Docker-grey?logo=docker)](https://hub.docker.com/u/llewellyn "Llewellyn on Docker: Containerize Your Creativity!") [![Open Collective](https://img.shields.io/badge/-Donate-green?logo=opencollective)](https://opencollective.com/joomla-component-builder "Donate towards JCB: Help Llewellyn financially so he can continue developing this great tool!") [![GPG Key](https://img.shields.io/badge/-GPG-blue?logo=gnupg)](https://git.vdm.dev/Llewellyn/gpg "Unlock Trust and Security with Llewellyn's GPG Key: Your Gateway to Verified Connections!")