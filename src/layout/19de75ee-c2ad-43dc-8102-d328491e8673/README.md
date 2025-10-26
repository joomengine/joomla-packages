### JCB! Layout
# Company Listings

## Key:
```php
echo LayoutHelper::render('companylistings', [?]);
```

## PHP:
```php
$items = $displayData->mine ?? [];
```

## HTML:
```html
<div class="row row-cols-1 row-cols-md-2 row-cols-lg-3 g-4">
	<?php foreach ($items as $item) : ?>
		<div class="col">
			<div class="card border-0 shadow-sm h-100">
				<div class="card-body d-flex flex-column justify-content-between">
					<div>
						<h5 class="card-title mb-1">
							<?php if (!empty($item->edit_link)): ?>
								<span class="me-2">
									<a href="<?php echo $item->edit_link; ?>" title="<?php echo Text::_('Edit Listing'); ?>"><span class="icon-pencil-2 article-edit"></span></a>
								</span>
							<?php endif; ?>
							<?php if (!empty($item->link)): ?>
								<a href="<?php echo $item->link; ?>" class="text-decoration-none">
									<?php echo $displayData->escape($item->name); ?>
								</a>
							<?php else: ?>
								<?php echo $displayData->escape($item->name); ?>
							<?php endif; ?>
						</h5>
						<p class="card-text small text-muted mb-2">
							<?php echo $displayData->escape($item->description, true, 200); ?>
						</p>
						<ul class="list-unstyled small mb-0">
							<?php if (!empty($item->contactname)) : ?>
								<li><strong><?php echo Text::_('Contact Name:'); ?></strong> <?php echo $displayData->escape($item->contactname); ?></li>
							<?php endif; ?>
							<?php if (!empty($item->email)) : ?>
								<li><strong><?php echo Text::_('Email:'); ?></strong>
									<a href="mailto:<?php echo $displayData->escape($item->email, false); ?>">
										<?php echo $displayData->escape($item->email, true, 30); ?>
									</a>
								</li>
							<?php endif; ?>
							<?php if (!empty($item->phone)) : ?>
								<li><strong><?php echo Text::_('Phone:'); ?></strong>
									<?php echo $displayData->escape($item->phone, false); ?>
								</li>
							<?php endif; ?>
							<?php if (!empty($item->website)) : ?>
								<li><strong><?php echo Text::_('Website:'); ?></strong>
									<a href="<?php echo $displayData->escape($item->website, false); ?>" target="_blank" rel="noopener">
										<?php echo $displayData->escape($item->website, true, 30); ?>
									</a>
								</li>
							<?php endif; ?>
							<?php if (!empty($item->created)): ?>
								<li><strong><?php echo Text::_('Status:'); ?></strong>
									<?php echo $item->published ? Text::_('Published') : Text::_('Unpublished'); ?>
								</li>
							<?php endif; ?>
							<?php if (!empty($item->created)): ?>
								<li><strong><?php echo Text::_('Created:'); ?></strong>
									<?php echo Html::_('date', $item->created, Text::_('DATE_FORMAT_LC3')); ?>
								</li>
							<?php endif; ?>
							<?php if (!empty($item->modified)): ?>
								<li><strong><?php echo Text::_('Last Modified:'); ?></strong>
									<?php echo Html::_('date', $item->modified, Text::_('DATE_FORMAT_LC3')); ?>
								</li>
							<?php endif; ?>
						</ul>
					</div>

					<?php if (!empty($item->edit_link)): ?>
						<div class="mt-3 text-end">
							<a href="<?php echo $item->edit_link; ?>" class="btn btn-sm btn-outline-primary">
								<span class="icon-pencil-2 article-edit"></span> <?php echo Text::_('Edit Listing'); ?>
							</a>
						</div>
					<?php endif; ?>
				</div>
			</div>
		</div>
	<?php endforeach; ?>
</div>
```

> Enhance your Joomla components with a reusable layout that ensures consistent design, easy updates, and full compatibility within the JCB framework.

### Used in [Joomla Component Builder](https://www.joomlacomponentbuilder.com) - [Source](https://git.vdm.dev/joomla/Component-Builder) - [Mirror](https://github.com/vdm-io/Joomla-Component-Builder) - [Download](https://git.vdm.dev/joomla/pkg-component-builder/releases)

---
[![Joomla Volunteer Portal](https://img.shields.io/badge/-Joomla-gold?logo=joomla)](https://volunteers.joomla.org/joomlers/1396-llewellyn-van-der-merwe "Join Llewellyn on the Joomla Volunteer Portal: Shaping the Future Together!") [![Octoleo](https://img.shields.io/badge/-Octoleo-black?logo=linux)](https://git.vdm.dev/octoleo "--quiet") [![Llewellyn](https://img.shields.io/badge/-Llewellyn-ffffff?logo=gitea)](https://git.vdm.dev/Llewellyn "Collaborate and Innovate with Llewellyn on Git: Building a Better Code Future!") [![Telegram](https://img.shields.io/badge/-Telegram-blue?logo=telegram)](https://t.me/Joomla_component_builder "Join Llewellyn and the Community on Telegram: Building Joomla Components Together!") [![Mastodon](https://img.shields.io/badge/-Mastodon-9e9eec?logo=mastodon)](https://joomla.social/@llewellyn "Connect and Engage with Llewellyn on Joomla Social: Empowering Communities, One Post at a Time!") [![X (Twitter)](https://img.shields.io/badge/-X-black?logo=x)](https://x.com/llewellynvdm "Join the Conversation with Llewellyn on X: Where Ideas Take Flight!") [![GitHub](https://img.shields.io/badge/-GitHub-181717?logo=github)](https://github.com/Llewellynvdm "Build, Innovate, and Thrive with Llewellyn on GitHub: Turning Ideas into Impact!") [![YouTube](https://img.shields.io/badge/-YouTube-ff0000?logo=youtube)](https://www.youtube.com/@OctoYou "Explore, Learn, and Create with Llewellyn on YouTube: Your Gateway to Inspiration!") [![n8n](https://img.shields.io/badge/-n8n-black?logo=n8n)](https://n8n.io/creators/octoleo "Effortless Automation and Impactful Workflows with Llewellyn on n8n!") [![Docker Hub](https://img.shields.io/badge/-Docker-grey?logo=docker)](https://hub.docker.com/u/llewellyn "Llewellyn on Docker: Containerize Your Creativity!") [![Open Collective](https://img.shields.io/badge/-Donate-green?logo=opencollective)](https://opencollective.com/joomla-component-builder "Donate towards JCB: Help Llewellyn financially so he can continue developing this great tool!") [![GPG Key](https://img.shields.io/badge/-GPG-blue?logo=gnupg)](https://git.vdm.dev/Llewellyn/gpg "Unlock Trust and Security with Llewellyn's GPG Key: Your Gateway to Verified Connections!")