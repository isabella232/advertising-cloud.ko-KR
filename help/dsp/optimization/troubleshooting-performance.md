---
title: 성능 문제 해결
description: 일반적인 성능 문제를 참조하고 문제를 해결하는 방법을 참조하십시오.
feature: DSP Optimization
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---

# 성능 문제 해결

| 문제 | 가능한 원인 | 수행할 작업 |
| --- | --- | --- |
| 배치에 드는 비용 없음 | 게재에 광고가 포함되지 않거나 광고가 활성화되지 않습니다. | 모든 예상 광고가 게재에 첨부되고 승인되고 활성화되어 있는지 확인합니다.<br><br>또한 게재에 각 광고에 대한 비행 기간을 제한할 수 있는 사용자 지정 광고 일정이 포함되어 있는지 확인합니다. 배치 보기에서 배치에 대한 광고 일정을 보려면  **[!UICONTROL ...]>[!UICONTROL Ad schedule]** 배치 이름 옆에 표시됩니다. |
|  | 영향을 받는 날짜가 구성된 비행 날짜 내에 없습니다. | 플라이트 날짜가 캠페인, 패키지 및 배치 수준에서 유효한지 &#x200B; 확인합니다. |
|  | 예산 목표가 달성되었거나 너무 낮습니다. | 캠페인, 패키지 및 배치 수준에서 예산 설정을 확인합니다. |
|  | 그 계좌에는 자금이 충분하지 않다. | 계정이 적절히 자금 조달되는지 확인하려면 다음 위치로 이동하십시오. **[!UICONTROL Settings]>[!UICONTROL Account]** 그리고 [!UICONTROL Usable Funds]. 자금을 더 추가해야 하는 경우 [!DNL Adobe] 계정 팀입니다. |
|  | 사용 가능한 재고가 없습니다. | 지정된 재고 출처([!UICONTROL Public], [!UICONTROL Private], 또는 [!UICONTROL On Demand]):<ul><li>올바르게 설정합니다.</li><li>경매를 통해 활성 및 전송</li><li>적용 가능한 광고 및 배치 유형과 호환됩니다.</li></ul><br>재고 출처가 모두 유효하고 활성 상태인 경우, 가능한 경우 추가 또는 모든 재고 출처를 타깃팅합니다. |
|  | 사용 가능한 사용자가 없습니다. | 지정된 대상 타겟에 충분한 활성 사용자가 포함되어 있는지 확인합니다. 그렇지 않으면 대상을 더 추가하여 타겟을 확장합니다. |
| 배치 비용 절감 | 다음 [!UICONTROL Non Bids] 배치 진단 보고서의 섹션에는 배치에 입찰하지 않은 가능한 이유가 표시됩니다. | [를 검토합니다. [!UICONTROL Non Bids] 보고서](/help/dsp/campaign-management/reports/placement-diagnostics.md) 게재가 입찰되지 않은 이유를 이해하기 위해 노력했습니다.  <!-- add link/edit text when file available: See the [in-depth guide to possible Non-Bid Reasons (NBR)](link) for more information. --> |
|  | 배치는 을 사용합니다 [사전 입찰 필터](/help/dsp/campaign-management/placements/placement-settings.md) 그건 입찰을 제한하는 거죠 | 사전 입찰 필터의 임계값을 5%까지 낮추어 소비와 성과 균형을 평가합니다. <!-- wording? and are users just supposed to manually monitor whether it makes a difference? --><br><br>사전 입찰 필터, 지역, 재고 및 대상과 같은 여러 배치 타겟을 사용하면 입찰과 지출을 누적 제한할 수 있습니다. |
|  | 그 배치는 승률이 낮다. | 를 늘립니다 [!UICONTROL Max Bid] 승률을 높이기 위해<br><br><b>참고:</b> 재고 가격은 배치 타겟팅에 따라 다를 수 있습니다.<br><br>10%의 승률은 건강하다고 여겨진다. |
|  | 적은 수의 재고가 있습니다. | 가능한 경우 추가 또는 모든 재고 출처를 Target 합니다.<br><br>사전 입찰 필터, 지역, 재고 및 대상과 같은 여러 배치 타겟을 사용하면 입찰과 지출을 누적 제한할 수 있습니다. |
|  | 사용 가능한 사용자 수가 적습니다. | 지정된 대상 타겟에 충분한 활성 사용자가 포함되어 있는지 확인합니다. 그렇지 않으면 대상을 더 추가하여 타겟을 확장합니다.<br><br>사전 입찰 필터, 지역, 재고 및 대상과 같은 여러 배치 타겟을 사용하면 입찰과 지출을 누적 제한할 수 있습니다. |
|  | 패키지에는 많은 활성 배치가 포함되어 있습니다. | 패키지 내의 활성 배치 수를 줄이거나 전체 패키지 예산을 늘리십시오.<br><br>패키지에 배치가 많지만 예산이 충분하지 않은 경우, DSP에서 각 배치에 충분한 예산을 할당하지 못할 수 있습니다. 각 배치에는 최소 2USD/요일을 사용할 수 있는 기회가 있어야 합니다. 예를 들어, 패키지에 USD/하루 10달러의 예산이 있는 경우 5개 이하의 배치를 포함하는 것이 가장 좋습니다. &#x200B; |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [배치 설정](/help/dsp/campaign-management/placements/placement-settings.md)
>* [패키지 설정](/help/dsp/campaign-management/packages/package-settings.md)
>* [캠페인 설정](/help/dsp/campaign-management/campaigns/campaign-settings.md)

