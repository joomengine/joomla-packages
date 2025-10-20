### JCB! Custom Code
# Convert Markdown To Html

## JCB (manual)
```
[CUSTOMCODE=convertMarkdownToHtml]
```

### Code
```php
	/**
	 * Convert Markdown text to HTML.
	 *
	 * Uses the Super Power class responsible for Markdown-to-HTML conversion.
	 * The converter instance is cached statically to avoid repeated instantiations
	 * within the same request, improving overall performance.
	 *
	 * Example:
	 * ```php
	 * echo $this->convertMarkdownToHtml('# Hello World');
	 * ```
	 *
	 * @param  string  $string  The Markdown-formatted string to convert.
	 *
	 * @return string  The resulting HTML output or an empty string on failure.
	 * @since  5.1.2
	 */
	protected function convertMarkdownToHtml(string $string): string
	{
		$string = trim($string);
		if ($string === '')
		{
			return '';
		}

		static $Super___0fb58adc_60dd_42f4_9060_b782a5fd0537___Power = null;

		if ($Super___0fb58adc_60dd_42f4_9060_b782a5fd0537___Power === null)
		{
			$Super___0fb58adc_60dd_42f4_9060_b782a5fd0537___Power = new Super___0fb58adc_60dd_42f4_9060_b782a5fd0537___Power();
		}

		try
		{
			// Sanitize: remove all existing HTML to ensure only Markdown is processed
			$string = $this->escape($string);
		}
		catch (\Throwable $e)
		{
			return '';
		}

		if (trim($string) === '')
		{
			return '';
		}

		try
		{
			return $Super___0fb58adc_60dd_42f4_9060_b782a5fd0537___Power->convert($string);
		}
		catch (\Throwable $e)
		{
			// Fail gracefully, return empty string
			return '';
		}
	}
[CUSTOMCODE=modelEscape]
```

> Add clean, self-contained code into your components with this reusable custom-code snippet designed for seamless integration and easy updates in JCB.

### Used in [Joomla Component Builder](https://www.joomlacomponentbuilder.com) - [Source](https://git.vdm.dev/joomla/Component-Builder) - [Mirror](https://github.com/vdm-io/Joomla-Component-Builder) - [Download](https://git.vdm.dev/joomla/pkg-component-builder/releases)

---
[![Joomla Volunteer Portal](https://img.shields.io/badge/-Joomla-gold?logo=joomla)](https://volunteers.joomla.org/joomlers/1396-llewellyn-van-der-merwe "Join Llewellyn on the Joomla Volunteer Portal: Shaping the Future Together!") [![Octoleo](https://img.shields.io/badge/-Octoleo-black?logo=linux)](https://git.vdm.dev/octoleo "--quiet") [![Llewellyn](https://img.shields.io/badge/-Llewellyn-ffffff?logo=gitea)](https://git.vdm.dev/Llewellyn "Collaborate and Innovate with Llewellyn on Git: Building a Better Code Future!") [![Telegram](https://img.shields.io/badge/-Telegram-blue?logo=telegram)](https://t.me/Joomla_component_builder "Join Llewellyn and the Community on Telegram: Building Joomla Components Together!") [![Mastodon](https://img.shields.io/badge/-Mastodon-9e9eec?logo=mastodon)](https://joomla.social/@llewellyn "Connect and Engage with Llewellyn on Joomla Social: Empowering Communities, One Post at a Time!") [![X (Twitter)](https://img.shields.io/badge/-X-black?logo=x)](https://x.com/llewellynvdm "Join the Conversation with Llewellyn on X: Where Ideas Take Flight!") [![GitHub](https://img.shields.io/badge/-GitHub-181717?logo=github)](https://github.com/Llewellynvdm "Build, Innovate, and Thrive with Llewellyn on GitHub: Turning Ideas into Impact!") [![YouTube](https://img.shields.io/badge/-YouTube-ff0000?logo=youtube)](https://www.youtube.com/@OctoYou "Explore, Learn, and Create with Llewellyn on YouTube: Your Gateway to Inspiration!") [![n8n](https://img.shields.io/badge/-n8n-black?logo=n8n)](https://n8n.io/creators/octoleo "Effortless Automation and Impactful Workflows with Llewellyn on n8n!") [![Docker Hub](https://img.shields.io/badge/-Docker-grey?logo=docker)](https://hub.docker.com/u/llewellyn "Llewellyn on Docker: Containerize Your Creativity!") [![Open Collective](https://img.shields.io/badge/-Donate-green?logo=opencollective)](https://opencollective.com/joomla-component-builder "Donate towards JCB: Help Llewellyn financially so he can continue developing this great tool!") [![GPG Key](https://img.shields.io/badge/-GPG-blue?logo=gnupg)](https://git.vdm.dev/Llewellyn/gpg "Unlock Trust and Security with Llewellyn's GPG Key: Your Gateway to Verified Connections!")