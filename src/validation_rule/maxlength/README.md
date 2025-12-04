### JCB! Validation Rule
# maxlength

> max text length allowed

### Code
```php
	/**
	 * Validates a string value against the field's required state and maximum length.
	 *
	 * This method determines whether a field value is valid by checking:
	 * - Whether the field is marked as required.
	 * - Whether an empty value is allowed.
	 * - Whether the normalized length (whitespace removed) exceeds the configured maximum.
	 *
	 * The maximum length is read from the field's `maxlength` attribute and defaults to 2000
	 * characters when not specified.
	 *
	 * All whitespace is removed before length validation using UTF-8 safe processing.
	 *
	 * @param  \SimpleXMLElement  $element  The `<field>` definition containing attributes such as `required` and `maxlength`.
	 * @param  mixed              $value    The value being validated; expected to be castable to string.
	 * @param  string|null        $group    The name group (fieldset or repeatable context), if any.
	 * @param  Registry|null      $input    Optional registry containing the full form data set.
	 * @param  Form|null          $form     The form object owning this field.
	 *
	 * @return bool  True if the value passes validation, false otherwise.
	 *
	 * @since  5.1.4
	 */
	public function test(\SimpleXMLElement $element, $value, $group = null, ?Registry $input = null, ?Form $form = null)
	{
		// If the field is empty and not required, the field is valid.
		$required = ((string) $element['required'] === 'true' || (string) $element['required'] === 'required');

		if (!$required && empty($value)) {
			return true;
		}

		$length = $element['maxlength'] ?? 2000;

		// Normalize whitespace and trim
		$string = trim(preg_replace('/\s+/u', '', $value));

		if (mb_strlen($string) > $length)
		{
			return false;
		}

		return true;
	}
```

> Add clean, self-contained validation rule into your component fields with this reusable rule designed for seamless integration and easy updates in JCB.

### Used in [Joomla Component Builder](https://www.joomlacomponentbuilder.com) - [Source](https://git.vdm.dev/joomla/Component-Builder) - [Mirror](https://github.com/vdm-io/Joomla-Component-Builder) - [Download](https://git.vdm.dev/joomla/pkg-component-builder/releases)

---
[![Joomla Volunteer Portal](https://img.shields.io/badge/-Joomla-gold?logo=joomla)](https://volunteers.joomla.org/joomlers/1396-llewellyn-van-der-merwe "Join Llewellyn on the Joomla Volunteer Portal: Shaping the Future Together!") [![Octoleo](https://img.shields.io/badge/-Octoleo-black?logo=linux)](https://git.vdm.dev/octoleo "--quiet") [![Llewellyn](https://img.shields.io/badge/-Llewellyn-ffffff?logo=gitea)](https://git.vdm.dev/Llewellyn "Collaborate and Innovate with Llewellyn on Git: Building a Better Code Future!") [![Telegram](https://img.shields.io/badge/-Telegram-blue?logo=telegram)](https://t.me/Joomla_component_builder "Join Llewellyn and the Community on Telegram: Building Joomla Components Together!") [![Mastodon](https://img.shields.io/badge/-Mastodon-9e9eec?logo=mastodon)](https://joomla.social/@llewellyn "Connect and Engage with Llewellyn on Joomla Social: Empowering Communities, One Post at a Time!") [![X (Twitter)](https://img.shields.io/badge/-X-black?logo=x)](https://x.com/llewellynvdm "Join the Conversation with Llewellyn on X: Where Ideas Take Flight!") [![GitHub](https://img.shields.io/badge/-GitHub-181717?logo=github)](https://github.com/Llewellynvdm "Build, Innovate, and Thrive with Llewellyn on GitHub: Turning Ideas into Impact!") [![YouTube](https://img.shields.io/badge/-YouTube-ff0000?logo=youtube)](https://www.youtube.com/@OctoYou "Explore, Learn, and Create with Llewellyn on YouTube: Your Gateway to Inspiration!") [![n8n](https://img.shields.io/badge/-n8n-black?logo=n8n)](https://n8n.io/creators/octoleo "Effortless Automation and Impactful Workflows with Llewellyn on n8n!") [![Docker Hub](https://img.shields.io/badge/-Docker-grey?logo=docker)](https://hub.docker.com/u/llewellyn "Llewellyn on Docker: Containerize Your Creativity!") [![Open Collective](https://img.shields.io/badge/-Donate-green?logo=opencollective)](https://opencollective.com/joomla-component-builder "Donate towards JCB: Help Llewellyn financially so he can continue developing this great tool!") [![GPG Key](https://img.shields.io/badge/-GPG-blue?logo=gnupg)](https://git.vdm.dev/Llewellyn/gpg "Unlock Trust and Security with Llewellyn's GPG Key: Your Gateway to Verified Connections!")