---
title: 개요 [!DNL Analytics for Advertising Cloud]
description: 개요 [!DNL Analytics for Advertising Cloud]
feature: Integration with Adobe Analytics
exl-id: 31367c8b-3410-4110-9ae6-11defe625355
source-git-commit: b40c6f08b94e546e5fc068c46b279292a4d8a14f
workflow-type: tm+mt
source-wordcount: '1086'
ht-degree: 0%

---

# 개요 [!DNL Analytics for Advertising Cloud]

*Advertising Cloud DSP 및 Advertising Cloud Search을 사용하는 광고주*

[!DNL Analytics for Advertising Cloud] Adobe Analytics과 Adobe Advertising Cloud을 통합하여 각 제품의 기능을 확장하고 개선합니다.

통합을 통해 광고주는 해당 사이트에서 클릭스루 및 뷰스루 사이트 상호 작용을 추적할 수 있습니다 [!DNL Analytics] 예를 들어 기업이 광고 비용을 어떻게 사이트 참여와 중요한 비즈니스 목표에 도달하는지 파악할 수 있습니다.

또한 Advertising Cloud은 [!DNL Analytics] 를 사용하여 수집 [!DNL Analytics] 태그는 이미 사이트에 있습니다. 이를 통해 보다 강력한 여정 관리, 자사 리마케팅 및 유료 미디어 사이트 보고를 수행할 수 있습니다. Advertising Cloud은 [!DNL Analytics] 비용 및 입찰 최적화를 위한 데이터.

제대로 채용되면 [!DNL Analytics for Advertising Cloud] 에서는 두 가지 기존 역할 사이의 줄을 흐리게 합니다. 광고 여정 관리(광고를 통해 사용자를 사이트에 보내는 작업) 및 웹 분석을 통해 해당 사이트 참여를 파악합니다.

주요 이점:

* 보내기 [!DNL Analytics] 자사 사이트 리마케팅을 위해 세그먼트를 Advertising Cloud에 바로 연결할 수 있습니다.
* 사용 [!DNL Analytics] 유료 미디어 광고를 최적화하기 위한 전환 신호로서의 사용자 지정 및 표준 이벤트.
* 활용 [!DNL Analytics] Analysis Workspace 를 사용하여 사이트 시작 지점 및 방문 동작을 더 잘 이해할 수 있습니다.
* 웹 분석가와 유료 미디어 팀 간의 긴밀한 공동 작업을 가능하게 합니다.
* 내에서 영구 Advertising Cloud 뷰스루 및 클릭스루 ID 사용 [!DNL Analytics] 사이트 참여를 이해하도록 했습니다.
* 데이터 또는 픽셀을 광고 서버나 다른 DSP으로 내보낼 때 달성할 수 없는 사용자 지정 지표, 사용자 지정 차원 및 사이트 활동을 사용하여 Analysis Workspace에서 기존의 유료 미디어 보고서를 향상시킵니다.
* 활용 [!DNL Analytics] Advertising Cloud 내에서 추적 및 최적화를 위해 웹 사이트에 이미 코드가 있습니다.

