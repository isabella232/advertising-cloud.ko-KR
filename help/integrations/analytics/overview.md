---
title: ' [!DNL Analytics for Advertising Cloud] 개요'
description: ' [!DNL Analytics for Advertising Cloud] 개요'
feature: Integration with Adobe Analytics
exl-id: 31367c8b-3410-4110-9ae6-11defe625355
source-git-commit: 56ac178bf10d8c934297521ca3075783e1bc2c36
workflow-type: tm+mt
source-wordcount: '1087'
ht-degree: 0%

---

# [!DNL Analytics for Advertising Cloud] 개요

*Advertising Cloud DSP 및 Advertising Cloud Search을 사용하는 광고주*

[!DNL Analytics for Advertising Cloud] Adobe Analytics과 Adobe Advertising Cloud을 통합하여 각 제품의 기능을 확장하고 개선합니다.

통합을 통해 광고주는 [!DNL Analytics] 인스턴스에서 클릭스루 및 뷰스루 사이트 상호 작용을 추적할 수 있으므로 브랜드는 광고 비용이 사이트 참여와 중요한 비즈니스 목표에 어떻게 도달하는지 확인할 수 있습니다.

또한 Advertising Cloud은 [!DNL Analytics]이 이미 사이트에서 [!DNL Analytics] 태그를 사용하여 수집하는 방대한 자사 데이터에 액세스할 수 있습니다. 이를 통해 보다 강력한 여정 관리, 자사 리마케팅 및 유료 미디어 사이트 보고를 수행할 수 있습니다. Advertising Cloud은 지출 및 입찰 최적화를 위해 [!DNL Analytics] 데이터를 추가로 사용할 수 있습니다.

올바르게 사용하는 경우 [!DNL Analytics for Advertising Cloud]은(는) 두 기존 역할 사이의 줄을 흐리게 합니다. 광고 여정 관리(광고를 통해 사용자를 사이트에 보내는 작업) 및 웹 분석을 통해 해당 사이트 참여를 파악합니다.

주요 이점:

* 자사 사이트 리마케팅을 위해 [!DNL Analytics] 세그먼트를 Advertising Cloud에 바로 보낼 수 있습니다.
* 유료 미디어 광고를 최적화하기 위해 [!DNL Analytics] 사용자 지정 및 표준 이벤트를 전환 신호로 사용합니다.
* 사이트 시작 지점 및 방문 동작을 더 잘 이해하려면 [!DNL Analytics] Analysis Workspace 를 사용하십시오.
* 웹 분석가와 유료 미디어 팀 간의 긴밀한 공동 작업을 가능하게 합니다.
* [!DNL Analytics] 내에서 영구 Advertising Cloud 뷰스루 및 클릭스루 ID를 사용하여 사이트 참여를 이해합니다.
* 데이터 또는 픽셀을 광고 서버나 다른 DSP으로 내보낼 때 달성할 수 없는 사용자 지정 지표, 사용자 지정 차원 및 사이트 활동을 사용하여 Analysis Workspace에서 기존의 유료 미디어 보고서를 향상시킵니다.
* Advertising Cloud 내에서 추적 및 최적화를 위해 웹 사이트에 이미 있는 [!DNL Analytics] 코드를 활용할 수 있습니다.

>[!TIP]
>
>  [!DNL Analytics for Advertising Cloud]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html?lang=en#analytics)에 대한 [비디오 소개를 시청하십시오.

## 유료 미디어 보고에 Analytics 사용

[!DNL Analytics for Advertising Cloud] 광고를 통해 사이트 행동을 유도하는 방법에 대한 보고 및 통찰력을 개선하여 다음을 수행할 수 있습니다.

* [!DNL Analytics] 내에서 영구 Advertising Cloud 뷰스루 및 클릭스루 ID를 사용하여 사이트 참여를 이해합니다.
* Analysis Workspace을 활용하여 사이트 시작 지점 및 방문 행동을 더 잘 이해합니다. Advertising Cloud 캠페인 엔티티 이름(배치 및 광고까지)과 클릭, 노출 횟수, 비용 등 관련 지표를 포함하는 유료 미디어 차원 및 이벤트 데이터에 액세스할 수 있습니다.

