---
title: 패키지 설정
description: 사용 가능한 패키지 설정에 대한 설명을 참조하십시오.
feature: Packages
exl-id: b4d415d1-86a5-40bd-b645-1709b267c174
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '706'
ht-degree: 0%

---

# 패키지 설정

## [!UICONTROL Basic Details]

**[!UICONTROL Name]:** 패키지 이름입니다. 최대 길이는 60자입니다.

**[!UICONTROL Description]**  : (선택 사항) 패키지에 대한 설명입니다.

**[!UICONTROL 3rd Party Billed Fees]:**  (선택 사항) 청구 불가능한 비용으로 추적할 정적 타사 비용입니다.

>[!NOTE]
>
>청구 가능한 수수료는 [!UICONTROL Net CPM] 지표에 반영됩니다.
* **[!UICONTROL CPM]:** 노출 1,000건당 비용(CPM)입니다.

* **[!UICONTROL CPM Description]:** CPM 비용에 대한 설명입니다.

[배치 수준](/help/dsp/campaign-management/placements/placement-settings.md)에서 패키지 수준 설정을 재정의할 수 있습니다.

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]:** (기존 패키지의 읽기 전용) 패키지에서 배치 및 상한에 지정할 수준:

* **[!UICONTROL Package level pacing]** : 이 간격 전략은 포함된 모든 배치를 그룹으로 간격 및 캡핑하여  *작동합니다*. 이 전략은 주어진 패키지 내의 모든 배치가 전체적으로 최적화되어 성능 및 규모에 따라 비용을 선택한 주요 성과 지표(KPI)로 분배합니다.

* **[!UICONTROL Placement level pacing]**  : 이 간격 전략은 포함된 모든 배치를 개별적으로 간격 및 캡핑하여  *작동합니다*. 가장 좋은 방법은 이 전략을 사용하여 보장된 비공개 시장 거래를 실행하는 것입니다.

**[!UICONTROL Flight Dates]** : 패키지의 시작 날짜 및 종료 날짜입니다.

선택적으로 패키지에 대한 짝수 간격 이외 항공편을 생성하려면 *[!UICONTROL *Activate Custom Flighting]**를 선택하고 아래 [!UICONTROL Flighting] 섹션에서 사용자 지정 항공편을 설정합니다. 사용자 지정 기능을 활성화하고 패키지를 저장하면 사용자 지정 조명을 비활성화할 수 없습니다.

>[!NOTE]
>
>* 비행 날짜는 캠페인 비행 날짜 내에 포함되어야 합니다. 또한 이 패키지에 할당된 모든 배치에 대한 비행 날짜는 이 날짜 내에 포함되어야 합니다.
> * 사용자 정의 조명이 활성화된 경우 패키지 시작 날짜를 편집할 수 없습니다.


**[!UICONTROL Budget]** : (패키지 수준 간격 전용 패키지) 총 예산 상한 및 예산 간격.

사용자 정의 조명이 있는 패키지의 경우 예산 간격은 항상 *[!UICONTROL All time]*&#x200B;입니다. 사용자 정의 기능을 사용하지 않는 패키지의 경우 예산 간격을 지정합니다. *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* 또는 *[!UICONTROL Weekly]*

**[!UICONTROL Gross Budget]** : (패키지 수준 간격 및 동적 마진 관리만 사용하는 패키지) 패키지 기간 동안의 총 예산 상한

**[!UICONTROL Optimization Goal]**  : (패키지 수준 간격 만 있는 패키지) 패키지에 대한 최적화 목표입니다. [최적화 목표 및 사용 방법](/help/dsp/optimization/optimization-goals.md)에서 각 최적화 목표에 대한 설명을 참조하십시오.

**[!UICONTROL Custom Goals]:** (사용자 지정 최적화 목표만 있는 패키지) 패키지 [에 ](/help/dsp/optimization/custom-goal-about.md) 대한 사용자 지정 목표입니다. 사용자 지정 목표 및 캠페인을 사용하는 우수 사례에 대한 자세한 내용은 [사용자 지정 목표 작성 우수 사례](/help/dsp/optimization/custom-goal-best-practices.md) 및 [성능 캠페인 설정 우수 사례](/help/dsp/optimization/campaign-best-practices-performance.md)를 참조하십시오.

