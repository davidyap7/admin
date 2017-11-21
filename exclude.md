---

copyright:

  years: 2017
lastupdated: "2017-11-21"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Hiding a public resource from users in your account
{: #exclude}

If you're an administrator for the account, you can choose to hide a public resource for everyone in your account by adding them to an excludes list with the `bx` [command line interface](/docs/cli/reference/bluemix_cli/bx_cli.html#bluemix_catalog_entry_visibility_set).
{:shortdesc: .shortdesc}

**Note:** Hiding an item in the catalog will not remove the item from the Cloud Foundry CLI or from the service provisioning lists available through the global navigation, such as Finance, Mobile, Watson, and Web Apps.

## How do I know if I have access?
{: #find-access}

You can use the CLI or the Identity and Access UI to determine whether you have access to allow users to view a private resource that has been added to the account. If you're an account owner, you can give access to a user in your account through the Identity and Access Management UI by assigning an access policy. For more information see [Managing access to your account](access.html).

## Step 1: Find a resource
{: #find-resource}

Enter `bx catalog search <service-id or service-name>` to search for a resource. Replace service-id or service-name with a resource name or ID. Find the ID or name of the service you want to hide in the information that returns.

## Step 2: Get the details of that service

Enter `bx catalog service <service-id or service-name>`. Using what you found in the previous command, use this command to examine more details of the resource. With the information that returns, you can see the hierarchy, which shows the child resources of the items in your resource.

## Step 3: Hide the resource
{: #vis-exc}

Enter the following command to prevent another in your account from seeing a public resource.

`bx catalog entry-visibility-set <resource-id> —-excludes-add <account-id or account-email>`

After the excludes flag, you can add a comma separated list of emails or account ID associated with accounts.

## Remove an account from the excludes list
{: #remove-exclude}

Enter the following command to remove an account ID or email from the excludes list.

`bx catalog entry-visibility-set <service-id> —-excludes-remove <account-id or account-email>`

## Managing visibility of child objects example
{: #child}

You can manage the visibility of all your resources. Each child resource has its individual visibility characteristics.

In this example, you can exclude an account from the public Cloudant service.

If you enter `bx catalog service cloudant`, you can see the resource's children.

```
ID                 cloudant
Name               cloudantnosqldb
Kind               service
Provider           IBM
Tags               data_management, ibm_created, ibm_dedicated_public, lite
Active             true
Description        Cloudant NoSQL DB is a fully managed data layer designed for modern web and mobile applications that leverages a flexible JSON schema. Cloudant is built upon and compatible with Apache CouchDB and accessible through a secure HTTPS API, which scales as your application grows. Cloudant is ISO27001 and SOC2 Type 1 certified, and all data is stored in triplicate across separate physical nodes in a cluster for HA/DR within a data center.
Bindable           true
RC Compatible      false
RC Provisionable   false
Children           Name                                          Kind         ID                                               Location
                   lite                                          plan         cloudant-lite
                   |__lite-eu-gb                             deployment   cloudant-lite:eu-gb                          eu-gb
                   |  |__lite-alias-eu-gb                    alias        cloudant-lite:alias:eu-gb                    eu-gb
                   |__lite-us-south                          deployment   cloudant-lite:us-south                       us-south
                      |__lite-alias-us-south                 alias        cloudant-lite:alias:us-south                 us-south
                   standard                                      plan         cloudant-standard
                   |__standard-eu-gb                         deployment   cloudant-standard:eu-gb                      eu-gb
                   |  |__standard-alias-eu-gb                alias        cloudant-standard:alias:eu-gb                eu-gb
                   |__standard-us-south                      deployment   cloudant-standard:us-south                   us-south
                      |__standard-alias-us-south             alias        cloudant-standard:alias:us-south             us-south
```

Find the ID for an object and exclude an account with the `bx catalog entry-visibility-set <resource-id> --excludes-add <account-id or account-email>`.

For more information about how visibility works, see the the [API docs](https://console.bluemix.net/apidocs/682).