[!DNL Analytics] 을 유료 미디어 보고 도구로 사용하려면 조직에서 Analysis Workspace에 액세스할 수 있는 Experience Cloud 로그인이 필요합니다. Advertising Cloud 팀이 Advertising Cloud 데이터를 Analysis Workspace의 개별 보고서 세트에 매핑하도록 돕습니다. Advertising Cloud 데이터를 모든 보고서 세트에 보낼 수 있지만, Advertising Cloud에 매핑된 보고서 세트와 매핑하지 않은 보고서 세트가 무엇인지 알고 있어야 합니다. 보고서 세트에 따라 보고된 데이터가 변경될 수 있습니다.

[Advertising Cloud ID [!DNL Analytics]](ids.md) 는 다른 eVar와 마찬가지로 작동하며, 사용자 지정 영구 만료가 적용됩니다. 기본적으로 Advertising Cloud 구현 중 속성 전환 확인 기간은 60일로 설정됩니다. 이 설정을 변경하려면 Adobe 계정 관리자에게 문의하십시오.

Advertising Cloud 차원은 &quot;(AMO ID)&quot; 접미사(예: &quot;광고 유형(AMO ID)&quot;)에 추가됩니다. 사용 가능한 차원 목록은 &quot;[Analysis Workspace의 Advertising Cloud 지표](advertising-cloud-metrics-in-analytics.md)&quot;를 참조하십시오.

>[!NOTE]
>
> [!DNL Analytics] 내에서 Advertising Cloud 데이터(또는 데이터 세트)를 보는 경우 지표와 보고서는 [!DNL Analytics] 내에서 설정된 규칙을 기반으로 합니다. 데이터는 광고 서버 보고서, [!DNL DSP] 보고서 또는 검색 엔진 보고서와 같이 다른 보고 시스템 내에 표시되는 데이터와 다를 수 있습니다. [!DNL Analytics]의 데이터 차이점을 이해하려면 eVar 데이터가 만료되는 시기, 방문을 정의하는 항목, 마지막 터치 속성으로 간주되는 항목 및 총 지속 속성 등을 알고 있어야 합니다. 자세한 내용은 [와 Advertising Cloud](data-variances.md) 간의 예상 데이터 차이를 참조하십시오. [!DNL Analytics] 

## Analytics를 사용하여 Advertising Cloud 캠페인 및 Portfolio 강화

추가 픽셀이 필요하지 않은 경우 다음 두 개의 기본 신호를 Advertising Cloud에 보내어 [!DNL Analytics for Advertising Cloud]을(를) 통해 최적화와 대상 세그멘테이션을 향상시킬 수 있습니다.

* 입찰 신호로 사용할 전환 지표:
   * 표준 지표(예: [!UICONTROL Revenue] 및 [!UICONTROL Cart Views]).
   * 페이지 보기 및 방문 지표와 같은 사이트 참여 지표입니다.
   * 사용자 지정 매출 지표입니다.
   * 예약된 매출 지표.
* 세그먼트는 [!DNL Analytics]에 만들어지고 Experience Cloud에 게시됩니다.

   [!DNL DSP]에서 자사 사이트 재타겟팅 및 유료 검색 광고에 [!DNL Analytics] 세그먼트를 사용할 수 있습니다.

   (Advertising Cloud Search만 해당) [!DNL Analytics] Audience Manager이 없는 광고주는 Experience Cloud과 공유되는 [!DNL Analytics] 세그먼트에서 Google 웹 사이트 태그 기반 대상(리마케팅 목록) 및 고객 일치 대상(고객 목록)을 만들 수도 있습니다.

### 입찰 신호로서의 사이트 전환 지표

[!DNL Analytics]의 표준 이벤트와 사용자 지정 이벤트를 사용하여 Advertising Cloud에서 가중 목표를 빌드할 수 있습니다. 목표는 [!DNL DSP] 패키지 및 검색 포트폴리오에 대한 입찰 결정을 알려줍니다.

