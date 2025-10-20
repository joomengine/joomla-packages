### JCB! Layout
# Entity Banner

## Key:
```php
echo LayoutHelper::render('entitybanner', [?]);
```

## PHP:
```php
$data = $displayData ?? null;
```

## HTML:
```html
<?php if ($data && !empty($data->name)) : ?>
<div class="container my-4">
	<div class="card border-0 shadow-sm overflow-hidden">

		<?php if (!empty($data->src)) : ?>
			<!-- Banner Section with background image -->
			<div
				class="position-relative text-center text-white"
				style="
					background-image: url('<?php echo $data->src; ?>');
					background-size: cover;
					background-position: center;
					height: 300px;">

				<!-- Overlay for contrast -->
				<div class="position-absolute top-0 start-0 w-100 h-100 bg-dark bg-opacity-50"></div>

				<!-- Centered heading -->
				<div class="position-absolute top-50 start-50 translate-middle w-100 px-3">
					<h1 class="display-4 fw-bold text-uppercase m-0 text-white"
						style="text-shadow: 2px 2px 6px rgba(0,0,0,0.8);">
						<?php echo $data->name; ?>
					</h1>
				</div>
			</div>
		<?php else : ?>
		<!-- Heading without banner -->
		<div
			class="d-flex align-items-center justify-content-center text-center bg-dark"
			style="height: 100px;">

			<h1 class="display-4 fw-bold text-uppercase m-0 text-white"
				style="text-shadow: 2px 2px 6px rgba(0,0,0,0.8);">
				<?php echo $data->name; ?>
			</h1>
		</div>
		<?php endif; ?>

		<!-- Description -->
		<?php if (!empty($data->description)) : ?>
			<div class="card-body">
				<div class="card-text text-center">
					<?php echo $data->description; ?>
				</div>
			</div>
		<?php endif; ?>
	</div>
</div>
<?php endif; ?>
```

> Enhance your Joomla components with a reusable layout that ensures consistent design, easy updates, and full compatibility within the JCB framework.

### Used in [Joomla Component Builder](https://www.joomlacomponentbuilder.com) - [Source](https://git.vdm.dev/joomla/Component-Builder) - [Mirror](https://github.com/vdm-io/Joomla-Component-Builder) - [Download](https://git.vdm.dev/joomla/pkg-component-builder/releases)

---
[![Joomla Volunteer Portal](https://img.shields.io/badge/-Joomla-gold?logo=joomla)](https://volunteers.joomla.org/joomlers/1396-llewellyn-van-der-merwe "Join Llewellyn on the Joomla Volunteer Portal: Shaping the Future Together!") [![Octoleo](https://img.shields.io/badge/-Octoleo-black?logo=linux)](https://git.vdm.dev/octoleo "--quiet") [![Llewellyn](https://img.shields.io/badge/-Llewellyn-ffffff?logo=gitea)](https://git.vdm.dev/Llewellyn "Collaborate and Innovate with Llewellyn on Git: Building a Better Code Future!") [![Telegram](https://img.shields.io/badge/-Telegram-blue?logo=telegram)](https://t.me/Joomla_component_builder "Join Llewellyn and the Community on Telegram: Building Joomla Components Together!") [![Mastodon](https://img.shields.io/badge/-Mastodon-9e9eec?logo=mastodon)](https://joomla.social/@llewellyn "Connect and Engage with Llewellyn on Joomla Social: Empowering Communities, One Post at a Time!") [![X (Twitter)](https://img.shields.io/badge/-X-black?logo=x)](https://x.com/llewellynvdm "Join the Conversation with Llewellyn on X: Where Ideas Take Flight!") [![GitHub](https://img.shields.io/badge/-GitHub-181717?logo=github)](https://github.com/Llewellynvdm "Build, Innovate, and Thrive with Llewellyn on GitHub: Turning Ideas into Impact!") [![YouTube](https://img.shields.io/badge/-YouTube-ff0000?logo=youtube)](https://www.youtube.com/@OctoYou "Explore, Learn, and Create with Llewellyn on YouTube: Your Gateway to Inspiration!") [![n8n](https://img.shields.io/badge/-n8n-black?logo=n8n)](https://n8n.io/creators/octoleo "Effortless Automation and Impactful Workflows with Llewellyn on n8n!") [![Docker Hub](https://img.shields.io/badge/-Docker-grey?logo=docker)](https://hub.docker.com/u/llewellyn "Llewellyn on Docker: Containerize Your Creativity!") [![Open Collective](https://img.shields.io/badge/-Donate-green?logo=opencollective)](https://opencollective.com/joomla-component-builder "Donate towards JCB: Help Llewellyn financially so he can continue developing this great tool!") [![GPG Key](https://img.shields.io/badge/-GPG-blue?logo=gnupg)](https://git.vdm.dev/Llewellyn/gpg "Unlock Trust and Security with Llewellyn's GPG Key: Your Gateway to Verified Connections!")