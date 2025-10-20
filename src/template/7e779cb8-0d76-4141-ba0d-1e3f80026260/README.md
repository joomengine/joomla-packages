### JCB! Template
# Companies

## Key:
```php
$this->loadTemplate('companies', [?]);
```

## HTML:
```html
<div class="container-xxl my-4">
	<div class="row row-cols-1 g-4">
		<?php foreach ($this->items as $item): ?>
		<?php
			$url = $item->link ?? '#';
			$name = $this->escape($item->name ?? '');
			$description = $this->escape($item->description ?? '', true, 100);
			$logo = is_array($this->logos) ? ($this->logos[$item->guid] ?? null) : null;
		?>
		<div class="col">
			<div class="card h-100 border-0 shadow-sm transition p-3"
				 role="button"
				 onclick="window.location.href='<?php echo $url; ?>'"
				 onmouseover="this.classList.add('shadow-lg')"
				 onmouseout="this.classList.remove('shadow-lg')">

				<div class="row g-3 align-items-center">
					<div class="col-md-9">
						<div class="card-body">
							<h5 class="card-title fs-4 fw-bold mb-2">
								<?php if (!empty($item->edit_link)): ?>
									<span class="position-relative z-2"><span class="me-3">
										<a href="<?php echo $item->edit_link; ?>" title="<?php echo Text::_('Edit Listing'); ?>"><span class="icon-pencil-2 article-edit"></span></a>
									</span></span>
								<?php endif; ?>
								<a href="<?php echo $url; ?>" 
								   class="stretched-link text-decoration-none text-dark">
									<?php echo $name; ?>
								</a>
							</h5>

							<?php if (!empty($description)): ?>
							<p class="card-text text-muted mb-3">
								<?php echo $description; ?>
							</p>
							<?php endif; ?>

							<?php echo LayoutHelper::render('companyrelationships', $item); ?>
						</div>
					</div>

					<div class="col-md-3 text-center">
						<?php if (!empty($logo)): ?>
							<img src="<?php echo $this->escape($logo); ?>"
								 alt="<?php echo $name; ?>"
								 class="img-fluid rounded border"
								 style="width:150px; height:150px; object-fit:contain;">
						<?php else: ?>
							<div class="bg-light d-flex align-items-center justify-content-center rounded border"
								 style="width:150px; height:150px;">
								<span class="text-muted small">150 × 150</span>
							</div>
						<?php endif; ?>
					</div>
				</div>
			</div>
		</div>
		<?php endforeach; ?>
	</div>
</div>
<script>
document.addEventListener('DOMContentLoaded', function () {
	const tooltipTriggerList = [].slice.call(document.querySelectorAll('[data-bs-toggle="tooltip"]'));
	tooltipTriggerList.map(function (el) {
		return new bootstrap.Tooltip(el);
	});
});
</script>
```

> Structure your Joomla views with a reusable template that ensures consistent rendering, streamlined development, and easy customization within JCB.

### Used in [Joomla Component Builder](https://www.joomlacomponentbuilder.com) - [Source](https://git.vdm.dev/joomla/Component-Builder) - [Mirror](https://github.com/vdm-io/Joomla-Component-Builder) - [Download](https://git.vdm.dev/joomla/pkg-component-builder/releases)

---
[![Joomla Volunteer Portal](https://img.shields.io/badge/-Joomla-gold?logo=joomla)](https://volunteers.joomla.org/joomlers/1396-llewellyn-van-der-merwe "Join Llewellyn on the Joomla Volunteer Portal: Shaping the Future Together!") [![Octoleo](https://img.shields.io/badge/-Octoleo-black?logo=linux)](https://git.vdm.dev/octoleo "--quiet") [![Llewellyn](https://img.shields.io/badge/-Llewellyn-ffffff?logo=gitea)](https://git.vdm.dev/Llewellyn "Collaborate and Innovate with Llewellyn on Git: Building a Better Code Future!") [![Telegram](https://img.shields.io/badge/-Telegram-blue?logo=telegram)](https://t.me/Joomla_component_builder "Join Llewellyn and the Community on Telegram: Building Joomla Components Together!") [![Mastodon](https://img.shields.io/badge/-Mastodon-9e9eec?logo=mastodon)](https://joomla.social/@llewellyn "Connect and Engage with Llewellyn on Joomla Social: Empowering Communities, One Post at a Time!") [![X (Twitter)](https://img.shields.io/badge/-X-black?logo=x)](https://x.com/llewellynvdm "Join the Conversation with Llewellyn on X: Where Ideas Take Flight!") [![GitHub](https://img.shields.io/badge/-GitHub-181717?logo=github)](https://github.com/Llewellynvdm "Build, Innovate, and Thrive with Llewellyn on GitHub: Turning Ideas into Impact!") [![YouTube](https://img.shields.io/badge/-YouTube-ff0000?logo=youtube)](https://www.youtube.com/@OctoYou "Explore, Learn, and Create with Llewellyn on YouTube: Your Gateway to Inspiration!") [![n8n](https://img.shields.io/badge/-n8n-black?logo=n8n)](https://n8n.io/creators/octoleo "Effortless Automation and Impactful Workflows with Llewellyn on n8n!") [![Docker Hub](https://img.shields.io/badge/-Docker-grey?logo=docker)](https://hub.docker.com/u/llewellyn "Llewellyn on Docker: Containerize Your Creativity!") [![Open Collective](https://img.shields.io/badge/-Donate-green?logo=opencollective)](https://opencollective.com/joomla-component-builder "Donate towards JCB: Help Llewellyn financially so he can continue developing this great tool!") [![GPG Key](https://img.shields.io/badge/-GPG-blue?logo=gnupg)](https://git.vdm.dev/Llewellyn/gpg "Unlock Trust and Security with Llewellyn's GPG Key: Your Gateway to Verified Connections!")