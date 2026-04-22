# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [v2.0.0] - 2026-04-22
### :bug: Bug Fixes
- [`4fca6f8`](https://github.com/terraform-az-modules/terraform-azurerm-vpn/commit/4fca6f85491b7e29f13c88e5fc98733009afd613) - consolidate versions.tf, remove provider_meta, upgrade to azurerm >= 4.0 *(commit by [@anmolnagpal](https://github.com/anmolnagpal))*
- [`eba873c`](https://github.com/terraform-az-modules/terraform-azurerm-vpn/commit/eba873c9a9d2399cd2316e2f18b501cceccb402c) - replace version placeholder in example versions.tf with >= 4.0 *(commit by [@anmolnagpal](https://github.com/anmolnagpal))*

### :wrench: Chores
- [`7f46fbd`](https://github.com/terraform-az-modules/terraform-azurerm-vpn/commit/7f46fbdfb19adc0d25b1de11c43c6c24ba688113) - **deps**: bump actions/checkout from 4 to 6 *(commit by [@dependabot[bot]](https://github.com/apps/dependabot))*
- [`bc7dcfb`](https://github.com/terraform-az-modules/terraform-azurerm-vpn/commit/bc7dcfbed0ce9907402adc583cabd09a7a772765) - **deps**: bump hashicorp/setup-terraform from 3 to 4 *(commit by [@dependabot[bot]](https://github.com/apps/dependabot))*
- [`ae6e99a`](https://github.com/terraform-az-modules/terraform-azurerm-vpn/commit/ae6e99a9d907ccd9e0da9793694f151c1016afbf) - **deps**: bump terraform-linters/setup-tflint from 4 to 6 *(commit by [@dependabot[bot]](https://github.com/apps/dependabot))*
- [`bade9a5`](https://github.com/terraform-az-modules/terraform-azurerm-vpn/commit/bade9a57e8586d1fbc8a2d978c166692108bff13) - add provider_meta for API usage tracking *(PR [#21](https://github.com/terraform-az-modules/terraform-azurerm-vpn/pull/21) by [@clouddrove-ci](https://github.com/clouddrove-ci))*
- [`5cda6ee`](https://github.com/terraform-az-modules/terraform-azurerm-vpn/commit/5cda6eeaf53e287a8126c2ea97246efcd639b0f6) - polish module with basic example, changelog, and version fixes *(PR [#22](https://github.com/terraform-az-modules/terraform-azurerm-vpn/pull/22) by [@clouddrove-ci](https://github.com/clouddrove-ci))*
- [`e7c6cfb`](https://github.com/terraform-az-modules/terraform-azurerm-vpn/commit/e7c6cfb4a38941be007ebccf1e1c1b854c030f24) - **deps**: bump actions/checkout from 3 to 6 *(commit by [@dependabot[bot]](https://github.com/apps/dependabot))*


## [1.0.4] - 2026-03-20

### Changes
- Add provider_meta for API usage tracking
- Add terraform tests and pre-commit CI workflow
- Add SECURITY.md, CONTRIBUTING.md, .releaserc.json
- Standardize pre-commit to antonbabenko v1.105.0
- Set provider: none in tf-checks for validate-only CI
- Bump required_version to >= 1.10.0
[v2.0.0]: https://github.com/terraform-az-modules/terraform-azurerm-vpn/compare/v1.0.4...v2.0.0
