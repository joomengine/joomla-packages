### JCB! Layout
# Note Ticket Conversation

## Key:
```php
echo LayoutHelper::render('noteticketconversation', [?]);
```

## PHP:
```php
// Extract data
$comments = $displayData['comments'] ?? [];
$user     = $displayData['user'] ?? null;
$userId   = (int) ($user?->id ?? 0);

// Group comments by day
$grouped = [];
foreach ($comments as $comment)
{
	try {
		$date = new Joomla___3864fa33_ab10_48d5_98ea_5e1397e6a191___Power($comment->created);
		$day  = $date->format('Y-m-d');
	} catch (Exception $e) {
		$day = date('Y-m-d');
	}
	$grouped[$day][] = $comment;
}
```

## HTML:
```html
<div class="container-fluid px-0">
	<div class="d-flex flex-column">
		<?php foreach ($grouped as $day => $items): ?>
			<div class="d-flex justify-content-center my-3">
				<span class="badge bg-light text-secondary border">
					<?php echo Html::_('date', $day, Text::_('DATE_FORMAT_LC3')); ?>
				</span>
			</div>
			<?php
			// Render bundles of consecutive comments by same author
			$bundles = [];
			$prevAuthor = null;
			foreach ($items as $comment)
			{
				if ($prevAuthor === $comment->created_by)
				{
					// Add to current bundle
					$bundles[count($bundles) - 1][] = $comment;
				}
				else
				{
					// Start new bundle
					$bundles[] = [$comment];
				}
				$prevAuthor = $comment->created_by;
			}
			foreach ($bundles as $bundle)
			{
				echo LayoutHelper::render('noteticketcomments',
					[
						'bundle'  => $bundle,
						'userId'  => $userId,
					]
				);
			}
			?>
		<?php endforeach; ?>
	</div>
</div>
```

> Enhance your Joomla components with a reusable layout that ensures consistent design, easy updates, and full compatibility within the JCB framework.

### Used in [Joomla Component Builder](https://www.joomlacomponentbuilder.com) - [Source](https://git.vdm.dev/joomla/Component-Builder) - [Mirror](https://github.com/vdm-io/Joomla-Component-Builder) - [Download](https://git.vdm.dev/joomla/pkg-component-builder/releases)

---
[![Joomla Volunteer Portal](https://img.shields.io/badge/-Joomla-gold?logo=joomla)](https://volunteers.joomla.org/joomlers/1396-llewellyn-van-der-merwe "Join Llewellyn on the Joomla Volunteer Portal: Shaping the Future Together!") [![Octoleo](https://img.shields.io/badge/-Octoleo-black?logo=linux)](https://git.vdm.dev/octoleo "--quiet") [![Llewellyn](https://img.shields.io/badge/-Llewellyn-ffffff?logo=gitea)](https://git.vdm.dev/Llewellyn "Collaborate and Innovate with Llewellyn on Git: Building a Better Code Future!") [![Telegram](https://img.shields.io/badge/-Telegram-blue?logo=telegram)](https://t.me/Joomla_component_builder "Join Llewellyn and the Community on Telegram: Building Joomla Components Together!") [![Mastodon](https://img.shields.io/badge/-Mastodon-9e9eec?logo=mastodon)](https://joomla.social/@llewellyn "Connect and Engage with Llewellyn on Joomla Social: Empowering Communities, One Post at a Time!") [![X (Twitter)](https://img.shields.io/badge/-X-black?logo=x)](https://x.com/llewellynvdm "Join the Conversation with Llewellyn on X: Where Ideas Take Flight!") [![GitHub](https://img.shields.io/badge/-GitHub-181717?logo=github)](https://github.com/Llewellynvdm "Build, Innovate, and Thrive with Llewellyn on GitHub: Turning Ideas into Impact!") [![YouTube](https://img.shields.io/badge/-YouTube-ff0000?logo=youtube)](https://www.youtube.com/@OctoYou "Explore, Learn, and Create with Llewellyn on YouTube: Your Gateway to Inspiration!") [![n8n](https://img.shields.io/badge/-n8n-black?logo=n8n)](https://n8n.io/creators/octoleo "Effortless Automation and Impactful Workflows with Llewellyn on n8n!") [![Docker Hub](https://img.shields.io/badge/-Docker-grey?logo=docker)](https://hub.docker.com/u/llewellyn "Llewellyn on Docker: Containerize Your Creativity!") [![Open Collective](https://img.shields.io/badge/-Donate-green?logo=opencollective)](https://opencollective.com/joomla-component-builder "Donate towards JCB: Help Llewellyn financially so he can continue developing this great tool!") [![GPG Key](https://img.shields.io/badge/-GPG-blue?logo=gnupg)](https://git.vdm.dev/Llewellyn/gpg "Unlock Trust and Security with Llewellyn's GPG Key: Your Gateway to Verified Connections!")