---
title: 사용 사례
description: Advertising DSP 미디어 데이터를 Audience Manager과 공유하는 사용 사례에 대해 알아봅니다
feature: Integration with Adobe Audience Manager
exl-id: 21d80cf6-f817-495a-bae4-fc9e44f1eda4
source-git-commit: ad4ab8b9b0a4b5b1cc4aab540900363d2fe671c2
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 0%

---

# Adobe Audience Manager에서 미디어 노출 데이터 캡처를 위한 사용 사례

*Advertising DSP만 사용하는 광고주*

*Adobe Advertising-Adobe Audience Manager 통합 전용 광고주*

다음은 Advertising DSP 미디어 노출 데이터를 캡처하여 이점을 얻을 수 있는 몇 가지 방법입니다 <!-- ad impression data? --> Audience Manager에서 확인하십시오.

## 최신성 및 빈도 관리

Audience Manager에서 노출 횟수 데이터를 캡처하면 특정 광고 또는 캠페인에 노출된 사용자 세그먼트를 만들어 빈도 관리를 향상시킬 수 있습니다. 빈도를 증가시키려는 경우 또는 빈도를 제한하려는 경우 광고 제외에 이러한 세그먼트를 사용할 수 있습니다.

또한, Audience Manager 사용 [!DNL Segment Builder]를 적용할 수 있습니다 [최신성 및 빈도 제어](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/recency-and-frequency.html) 다음 중 [규칙 기반 특성](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) 에는 실행 가능한 신호가 포함되어 있습니다. 예를 들어 미디어 캠페인 내에서 특정 크리에이티브를 사용자에게 표시하는 횟수를 제한할 수 있습니다. 읽기 &quot;[즉각적인 장치 간 억제](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/instant-cross-device-suppression.html)&quot;를 클릭하여 방법을 알아보십시오.<!-- The AM pulled this paragraph verbatim from AEM doc; I change only a word or two. -->

## 순차적 메시징

노출 데이터를 캡처하여 캠페인이나 광고에 노출된 사용자 세그먼트를 만들고 이 세그먼트를 순차적 메시징 또는 억제에 사용할 수 있습니다. 예를 들어 크리에이티브를 본 사용자를 재타겟팅할 수 있습니다 `123` 그러나 클릭 또는 전환은 창의적으로 표시되지 않았습니다 `456`.

Audience Manager에서 이 예를 실행하려면 다음 단계를 수행합니다.<!-- The AM pulled this example/procedure verbatim from AEM doc; I changed only a word or two. -->

1. 크리에이티브를 본 사용자를 캡처할 트레이트를 만듭니다.

   예를 들어 트레이트의 이름을 지정하려면 `Creative Trait 123`, 다음 트레이트 규칙을 사용합니다.

   `d_creative == 123 AND d_event == imp`

1. 클릭하거나 변환하는 사용자를 캡처하기 위한 트레이트를 만듭니다.

   예를 들어 이 트레이트의 이름을 지정하려면 `Click and Converter`, 다음 트레이트 규칙을 사용합니다.

   `d_event == click OR d_event=conv`

1. 라는 세그먼트를 만듭니다. `Retarget Users` creative를 본 사용자를 채우기 위해 `123` 그러나 클릭하거나 전환하지 않았습니다. 다음 트레이트 규칙을 사용합니다.

   `Creative Trait 123 AND NOT Click and Converter`

1. 세그먼트 매핑 `Retarget Users` 대상을 대상으로 타깃팅하고 대상을 창의적으로 사용하여 사용자를 타깃팅합니다 `456`.

## [!DNL Adobe Audience Analytics] 및 캠페인 노출 데이터

Audience Manager 내에서 캠페인 노출 및 클릭 데이터를 사용할 수 있게 되면 특정 캠페인이나 전술에 노출되거나 상호 작용한 사용자의 트레이트 및 세그먼트를 만들 수 있습니다. 다음 포함 [[!DNL Audience Analytics] 통합](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html), Audience Manager 세그먼트를 [!DNL Analytics] 추가 분석. 가능한 사용 사례는 다음과 같습니다.

