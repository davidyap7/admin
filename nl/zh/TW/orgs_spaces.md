---

copyright:

  years: 2015, 2017
lastupdated: "2017-05-03"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# 建立組織及空間
{: #orgsspacesusers}

身為帳戶擁有者，您可以使用「管理組織」頁面來管理組織。組織管理員也可以使用「管理組織」頁面來管理將他們設為管理員的任何組織。
{:shortdesc}

若要管理組織及空間，請從 {{site.data.keyword.Bluemix_notm}} 功能表列按一下**管理** &gt; **帳戶** &gt; **組織**。 

**附註**：您必須是「隨收隨付制」帳戶的帳戶擁有者，才能建立組織。

## 建立組織
{: #createorg}

組織可以跨越多個地區，而且是由下列項目所定義：

<dl>
<dt>團隊成員</dt>
<dd>組織及空間中具有基本許可權的角色。您必須先被指派給組織，才能獲授與組織內空間的其他許可權。如需詳細資訊，請參閱[使用者及角色](/docs/iam/users_roles.html#userrolesinfo)。</dd>
<dt>網域</dt>
<dd>提供網際網路上配置給組織的路徑。路徑具有一個子網域及一個網域。子網域一般是應用程式名稱。網域可能是系統網域，或您針對應用程式所登錄的自訂網域。請參閱[管理自訂網域](/docs/admin/manageorg.html#managedomains)。<br/>
<p>**附註：**如果您新增自訂網域，則必須配置 DNS 伺服器來解析自訂網域，以指向 {{site.data.keyword.Bluemix_notm}} 系統網域。使用此方式，{{site.data.keyword.Bluemix_notm}} 接到您的自訂網域的要求時，可以將它適當地遞送至您的應用程式。</p></dd>
<dt>配額</dt>
<dd>代表組織可用的資源，包括可配置供組織使用的服務數目及記憶體量。建立組織時，會指派配額。組織空間中的任何應用程式或服務都會使用配額。使用「隨收隨付制」或「訂閱」方案，您可以在組織需要變更時，調整 Cloud Foundry 應用程式及容器的配額。請參閱[管理配額](/docs/admin/manageorg.html#managequota)。<p>**附註：**在「訂閱」帳戶中，配額是觸發消費通知的使用者定義限制。</p></dd>
</dl>

在 {{site.data.keyword.Bluemix_notm}} 中，您可以使用組織來啟用團隊成員之間的協同作業，以及使用下列方式促進專案資源的邏輯分組：

<ul>
<li>您可以將組織中的一組空間、應用程式、服務、網域、路徑及團隊成員群組在一起。</li>
<li>您可以根據每位使用者管理空間及組織的存取權。</li>
</ul>

建立組織時，組織名稱在 {{site.data.keyword.Bluemix_notm}} 內必須是唯一的。
如果另一位 {{site.data.keyword.Bluemix_notm}}「公用」、「專用」或「本端」使用者已在使用組織名稱，則您必須指定新的名稱。建立組織之後，您會自動獲指派*組織管理員* 許可權，這可讓您編輯組織名稱、新增團隊成員，以及在組織中建立或刪除空間。

您可以使用 [`bx iam org-delete`](/docs/cli/reference/bluemix_cli/bx_cli.html#bluemix_iam_org_delete) 指令來刪除組織。當您刪除組織時，會刪除組織內的所有空間、應用程式及服務。

可以將下列[使用者角色](/docs/iam/users_roles.html#userrolesinfo)指派給組織中的團隊成員：

<ul>
<li>組織管理員</li>
<li>組織帳單管理員</li>
<li>組織審核員</li>
</ul>

只有具有「隨收隨付制」帳戶的帳戶擁有者才能建立組織。您可以完成下列步驟來建立組織：

1. 按一下**管理** &gt; **帳戶** &gt; **組織**。
2. 按一下**新增組織**。
3. 輸入組織名稱。
4. 按一下**新增**。

<!-- Add info on Manage infrastructure option under a space -->

## 建立空間
{: #spaceinfo}

在組織內，您可以使用空間來群組一組應用程式、服務及團隊成員。在 {{site.data.keyword.Bluemix_notm}} 中，空間關聯於特定地區。

將團隊成員新增至組織之後，即可將空間的許可權授與他們。與組織類似，空間也會有一組[使用者角色](/docs/iam/users_roles.html#userrolesinfo)，其具有指派給團隊成員的特定許可權：

<ul>
<li>空間管理員</li>
<li>空間開發人員</li>
<li>空間審核員</li>
</ul>

**附註**：團隊成員必須至少獲指派空間中的一個許可權。

您可以在組織中建立空間；例如，建立 *dev* 空間作為開發環境、*test*
空間作為測試環境，以及 *production* 空間作為正式作業環境。
然後，您可以建立應用程式與空間的關聯。請完成下列步驟，以建立空間：

1. 按一下**管理** &gt; **帳戶** &gt; **組織**。
2. 識別您要新增空間的組織，然後選取**檢視詳細資料**。
4. 按一下**新增空間**。
5. 輸入空間名稱。
6. 按一下**新增**。
