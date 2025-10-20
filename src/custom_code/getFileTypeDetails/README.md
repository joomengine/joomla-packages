### JCB! Custom Code
# getFileTypeDetails

## JCB (manual)
```
[CUSTOMCODE=getFileTypeDetails]
```

### Code
```php
	/**
	 * Get the file type details, if it exists.
	 *
	 * @param string $guid    The file type guid
	 * @param string $target  The target entity name
	 *
	 * @return array
	 * @since 5.0.2
	 */
	public function getFileTypeDetails(string $guid, string $target): array
	{
		if (Super___9c513baf_b279_43fd_ae29_a585c8cbc4f0___Power::valid($guid))
		{
			try
			{
				$target = base64_decode($target);
				$type = Super___884eca78_281f_4eab_b962_d97e355af16d___Power::_('File.Type')->get($guid, $target);
			}
			catch (\Exception $error)
			{
				return ['error' => $error->getMessage()];
			}

			if ($type !== null)
			{
				return ['data' => $type];
			}
		}

		return ['error' => Text::_('File type details could not be found')];
	}

	/**
	 * Upload a file, of a given file type and link it to an entity.
	 *
	 * @param string $guid    The file type guid
	 * @param string $entity  The entity guid
	 * @param string $target  The target entity name
	 *
	 * @return array
	 * @since 5.0.2
	 */
	public function uploadFile(string $guid, string $entity, string $target): array
	{
		if (Super___9c513baf_b279_43fd_ae29_a585c8cbc4f0___Power::valid($guid)
			&& Super___9c513baf_b279_43fd_ae29_a585c8cbc4f0___Power::valid($entity))
		{
			try
			{
				$target = base64_decode($target);
				Super___884eca78_281f_4eab_b962_d97e355af16d___Power::_('File.Manager')->upload($guid, $entity, $target);
			}
			catch (\Exception $error)
			{
				return ['error' => $error->getMessage()];
			}

			return ['success' => Text::_('The file was successfully uploaded')];
		}

		return ['error' => Text::_('The file failed to upload')];
	}

	/**
	 * Delete a file of a given entity.
	 *
	 * @param string $guid    The file guid
	 *
	 * @return array
	 * @since 5.0.2
	 */
	public function deleteFile(string $guid): array
	{
		if (Super___9c513baf_b279_43fd_ae29_a585c8cbc4f0___Power::valid($guid))
		{
			try
			{
				Super___884eca78_281f_4eab_b962_d97e355af16d___Power::_('File.Manager')->delete($guid);
			}
			catch (\Exception $error)
			{
				return ['error' => $error->getMessage()];
			}

			return ['success' => Text::_('The file was successfully deleted')];
		}

		return ['error' => Text::_('The file could not be deleted')];
	}

	/**
	 * Load the display of the files linked this entity.
	 *
	 * @param string $entity  The entity guid
	 * @param string $target  The target entity name
	 *
	 * @return array
	 * @since 5.0.2
	 */
	public function displayFiles(string $entity, string $target): array
	{
		if (Super___9c513baf_b279_43fd_ae29_a585c8cbc4f0___Power::valid($entity))
		{
			$display = null;

			try
			{
				$target = base64_decode($target);
				$data = Super___884eca78_281f_4eab_b962_d97e355af16d___Power::_('File.Display')->get($entity, $target);

				if ($data !== null)
				{
					$displayData =  ['data' => $data, 'entity' => $entity, 'target' => $target];
					$display = Joomla___7ab82272_0b3d_4bb1_af35_e63a096cfe0b___Power::render('filedisplay', $displayData);
				}
				else
				{
					return ['data' => '<b>' . Text::sprintf('No files linked to %s.', $target) . '</b>'];
				}
			}
			catch (\Exception $error)
			{
				return ['error' => $error->getMessage()];
			}

			if (!empty($display))
			{
				return ['data' => $display];
			}
		}

		return ['error' => Text::_('The file display could not be loaded')];
	}
```

> Add clean, self-contained code into your components with this reusable custom-code snippet designed for seamless integration and easy updates in JCB.

### Used in [Joomla Component Builder](https://www.joomlacomponentbuilder.com) - [Source](https://git.vdm.dev/joomla/Component-Builder) - [Mirror](https://github.com/vdm-io/Joomla-Component-Builder) - [Download](https://git.vdm.dev/joomla/pkg-component-builder/releases)

---
[![Joomla Volunteer Portal](https://img.shields.io/badge/-Joomla-gold?logo=joomla)](https://volunteers.joomla.org/joomlers/1396-llewellyn-van-der-merwe "Join Llewellyn on the Joomla Volunteer Portal: Shaping the Future Together!") [![Octoleo](https://img.shields.io/badge/-Octoleo-black?logo=linux)](https://git.vdm.dev/octoleo "--quiet") [![Llewellyn](https://img.shields.io/badge/-Llewellyn-ffffff?logo=gitea)](https://git.vdm.dev/Llewellyn "Collaborate and Innovate with Llewellyn on Git: Building a Better Code Future!") [![Telegram](https://img.shields.io/badge/-Telegram-blue?logo=telegram)](https://t.me/Joomla_component_builder "Join Llewellyn and the Community on Telegram: Building Joomla Components Together!") [![Mastodon](https://img.shields.io/badge/-Mastodon-9e9eec?logo=mastodon)](https://joomla.social/@llewellyn "Connect and Engage with Llewellyn on Joomla Social: Empowering Communities, One Post at a Time!") [![X (Twitter)](https://img.shields.io/badge/-X-black?logo=x)](https://x.com/llewellynvdm "Join the Conversation with Llewellyn on X: Where Ideas Take Flight!") [![GitHub](https://img.shields.io/badge/-GitHub-181717?logo=github)](https://github.com/Llewellynvdm "Build, Innovate, and Thrive with Llewellyn on GitHub: Turning Ideas into Impact!") [![YouTube](https://img.shields.io/badge/-YouTube-ff0000?logo=youtube)](https://www.youtube.com/@OctoYou "Explore, Learn, and Create with Llewellyn on YouTube: Your Gateway to Inspiration!") [![n8n](https://img.shields.io/badge/-n8n-black?logo=n8n)](https://n8n.io/creators/octoleo "Effortless Automation and Impactful Workflows with Llewellyn on n8n!") [![Docker Hub](https://img.shields.io/badge/-Docker-grey?logo=docker)](https://hub.docker.com/u/llewellyn "Llewellyn on Docker: Containerize Your Creativity!") [![Open Collective](https://img.shields.io/badge/-Donate-green?logo=opencollective)](https://opencollective.com/joomla-component-builder "Donate towards JCB: Help Llewellyn financially so he can continue developing this great tool!") [![GPG Key](https://img.shields.io/badge/-GPG-blue?logo=gnupg)](https://git.vdm.dev/Llewellyn/gpg "Unlock Trust and Security with Llewellyn's GPG Key: Your Gateway to Verified Connections!")