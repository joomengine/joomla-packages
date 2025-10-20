### JCB! Layout
# Search Box

## Key:
```php
echo LayoutHelper::render('searchbox', [?]);
```

## PHP:
```php
$baseUrl = $displayData['url'] ?? null;
$value   = $displayData['value'] ?? null;
$random  = Super___1f28cb53_60d9_4db1_b517_3c7dc6b429ef___Power::random(5);
```

## HTML:
```html
<?php if (!empty($baseUrl)): ?>
<div class="container-fluid">
	<div class="d-flex justify-content-end">
		<div class="input-group w-30">
			<input
				type="text"
				class="form-control"
				id="searchInput-<?php echo $random; ?>"
				placeholder="<?php echo Text::_('Search...'); ?>"
				aria-label="<?php echo Text::_('Search'); ?>"
				<?php if (!empty($value)): ?>value="<?php echo $value; ?>"<?php endif; ?>
			>
			<button class="btn btn-outline-secondary" type="button" id="searchButton-<?php echo $random; ?>">
				<i class="icon-search"></i>
			</button>

			<?php if (!empty($value)): ?>
			<button class="btn btn-outline-secondary" type="button" id="clearButton-<?php echo $random; ?>" title="<?php echo Text::_('Clear Search'); ?>">
				<i class="icon-cancel"></i>
			</button>
			<?php endif; ?>
		</div>
	</div>
</div>

<script>
document.addEventListener('DOMContentLoaded', function() {
	const input<?php echo $random; ?>  = document.getElementById('searchInput-<?php echo $random; ?>');
	const button<?php echo $random; ?> = document.getElementById('searchButton-<?php echo $random; ?>');
	const baseUrl<?php echo $random; ?> = '<?php echo $baseUrl; ?>';
	<?php if (!empty($value)): ?>
	const clearButton<?php echo $random; ?> = document.getElementById('clearButton-<?php echo $random; ?>');
	<?php endif; ?>

	function sanitizeInput<?php echo $random; ?>(text) {
		// Keep only letters, numbers, basic punctuation, and spaces
		return text.replace(/[^a-zA-Z0-9\s\-_.]/g, '').trim();
	}

	function triggerSearch<?php echo $random; ?>() {
		const term = sanitizeInput<?php echo $random; ?>(input<?php echo $random; ?>.value);
		if (term.length === 0) {
			return; // do nothing on empty input
		}
		window.location.href = baseUrl<?php echo $random; ?> + encodeURIComponent(term);
	}

	// Trigger search on Enter key
	input<?php echo $random; ?>.addEventListener('keypress', function(event) {
		if (event.key === 'Enter') {
			event.preventDefault();
			triggerSearch<?php echo $random; ?>();
		}
	});

	// Trigger search on icon click
	button<?php echo $random; ?>.addEventListener('click', function() {
		triggerSearch<?php echo $random; ?>();
	});

	<?php if (!empty($value)): ?>
	// Clear search and reload to base URL
	clearButton<?php echo $random; ?>.addEventListener('click', function() {
		window.location.href = baseUrl<?php echo $random; ?>;
	});
	<?php endif; ?>
});
</script>
<?php endif; ?>
```

> Enhance your Joomla components with a reusable layout that ensures consistent design, easy updates, and full compatibility within the JCB framework.

### Used in [Joomla Component Builder](https://www.joomlacomponentbuilder.com) - [Source](https://git.vdm.dev/joomla/Component-Builder) - [Mirror](https://github.com/vdm-io/Joomla-Component-Builder) - [Download](https://git.vdm.dev/joomla/pkg-component-builder/releases)

---
[![Joomla Volunteer Portal](https://img.shields.io/badge/-Joomla-gold?logo=joomla)](https://volunteers.joomla.org/joomlers/1396-llewellyn-van-der-merwe "Join Llewellyn on the Joomla Volunteer Portal: Shaping the Future Together!") [![Octoleo](https://img.shields.io/badge/-Octoleo-black?logo=linux)](https://git.vdm.dev/octoleo "--quiet") [![Llewellyn](https://img.shields.io/badge/-Llewellyn-ffffff?logo=gitea)](https://git.vdm.dev/Llewellyn "Collaborate and Innovate with Llewellyn on Git: Building a Better Code Future!") [![Telegram](https://img.shields.io/badge/-Telegram-blue?logo=telegram)](https://t.me/Joomla_component_builder "Join Llewellyn and the Community on Telegram: Building Joomla Components Together!") [![Mastodon](https://img.shields.io/badge/-Mastodon-9e9eec?logo=mastodon)](https://joomla.social/@llewellyn "Connect and Engage with Llewellyn on Joomla Social: Empowering Communities, One Post at a Time!") [![X (Twitter)](https://img.shields.io/badge/-X-black?logo=x)](https://x.com/llewellynvdm "Join the Conversation with Llewellyn on X: Where Ideas Take Flight!") [![GitHub](https://img.shields.io/badge/-GitHub-181717?logo=github)](https://github.com/Llewellynvdm "Build, Innovate, and Thrive with Llewellyn on GitHub: Turning Ideas into Impact!") [![YouTube](https://img.shields.io/badge/-YouTube-ff0000?logo=youtube)](https://www.youtube.com/@OctoYou "Explore, Learn, and Create with Llewellyn on YouTube: Your Gateway to Inspiration!") [![n8n](https://img.shields.io/badge/-n8n-black?logo=n8n)](https://n8n.io/creators/octoleo "Effortless Automation and Impactful Workflows with Llewellyn on n8n!") [![Docker Hub](https://img.shields.io/badge/-Docker-grey?logo=docker)](https://hub.docker.com/u/llewellyn "Llewellyn on Docker: Containerize Your Creativity!") [![Open Collective](https://img.shields.io/badge/-Donate-green?logo=opencollective)](https://opencollective.com/joomla-component-builder "Donate towards JCB: Help Llewellyn financially so he can continue developing this great tool!") [![GPG Key](https://img.shields.io/badge/-GPG-blue?logo=gnupg)](https://git.vdm.dev/Llewellyn/gpg "Unlock Trust and Security with Llewellyn's GPG Key: Your Gateway to Verified Connections!")