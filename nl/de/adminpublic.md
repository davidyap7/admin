---



copyright:

  years: 2015, 2017
lastupdated: "2017-11-16"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# {{site.data.keyword.Bluemix_notm}}-Anmeldung

Sie können sich unter Verwendung einer vorhandenen IBMid, durch Erstellung einer neuen IBMid oder unter Verwendung einer eingebundenen ID für ein {{site.data.keyword.Bluemix}}-Konto anmelden. Eine eingebundene ID ist eine ID innerhalb einer Unternehmensdomäne, die für IBM registriert wurde, um über die Domäne und die Benutzerberechtigungsnachweise auf IBM Webanwendungen zugreifen zu können.
{:shortdesc}  

{: #federatedid}
Die Anmeldung an {{site.data.keyword.Bluemix_notm}} mit einer eingebundenen ID ist nur dann möglich, wenn Ihr Unternehmen bereits bei IBM registriert wurde.  Nach der Registrierung der Unternehmensdomäne bei IBM können sich die Benutzer unter Verwendung der bestehenden Benutzerberechtigungsnachweise des Unternehmens bei IBM Produkten und Services anmelden. Die Authentifizierung erfolgt über den Identitätsprovider Ihres Unternehmens. Bei der Anmeldung an {{site.data.keyword.Bluemix_notm}} mit einer eingebundenen ID werden Sie zur Anmeldung über die Anmeldeseite Ihres Unternehmens aufgefordert. Weitere Informationen zum Anfordern der Registrierung der Domäne Ihres Unternehmens oder Ihrer Organisation bei IBM und zu den hierfür erforderlichen Schritten finden Sie in der Veröffentlichung [IBMid Enterprise Federation Adoption Guide ![Symbol für externen Link](../icons/launch-glyph.svg)](https://ibm.box.com/v/IBMid-Federation-Guide){: new_window}. Für die Registrierung eingebundener IDs muss ein IBM Sponsor, wie beispielsweise ein Angebotsmanager oder Kundenansprechpartner, kontaktiert werden.

IBM nutzt Security Assertion Markup Language 2.0 (SAML 2.0) für diese Identitätseinbindung. SAML 2.0 ist eine Standardversion für den Austausch von Authentifizierungsdaten zwischen Sicherheitsdomänen. Es handelt sich dabei um ein XML-basiertes Protokoll, das ein Sicherheitstoken mit Zusicherungen verwendet, die zum Übergeben von Informationen zwischen dem sog. "Identity Provider" der Organisationen und der "IBM Rely Party (RP)" dient, die auch als Service-Provider bezeichnet wird. 

| Anmeldemethoden | Details |    
|-----------------|---------|
|Vorhandene IBMid | Wenn Sie bereits über eine IBMid verfügen, können Sie sich mit Ihren bestehenden Berechtigungsnachweisen für andere IBM Produkte und Services bei {{site.data.keyword.Bluemix_notm}} anmelden. Bei der Anmeldung ist die Eingabe einer Telefonnummer erforderlich. |
|Neue IBMid | Wenn Sie noch keine IBMid besitzen, können Sie diese erstellen. Mit einer IBMid können Sie sich mit nur einem Benutzernamen für alle IBM Produkte und Services, einschließlich {{site.data.keyword.Bluemix_notm}}, anmelden. Für die neuen Berechtigungsnachweise müssen Sie Ihre persönlichen Daten (Vor- und Nachname, Telefonnummer und Kennwort) eingeben. Sie können sich mit dieser IBMid anmelden, wenn Sie andere IBM Produkte oder Services verwenden.  |
|Eingebundene ID | Wenn Ihr Unternehmen die Registrierung der Benutzerberechtigungsnachweise für die Unternehmensdomäne bei IBM angefordert hat, können Sie sich mit den Benutzerberechtigungsnachweisen bei {{site.data.keyword.Bluemix_notm}} anmelden, die Sie bereits für die Unternehmensanmeldung verwenden. Bei der Anmeldung ist die Eingabe einer Telefonnummer erforderlich. |
{:caption="Tabelle 1. Anmeldemethoden" caption-side="top"}
