### JCB! Layout
# Company Portfolio

## Key:
```php
echo LayoutHelper::render('companyportfolio', [?]);
```

## PHP:
```php
$client_name = $displayData->client_name ?? '';
$project_title = $displayData->project_title ?? '';
$target_industry = $displayData->target_industry ?? '';
$services_provided = $displayData->services_provided ?? '';
$project_url = $displayData->project_url ?? '';
$portfolio_desc = $displayData->description ?? '';
```

## HTML:
```html
<div class="row g-4">
	<div class="col-12 col-lg-8">
		<?php if (!empty($project_title)): ?>
			<h4 class="mb-2"><?php echo $project_title; ?></h4>
		<?php endif; ?>

		<ul class="list-unstyled small mb-3">
			<?php if (!empty($client_name)): ?>
				<li><strong><?php echo Text::_('Client'); ?>:</strong> <?php echo $client_name; ?></li>
			<?php endif; ?>
			<?php if (!empty($target_industry)): ?>
				<li><strong><?php echo Text::_('Industry'); ?>:</strong> <?php echo $target_industry; ?></li>
			<?php endif; ?>
			<?php if (!empty($services_provided)): ?>
				<li><strong><?php echo Text::_('Services'); ?>:</strong> <?php echo $services_provided; ?></li>
			<?php endif; ?>
			<?php if (!empty($project_url)): ?>
				<li><strong><?php echo Text::_('Url'); ?>:</strong> <a href="<?php echo $project_url; ?>"><?php echo $project_url; ?></a></li>
			<?php endif; ?>
		</ul>

		<?php if (trim($portfolio_desc) !== ''): ?>
			<div class="text-muted">
				<?php echo $portfolio_desc; ?>
			</div>
		<?php endif; ?>
	</div>
</div>
```

> Enhance your Joomla components with a reusable layout that ensures consistent design, easy updates, and full compatibility within the JCB framework.

### Used in [Joomla Component Builder](https://www.joomlacomponentbuilder.com) - [Source](https://git.vdm.dev/joomla/Component-Builder) - [Mirror](https://github.com/vdm-io/Joomla-Component-Builder) - [Download](https://git.vdm.dev/joomla/pkg-component-builder/releases)

---
[![Joomla Volunteer Portal](https://img.shields.io/badge/-Joomla-gold?logo=joomla)](https://volunteers.joomla.org/joomlers/1396-llewellyn-van-der-merwe "Join Llewellyn on the Joomla Volunteer Portal: Shaping the Future Together!") [![Octoleo](https://img.shields.io/badge/-Octoleo-black?logo=linux)](https://git.vdm.dev/octoleo "--quiet") [![Llewellyn](https://img.shields.io/badge/-Llewellyn-ffffff?logo=gitea)](https://git.vdm.dev/Llewellyn "Collaborate and Innovate with Llewellyn on Git: Building a Better Code Future!") [![Telegram](https://img.shields.io/badge/-Telegram-blue?logo=telegram)](https://t.me/Joomla_component_builder "Join Llewellyn and the Community on Telegram: Building Joomla Components Together!") [![Mastodon](https://img.shields.io/badge/-Mastodon-9e9eec?logo=mastodon)](https://joomla.social/@llewellyn "Connect and Engage with Llewellyn on Joomla Social: Empowering Communities, One Post at a Time!") [![X (Twitter)](https://img.shields.io/badge/-X-black?logo=x)](https://x.com/llewellynvdm "Join the Conversation with Llewellyn on X: Where Ideas Take Flight!") [![GitHub](https://img.shields.io/badge/-GitHub-181717?logo=github)](https://github.com/Llewellynvdm "Build, Innovate, and Thrive with Llewellyn on GitHub: Turning Ideas into Impact!") [![YouTube](https://img.shields.io/badge/-YouTube-ff0000?logo=youtube)](https://www.youtube.com/@OctoYou "Explore, Learn, and Create with Llewellyn on YouTube: Your Gateway to Inspiration!") [![n8n](https://img.shields.io/badge/-n8n-black?logo=n8n)](https://n8n.io/creators/octoleo "Effortless Automation and Impactful Workflows with Llewellyn on n8n!") [![Docker Hub](https://img.shields.io/badge/-Docker-grey?logo=docker)](https://hub.docker.com/u/llewellyn "Llewellyn on Docker: Containerize Your Creativity!") [![Open Collective](https://img.shields.io/badge/-Donate-green?logo=opencollective)](https://opencollective.com/joomla-component-builder "Donate towards JCB: Help Llewellyn financially so he can continue developing this great tool!") [![GPG Key](https://img.shields.io/badge/-GPG-blue?logo=gnupg)](https://git.vdm.dev/Llewellyn/gpg "Unlock Trust and Security with Llewellyn's GPG Key: Your Gateway to Verified Connections!")