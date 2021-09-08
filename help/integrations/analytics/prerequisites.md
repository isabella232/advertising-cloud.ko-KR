---
title: 구현에 대한 사전 요구 사항 및 키 정보 [!DNL Analytics for Advertising Cloud]
description: 구현에 대한 사전 요구 사항 및 키 정보 [!DNL Analytics for Advertising Cloud]
feature: Integration with Adobe Analytics
exl-id: 08e54e2b-ed9b-4489-8de5-ab1379b7133c
source-git-commit: e2ee41c7e3e195f062ad1cc67080ed913d6d3d06
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# [!DNL Analytics for Advertising Cloud] 구현을 위한 사전 요구 사항 및 주요 정보

*Advertising Cloud DSP 및 Advertising Cloud Search을 사용하는 광고주*

Advertising Cloud을 Adobe Analytics과 통합하기 전에 다음 정보를 검토하십시오.

## [!DNL Analytics]에 Advertising Cloud 데이터 보고를 위한 요구 사항

* Experience Cloud ID 서비스: `visitorAPI.js` 버전 2.0 이상
* 모든 Adobe Analytics 버전( [!DNL Prime], [!DNL Premium] 또는 [!DNL Ultimate] 포함)
* Adobe Analytics: `appMeasurement.js` 버전 2.1 이상

>[!TIP]
>
>데이터 품질을 개선하려면 CNAME을 지원하는 최신 버전의 Experience Cloud ID 서비스와 JavaScript용 Analytics AppMeasurement 최신 버전을 사용하십시오.

## Advertising Cloud과 Analytics 세그먼트 공유를 위한 요구 사항

* Experience Cloud ID 서비스: `visitorAPI.js` 버전 2.1 이상
* Adobe Analytics: `!DNL appMeasurement.js` 버전 1.8 이상

## Advertising Cloud에서 [!DNL Analytics] 데이터 보고 요구 사항

Advertising Cloud 구현 팀에 다음을 제공합니다.

* 유료 미디어 활동에 대한 보고 및 Advertising Cloud의 최적화 및 보고를 위한 사이트 활동을 피드하는 데 사용할 [!DNL Analytics] 보고서 세트 ID입니다
* 회사의 Experience Cloud 조직 ID(조직 ID)입니다.

