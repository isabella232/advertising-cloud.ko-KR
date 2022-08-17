---
title: '"[!DNL Adobe][!DNL Audience Analytics] Advertising Cloud 고객용"'
description: 사용 방법 알아보기 [!DNL Adobe][!DNL Audience Analytics] 광고 사용 사례
feature: Integration with Adobe Audience Manager
source-git-commit: d83e36847d0e14bc7e83106c0a221680060c2e58
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# [!DNL Adobe][!DNL Adobe] Advertising Cloud 고객용

[[!DNL Adobe][!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) 은 Audience Manager 고객이 세그먼트를 보낼 수 있도록 해주는 Adobe Audience Manager과 Adobe Analytics 간의 통합입니다 [!DNL Analytics] 사이트 활동에 대한 보강된 인사이트를 제공합니다.

Advertising Cloud 고객은 [!DNL Audience Analytics]. 통합을 통해 다음을 수행할 수 있습니다.

* Advertising Cloud 노출 데이터를에 바로 전송 [!DNL Analytics] 상위 단계 활동이 다운스트림 사이트 활동에 미치는 영향을 판별하는 데 사용됩니다.

* 상위 단계 노출 광고에서 마케팅 채널 및 사이트 시작 지점을 결정합니다.

* 통합 레이어 [!DNL Analytics for Advertising Cloud] 타사 인구 통계 세그먼트를 [Audience Manager [!DNL Audience Marketplace]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/audience-marketplace/audience-marketplace.html) with [!DNL Analytics for Advertising Cloud] 데이터 를 참조하십시오.

   [!DNL Audience Marketplace] 에서는 구매자가 대상으로 데이터를 보낼 수 있는 &quot;활성화&quot; 구독 모델을 사용하여 타사 데이터 피드에 대한 액세스를 제공합니다. 데이터가 [!DNL Analytics] 수신하면 활성화 비용이 적용되지 않습니다.

* (Advertising Cloud DSP을 사용하는 광고주) 전체적인 여정 관리 통찰력을 위해 노출 세그먼트를 추가합니다.

   Advertising Cloud DSP은 Adobe Experience Platform 또는 Audience Manager 노출 추적 픽셀의 구현을 통해 노출 데이터를 Audience Manager에 실행 가능한 신호로 보낼 수 있습니다. 동일한 데이터를에 전달 [!DNL Analytics] 고급 데이터 분석을 활성화합니다. 참조:[Adobe Audience Manager과 Advertising Cloud Media 데이터 통합 개요](/help/integrations/audience-manager/media-data-integration/overview.md)&quot;&quot;을 참조하십시오.

에 대한 자세한 정보 [!DNL Audience Analytics], 사전 요구 사항 및 워크플로우를 포함한 자세한 내용은 &quot;[Audience Analytics 개요](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html).&quot;

## 사용 방법의 예 [!DNL Audience Analytics] Advertising Cloud 데이터를 사용한 데이터

다음은 내에서 결합된 데이터를 사용할 수 있는 방법의 예입니다 [!DNL Analytics] [!DNL Analysis Workspace].

### 상위 단계 활동이 다운스트림 활동에 미치는 영향 을 참조하십시오

Audience Manager 노출 세그먼트를 사용하여 상위 단계 사이트 활동이 다운스트림 사이트 활동에 미치는 영향을 확인할 수 있습니다. 추적 픽셀에 Advertising Cloud 또는 타사 매크로 ID를 포함하여 캠페인 수준부터 사용자가 노출된 사이트 수준까지 세부 수준에서 미치는 영향을 추적합니다.

주요 이점:

* 단계/광고 유형별로 노출을 추적하고 사용 [!DNL Audience Analytics] 엔트리 레벨 가격 결정 및 고객 여정의 다음 단계와 겹치기

* 상위 단계 활동이 다운스트림 사이트 활동에 미치는 영향을 결정합니다.

* Connect [!DNL Analytics for Advertising Cloud]<!-- which doesn't include the last exposure event --> 및 [!DNL Audience Analytics] 데이터 <!-- (which includes the user's last exposure event) --> 를 입력하여 사이트에 대한 전체적인 여정을 결정합니다.

다음은에서 만들 수 있는 보고서의 예입니다 [!DNL Analysis Workspace].

![상위 단계 활동이 다운스트림 사이트 활동에 미치는 영향을 참조하십시오](/help/integrations/assets/audience-analytics-upper-funnel-exposure.png)

### 사용 [!DNL Audience Analytics] 사용자 프로필 분석을 위한 타사 세그먼트 데이터

타사 Audience Manager 세그먼트를 사용하여 사용자가 사이트와 상호 작용하는 방법을 보다 효과적으로 분석할 수 있습니다. 정보를 사용하여 타사 세그먼트의 프로필과 미디어 캠페인 사이트의 주요 성능 지표가 어떻게 상호 작용하는지 기준으로 미디어를 활성화할 새로운 타사 대상을 결정할 수 있습니다.

>[!TIP]
> Audience Manager 사용 `Audiences ID` 및 `Audiences Name` 차원 전체 [!DNL Analytics], 다른 차원처럼 [!DNL Analytics] 를 수집합니다.

다음은에서 만들 수 있는 보고서의 예입니다 [!DNL Analysis Workspace].

![타사 세그먼트를 사용하여 사용자 프로필 분석 강화](/help/integrations/assets/audience-analytics-third-party-report.png)

>[!MORELIKETHIS]
>
>* [Adobe Audience Manager과 Advertising Cloud 통합](/help/integrations/audience-manager/overview.md)

