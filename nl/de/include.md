---

copyright:

  years: 2017
lastupdated: "2017-12-06"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Konten zur privaten Ressource hinzufügen
{: #include}

Der Zugriff auf private Ressourcen, die Sie erstellen, ist standardmäßig eingeschränkt. Wenn Sie ein Administrator des Kontos sind, können Sie die Benutzer auswählen, denen Ihre Ressource angezeigt wird, indem Sie diese Benutzer über die `bx`-[Befehlszeilenschnittstelle](/docs/cli/reference/bluemix_cli/bx_cli.html#bluemix_catalog_entry_visibility_set) in einer Einschlussliste hinzufügen.
{:shortdesc: .shortdesc}

## Wie kann ich feststellen, ob ich über Zugriff verfüge? 
{: #find-access}

Sie können über die Befehlszeilenschnittstelle oder die IAM-Benutzerschnittstelle ermitteln, ob Sie über den erforderlichen Zugriff verfügen, um dafür zu sorgen, dass Benutzern eine private Ressource angezeigt wird, die dem Konto hinzugefügt wurde. Als Kontoeigner können Sie einem Benutzer in Ihrem Konto über die IAM-Benutzerschnittstelle Zugriff erteilen, indem Sie eine Zugriffsrichtlinie zuordnen. Weitere Informationen finden Sie unter [Zugriff auf Konto verwalten](access.html). 

## Schritt 1: Eigene Ressource suchen
{: #find-resource}

Geben Sie den Befehl `bx catalog service <service-id or service-name>`. Ersetzen Sie 'service-id or service-name' durch den Namen oder die ID Ihrer Ressource. In den zurückgegebenen Informationen wird die Hierarchie angezeigt, die Aufschluss über die untergeordneten Ressourcen der Elemente in Ihrer Ressource gibt. 

## Schritt 2: Sichtbarkeit durch Einschließen eines Kontos festlegen
{: #vis-inc}

Geben Sie den folgenden Befehl ein, um es einem Konto zu ermöglichen, Ihre private Ressource zu sehen. 

`bx catalog entry-visibility-set <service-id> --includes-add <account-id or account-email>`

Geben Sie im Anschluss an das Flag 'includes-add' eine durch Kommas unterteilte Aufzählung von E-Mail-Adressen oder IDs an, die Konten zugeordnet sind. 

Der Prozess für das Aufnehmen der Ressource nimmt nach der Befehlseingabe etwa 30 Minuten in Anspruch. Melden Sie sich nach 30 Minuten ab und erneut mit Ihrem Konto an, um die aufgenommene Ressource angezeigt zu bekommen. 

## Konto aus Einschlussliste entfernen
{: #remove-exclude}

Geben Sie den folgenden Befehl ein, um ein Konto aus der Einschlussliste zu entfernen. 

`bx catalog entry-visibility-set <service-id> --includes-remove <account-id or account-email>`

## Sichtbarkeit untergeordneter Objekte verwalten
{: #child-vis}

Sie können die Sichtbarkeit Ihrer Ressource und der untergeordneten Elemente verwalten. 

Ist die Einschlussliste leer, bedeutet das, dass sie nur den Administratoren Ihres Kontos angezeigt wird. Ihr Konto muss in der Einschlussliste für alle Mitglieder des Kontos enthalten sein, damit sie angezeigt wird. 

Wenn Sie beispielsweise den Befehl `bx catalog service <your_service>` eingeben, werden Ihnen die untergeordneten Elemente der Ressource angezeigt. 

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

Sie können die Ressourcen-ID für die untergeordnete Bereitstellung abrufen und anschließend mit dem folgenden Befehl ein Konto aufnehmen: `bx catalog entry-visibility-set <service-id> —-includes-add <some-other-account>`.

Die untergeordneten Elemente eines Objekts können die Sichtbarkeit übernehmen. Diese Vererbung ist jedoch relativ komplex. Ist das untergeordnete Objekt privat, wird die zugehörigen eigene Sichtbarkeitskonfiguration angewendet. Ist das untergeordnete Objekt jedoch als öffentlich konfiguriert, wird die Sichtbarkeit des übergeordneten Elements übernommen. Durch das Festlegen der Sichtbarkeit eines privaten untergeordneten Objekts wird die Sichtbarkeit möglicherweise stärker eingeschränkt als die des übergeordneten Objekts. 

Weitere Informationen zur Sichtbarkeit finden Sie in der [API-Dokumentation](https://console.bluemix.net/apidocs/682). 