이 두 ID는 Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/run-debugger.html)의 [요약 화면에서 찾을 수 있습니다.

![Experience Cloud Debugger 요약 화면](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Advertising Cloud의 데이터 {#lookback-a4adc}

보고 및 최적화를 위해 [!DNL Analytics] 데이터가 Advertising Cloud에 전송되므로, 데이터는 Advertising Cloud의 광고주용으로 구성된 노출 및 클릭 전환 창을 포함한 속성 규칙에 따라 달라집니다.

![Advertising Cloud의 광고주 수준 전환 창 설정](/help/integrations/assets/a4adc-lookbacks.png)

* Advertising Cloud 속성 클릭 전환 확인 기간: 첫 번째 클릭이 발생한 후 클릭이 전환으로 인한 것일 수 있는 일 수입니다. 기본적으로 이 값은 60일입니다. 최대 기간은 90일입니다
* Advertising Cloud 속성 노출 전환 확인 기간: 광고 노출이 발생한 후 일 수로, 노출이 전환으로 인한 것일 수 있습니다. 기본적으로 이 값은 14일입니다. 최대 기간은 30일입니다

   >[!NOTE]
   >
   > 노출 전환 확인 기간은 [!DNL Analytics for Advertising Cloud]이 아닌 Advertising Cloud에만 해당되며, 보고에 따라 다릅니다.

[!DNL Analytics for Advertising Cloud] JavaScript는 이러한 설정을 사용하여 뷰스루 항목 또는 사이트에 대한 클릭스루 항목을 유효하다고 간주할 때까지의 시간을 결정합니다. 뷰스루 및 클릭스루가 결정되는 방법에 대한 자세한 내용은 &quot;[Analytics에서 사용하는 Advertising Cloud ID](ids.md)&quot;를 참조하십시오.

## [!DNL Analytics]의 Advertising Cloud 데이터

[!DNL Analytics] 는 Analytics 히트 내에서 클릭스루와 뷰스루 모두에 적용되는 광고주의 eVar 지속성 설정에 따라 Advertising Cloud ID(AMO ID)를 설정합니다. 지속성 설정은 Advertising Cloud 백 엔드에서 구성되며 Adobe 계정 관리자가 변경할 수 있습니다.

* [!DNL Analytics for Advertising Cloud] eVar 만료: AMO ID의 경우 기본적으로 60일

>[!NOTE]
>
>다른 기간에 대한 데이터를 세그먼트화하려면 Analysis Workspace 내에서 다른 전환 확인 기간을 사용하여 [사용자 지정 세그먼트](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html)를 설정할 수 있습니다.

## 지원되는 광고 환경

* 검색
* 표시
* 비디오
* 온라인 비디오
* 기본

각 채널에서 지원되는 최신 광고 환경에 대해서는 Adobe 계정 관리자에게 문의하십시오.

## 구현하기 전에 알아야 할 사항

* 이 통합에 대해 추가 비용이 청구되지 않으며, 서버 호출로 인해 추가 [!DNL Analytics] 또는 Advertising Cloud 비용이 발생하지 않습니다.

* [!DNL Analytics for Advertising Cloud] 광고 서버와 전혀 관계없는 데이터: 모든 광고 서버에서 뷰스루 또는 클릭스루가 발생할 수 있으며 적절한 ID가 사이트 시작 시 생성됩니다.

* 통합은 후속 유료 미디어 및 광고 노력의 입찰 최적화를 위해 [!DNL Analytics] 표준 및 사용자 지정 이벤트만 Advertising Cloud에 전달합니다. 입찰 최적화를 위해 [!DNL Analytics] 세그먼트, 계산된 지표 및 eVar를 Advertising Cloud에 전달하지 않습니다.

* Advertising Cloud은 Advertising Cloud에 구성된 [클릭 및 뷰스루 전환 확인 창](#lookback-a4adc)을 기반으로 사용자가 사이트에 들어가기 전에 클릭하거나 본 마지막 광고에 따라 [!DNL Analytics] 내에 영구 ID를 생성합니다. 사이트 방문자가 프로필 내에 두 유형의 사이트 시작 상호 작용을 가지고 있고, 클릭이 전환 기간 내에 있는 경우 방문자의 클릭스루 ID는 사이트 보고에 대한 뷰스루 ID를 무시합니다.

* [!DNL Analytics for Advertising Cloud] Adobe Analytics의 전환 추적에서는 구성 가능한 추적 전환 확인 기간(기본적으로 60일)을 사용합니다. Advertising Cloud 보고서는 이 추적 전환 확인 기간의 종료를 통한 사이트 전환 및 참여를 반영합니다.

* 모든 광고 유형이 지원됩니다. 그러나 모든 광고 환경이 지원되는 것은 아닙니다.

   예를 들어, CTV에서 클릭이 발생하지 않고 동일한 장치에서 전환이 발생하지 않으므로 연결된 TV(CTV) 광고가 추적되지 않습니다. 그러나 데스크탑 환경 내에서 광고를 보면 일부 뷰스루 사이트 항목 데이터가 추적될 수 있습니다.

* [!DNL Analytics] 전환은 현재 추적되며 동일한 장치의 방문자에게만 적용됩니다.

* [!DNL Analytics for Advertising Cloud] 은 인앱 뷰스루 전환을 지원하지 않습니다.

* 뷰스루 추적은 [!DNL Analytics] 의 서버측 전달 구현을 사용하는 광고주에는 지원되지 않습니다.

### 추가 ID

사이트에 대해 Experience Cloud ID 서비스가 구현되면 [!DNL Analytics] 또는 Advertising Cloud의 데이터가 포함된 히트에 보충 ID가 들어 있습니다.

예: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

정확한 데이터 통합을 위해 [!DNL Analytics for Advertising Cloud] 활동에서 콘텐츠를 전달하거나 목표 지표를 기록하기 위해 사용하는 모든 Advertising Cloud 호출에는 동일한 보충 ID를 공유하는 해당 [!DNL Analytics] 히트가 있어야 합니다.

[!DNL Analytics]에서 문제를 해결하는 경우 [!DNL Analytics] 히트에 대한 보충 ID가 있는지 확인하십시오. [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html)에서 이 ID를 `sdid` 매개 변수로 Advertising Cloud 탭에 볼 수 있습니다.

>[!NOTE]
>
> 이 구현은 [!DNL Analytics for Target] 통합과 유사하게 작동합니다.

>[!MORELIKETHIS]
>
>* [개요 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Advertising Cloud용 Analytics용 JavaScript 코드](/help/integrations/analytics/javascript.md)

