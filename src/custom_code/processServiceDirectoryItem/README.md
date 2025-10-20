### JCB! Custom Code
# Process Service Directory Item

## JCB (manual)
```
[CUSTOMCODE=processServiceDirectoryItem]
```

### Code
```php
	/**
	 * The entity value.
	 *
	 * @var  string
	 * @since 5.1.3
	 */
	protected string $entity;

	/**
	 * The entity type value.
	 *
	 * @var  string
	 * @since 5.1.3
	 */
	protected string $entity_type;

	/**
	 * The companies.
	 *
	 * @var  array
	 * @since 5.1.3
	 */
	protected array $companies = [];

	/**
	 * The mapper defining dataset relations.
	 *
	 * @var  array
	 * @since 5.1.3
	 */
	protected array $mapper = [];

	/**
	 * The base URL of the site.
	 *
	 * @var  string
	 * @since 5.1.3
	 */
	protected string $baseUrl = 'error';

	/**
	 * The return URL of the page.
	 *
	 * @var  string|null
	 * @since 5.1.3
	 */
	protected ?string $returnUrl = null;

	/**
	 * Default query parameters for image downloads.
	 *
	 * @var  array
	 * @since 5.1.3
	 */
	protected array $urlQueryParams = [
		'option'     => 'com_[[[component]]]',
		'controller' => 'download',
		'task'       => 'download.image',
	];

	/**
	 * Escapable fields on the main item.
	 *
	 * @var  array
	 * @since 5.1.3
	 */
	protected array $mainEscapeFields = [];

	/**
	 * Process and update an item.
	 *
	 * @param  object       $item    The item to process.
	 *
	 * @return object  The processed and updated item.
	 * @since  5.1.3
	 */
	protected function processItem(object $item): object
	{
		$item = $this->buildItemLink($item);
		$item = $this->buildCategoryLinks($item);
		$item = $this->convertDescriptions($item);
		$item = $this->escapeFields($item, $this->mainEscapeFields);
		$item = $this->processLinkedDataSets($item, $this->mapper);

		return $item;
	}

	/**
	 * Build the item link if slug available.
	 *
	 * @param  object       $item    The item to modify.
	 *
	 * @return object
	 * @since  5.1.3
	 */
	protected function buildItemLink(object $item): object
	{
		$return = '';
		if (!empty($this->returnUrl))
		{
			$return = "&return={$this->returnUrl}";
		}

		if (!empty($item->slug))
		{
			$item->link = Joomla___d4c76099_4c32_408a_8701_d0a724484dfd___Power::_(
				Joomla___92167f18_8543_40e8_92af_053ef4c210d1___Power::getListingRoute($item->slug) . $return
			);
		}

		if ($this->allowCompanyEdit($item))
		{
			$item->edit_link = Joomla___d4c76099_4c32_408a_8701_d0a724484dfd___Power::_(
				"/index.php?option=com_[[[component]]]&view=company&task=company.edit&id={$item->id}{$return}"
			);
		}

		return $item;
	}

	/**
	 * Build the category route and link if available.
	 *
	 * @param  object  $item  The item to modify.
	 *
	 * @return object
	 * @since  5.1.3
	 */
	protected function buildCategoryLinks(object $item): object
	{
		if (!empty($item->category_id) && !empty($item->category_alias))
		{
			$item->category_slug = $item->category_id . ':' . $item->category_alias;
			$item->category_link = Joomla___d4c76099_4c32_408a_8701_d0a724484dfd___Power::_(
				Joomla___92167f18_8543_40e8_92af_053ef4c210d1___Power::getCategoryRoute($item->category_slug)
			);
		}

		return $item;
	}

	/**
	 * Convert markdown fields to HTML.
	 *
	 * @param  object  $item  The item to modify.
	 *
	 * @return object
	 * @since  5.1.3
	 */
	protected function convertDescriptions(object $item): object
	{
		if (!empty($item->description))
		{
			$item->description = $this->convertMarkdownToHtml($item->description);
		}

		if (!empty($item->category_description))
		{
			$item->category_description = $this->convertMarkdownToHtml($item->category_description);
		}

		return $item;
	}

	/**
	 * Escape given fields safely.
	 *
	 * @param  object  $item     The item to escape fields on.
	 * @param  array   $fields   Field names to escape.
	 *
	 * @return object
	 * @since  5.1.3
	 */
	protected function escapeFields(object $item, array $fields): object
	{
		foreach ($fields as $field)
		{
			if (!empty($item->{$field}))
			{
				$item->{$field} = $this->escape((string) $item->{$field});
			}
		}

		return $item;
	}

	/**
	 * Process all linked datasets defined in the mapper.
	 *
	 * @param  object  $item     The item to update.
	 *
	 * @return object
	 * @since  5.1.3
	 */
	protected function processLinkedDataSets(object $item): object
	{
		foreach ($this->mapper as $pointer => $config)
		{
			$dataSet = $item->{$pointer} ?? null;

			if (!empty($dataSet))
			{
				$dataSet = $this->processDataSet($dataSet, $config, $item);
			}

			$setField = $config['set'] ?? null;
			if ($setField !== null)
			{
				$item->{$setField} = !empty($dataSet) ? $dataSet : null;
				unset($item->{$pointer});
			}
		}

		return $item;
	}

	/**
	 * Process a single dataset mapping.
	 *
	 * @param  array   $dataSet  The dataset to process.
	 * @param  array   $config   The mapper configuration for this dataset.
	 * @param  object  $item     The parent item for cross-field updates.
	 *
	 * @return array|null  The processed dataset or null.
	 * @since  5.1.3
	 */
	protected function processDataSet(array $dataSet, array $config, object &$item): ?array
	{
		foreach ($dataSet as $n => &$value)
		{
			$routeMethod = $config['route'] ?? null;
			$escapeSet = $config['escape'] ?? [];
			$set = $config['set'] ?? '';

			if ($routeMethod)
			{
				$value = $this->setLinkedEntityRoute($value, $routeMethod);
			}

			if (!empty($value->description))
			{
				$value->description = $this->convertMarkdownToHtml($value->description);
			}

			$value = $this->escapeFields($value, $escapeSet);

			if ($set === 'files')
			{
				$this->processFileRecord($value, $item, $dataSet, $n);
			}

			if ($set === 'social_handles')
			{
				if (!$this->processSocialHandle($value))
				{
					unset($dataSet[$n]);
				}
			}
		}
		unset($value);

		return !empty($dataSet) ? $dataSet : null;
	}

	/**
	 * Build route for linked entity.
	 *
	 * @param  object  $value        Entity object to update.
	 * @param  string  $routeMethod  Route method name.
	 *
	 * @return object
	 * @since  5.1.3
	 */
	protected function setLinkedEntityRoute(object $value, string $routeMethod): object
	{
		$value->slug = ($value->id ?? '0') . (isset($value->alias) ? ':' . $value->alias : '');
		$value->link = Joomla___d4c76099_4c32_408a_8701_d0a724484dfd___Power::_(
			Joomla___92167f18_8543_40e8_92af_053ef4c210d1___Power::{$routeMethod}($value->slug)
		);

		return $value;
	}

	/**
	 * Process a single file entity, building download URLs.
	 *
	 * @param  object  $value     The file entity.
	 * @param  object  $item      The parent item.
	 * @param  array   &$dataSet  The dataset reference.
	 * @param  int     $n         Current index in dataset.
	 *
	 * @since  5.1.3
	 */
	protected function processFileRecord(object &$value, object &$item, array &$dataSet, int $n): void
	{
		if (empty($value->name))
		{
			return;
		}

		$query = $this->urlQueryParams;

		$query['file'] = $value->guid;
		$query['name'] = $value->name;

		$value->src = $this->baseUrl . Joomla___d4c76099_4c32_408a_8701_d0a724484dfd___Power::_(
			'index.php?' . http_build_query($query)
		);

		if (str_starts_with($value->name, 'logo__'))
		{
			$item->logo = $value->src;
			unset($dataSet[$n]);
		}

		if (str_starts_with($value->name, 'banner__'))
		{
			$item->banner = $value->src;
			unset($dataSet[$n]);
		}
	}

	/**
	 * Process and normalize social media handles or full profile URLs.
	 *
	 * - If the handle is a full URL (starting with http/https), normalize it, strip
	 *   the domain (leaving only the path), and use that as the clean handle.
	 * - If the handle is not a full URL, assume it's a raw handle and build a full
	 *   URL by combining the website and handle.
	 * - Always ensures consistent, lowercase, HTTPS-based URLs.
	 *
	 * @param  object  $value  The handle object to validate and clean.
	 *
	 * @return bool  True if valid and processed, false otherwise.
	 * @since  5.1.2
	 */
	protected function processSocialHandle(object &$value): bool
	{
		$handle  = trim((string) ($value->handle ?? ''));
		$website = trim((string) ($value->website ?? ''));

		// Both fields required
		if ($handle === '' || $website === '')
		{
			return false;
		}

		// If handle is already a full URL
		if (preg_match('#^https?://#i', $handle))
		{
			// Normalize to HTTPS and lowercase for consistency
			$link = preg_replace('#^http://#i', 'https://', strtolower($handle));
			$link = rtrim($link, '/');

			// Parse URL safely and extract the path portion as the clean handle
			$parsed = parse_url($link);
			$cleanHandle = '';

			if (!empty($parsed['path']))
			{
				$cleanHandle = ltrim($parsed['path'], '/');
			}

			if (!empty($parsed['query']))
			{
				// Include query string if present (e.g. ?id=123)
				$cleanHandle .= '?' . $parsed['query'];
			}

			$value->handle = $cleanHandle;
			$value->link   = $link;

			return true;
		}

		// Handle is plain text → build full link
		$cleanWebsite = rtrim(preg_replace('#^https?://#i', '', strtolower($website)), '/');
		$cleanHandle  = ltrim($handle, '/');

		$link = 'https://' . $cleanWebsite . '/' . $cleanHandle;
		$link = rtrim($link, '/');

		$value->handle = $cleanHandle;
		$value->link   = $link;

		return true;
	}
[CUSTOMCODE=allowCompanyEdit]
[CUSTOMCODE=convertMarkdownToHtml]
[CUSTOMCODE=getTimeBasedRandomSeed]
```