**[!UICONTROL Package Goal Type]:** (사용자 지정 최적화 목표만 있는 패키지) 패키지의 목적입니다. 이 설정은 패키지를 최적화하는 방법을 결정하는 데 도움이 됩니다.

* *[!UICONTROL Prospecting]:* 대상 패키지는 신규 고객 획득에 중점을 둡니다.

* *[!UICONTROL Retargeting]* : 패키지를 다시 타겟팅하는 것은 이전 방문자 또는 고객을 다시 노출하는 데 중점을 둡니다.

* *[!UICONTROL Other]:* 기타 모든 목적.

**[!UICONTROL Linked Package for Optimization Learnings Carryover]:** (사용자 지정 최적화 목표만 있는 패키지) 기록 데이터가 패키지 최적화를 위해 입력으로 사용되는 다른 패키지입니다.

**[!UICONTROL Target]**  : (패키지 수준 간격 만 있는 패키지) 성과를 추적하는 데 사용되는 대상 목표입니다.

>[!NOTE]
>
>이 필드는 벤치마크일 뿐이며 의사 결정에 사용되지 않습니다.

**[!UICONTROL Frequency Cap]**  : (패키지 수준 게재 전용인 패키지) 고유한 장치 또는 사람(지정된 내용에 따라)이 패키지에서 광고를 제공할 수  [!UICONTROL Cross Device Level]있는 횟수입니다. 옵션에는 *[!UICONTROL Unlimited]* 또는 일, 주 또는 개월당 특정 금액이 포함됩니다.

>[!NOTE]
>
>* 캠페인, 패키지 및 배치 수준에서 빈도 캡을 설정할 수 있습니다. DSP은 캠페인 계층에서 가장 엄격한 빈도 제한을 준수합니다.
>* 가장 좋은 방법은 패키지 수준에서 잠재 고객 및 재타겟팅 모두에 대한 주파수 캡을 설정하는 것입니다.
> * 빈도 캡이 높을수록 소비와 노출이 높지만 도달 범위가 감소합니다. 빈도가 낮아지면 소비와 노출이 낮아지지만 도달 범위가 늘어납니다.


**[!UICONTROL Pace on]:** (패키지 수준 게재 전용인 패키지) 게시의 기반이 되는 사항:

* *[!UICONTROL Budget]:*  (기본값) 이 옵션은 할당된 패키지 예산 내에서 가능한 한 많은 노출 횟수를 제공합니다.

* *[!UICONTROL Impressions]:* 이 옵션은 지정된 간격에 도달할 때까지 노출 횟수를 전달합니다. 이 옵션을 선택하면 노출 횟수 및 간격을 지정합니다. *모든 시간,* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* 또는 *[!UICONTROL Weekly]*

**[!UICONTROL Pacing Fill Strategy]:** (패키지 수준 게재 전용 패키지) 광고 게재 속도를 높이는 방법:

* *[!UICONTROL Even]* : 첫 번째 비행 시에는 50%의 배달 목표를 가지고, 각 비행 내내 균일하게 전달을 지연합니다.

* *[!UICONTROL Slightly Ahead]:* (기본값) 55~65%가 비행 지속 기간의 절반을 완료하도록 게재를 가속화합니다.

* *[!UICONTROL Frontload]:* 5~75%가 비행 중간에 완료되도록 배달 속도를 높입니다.

* *[!UICONTROL Aggressive Frontload]:* 75-85%가 비행 중간에 완료되도록 전송을 가속화합니다.

## [!UICONTROL Flighting]

(패키지 수준 간격 및 &quot;[!UICONTROL Activate Custom Flighting]&quot;이 활성화된 패키지) [!UICONTROL Goals & Budget] 섹션에 지정된 전체 [!UICONTROL Flight Dates] 내 사용자 지정 비행 기간.

각 비행에 대해 시작 날짜, 종료 날짜 및 타겟 노출 횟수를 입력합니다. 다른 비행을 추가하려면 **[!UICONTROL Add Flight]** 을 클릭하십시오.

>[!MORELIKETHIS]
>
>* [패키지 관리 정보](package-about.md)
>* [패키지 만들기](package-create.md)
>* [패키지 편집](package-edit.md)
>* [패키지에 배치 첨부](package-attach-placement.md)
>* [Campaign 관리에 대한 FAQ](/help/dsp/campaign-management/campaign-management-faq.md)