* **DSP과 간의 상호 작용 분석 [!DNL Adobe Advertising Search] 광고:** 표준 [[!DNL Analytics for Advertising] 통합](/help/integrations/analytics/overview.md) 은 DSP과 [!DNL 간의 상호 작용에 대한 통찰력을 제공하지 않습니다 [!DNL Search]] 두 채널 모두 AMO ID 속성 규칙을 따르는 AMO ID를 사용하므로 검색 클릭이 디스플레이 뷰스루를 재정의합니다. Audience Manager에서 DSP 노출 세그먼트를 만들면 [!DNL Audience Analytics] DSP과 [!DNL 간의 상호 작용을 분석하려면 [!DNL Search]] [!DNL Analytics].

* **빈도 분석:** 사용자가 특정 광고 또는 캠페인에 몇 번이나 노출되었는지를 기준으로 Audience Manager에서 세그먼트를 만들 수 있습니다. 그런 다음 Analytics에서 다른 노출 세그먼트를 분석하여 DSP 노출 수에 따라 사용자 동작이 어떻게 변경되는지 확인할 수 있습니다.

## [!DNL Audience Optimization Reports]

활용할 수 있습니다 [Audience Manager [!DNL Audience Optimization Reports]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-reports.html) 캠페인 내 세그먼트에 대한 잠재적 성능 기회를 식별하기 위해 이 보고서는 캠페인 노출, 클릭 및 전환 데이터를 세그먼트 지표와 결합하여 세그먼트 중심의 최적화 및 효과적인 채널 혼합을 알려줍니다.

### 관련 Audience Optimization 보고서 유형

| 보고서 | 설명 |
| ------ | ----------- |
| [[!UICONTROL Segment Performance] 보고서](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/segment-performance.html) | 노출 횟수 및 전환율에 따라 매핑된 세그먼트와 매핑되지 않은 세그먼트를 비교합니다. |
| [[!UICONTROL Trend Analysis and Volume Analysis] Reports]9https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/trend-analysis-volume-analysis.html) | 다양한 광고 차원에 대한 노출 횟수, 클릭스루 비율 및 전환 시 데이터를 반환합니다. |
| [[!UICONTROL Optimal Frequency] 보고서](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/optimal-frequency.html) | 제공된 노출 수와 전환 수 간의 최적의 균형을 찾는 데 도움이 됩니다. 이 기능을 사용하면 감소 결과를 보기 전에 표시할 노출 횟수를 조정할 수 있습니다. |
| [[!UICONTROL Unique User Reach] 보고서](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/unique-user-reach.html) | 각 버블의 크기가 선택한 차원에 대한 고유한 사용자 수와 직접 비례하여 표시되는 버블 차트입니다. |

### 고려 사항

* If [!DNL Audience Optimization Reports] 사용자에게 역할 기반 액세스 제어(RBAC)가 있는 다음 [!DNL Adobe Customer Care] 광고주 ID와 조직의 Audience Manager 데이터 소스 통합 코드 간의 매핑을 구성해야 합니다. 그런 다음 관리자 사용자는 다른 사용자에게 RBAC 권한을 제공할 수 있습니다.

* 의 전환 보고 [!DNL Audience Optimization Reports] 최종 사용자가 일부 설정을 필요로 합니다. 메타데이터 파일을 채워야 합니다.

* [!DNL Audience Optimization Reports] 은 캠페인 메타데이터에 대한 변경(예: 캠페인 이름 또는 배치 이름)을 지원하지 않습니다.

* 검색 광고에 대한 클릭은 [!DNL Audience Optimization Reports] 노출 횟수와 상관 관계가 있는 경우에만 해당됩니다. 즉, 검색 클릭은 노출 후 전환으로 처리됩니다. 따라서 많은 검색 클릭이 [!DNL Audience Optimization Reports].

>[!MORELIKETHIS]
>
>* [Adobe Audience Manager에 DSP Media Exposure 데이터 보내기 개요](overview.md)
>* [Advertising DSP 캠페인에서 클릭 및 노출 데이터 수집](collect.md)