> Add clean, self-contained code into your components with this reusable custom-code snippet designed for seamless integration and easy updates in JCB.

### Used in [Joomla Component Builder](https://www.joomlacomponentbuilder.com) - [Source](https://git.vdm.dev/joomla/Component-Builder) - [Mirror](https://github.com/vdm-io/Joomla-Component-Builder) - [Download](https://git.vdm.dev/joomla/pkg-component-builder/releases)

---
[![Joomla Volunteer Portal](https://img.shields.io/badge/-Joomla-gold?logo=joomla)](https://volunteers.joomla.org/joomlers/1396-llewellyn-van-der-merwe "Join Llewellyn on the Joomla Volunteer Portal: Shaping the Future Together!") [![Octoleo](https://img.shields.io/badge/-Octoleo-black?logo=linux)](https://git.vdm.dev/octoleo "--quiet") [![Llewellyn](https://img.shields.io/badge/-Llewellyn-ffffff?logo=gitea)](https://git.vdm.dev/Llewellyn "Collaborate and Innovate with Llewellyn on Git: Building a Better Code Future!") [![Telegram](https://img.shields.io/badge/-Telegram-blue?logo=telegram)](https://t.me/Joomla_component_builder "Join Llewellyn and the Community on Telegram: Building Joomla Components Together!") [![Mastodon](https://img.shields.io/badge/-Mastodon-9e9eec?logo=mastodon)](https://joomla.social/@llewellyn "Connect and Engage with Llewellyn on Joomla Social: Empowering Communities, One Post at a Time!") [![X (Twitter)](https://img.shields.io/badge/-X-black?logo=x)](https://x.com/llewellynvdm "Join the Conversation with Llewellyn on X: Where Ideas Take Flight!") [![GitHub](https://img.shields.io/badge/-GitHub-181717?logo=github)](https://github.com/Llewellynvdm "Build, Innovate, and Thrive with Llewellyn on GitHub: Turning Ideas into Impact!") [![YouTube](https://img.shields.io/badge/-YouTube-ff0000?logo=youtube)](https://www.youtube.com/@OctoYou "Explore, Learn, and Create with Llewellyn on YouTube: Your Gateway to Inspiration!") [![n8n](https://img.shields.io/badge/-n8n-black?logo=n8n)](https://n8n.io/creators/octoleo "Effortless Automation and Impactful Workflows with Llewellyn on n8n!") [![Docker Hub](https://img.shields.io/badge/-Docker-grey?logo=docker)](https://hub.docker.com/u/llewellyn "Llewellyn on Docker: Containerize Your Creativity!") [![Open Collective](https://img.shields.io/badge/-Donate-green?logo=opencollective)](https://opencollective.com/joomla-component-builder "Donate towards JCB: Help Llewellyn financially so he can continue developing this great tool!") [![GPG Key](https://img.shields.io/badge/-GPG-blue?logo=gnupg)](https://git.vdm.dev/Llewellyn/gpg "Unlock Trust and Security with Llewellyn's GPG Key: Your Gateway to Verified Connections!")