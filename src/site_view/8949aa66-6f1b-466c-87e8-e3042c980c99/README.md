### JCB! Site View
# Directory (Service Providers) (directory)

Directory or Categories of Companies

## HTML:
```html
<?php if (!empty($items)): ?>
<?php echo LayoutHelper::render('searchbox', ['url' => $search_link, 'value' => $search_value]); ?>
<div class="container-xxl my-4">
	<div class="row row-cols-1 row-cols-sm-2 row-cols-md-3 g-4">
		<?php foreach ($items as $item): ?>
		<?php
			$url = $item->link ?? null;
			$name = $this->escape($item->name ?? 'error');
			$description = $this->escape($item->description ?? '');
			$image = $this->images[$item->guid] ?? null;
		?>
		<div class="col">
			<div class="card h-100 border-0 shadow-sm transition"
				 role="button"<?php if (!empty($url)): ?>
				 onclick="window.location.href='<?php echo $url; ?>'"
				 onmouseover="this.classList.add('shadow-lg')"
				 onmouseout="this.classList.remove('shadow-lg')"<?php endif; ?>>

				<!-- Image -->
				<?php if (!empty($image)) : ?>
					<img src="<?php echo $image; ?>" class="card-img-top" alt="<?php echo $name; ?>" width="400" height="200" loading="lazy">
				<?php else : ?>
					<div class="card-img-top bg-light d-flex align-items-center justify-content-center" style="height:200px;">
						<span class="text-muted small">400 × 200</span>
					</div>
				<?php endif; ?>

				<!-- Body -->
				<div class="card-body text-center">
					<h5 class="card-title mb-0 d-inline-flex align-items-center justify-content-center"><?php if (!empty($url)): ?>
						<a href="<?php echo $url; ?>" class="stretched-link text-decoration-none text-dark"
							<?php if (!empty($description)): ?>data-bs-toggle="tooltip" data-bs-html="true" title="<?php echo $description; ?>"<?php endif; ?>>
							<?php echo $name; ?>
						</a><?php else: ?>
							<?php echo $name; ?><?php endif; ?>
						<?php if (!empty($description)): ?>
							<i class="fas fa-circle-info ms-2 text-secondary"
								data-bs-toggle="tooltip"
								data-bs-html="true"
								title="<?php echo $description; ?>">
							</i>
						<?php endif; ?>
					</h5>
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
<?php else: ?>
	<div class="alert alert-warning mb-0" role="alert"><?php echo Text::_('No Categories'); ?></div>
<?php endif; ?>

<?php if ($access_listing): ?>
	<?php echo $this->loadTemplate('companylistings'); ?>
	<?php if ($create_listing): ?>
		<div class="container text-center">
			<a href="<?php echo $create_listing_url; ?>" class="btn btn-success btn-lg w-100 py-4 fs-3 fw-bold shadow-lg">
				<i class="bi bi-plus-circle me-2"></i> <?php echo Text::_('Create Listing'); ?>
			</a>
		</div>
	<?php endif; ?>
<?php elseif (!empty($this->user->name)): ?>
	<div class="alert alert-secondary mb-4" role="alert">
		<b><?php echo Text::sprintf('Welcome back, %s!', $this->escape($this->user->name)); ?></b><br>
		<?php echo Text::_('Your account is not permitted to add a listing.'); ?>
	</div>
<?php elseif ((bool) $this->params->get('show_login', 0)): ?>
	<?php echo Text::_('You must be signed in to view or manage your company listings.'); ?>
	<?php echo $this->loadTemplate('loginmodule'); ?>
<?php endif; ?>
<br>
```

> Deliver dynamic, custom front-end experiences with this reusable Site View crafted for seamless data flow and design flexibility in JCB.

### Used in [Joomla Component Builder](https://www.joomlacomponentbuilder.com) - [Source](https://git.vdm.dev/joomla/Component-Builder) - [Mirror](https://github.com/vdm-io/Joomla-Component-Builder) - [Download](https://git.vdm.dev/joomla/pkg-component-builder/releases)

---
[![Joomla Volunteer Portal](https://img.shields.io/badge/-Joomla-gold?logo=joomla)](https://volunteers.joomla.org/joomlers/1396-llewellyn-van-der-merwe "Join Llewellyn on the Joomla Volunteer Portal: Shaping the Future Together!") [![Octoleo](https://img.shields.io/badge/-Octoleo-black?logo=linux)](https://git.vdm.dev/octoleo "--quiet") [![Llewellyn](https://img.shields.io/badge/-Llewellyn-ffffff?logo=gitea)](https://git.vdm.dev/Llewellyn "Collaborate and Innovate with Llewellyn on Git: Building a Better Code Future!") [![Telegram](https://img.shields.io/badge/-Telegram-blue?logo=telegram)](https://t.me/Joomla_component_builder "Join Llewellyn and the Community on Telegram: Building Joomla Components Together!") [![Mastodon](https://img.shields.io/badge/-Mastodon-9e9eec?logo=mastodon)](https://joomla.social/@llewellyn "Connect and Engage with Llewellyn on Joomla Social: Empowering Communities, One Post at a Time!") [![X (Twitter)](https://img.shields.io/badge/-X-black?logo=x)](https://x.com/llewellynvdm "Join the Conversation with Llewellyn on X: Where Ideas Take Flight!") [![GitHub](https://img.shields.io/badge/-GitHub-181717?logo=github)](https://github.com/Llewellynvdm "Build, Innovate, and Thrive with Llewellyn on GitHub: Turning Ideas into Impact!") [![YouTube](https://img.shields.io/badge/-YouTube-ff0000?logo=youtube)](https://www.youtube.com/@OctoYou "Explore, Learn, and Create with Llewellyn on YouTube: Your Gateway to Inspiration!") [![n8n](https://img.shields.io/badge/-n8n-black?logo=n8n)](https://n8n.io/creators/octoleo "Effortless Automation and Impactful Workflows with Llewellyn on n8n!") [![Docker Hub](https://img.shields.io/badge/-Docker-grey?logo=docker)](https://hub.docker.com/u/llewellyn "Llewellyn on Docker: Containerize Your Creativity!") [![Open Collective](https://img.shields.io/badge/-Donate-green?logo=opencollective)](https://opencollective.com/joomla-component-builder "Donate towards JCB: Help Llewellyn financially so he can continue developing this great tool!") [![GPG Key](https://img.shields.io/badge/-GPG-blue?logo=gnupg)](https://git.vdm.dev/Llewellyn/gpg "Unlock Trust and Security with Llewellyn's GPG Key: Your Gateway to Verified Connections!")