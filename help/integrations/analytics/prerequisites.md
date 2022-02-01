---
title: 구현을 위한 사전 요구 사항 및 주요 정보 [!DNL Analytics for Advertising Cloud]
description: 구현을 위한 사전 요구 사항 및 주요 정보 [!DNL Analytics for Advertising Cloud]
feature: Integration with Adobe Analytics
exl-id: 08e54e2b-ed9b-4489-8de5-ab1379b7133c
source-git-commit: b40c6f08b94e546e5fc068c46b279292a4d8a14f
workflow-type: tm+mt
source-wordcount: '845'
ht-degree: 0%

---

# 구현을 위한 사전 요구 사항 및 주요 정보 [!DNL Analytics for Advertising Cloud]

*Advertising Cloud DSP 및 Advertising Cloud Search을 사용하는 광고주*

Advertising Cloud을 Adobe Analytics과 통합하기 전에 다음 정보를 검토하십시오.

## 의 Advertising Cloud 데이터 보고를 위한 요구 사항 [!DNL Analytics]

* 다음 중 하나를 수행합니다.
   * Adobe Experience Platform 웹 SDK: `alloy.js`
   * Experience Cloud ID 서비스: `visitorAPI.js` 버전 2.0 이상
* 모든 버전의 Adobe Analytics(포함) [!DNL Prime], [!DNL Premium], 또는 [!DNL Ultimate])
* Adobe Analytics: `appMeasurement.js` 버전 2.1 이상

>[!TIP]
>
>데이터 품질을 개선하려면 각 라이브러리의 최신 버전을 사용하십시오.

## Advertising Cloud과 Analytics 세그먼트 공유를 위한 요구 사항

* Experience Cloud ID 서비스: `visitorAPI.js` 버전 2.1 이상
* Adobe Analytics: `!DNL appMeasurement.js` 버전 1.8 이상

## 보고 요구 사항 [!DNL Analytics] Advertising Cloud의 데이터

Advertising Cloud 구현 팀에 다음을 제공합니다.

* 다음 [!DNL Analytics] 유료 미디어 활동에 대한 보고 및 Advertising Cloud의 최적화 및 보고를 위한 사이트 활동을 피드하는 데 사용할 보고서 세트 ID입니다
* 회사의 Experience Cloud 조직 ID(조직 ID)입니다.

