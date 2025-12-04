### JCB! Site View
# Category (category)

Category of companies

## HTML:
```html
<?php echo LayoutHelper::render('entitybanner', $this->banner ?? null); ?>
<?php echo LayoutHelper::render('searchbox', ['url' => $search_link, 'value' => $search_value]); ?>
<?php if (!empty($this->items)): ?>
	<?php echo $this->loadTemplate('companies'); ?>
<?php else: ?>
	<div class="container-xxl my-4">
		<div class="row">
			<div class="alert alert-warning mb-0" role="alert"><?php echo Text::_('No Items Found'); ?></div>
		</div>
	</div>
<?php endif; ?>

<?php
// Show only if there are items
if (!empty($this->items) && isset($this->pagination)) :
	$showLinks   = isset($this->pagination->pagesTotal) && $this->pagination->pagesTotal > 1;
	$showResults = $this->params->def('show_pagination_results', 1);
	?>
	<div class="pagination d-flex justify-content-between align-items-center flex-wrap mt-3">
		<?php if ($showLinks) : ?>
			<div class="page-links">
				[[[PAGESLINKS]]]
			</div>
		<?php else : ?>
			<!-- Keep layout stable when links are hidden -->
			<div class="page-links"></div>
		<?php endif; ?>

		<?php if ($showResults) : ?>
			<div class="page-info d-flex align-items-center justify-content-end text-end">
				<span class="me-2">[[[PAGESCOUNTER]]]</span>
				[[[LIMITBOX]]]
			</div>
		<?php endif; ?>
	</div>
<?php endif; ?>
```

> Deliver dynamic, custom front-end experiences with this reusable Site View crafted for seamless data flow and design flexibility in JCB.

### Used in [Joomla Component Builder](https://www.joomlacomponentbuilder.com) - [Source](https://git.vdm.dev/joomla/Component-Builder) - [Mirror](https://github.com/vdm-io/Joomla-Component-Builder) - [Download](https://git.vdm.dev/joomla/pkg-component-builder/releases)

---
[![Joomla Volunteer Portal](https://img.shields.io/badge/-Joomla-gold?logo=joomla)](https://volunteers.joomla.org/joomlers/1396-llewellyn-van-der-merwe "Join Llewellyn on the Joomla Volunteer Portal: Shaping the Future Together!") [![Octoleo](https://img.shields.io/badge/-Octoleo-black?logo=linux)](https://git.vdm.dev/octoleo "--quiet") [![Llewellyn](https://img.shields.io/badge/-Llewellyn-ffffff?logo=gitea)](https://git.vdm.dev/Llewellyn "Collaborate and Innovate with Llewellyn on Git: Building a Better Code Future!") [![Telegram](https://img.shields.io/badge/-Telegram-blue?logo=telegram)](https://t.me/Joomla_component_builder "Join Llewellyn and the Community on Telegram: Building Joomla Components Together!") [![Mastodon](https://img.shields.io/badge/-Mastodon-9e9eec?logo=mastodon)](https://joomla.social/@llewellyn "Connect and Engage with Llewellyn on Joomla Social: Empowering Communities, One Post at a Time!") [![X (Twitter)](https://img.shields.io/badge/-X-black?logo=x)](https://x.com/llewellynvdm "Join the Conversation with Llewellyn on X: Where Ideas Take Flight!") [![GitHub](https://img.shields.io/badge/-GitHub-181717?logo=github)](https://github.com/Llewellynvdm "Build, Innovate, and Thrive with Llewellyn on GitHub: Turning Ideas into Impact!") [![YouTube](https://img.shields.io/badge/-YouTube-ff0000?logo=youtube)](https://www.youtube.com/@OctoYou "Explore, Learn, and Create with Llewellyn on YouTube: Your Gateway to Inspiration!") [![n8n](https://img.shields.io/badge/-n8n-black?logo=n8n)](https://n8n.io/creators/octoleo "Effortless Automation and Impactful Workflows with Llewellyn on n8n!") [![Docker Hub](https://img.shields.io/badge/-Docker-grey?logo=docker)](https://hub.docker.com/u/llewellyn "Llewellyn on Docker: Containerize Your Creativity!") [![Open Collective](https://img.shields.io/badge/-Donate-green?logo=opencollective)](https://opencollective.com/joomla-component-builder "Donate towards JCB: Help Llewellyn financially so he can continue developing this great tool!") [![GPG Key](https://img.shields.io/badge/-GPG-blue?logo=gnupg)](https://git.vdm.dev/Llewellyn/gpg "Unlock Trust and Security with Llewellyn's GPG Key: Your Gateway to Verified Connections!")