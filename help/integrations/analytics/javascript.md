---
title: ' [!DNL Analytics for Advertising Cloud]에 대한 JavaScript 코드'
description: ' [!DNL Analytics for Advertising Cloud]에 대한 JavaScript 코드'
feature: Integration with Adobe Analytics
exl-id: 184508ce-df8d-4fa0-b22b-ca0546a61d58
source-git-commit: 56ac178bf10d8c934297521ca3075783e1bc2c36
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# [!DNL Analytics for Advertising Cloud]에 대한 JavaScript 코드

*Advertising Cloud-Adobe Analytics 통합만 있는 광고주*

*Advertising Cloud DSP만 사용하는 광고주*

Advertising Cloud DSP의 경우 [!DNL Analytics for Advertising Cloud] 통합은 뷰스루 및 클릭스루 사이트 상호 작용을 추적합니다. 클릭스루 방문은 웹 페이지의 표준 Adobe Analytics 코드로 추적됩니다. [!DNL Analytics] 코드는 랜딩 페이지 URL에서 AMO ID 및 EF ID 매개 변수를 캡처하고 각각 예약된 eVar에서 추적합니다. 웹 페이지에서 두 줄의 JavaScript 코드를 배포하여 뷰스루 방문을 추적할 수 있습니다.

사이트 방문의 첫 번째 페이지 보기에서 Advertising Cloud JavaScript 코드는 방문자가 이전에 광고를 보거나 클릭했는지 확인합니다. 사용자가 이전에 클릭스루를 통해 사이트에 들어갔거나 광고를 보지 않은 경우 방문자는 무시됩니다. 방문자가 광고를 보고 Advertising Cloud 내에서 [클릭 전환 창](/help/integrations/analytics/prerequisites.md#lookback-a4adc) 설정 중에 클릭스루를 통해 사이트에 들어가지 않은 경우, Advertising Cloud JavaScript 코드는 [Experience Cloud ID 서비스](https://experienceleague.adobe.com/docs/id-service/using/home.html)를 사용하여 Advertising Cloud의 데이터를 방문자의 Adobe Analytics 히트에 연결하는 데 사용되는 보조 ID(`SDID`)를 생성합니다. 그런 다음 Adobe Analytics은 Advertising Cloud에서 광고 노출과 관련된 AMO ID 및 EF ID를 쿼리합니다. 그러면 AMO ID 및 EF ID가 해당 eVar에서 채워집니다. 이 값은 지정된 기간(기본적으로 60일) 동안 지속됩니다.

[!DNL Analytics] EF ID를 키로 사용하여 사이트 트래픽 지표(페이지 보기, 방문 및 체류 시간 등)와  [!DNL Analytics]  사용자 지정 또는 표준 이벤트를 Advertising Cloud 시간별로 전송합니다. 그런 다음 이 [!DNL Analytics] 지표는 Advertising Cloud 속성 시스템을 통해 실행되어 전환을 클릭 및 노출 내역에 연결합니다.

>[!NOTE]
>
>Advertising Cloud JavaScript 추적 로직은 Adobe 측에서 발생하므로 페이지 로드 시간에 거의 영향을 주지 않습니다.
>
>반면 Advertising Cloud DSP에 대한 [!DNL DCM] 데이터 커넥터에 대한 [!DNL Analytics]([!DNL Google Campaign Manager 360] 사용)의 로직은 클라이언트측에서 발생합니다. 클라이언트측 결합은 페이지 로드 속도를 저하하고 데이터 손실 위험을 높입니다. 이 문제는 [!DNL Analytics] JavaScript가 [!DNL DoubleClick]을 ping하고 [!DNL DoubleClick]가 마지막 클릭/노출 데이터를 [!DNL Analytics]에 다시 전달할 때까지 기다려야 하기 때문에 발생합니다. [!DNL DSP] 팀이 [!DNL DCM] 데이터 커넥터를 설정할 때 페이지를 지연시킬 기간을 지정해야 합니다.

## JavaScript 코드 배포

JavaScript 라이브러리는 [!DNL Analytics] 과 Advertising Cloud이 서로 통신할 수 있도록 하는 두 줄로 구성됩니다. Advertising Cloud 구현 중에 [!DNL Analytics for Advertising Cloud] 통합이 완료된 경우 배포 방법에 대한 지침과 함께 이 코드를 받았어야 합니다.

코드가 없는 경우 Advertising Cloud 지원 팀에 문의하십시오.

### 코드를 배치할 위치

[!DNL Analytics for Advertising Cloud] JavaScript 함수는 Experience Cloud ID 서비스 뒤에 와야 하며, 보조 ID(`SDID`)를 Analytics 호출에 포함할 수 있습니다.

![코드 배치](/help/integrations/assets/a4adc-code-placement.png)

### 코드 배포 확인

아래 설명된 대로 Advertising Cloud으로 이동하는 요청과 [!DNL Analytics]로 가는 요청 간 4개의 ID의 값을 비교하여 패킷 스니퍼 유형(예: [!DNL Charles], [!DNL Fiddler] 또는 [!DNL Chrome Developer Tools])을 사용하여 유효성 검사를 수행할 수 있습니다.

#### [!DNL Chrome Developer Tools]으로 코드를 확인하는 방법 {#validate-js-chrome}

1. [!DNL Chrome Developer Tools] 을 열고 **네트워크** 탭을 클릭합니다.
1. [!DNL Analytics for Advertising Cloud] JavaScript가 포함된 웹 사이트 페이지를 로드합니다.
1. [!UICONTROL Network] 탭을 `last` 기준으로 필터링하고 두 행을 검토합니다.

   ![마지막 필터링](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * 첫 번째 행은 JavaScript 라이브러리에 대한 호출이며 제목은 `last-event-tag-latest.min.js`입니다.
   * 두 번째 행은 Advertising Cloud에 요청을 보내는 호출입니다. 시작은 다음과 같습니다. `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

      Advertising Cloud에 대한 호출이 표시되지 않으면 방문의 첫 번째 페이지 보기가 아닐 수 있습니다. 테스트를 위해 다음 호출이 해당 방문에 대한 첫 번째 페이지 보기가 되도록 쿠키를 제거할 수 있습니다.

      1. 애플리케이션 탭에서 `adcloud` 쿠키를 찾고 쿠키에 `y` 값과 30분 후에 만료되는 UTC Epoch 타임스탬프가 있는 `_les_v`(마지막 방문)가 포함되어 있는지 확인합니다.
      1. `ad cloud` 쿠키를 삭제하고 페이지를 새로 고칩니다.
1. `/b/ss` 을 필터링하여 Analytics 히트를 확인합니다.

   ![필터링  `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. 두 히트 간의 ID 값을 비교합니다. 모든 값은 `/b/ss/` 바로 뒤에 있는 URL 경로인 Analytics 히트의 보고서 세트 ID를 제외하고 쿼리 문자열 매개 변수에 있습니다.

   | ID | Analytics 매개 변수 | Advertising Cloud 매개 변수 |
   |--- |--- |--- |
   | Experience Cloud IMS 조직 | `mcorgid` | `_les_imsOrgid` |
   | 보조 데이터 ID | sdid | `_les_sdid` |
   | Analytics 보고서 세트 | `/b/ss/` 뒤의 값 | `_les_rsid` |
   | Experience Cloud 방문자 ID | mid | `_les_mid` |

   ID 값이 일치하면 JavaScript 구현이 확인됩니다. Advertising Cloud은 클릭스루 또는 뷰스루 추적 세부 정보가 있는 경우 [!DNL Analytics] 서버를 전송합니다.

#### [!DNL Adobe Experience Cloud Debugger]으로 코드를 확인하는 방법

1. 홈 페이지에서 [[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using/run-debugger.html) 를 엽니다.
1. [!UICONTROL Network] 탭으로 이동합니다.
1. [!UICONTROL Solutions Filter] 도구 모음에서 [!UICONTROL Advertising Cloud] 및 [!UICONTROL Analytics] 를 클릭합니다.
1. [!UICONTROL Request URL – Hostname] 매개 변수 행에서 `lasteventf-tm.everesttech.net`을 찾습니다.
1. [!UICONTROL Request – Parameters*] 행에서 생성된 신호를 감사합니다. 이는 &quot;[How to Confirm the Code with [!DNL Chrome Developer Tools]](#validate-js-chrome)&quot;의 3단계와 유사합니다.
   * `SDID` 매개 변수가 Adobe Analytics 필터의 `Supplemental Data ID`과 일치하는지 확인합니다.
   * 코드가 생성되지 않으면 [!UICONTROL Application] 탭에서 Advertising Cloud 쿠키가 제거되었는지 확인합니다. 페이지가 제거되면 페이지를 새로 고침하고 프로세스를 반복합니다.

   ![의  [!DNL Analytics for Advertising Cloud] JavaScript 코드 감사  [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [개요 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [구현을 위한 사전 요구 사항 및 주요 정보 [!DNL Analytics for Advertising Cloud]](prerequisites.md)

