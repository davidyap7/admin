---

copyright:

  years: 2017
lastupdated: "2017-11-21"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Changing account ownership

You can change account ownership with the command line interface. After you've created and customized private resources in your catalog, you can transfer ownership of those resources to someone else. After you transfer ownership, you won't be able to see the resource from your account. Changing account ownership cannot be undone, so exercise caution.
{:shortdesc: .shortdesc}

## How to change the owner of a catalog resource

To change the owner of a resource, with the [CLI](docs/cli/reference/bluemix_cli/bx_cli.html#bx_commands_settings) use the following command:

`bx catalog entry-visibility-set <service-id> --owner <account-id or account-email>`