두 ID 모두 [Adobe Experience Cloud Debugger 요약 화면](https://experienceleague.adobe.com/docs/debugger/using/run-debugger.html).

![Experience Cloud Debugger 요약 화면](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Advertising Cloud의 데이터 {#lookback-a4adc}

왜냐면 [!DNL Analytics] 보고 및 최적화를 위해 데이터가 Advertising Cloud에 전송되고, 데이터는 Advertising Cloud의 광고주용으로 구성된 노출 및 클릭 전환 확인 기간을 포함한 속성 규칙에 따라 달라집니다.

![Advertising Cloud의 광고주 수준 전환 창 설정](/help/integrations/assets/a4adc-lookbacks.png)

* Advertising Cloud 속성 클릭 전환 확인 기간: 첫 번째 클릭이 발생한 후 클릭이 전환으로 인한 것일 수 있는 일 수입니다. 기본적으로 이 값은 60일입니다. 최대 기간은 90일입니다
* Advertising Cloud 속성 노출 전환 확인 기간: 광고 노출이 발생한 후 일 수로, 노출이 전환으로 인한 것일 수 있습니다. 기본적으로 이 값은 14일입니다. 최대 기간은 30일입니다

   >[!NOTE]
   >
   > 노출 전환 확인 기간은 Advertising Cloud에만 국한되며, [!DNL Analytics for Advertising Cloud], 보고 .

다음 [!DNL Analytics for Advertising Cloud] JavaScript는 이러한 설정을 사용하여 사이트에 대한 뷰스루 항목 또는 클릭스루 항목을 유효하다고 간주하기 위해 얼마나 오래 전까지 있는지를 결정합니다. 뷰스루 및 클릭스루가 결정되는 방법에 대한 자세한 내용은 &quot;[Analytics에서 사용하는 Advertising Cloud ID](ids.md).&quot;

## 의 Advertising Cloud 데이터 [!DNL Analytics]

[!DNL Analytics] 는 Analytics 히트 내에서 클릭스루와 뷰스루 모두에 적용되는 광고주의 eVar 지속성 설정에 따라 Advertising Cloud ID(AMO ID)를 설정합니다. 지속성 설정은 Advertising Cloud 백엔드 및 [!DNL Adobe] 계정 팀이 변경할 수 있습니다.

* [!DNL Analytics for Advertising Cloud] eVar 만료: AMO ID의 경우 기본적으로 60일

>[!NOTE]
>
>다른 기간에 대한 데이터를 세그먼트화하려면 다음을 수행할 수 있습니다 [사용자 지정 세그먼트 설정](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) Analysis Workspace에서 전환 확인 기간이 서로 다릅니다.

## 지원되는 광고 환경

* 검색
* 표시
* 비디오
* 온라인 비디오
* 기본

다음 사항에 문의하십시오. [!DNL Adobe] 각 채널에서 지원되는 최신 광고 환경을 위한 계정 팀입니다.

## 구현하기 전에 알아야 할 사항

* Advertising Cloud 구현 팀이 통합을 설정합니다.

* 이 통합에 대해 추가 비용이 청구되지 않으며, 서버 호출로 인해 추가 비용이 발생하지 않습니다 [!DNL Analytics] 또는 Advertising Cloud 비용을 절감할 수 있습니다.

* [!DNL Analytics for Advertising Cloud] 광고 서버와 전혀 관계없는 데이터: 모든 광고 서버에서 뷰스루 또는 클릭스루가 발생할 수 있으며 적절한 ID가 사이트 시작 시 생성됩니다.

* 통합은 만 전달합니다 [!DNL Analytics] 후속 유료 미디어 및 광고 노력의 입찰 최적화를 위해 Advertising Cloud에 대한 표준 및 사용자 지정 이벤트입니다. 통과되지 않습니다 [!DNL Analytics] 입찰 최적화를 위해 세그먼트, 계산된 지표 및 eVar를 Advertising Cloud에 보냅니다.

* Advertising Cloud은 내에서 영구 ID를 생성합니다 [!DNL Analytics] 사용자가 사이트를 방문하기 전에 클릭한 마지막 광고 또는 본 클릭 수를 기준으로 [클릭 및 뷰스루 전환 확인 기간](#lookback-a4adc) Advertising Cloud에 구성되어 있습니다. 사이트 방문자가 프로필 내에 두 유형의 사이트 시작 상호 작용을 가지고 있고, 클릭이 전환 기간 내에 있는 경우 방문자의 클릭스루 ID는 사이트 보고에 대한 뷰스루 ID를 무시합니다.

* [!DNL Analytics for Advertising Cloud] Adobe Analytics의 전환 추적에서는 구성 가능한 추적 전환 확인 기간(기본적으로 60일)을 사용합니다. Advertising Cloud 보고서는 이 추적 전환 확인 기간의 종료를 통한 사이트 전환 및 참여를 반영합니다.

* 모든 광고 유형이 지원됩니다. 그러나 모든 광고 환경이 지원되는 것은 아닙니다.

   예를 들어, CTV에서 클릭이 발생하지 않고 동일한 장치에서 전환이 발생하지 않으므로 연결된 TV(CTV) 광고가 추적되지 않습니다. 그러나 데스크탑 환경 내에서 광고를 보면 일부 뷰스루 사이트 항목 데이터가 추적될 수 있습니다.

* [!DNL Analytics] 전환은 현재 추적되며 동일한 장치의 방문자에게만 적용됩니다.

* [!DNL Analytics for Advertising Cloud] 은 인앱 뷰스루 전환을 지원하지 않습니다.

* 의 서버측 전달 구현을 사용하는 광고주에는 뷰스루 추적이 지원되지 않습니다 [!DNL Analytics].

### 추가 ID

사이트에 대해 Experience Cloud ID 서비스가 구현되면 의 데이터가 포함된 히트가 발생합니다 [!DNL Analytics] 또는 Advertising Cloud에는 보충 ID가 포함되어 있습니다.

예: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

정확한 데이터 통합을 위해 [!DNL Analytics for Advertising Cloud] 콘텐츠를 전달하거나 목표 지표를 기록하려면 해당 기능이 있어야 합니다 [!DNL Analytics] 동일한 보충 ID를 공유하는 히트.

에서 문제를 해결하는 경우 [!DNL Analytics]에 대한 보조 ID가 있는지 확인합니다. [!DNL Analytics] 히트 수. 에서 [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html)의 경우 Advertising Cloud 탭에서 이 ID를 `sdid` 매개 변수.

>[!NOTE]
>
> 이 구현은 다음과 유사하게 작동합니다 [!DNL Analytics for Target] 통합.

>[!MORELIKETHIS]
>
>* [개요 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Advertising Cloud용 Analytics용 JavaScript 코드](/help/integrations/analytics/javascript.md)

