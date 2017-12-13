---



copyright:

  years: 2015, 2017
lastupdated: "2017-11-16"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# {{site.data.keyword.Bluemix_notm}} 등록

기존 IBM ID 사용, 새 IBM ID 작성 또는 연합 ID 사용으로 {{site.data.keyword.Bluemix}} 계정을 등록할 수 있습니다. 연합 ID는 도메인과 사용자 신임 정보를 사용하여 IBM 웹 애플리케이션에 액세스할 수 있도록 IBM에 등록된 회사의 도메인 내에서 사용되는 ID입니다.
{:shortdesc}  

{: #federatedid}
사용자 회사에서 등록할 수 있도록 IBM과 이미 작업을 한 경우에만 연합 ID를 사용하여 {{site.data.keyword.Bluemix_notm}}에 등록할 수 있습니다. 회사의 도메인을 IBM에 등록하면 사용자가 기존 회사 사용자 신임 정보를 사용하여 IBM 제품과 서비스에 로그인할 수 있습니다. 그런 다음 회사의 ID 제공자가 인증을 처리합니다. 연합 ID를 사용하여 {{site.data.keyword.Bluemix_notm}}에 로그인하는 경우 회사의 로그인 페이지를 통해 로그인하도록 프롬프트가 표시됩니다. 회사 또는 조직의 도메인을 IBM에 등록하도록 요청하는 방법에 대한 정보 또는 프로세스에 대한 자세한 정보는 [IBMid Enterprise Federation Adoption Guide ![외부 링크 아이콘](../icons/launch-glyph.svg)](https://ibm.box.com/v/IBMid-Federation-Guide){: new_window}를 참조하십시오. 연합 ID 등록을 요청하는 경우 오퍼링 중재자 또는 클라이언트 중재자와 같은 IBM 스폰서가 필요합니다. 

IBM은 이 ID 연합에 대해 SAML 2.0(Security Assertion Markup Language 2.0)의 레버리지를 활용합니다. SAML 2.0는 보안 도메인 간에 인증 데이터를 교환하기 위한 표준 버전입니다. 이는 조직 "ID 제공자" 및 "IBM RP(Rely Party)"(또는 서비스 제공자라고도 함) 간의 정보 전달을 위해 어설션이 포함된 보안 토큰을 사용하는 XML 기반 프로토콜입니다. 

| 등록 방법      | 세부사항|    
|-----------------|---------|
|기존 IBM ID| IBM ID가 이미 있는 경우 기타 IBM 제품과 서비스에 사용하는 기존 신임 정보로 {{site.data.keyword.Bluemix_notm}}에 등록하십시오. 등록할 때 전화번호를 입력해야 합니다. |
|새 IBM ID| IBM ID가 없는 경우에는 이를 작성할 수 있습니다. IBM ID를 사용하면 {{site.data.keyword.Bluemix_notm}}를 비롯하여 사용하는 모든 IBM 제품과 서비스에 하나의 로그인 사용자 이름을 사용할 수 있습니다. 이름과 성, 전화번호, 새 신임 정보의 비밀번호를 포함한 개인 정보를 입력해야 합니다. 기타 IBM 제품과 서비스 사용 시 이 IBM ID를 사용하여 로그인할 수 있습니다. |
|연합 ID| 사용자 회사가 회사 도메인에서 생성된 사용자 신임 정보를 IBM에 등록하도록 요청한 경우 회사의 로그인에 이미 사용하고 있는 신임 정보를 이용해 {{site.data.keyword.Bluemix_notm}}에 등록할 수 있습니다. 등록할 때 전화번호를 입력해야 합니다. |
{:caption="표 1. 등록 방법" caption-side="top"}
