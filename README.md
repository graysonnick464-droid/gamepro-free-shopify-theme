# GamePro Free

GamePro Free is a free, open-source Shopify Online Store 2.0 theme for gaming accessories and electronics stores. It is built on Shopify's Dawn foundation and adds an original, product-first homepage with a dark editorial hero and generic demo imagery.

The bundled generic catalog is placeholder content. Replace it with your own Shopify collection and product selections in the theme editor before publishing.

## Features

- JSON templates for home, product, collection, cart, search, pages, contact, 404, collections, blog, and article views
- Theme-editor sections for hero, categories, featured product, product grid, trust messaging, and newsletter
- Product form, cart page, collection sorting, recommendations, search, contact form, and policy links
- Responsive Concept-inspired electronics storefront design
- Optional generic demo catalog that can be disabled in the theme editor
- MIT license and GitHub Actions Theme Check workflow

## Quick Start

### Upload a ZIP

1. Download the repository and unzip it.
2. Create a new ZIP whose root directly contains `assets`, `config`, `layout`, `locales`, `sections`, `snippets`, and `templates`.
3. In Shopify admin, open **Online Store > Themes**, select **Add theme > Upload ZIP file**, and upload the new archive.

Do not upload the GitHub archive with its outer repository folder intact. Shopify must find `layout/theme.liquid` and `config/settings_schema.json` at the archive root.

### Shopify CLI

Install the latest Shopify CLI, clone the theme, then preview it against a development store:

```bash
git clone https://github.com/WOOK98/gamepro-free-shopify-theme.git
cd gamepro-free-shopify-theme
shopify theme dev --store=your-store.myshopify.com
```

To upload a distributable copy:

```bash
shopify theme push --unpublished
```

## Customize

In the Shopify theme editor:

1. Select a hero image and edit the hero copy.
2. Choose a Shopify product in `Featured product`.
3. Choose a Shopify collection in `Product grid`.
4. Disable the generic demo fallback after your catalog is connected.
5. Configure navigation menus, policy pages, and social links.

## Architecture

```text
assets/       CSS, JavaScript, SVG, and demo images
config/       Global theme settings
layout/       Storefront shell
locales/      Theme translations
sections/     Merchant-configurable page modules
snippets/     Reusable Liquid fragments
templates/    JSON page templates
docs/         Review notes and roadmap
```

## Development

Run Shopify Theme Check before opening a pull request:

```bash
shopify theme check
```

The theme intentionally uses server-rendered Liquid for storefront content and JavaScript only for progressive enhancement.

## Demo Assets

The repository intentionally excludes merchant product photos and third-party branding. The bundled hero image is original, unbranded demo artwork and may be replaced from the theme editor.

## Project Status

Version `1.0.0` is installable and intended as a practical starting point. See [docs/ROADMAP.md](docs/ROADMAP.md) for optional future improvements.

## Documentation

- [中文安装与使用教程](docs/USAGE_ZH.md)
- [Release checklist](docs/RELEASE_CHECKLIST.md)
- [Open-source review](docs/OPEN_SOURCE_REVIEW.md)
- [Roadmap](docs/ROADMAP.md)

## Contributing

Contributions are welcome. Read [CONTRIBUTING.md](CONTRIBUTING.md) and [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) first.

## License

Theme code and the bundled original demo artwork are available under the [MIT License](LICENSE).

## Acknowledgements

GamePro Free is built on [Shopify Dawn](https://github.com/Shopify/dawn), also released under the MIT License.
