---
title: 용 JavaScript 코드 [!DNL Analytics for Advertising]
description: 용 JavaScript 코드 [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '939'
ht-degree: 0%

---

# 용 JavaScript 코드 [!DNL Analytics for Advertising]

*Adobe Advertising-Adobe Analytics 통합 전용 광고주*

*Advertising DSP만 사용하는 광고주*

Advertising DSP의 경우, [!DNL Analytics for Advertising] 통합은 뷰스루 및 클릭스루 사이트 상호 작용을 추적합니다. 클릭스루 방문은 웹 페이지의 표준 Adobe Analytics 코드로 추적됩니다. a [!DNL Analytics] 코드는 랜딩 페이지 URL에서 AMO ID 및 EF ID 매개 변수를 캡처하고 각각 예약된 eVar에서 추적합니다. 웹 페이지에서 JavaScript 코드 조각을 배포하여 뷰스루 방문을 추적할 수 있습니다.

사이트 방문의 첫 번째 페이지 보기에서 Advertising JavaScript Adobe 코드는 방문자가 광고를 보고 클릭했는지 여부를 확인합니다. 사용자가 이전에 클릭스루를 통해 사이트에 들어갔거나 광고를 보지 않은 경우 방문자는 무시됩니다. 방문자가 광고를 보고 [전환 확인 기간 을 클릭합니다.](/help/integrations/analytics/prerequisites.md#lookback-a4adc) Adobe 광고 내에서 설정되면 Adobe 광고 JavaScript 코드 중 하나)는 [Experience Cloud ID 서비스](https://experienceleague.adobe.com/docs/id-service/using/home.html) 추가 ID를 생성하려면`SDID`) 또는 b) Adobe Experience Platform 사용 [!DNL Web SDK] `generateRandomID` 생성 방법 `[!DNL StitchID]`. 두 ID는 Adobe 광고의 데이터를 방문자의 Adobe Analytics 히트에 연결하는 데 사용됩니다. 그런 다음 Adobe Analytics은 Adobe 광고에서 광고 노출과 연관된 AMO ID 및 EF ID를 쿼리합니다. 그러면 AMO ID 및 EF ID가 해당 eVar에서 채워집니다. 이 값은 지정된 기간(기본적으로 60일) 동안 지속됩니다.

[!DNL Analytics] 사이트 트래픽 지표(페이지 보기 수, 방문 및 체류 시간 등)와 [!DNL Analytics] EF ID를 키로 사용하여 광고 시간별로 Adobe을 지정하는 사용자 지정 또는 표준 이벤트. 다음 [!DNL Analytics] 그런 다음 Adobe 광고 속성 시스템을 통해 지표를 실행하여 전환을 클릭 및 노출 내역에 연결합니다.

>[!NOTE]
>
>Adobe Advertising JavaScript 추적 로직은 Adobe 측에서 발생하므로 페이지 로드 시간에 거의 영향을 주지 않습니다.
>
>반면에, [!DNL DCM] 데이터 커넥터 [!DNL Analytics] (사용 [!DNL Google Campaign Manager 360]) for Advertising DSP은 클라이언트측에서 발생합니다. 클라이언트측 결합은 페이지 로드 속도를 저하하고 데이터 손실 위험을 높입니다. 이 문제는 [!DNL Analytics] JavaScript가 ping을 수행해야 합니다. [!DNL DoubleClick] 그리고 [!DNL DoubleClick] 마지막 클릭/노출 데이터를에 다시 전달하려면 [!DNL Analytics]. 다음 경우에 [!DNL DSP] 팀이 설정 [!DNL DCM] data connector에서 페이지를 지연시킬 시간을 지정해야 합니다.

## JavaScript 코드 배포

JavaScript 라이브러리는 [!DNL Analytics] 및 Adobe 광고를 사용하여 서로 통신합니다. 만약 [!DNL Analytics for Advertising] Adobe 광고 구현 중에 통합이 완료되었다면, 배포 방법에 대한 지침과 함께 이 코드를 이미 받았어야 합니다.

### 코드

#### Experience Cloud Identity 서비스를 사용하는 구현 `visitorAPI.js` 코드

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id');
</script>
```

#### Experience Platform을 사용하는 구현 [!DNL Web SDK] `alloy.js`코드

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id').generateRandomId();
</script>
```

### 코드를 배치할 위치

다음 [!DNL Analytics for Advertising] JavaScript 함수는 Experience Cloud ID 서비스 뒤에 와야 하며, 보조 ID(`SDID`) 또는 `[!DNL StitchID]` Analytics 호출에 포함할 수 있습니다.

![코드 배치](/help/integrations/assets/a4adc-code-placement.png)

### 코드 배포 확인

패킷 스니퍼 유형(예: [!DNL Charles], [!DNL Fiddler], 또는 [!DNL Chrome Developer Tools])를 사용하십시오. [!DNL Analytics]아래에 설명된 대로,

#### 로 코드를 확인하는 방법 [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. 열기 [!DNL Chrome Developer Tools] 을 클릭하고 **네트워크** 탭.

1. 가 포함된 웹 사이트 페이지 로드 [!DNL Analytics for Advertising] JavaScript.

1. 필터 [!UICONTROL Network] 탭별 `last` 및 의 두 행을 검토합니다.

   ![마지막 필터링](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * 첫 번째 행은 JavaScript 라이브러리에 대한 호출이며 제목은 입니다 `last-event-tag-latest.min.js`.
   * 두 번째 행은 Adobe 광고에 요청을 보내는 호출입니다. 시작은 다음과 같습니다. `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

      광고 Adobe 호출이 표시되지 않으면 방문의 첫 번째 페이지 보기가 아닐 수 있습니다. 테스트를 위해 다음 호출이 해당 방문에 대한 첫 번째 페이지 보기가 되도록 쿠키를 제거할 수 있습니다.

      1. Application 탭에서 `adcloud` 쿠키를 쿠키 로 설정하고 쿠키에 가 포함되어 있는지 확인합니다. `_les_v` (마지막 방문) 값을 갖는 `y` 30분 후에 만료되는 UTC epoch 타임스탬프입니다.
      1. 삭제 `ad cloud` 쿠키를 사용하여 페이지를 새로 고칩니다.

1. (Experience Cloud Identity 서비스를 사용하는 구현 `visitorAPI.js` 코드) 필터 `/b/ss` analytics 히트를 확인합니다.

   ![필터링 `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. (Experience Platform을 사용하는 구현 [!DNL Web SDK] `alloy.js`코드) 필터 `/interact` Edge Network에 대한 요청 페이로드가 포함되어 있는지 확인하려면 `advertisingStitchID`.

   ![필터링 `/interact`](/help/integrations/assets/a4adc-code-validation-filter-interact.png)

1. 두 히트 간의 ID 값을 비교합니다. 모든 값은 바로 다음 URL 경로인 Analytics 히트에서 보고서 세트 ID를 제외하고 쿼리 문자열 매개 변수에 있습니다 `/b/ss/`.

   | ID | Analytics 매개 변수 | 에지 네트워크 | Adobe 광고 매개 변수 |
   | --- | --- | --- | --- |
   | Experience Cloud IMS 조직 | `mcorgid` |  | `_les_imsOrgid` |
   | 보조 데이터 ID | sdid |  | `_les_sdid` |
   | 결합 ID | stitchId | `advertisingStitchID` 아래에 `_adcloud` 속성 |  |
   | Analytics 보고서 세트 | 다음 값 `/b/ss/` |  | `_les_rsid` |
   | Experience Cloud 방문자 ID | mid |  | `_les_mid` |

   ID 값이 일치하면 JavaScript 구현이 확인됩니다. Adobe 광고는 [!DNL Analytics] 모든 클릭스루 또는 뷰스루 추적 세부 사항이 있는 경우 이를 제공합니다.

#### 로 코드를 확인하는 방법 [!DNL Adobe Experience Cloud Debugger]

1. 를 엽니다. [[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html) 참조하십시오.
1. 로 이동합니다. [!UICONTROL Network] 탭.
1. 에서 [!UICONTROL Solutions Filter] 도구 모음 [!UICONTROL Adobe Advertising] 및 [!UICONTROL Analytics].
1. 에서 [!UICONTROL Request URL – Hostname] 매개 변수 행, 찾기 `lasteventf-tm.everesttech.net`.
1. 에서 [!UICONTROL Request – Parameters] 행의 3단계와 유사하게 생성된 신호를 감사하십시오.[로 코드를 확인하는 방법 [!DNL Chrome Developer Tools]](#validate-js-chrome).&quot;
   * (Experience Cloud Identity 서비스를 사용하는 구현 `visitorAPI.js` 코드) `Sdid` 매개 변수와 일치함 `Supplemental Data ID` ( Adobe Analytics 필터) 아래에 그룹화됩니다.
   * (Experience Platform을 사용하는 구현 [!DNL Web SDK] `alloy.js`코드)의 값이 `advertisingStitchID` 매개 변수와 일치함 `Sdid` Experience Platform 에지 네트워크로 전송됩니다.
   * 코드가 생성되지 않으면 Adobe 광고 쿠키가 [!UICONTROL Application] 탭. 페이지가 제거되면 페이지를 새로 고침하고 프로세스를 반복합니다.

   ![감사 [!DNL Analytics for Advertising] 의 JavaScript 코드 [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [개요 [!DNL Analytics for Advertising]](overview.md)
>* [구현을 위한 사전 요구 사항 및 주요 정보 [!DNL Analytics for Advertising]](prerequisites.md)