>[!TIP]
>
> 보기 [비디오 소개 [!DNL Analytics for Advertising Cloud]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html?lang=en#analytics).

## 유료 미디어 보고에 Analytics 사용

[!DNL Analytics for Advertising Cloud] 광고를 통해 사이트 행동을 유도하는 방법에 대한 보고 및 통찰력을 개선하여 다음을 수행할 수 있습니다.

* 내에서 영구 Advertising Cloud 뷰스루 및 클릭스루 ID 사용 [!DNL Analytics] 사이트 참여를 이해하도록 했습니다.
* Analysis Workspace을 활용하여 사이트 시작 지점 및 방문 행동을 더 잘 이해합니다. Advertising Cloud 캠페인 엔티티 이름(배치 및 광고까지)과 클릭, 노출 횟수, 비용 등 관련 지표를 포함하는 유료 미디어 차원 및 이벤트 데이터에 액세스할 수 있습니다.

를 사용하려면 [!DNL Analytics] 유료 미디어 보고 도구로서, 조직은 Analysis Workspace에 대한 액세스 권한을 사용하여 Experience Cloud 로그인이 필요합니다. Advertising Cloud 팀이 Advertising Cloud 데이터를 Analysis Workspace의 개별 보고서 세트에 매핑하도록 돕습니다. Advertising Cloud 데이터를 모든 보고서 세트에 보낼 수 있지만, Advertising Cloud에 매핑된 보고서 세트와 매핑하지 않은 보고서 세트가 무엇인지 알고 있어야 합니다. 보고서 세트에 따라 보고된 데이터가 변경될 수 있습니다.

[내의 Advertising Cloud ID [!DNL Analytics]](ids.md) 는 다른 eVar와 마찬가지로 사용자 지정 및 영구 만료와 함께 작동합니다. 기본적으로 Advertising Cloud 구현 중 속성 전환 확인 기간은 60일로 설정됩니다. 이 설정을 변경하려면 [!DNL Adobe] 계정 팀입니다.

Advertising Cloud 차원은 &quot;(AMO ID)&quot; 접미사(예: &quot;광고 유형(AMO ID)&quot;)에 추가됩니다. 참조:[Analysis Workspace의 Advertising Cloud 지표](advertising-cloud-metrics-in-analytics.md)사용 가능한 차원 목록에 대해 &quot;을 참조하십시오.

>[!NOTE]
>
> 내에서 Advertising Cloud 데이터(또는 데이터 세트)를 보는 경우 [!DNL Analytics]지표와 보고서는 내에서 설정된 규칙을 기반으로 합니다 [!DNL Analytics]. 데이터는 광고 서버 보고서와 같은 다른 보고 시스템 내에 표시되는 데이터와 다를 수 있습니다. [!DNL DSP] 보고서 또는 검색 엔진 보고서. 의 데이터 차이점을 파악하려면 [!DNL Analytics], eVar 데이터가 만료되는 시기, 방문을 정의하는 항목, 마지막 터치 기여도 및 총 유지 기여도 분석으로 간주되는 항목 등을 알고 있어야 합니다. 자세한 내용은 [다음 사이 예상되는 데이터 분산 [!DNL Analytics] 및 Advertising Cloud](data-variances.md).

## Analytics를 사용하여 Advertising Cloud 캠페인 및 Portfolio 강화

추가 픽셀을 필요로 하지 않고 [!DNL Analytics for Advertising Cloud] Advertising Cloud에 두 개의 기본 신호를 보내어 보다 나은 최적화와 더 쉬운 대상 세그멘테이션을 가능하게 합니다.

* 입찰 신호로 사용할 전환 지표:
   * 표준 지표(예: ) [!UICONTROL Revenue] 및 [!UICONTROL Cart Views].
   * 페이지 보기 및 방문 지표와 같은 사이트 참여 지표입니다.
   * 사용자 지정 매출 지표입니다.
   * 예약된 매출 지표.
* 에서 만들어진 세그먼트 [!DNL Analytics] Experience Cloud에 게시되었습니다.

   다음을 사용할 수 있습니다 [!DNL Analytics] 의 자사 사이트 재타겟팅을 위한 세그먼트 [!DNL DSP] 그리고 유료 검색 광고입니다.

   (Advertising Cloud Search만 해당) [!DNL Analytics] 그러나 Audience Manager은 다음 방법으로 Google 웹 사이트 태그 기반 대상(리마케팅 목록)과 고객 일치 대상(고객 목록)을 만들 수도 없습니다 [!DNL Analytics] Experience Cloud과 공유되는 세그먼트.

### 사이트 전환 지표를 입찰 신호로 사용

에서 표준 이벤트와 사용자 지정 이벤트를 사용할 수 있습니다. [!DNL Analytics] Advertising Cloud에서 가중 목표를 빌드하려면 다음을 수행하십시오. 목표에 대한 입찰 결정 정보를 제공합니다. [!DNL DSP] 패키지 및 검색 포트폴리오.

>[!NOTE]
>
> 계산된 지표는 [!DNL Analytics] Advertising Cloud으로 전환합니다.

Advertising Cloud 팀은 유료 미디어 성능에 적용할 수 있는 이벤트를 식별하고 Advertising Cloud에 매핑하는 데 도움을 줍니다. 이 이벤트는에 표시됩니다 [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Transaction Properties].

참조:[Advertising Cloud의 Analytics 지표](analytics-data-in-advertising-cloud.md)사용 가능한 지표 목록에 대해 &quot;을 참조하십시오.

### 사이트 재타깃팅을 위한 Analytics 세그먼트

Advertising Cloud에서 수집할 수 있음 [!DNL Analytics] Advertising Cloud DSP을 위한 리마케팅 목적의 세그먼트 [!DNL Search] 광고 사이에 기본 Experience Cloud 대상 통합을 사용하여 광고 [!DNL Analytics] 및 Experience Cloud.

에 액세스하려면 [!DNL Analytics] 세그먼트이면 광고주 계정에는 [Experience Cloud ID 서비스](https://experienceleague.adobe.com/docs/id-service/using/home.html) 활성화되었습니다. ID 서비스가 활성화되어 있으면 모든 Experience Cloud 세그먼트( [!DNL Analytics] 세그먼트를 만들어 Experience Cloud에 게시, Adobe Audience Manager에서 만든 세그먼트, 를 사용하여 Experience Cloud에서 만든 세그먼트 [!DNL People core service], Adobe Experience Platform에서 만들고 Audience Manager을 통해 Advertising Cloud으로 보낸 세그먼트)는 처리되는 즉시 Advertising Cloud 내에서 사용할 수 있게 됩니다.

[!DNL Analytics] 세그먼트는 24시간 이내에 사용할 수 있으며 매일 업데이트됩니다.

Experience Cloud 대상 서비스에 대한 자세한 내용은 [Experience Cloud 대상](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## 통합 사용 방법의 예

### Analysis Workspace에서 Advertising Cloud 데이터 사용

Advertising Cloud 데이터를 사용하여 Analysis Workspace에서 시각적 보고서를 만드는 방법에 대해 알아보려면 비디오 &quot;[작업 공간 및 보고 소개](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html).&quot;

### Advertising Cloud 대시보드 만들기

Analysis Workspace에서 목표에 대해 Advertising Cloud 데이터를 추적하는 방법을 배우려면 비디오 &quot;[Adobe Analytics을 사용하여 Advertising Cloud 대시보드 만들기](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-dashboards-a4adc.html).&quot;

### 사이트 시작 분석에 Advertising Cloud ID 사용

Advertising Cloud 사이트 시작 보고서를 만들어 주별, 시간별, 브라우저 및 지리적 영향을 모니터링하는 방법을 보려면 비디오 &quot;[Advertising Cloud 사이트 시작 보고서 만들기](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-site-entry-a4adc.html).&quot;

>[!MORELIKETHIS]
>
>* [비디오: 소개 [!DNL Analytics for Advertising Cloud]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html)
>* [구현을 위한 사전 요구 사항 및 주요 정보 [!DNL Analytics for Advertising Cloud]](prerequisites.md)
>* [Analytics에서 사용하는 Advertising Cloud ID](ids.md)
>* [Advertising Cloud용 Analytics용 JavaScript 코드](/help/integrations/analytics/javascript.md)
>* [다음 사이 예상되는 데이터 분산 [!DNL Analytics] 및 Advertising Cloud](data-variances.md)
>* [Analysis Workspace의 Advertising Cloud 지표](/help/integrations/analytics/advertising-cloud-metrics-in-analytics.md)
>* [[!DNL Analytics] Advertising Cloud의 데이터](/help/integrations/analytics/analytics-data-in-advertising-cloud.md)

