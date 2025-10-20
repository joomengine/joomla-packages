### JCB! Layout
# Addresses

## Key:
```php
echo LayoutHelper::render('addresses', [?]);
```

## PHP:
```php
$items = $displayData ?? [];
$count = is_array($items) ? count($items) : 0;

$uid = 'bs-carousel-' . substr(md5(uniqid('', true)), 0, 8);

// How many cards you want per *slide* on large screens
$perSlide = 4;

// Chunk items into slides (only used if we actually show the carousel)
$slides = $count > 3 ? array_chunk($items, $perSlide) : [];
```

## HTML:
```html
<?php if ($count === 0) : ?>
	<!-- nothing to render -->
<?php elseif ($count <= $perSlide) : ?>
	<div class="container px-0">
		<div class="row row-cols-1 row-cols-sm-2 row-cols-md-3 g-3">
			<?php foreach ($items as $item): ?>
				<div class="col">
					<div class="card h-100">
						<div class="card-body">
							<?php echo LayoutHelper::render('address', $item); ?>
						</div>
					</div>
				</div>
			<?php endforeach; ?>
		</div>
	</div>
<?php else : ?>
	<div class="container px-0">
		<div class="d-flex flex-row flex-nowrap overflow-auto gap-3 p-2">
			<?php foreach ($items as $item): ?>
				<div class="card flex-shrink-0" style="width: 18rem;">
					<div class="card-body">
						<?php echo LayoutHelper::render('address', $item); ?>
					</div>
				</div>
			<?php endforeach; ?>
		</div>
	</div>
<?php endif; ?>
```

> Enhance your Joomla components with a reusable layout that ensures consistent design, easy updates, and full compatibility within the JCB framework.

### Used in [Joomla Component Builder](https://www.joomlacomponentbuilder.com) - [Source](https://git.vdm.dev/joomla/Component-Builder) - [Mirror](https://github.com/vdm-io/Joomla-Component-Builder) - [Download](https://git.vdm.dev/joomla/pkg-component-builder/releases)

---
[![Joomla Volunteer Portal](https://img.shields.io/badge/-Joomla-gold?logo=joomla)](https://volunteers.joomla.org/joomlers/1396-llewellyn-van-der-merwe "Join Llewellyn on the Joomla Volunteer Portal: Shaping the Future Together!") [![Octoleo](https://img.shields.io/badge/-Octoleo-black?logo=linux)](https://git.vdm.dev/octoleo "--quiet") [![Llewellyn](https://img.shields.io/badge/-Llewellyn-ffffff?logo=gitea)](https://git.vdm.dev/Llewellyn "Collaborate and Innovate with Llewellyn on Git: Building a Better Code Future!") [![Telegram](https://img.shields.io/badge/-Telegram-blue?logo=telegram)](https://t.me/Joomla_component_builder "Join Llewellyn and the Community on Telegram: Building Joomla Components Together!") [![Mastodon](https://img.shields.io/badge/-Mastodon-9e9eec?logo=mastodon)](https://joomla.social/@llewellyn "Connect and Engage with Llewellyn on Joomla Social: Empowering Communities, One Post at a Time!") [![X (Twitter)](https://img.shields.io/badge/-X-black?logo=x)](https://x.com/llewellynvdm "Join the Conversation with Llewellyn on X: Where Ideas Take Flight!") [![GitHub](https://img.shields.io/badge/-GitHub-181717?logo=github)](https://github.com/Llewellynvdm "Build, Innovate, and Thrive with Llewellyn on GitHub: Turning Ideas into Impact!") [![YouTube](https://img.shields.io/badge/-YouTube-ff0000?logo=youtube)](https://www.youtube.com/@OctoYou "Explore, Learn, and Create with Llewellyn on YouTube: Your Gateway to Inspiration!") [![n8n](https://img.shields.io/badge/-n8n-black?logo=n8n)](https://n8n.io/creators/octoleo "Effortless Automation and Impactful Workflows with Llewellyn on n8n!") [![Docker Hub](https://img.shields.io/badge/-Docker-grey?logo=docker)](https://hub.docker.com/u/llewellyn "Llewellyn on Docker: Containerize Your Creativity!") [![Open Collective](https://img.shields.io/badge/-Donate-green?logo=opencollective)](https://opencollective.com/joomla-component-builder "Donate towards JCB: Help Llewellyn financially so he can continue developing this great tool!") [![GPG Key](https://img.shields.io/badge/-GPG-blue?logo=gnupg)](https://git.vdm.dev/Llewellyn/gpg "Unlock Trust and Security with Llewellyn's GPG Key: Your Gateway to Verified Connections!")