>[!NOTE]
>
> [!DNL Analytics]에서 계산된 지표를 Advertising Cloud에 매핑할 수 없습니다.

Advertising Cloud 팀이 유료 미디어 성능에 적용할 수 있는 이벤트를 식별하고 Advertising Cloud에 매핑하도록 도와줍니다. 이 이벤트는 [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Transaction Properties]에 표시됩니다.

사용 가능한 지표 목록은 &quot;[Advertising Cloud의 Analytics 지표](analytics-data-in-advertising-cloud.md)&quot;를 참조하십시오.

### 사이트 재타깃팅을 위한 Analytics 세그먼트

Advertising Cloud은 [!DNL Analytics] 와 Experience Cloud 간의 기본 Experience Cloud 대상 통합을 사용하여 Advertising Cloud DSP 및 [!DNL Search] 광고를 위해 [!DNL Analytics] 세그먼트를 수집할 수 있습니다.

[!DNL Analytics] 세그먼트에 액세스하려면 광고주 계정에 [Experience Cloud ID 서비스](https://experienceleague.adobe.com/docs/id-service/using/home.html)가 활성화되어 있어야 합니다. ID 서비스가 활성화되어 있으면, 모든 Experience Cloud 세그먼트( [!DNL Analytics]에서 생성되고 Experience Cloud에 게시된 세그먼트 포함, Adobe Audience Manager에서 생성된 세그먼트, [!DNL People core service]를 사용하여 Experience Cloud에서 생성된 세그먼트, Adobe Experience Platform에서 만들어 Audience Manager을 통해 Advertising Cloud으로 전송된 세그먼트 포함)가 처리되는 즉시 Advertising Cloud 내에서 사용할 수 있게 됩니다.

[!DNL Analytics] 세그먼트는 24시간 이내에 사용할 수 있으며 매일 업데이트됩니다.

Experience Cloud 대상 서비스에 대한 자세한 내용은 [Experience Cloud 대상](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html)을 참조하십시오.

## 통합 사용 방법의 예

### Analysis Workspace에서 Advertising Cloud 데이터 사용

Advertising Cloud 데이터를 사용하여 Analysis Workspace에서 시각적 보고서를 만드는 방법에 대해 알아보려면 비디오 &quot;[작업 공간 소개 및 보고](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html)&quot;를 참조하십시오.

### Advertising Cloud 대시보드 만들기

Analysis Workspace에서 목표에 대해 Advertising Cloud 데이터를 추적하는 방법을 배우려면 비디오 &quot;[Adobe Analytics](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-dashboards-a4adc.html)로 Advertising Cloud 대시보드 만들기&quot;를 참조하십시오.

### 사이트 시작 분석에 Advertising Cloud ID 사용

Advertising Cloud 사이트 시작 보고서를 만들어 요일, 시간, 브라우저 및 지리적 영향을 모니터링하는 방법을 보려면 비디오 &quot;[Advertising Cloud 사이트 시작 보고서 만들기](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-site-entry-a4adc.html)&quot;를 참조하십시오.

>[!MORELIKETHIS]
>
>* [비디오: 소개 [!DNL Analytics for Advertising Cloud]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html)
>* [구현을 위한 사전 요구 사항 및 주요 정보 [!DNL Analytics for Advertising Cloud]](prerequisites.md)
>* [Analytics에서 사용하는 Advertising Cloud ID](ids.md)
>* [Advertising Cloud용 Analytics용 JavaScript 코드](/help/integrations/analytics/javascript.md)
>* [Advertising Cloud과  [!DNL Analytics] 간의 예상 데이터 분산](data-variances.md)
>* [Analysis Workspace의 Advertising Cloud 지표](/help/integrations/analytics/advertising-cloud-metrics-in-analytics.md)
>* [[!DNL Analytics] Advertising Cloud의 데이터](/help/integrations/analytics/analytics-data-in-advertising-cloud.md)

