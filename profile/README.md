# MACH composer

[![MACH
composer](https://github.com/labd/mach-composer/blob/main/docs/src/_img/logo.png?raw=true)](https://docs.machcomposer.io)

MACH composer is a framework that you use to orchestrate and extend modern
digital commerce & experience platforms, based on MACH technologies and cloud
native services. It provides a standards-based, future-proof tool-set and
methodology to hand to your teams when building these types of platforms.

It is specifically aimed at building large scale and multi-tenant MACH systems
that span geographies, organisations and brands. All from the same MACH
ecosystem.


## MACH composer installation

Currently, the [MACH composer source](https://github.com/labd/mach-composer) is
still hosted in the Lab Digital organisation. Usually you don't need that for
using MACH composer itself, as we have binaries available for several platforms.

### MacOS

```bash
brew tap labd/mach-composer
brew install mach-composer
```

### Windows

```ps
choco install mach-composer --version=2.5.0
```

## Github actions

For integrating MACH composer into Github Action CI/CD workflows, we provide
three actions:

- [setup-mach-composer](https://github.com/mach-composer/setup-mach-composer):
  an action that installs a specified version of MACH composer
- [plan-action](https://github.com/mach-composer/plan-action): an action that
  executes `mach-composer plan` and posts the output of that as a PR comment


## CLI plugins

MACH composer CLI has a plugin system, through wich integrations with several SAAS and Cloud services are provided.

- [mach-composer-plugin-amplience](https://github.com/mach-composer/mach-composer-plugin-amplience)
- [mach-composer-plugin-apollostudio](https://github.com/mach-composer/mach-composer-plugin-apollostudio)
- [mach-composer-plugin-aws](https://github.com/mach-composer/mach-composer-plugin-aws)
- [mach-composer-plugin-azure](https://github.com/mach-composer/mach-composer-plugin-azure) \[DEPRECATED]
- [mach-composer-plugin-azure-minimal](https://github.com/mach-composer/mach-composer-plugin-azure-minimal)
- [mach-composer-plugin-commercelayer](https://github.com/mach-composer/mach-composer-plugin-commercelayer)
- [mach-composer-plugin-commercetools](https://github.com/mach-composer/mach-composer-plugin-commercetools)
- [mach-composer-plugin-contentful](https://github.com/mach-composer/mach-composer-plugin-contentful)
- [mach-composer-plugin-gcp](https://github.com/mach-composer/mach-composer-plugin-gcp)
- [mach-composer-plugin-honeycomb](https://github.com/mach-composer/mach-composer-plugin-honeycomb)
- [mach-composer-plugin-vercel](https://github.com/mach-composer/mach-composer-plugin-vercel)
- [mach-composer-plugin-sentry](https://github.com/mach-composer/mach-composer-plugin-sentry)

You can install these plugins by adding them in your MACH composer YAML configuration:

```yaml
  mach_composer:
    version: 1
    variables_file: prd-secrets.yml
    plugins:
      amplience:
        source: mach-composer/amplience
        version: 0.1.3
      apollostudio:
        source: mach-composer/apollostudio
        version: 0.0.2
      aws:
        source: mach-composer/aws
        version: 0.1.0
      azure:
        source: mach-composer/azure
        version: 0.1.0
      azure-minimal:
        source: mach-composer/azure-minimal
        version: 0.1.0
      commercelayer:
        source: mach-composer/commercelayer
        version: 0.0.3
      commercetools:
        source: mach-composer/commercetools
        version: 0.1.8
      contentful:
        source: mach-composer/contentful
        version: 0.1.0
      gcp:
        source: mach-composer/gcp
        version: 0.1.1
      honeycomb:
        source: mach-composer/honeycomb
        version: 0.1.0
      sentry:
        source: mach-composer/sentry
        version: 0.1.3
      vercel:
        source: mach-composer/vercel
        version: 0.2.0
```

MACH composer wil automatically install these for you.

