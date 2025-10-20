### JCB! Custom Code
# Get Time Based Random Seed

## JCB (manual)
```
[CUSTOMCODE=getTimeBasedRandomSeed]
```

### Code
```php
	/**
	 * Get or regenerate a time-based random seed that stays stable for one minute.
	 *
	 * This ensures consistent random ordering within a short window (e.g. pagination)
	 * while automatically changing after one minute. The seed is stored in the Joomla
	 * session and automatically refreshed when expired.
	 *
	 * @param  string  $sessionKey  Optional unique key to allow multiple independent seeds.
	 *
	 * @return int  The current time-based random seed.
	 * @since  5.1.3
	 */
	protected function getTimeBasedRandomSeed(string $sessionKey = '[[[component]]]_random_seed'): int
	{
		// Get session object
		$session = Factory::getApplication()->getSession();

		// Retrieve the stored seed data
		$seedData = $session->get($sessionKey);

		// Current minute window (rounded down to the current minute)
		$currentMinute = (int) (time() / 60);

		// If no seed exists or it's expired, regenerate it
		if (empty($seedData) || !isset($seedData['time']) || $seedData['time'] < $currentMinute)
		{
			$seed = random_int(1, 999999);
			$session->set($sessionKey, [
				'seed' => $seed,
				'time' => $currentMinute
			]);

			return $seed;
		}

		// Return existing active seed
		return (int) $seedData['seed'];
	}
```

> Add clean, self-contained code into your components with this reusable custom-code snippet designed for seamless integration and easy updates in JCB.

### Used in [Joomla Component Builder](https://www.joomlacomponentbuilder.com) - [Source](https://git.vdm.dev/joomla/Component-Builder) - [Mirror](https://github.com/vdm-io/Joomla-Component-Builder) - [Download](https://git.vdm.dev/joomla/pkg-component-builder/releases)

---
[![Joomla Volunteer Portal](https://img.shields.io/badge/-Joomla-gold?logo=joomla)](https://volunteers.joomla.org/joomlers/1396-llewellyn-van-der-merwe "Join Llewellyn on the Joomla Volunteer Portal: Shaping the Future Together!") [![Octoleo](https://img.shields.io/badge/-Octoleo-black?logo=linux)](https://git.vdm.dev/octoleo "--quiet") [![Llewellyn](https://img.shields.io/badge/-Llewellyn-ffffff?logo=gitea)](https://git.vdm.dev/Llewellyn "Collaborate and Innovate with Llewellyn on Git: Building a Better Code Future!") [![Telegram](https://img.shields.io/badge/-Telegram-blue?logo=telegram)](https://t.me/Joomla_component_builder "Join Llewellyn and the Community on Telegram: Building Joomla Components Together!") [![Mastodon](https://img.shields.io/badge/-Mastodon-9e9eec?logo=mastodon)](https://joomla.social/@llewellyn "Connect and Engage with Llewellyn on Joomla Social: Empowering Communities, One Post at a Time!") [![X (Twitter)](https://img.shields.io/badge/-X-black?logo=x)](https://x.com/llewellynvdm "Join the Conversation with Llewellyn on X: Where Ideas Take Flight!") [![GitHub](https://img.shields.io/badge/-GitHub-181717?logo=github)](https://github.com/Llewellynvdm "Build, Innovate, and Thrive with Llewellyn on GitHub: Turning Ideas into Impact!") [![YouTube](https://img.shields.io/badge/-YouTube-ff0000?logo=youtube)](https://www.youtube.com/@OctoYou "Explore, Learn, and Create with Llewellyn on YouTube: Your Gateway to Inspiration!") [![n8n](https://img.shields.io/badge/-n8n-black?logo=n8n)](https://n8n.io/creators/octoleo "Effortless Automation and Impactful Workflows with Llewellyn on n8n!") [![Docker Hub](https://img.shields.io/badge/-Docker-grey?logo=docker)](https://hub.docker.com/u/llewellyn "Llewellyn on Docker: Containerize Your Creativity!") [![Open Collective](https://img.shields.io/badge/-Donate-green?logo=opencollective)](https://opencollective.com/joomla-component-builder "Donate towards JCB: Help Llewellyn financially so he can continue developing this great tool!") [![GPG Key](https://img.shields.io/badge/-GPG-blue?logo=gnupg)](https://git.vdm.dev/Llewellyn/gpg "Unlock Trust and Security with Llewellyn's GPG Key: Your Gateway to Verified Connections!")