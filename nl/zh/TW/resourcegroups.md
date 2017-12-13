---



copyright:

  years: 2017
lastupdated: "2017-11-16"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# 管理資源群組
{: #rgs}

資源群組可讓您在可自訂的分組中組織帳戶資源，以同時快速地指派使用者存取多個資源。任何使用「{{site.data.keyword.Bluemix}} 身分及存取管理 (IAM)」存取控制所管理的帳戶資源，都屬於您帳戶內的資源群組。Cloud Foundry 服務仍會指派給組織及空間，而且不能新增至資源群組。

若要開始管理資源群組，請移至 {{site.data.keyword.Bluemix}} 主控台中的**管理** &gt; **帳戶** &gt; **資源群組**。從這裡，您可以檢視資源群組、將其重新命名，並建立新的資源群組。

## 檢視資源群組內的資源

若要輕鬆檢視資源群組內所含的資源，請從儀表板依資源群組進行過濾。

## 建立資源群組

如果您具有「隨收隨付制」或「訂閱」帳戶，則可以建立多個資源群組來輕鬆地管理配額，以及檢視一組資源的計費使用情形。您也可以將資源分組，以更輕鬆地同時指派使用者存取多個實例。

如果您具有「精簡」或試用帳戶，則無法建立其他資源群組，但可以重新命名預設資源群組。

每一個資源群組都是免費的，不過，資源群組與 Cloud Foundry 組織或空間之間的連線會計入您的帳戶配額。如需相關資訊，請參閱[何謂別名？](/docs/manageapps/connecting_apps.html#what_is_alias)。
{: tip}

1. 移至**管理** &gt; **帳戶** &gt; **資源群組**。
2. 按一下**建立資源群組**。
3. 輸入資源群組的名稱。
4. 按一下**新增**。

## 重新命名資源群組

您的第一個資源群組會建立並命名為 `Default`。您可以選擇更新此群組或您建立之任何其他群組的名稱。

1. 移至**管理** &gt; **帳戶** &gt; **資源群組**。
2. 按一下**編輯**。
3. 輸入唯一名稱，然後按一下**儲存**。

## 使用 {{site.data.keyword.Bluemix_notm}} CLI 管理資源群組及資源

{{site.data.keyword.Bluemix_notm}} CLI 具有多個支援資源管理的指令。如需相關資訊，請參閱[用來管理資源群組及資源的指令](/docs/cli/reference/bluemix_cli/bx_cli.html#commands-for-managing-resource-groups-and-resources)。

## 管理對資源群組的存取權

Cloud IAM 可讓您彈性地提供使用者對帳戶中資源的精細存取權。您可以使用 Cloud IAM 將原則指派給使用者，讓使用者可以存取資源群組中的所有資源、資源群組內的單一服務類型，或帳戶中的個別服務實例。讓使用者存取資源群組內的資源，並不會授與使用者對管理資源群組本身的存取權。您可以設定存取權，以個別檢視、編輯及管理實際的資源群組。

如需管理對資源群組存取的相關資訊，請參閱[管理 IAM 存取](/docs/iam/mngiam.html#iammanidaccser)。
