---
title: 배치 진단 보고서 보기
description: 배치 설정 및 간격 관련 문제를 진단하는 방법을 알아봅니다.
feature: DSP Placements
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# 배치 진단 보고서 보기

<!-- Does this really belong in the Campaign Management > Reports section or in the Placements section? -->

다음 도구를 사용하면 캠페인이 활성화되면 배치 설정 및 간격 관련 문제를 진단할 수 있습니다.

* **[!UICONTROL Change Log]:** 이름, 상태 및 최대 입찰과 같은 주요 배치 설정에 대한 변경 사항을 표시합니다. 각 항목에는 변경한 사람의 날짜 및 사용자 이름이 포함됩니다.
* **[!UICONTROL Ad Approvals]:** 인벤토리 공급자가 광고를 승인했는지 또는 거부했는지 여부를 표시합니다. 선택적으로 광고 상태를 변경하거나(예: 거부된 광고 일시 중지) 광고 설정을 열 수 있습니다.
* **[!UICONTROL Non Bids]:** DSP이 배치에 입찰하지 않은 이유를 표시합니다.

1. 진단 보고서를 엽니다.
   1. 배치 설정을 엽니다.
      1. 주 메뉴에서 **[!UICONTROL Campaigns]**.
      1. 캠페인 이름을 클릭한 다음 **[!UICONTROL Placements]**.
      1. 배치 이름 옆에 있는 를 클릭합니다  **[!UICONTROL ...]>[!UICONTROL Edit]**.
   1. 오른쪽 상단에서 ![배치 진단](/help/dsp/assets/placement-diagnostics.png) 또는 **[!UICONTROL Diagnostic]**.
1. 다음 중 하나를 수행합니다.
   * 변경 로그를 보려면
      1. 클릭 **[!UICONTROL Change Log]**.
      1. (선택 사항) 보고서 결과를 필터링합니다.
         * 날짜 메뉴에서 보고서 기간을 기본 최근 14일에서 다른 기간( )으로 변경합니다.*[!UICONTROL Last 30 days],* *[!UICONTROL Last 60 days],* *[!UICONTROL Last 90 days],* 또는 *[!UICONTROL Last 1 year]*).
         * 왼쪽 메뉴에서 특정 사용자 이름으로 보고서를 필터링합니다.
         * 오른쪽 메뉴에서 특정 배치 설정별로 보고서를 필터링합니다.
   * 광고 승인 상태를 보려면
      1. 오른쪽 상단에서 **[!UICONTROL Ad Approvals]**.
      1. (선택 사항) 광고를 일시 중지하거나 활성화하려면 상태 스위치(![상태 스위치](/help/dsp/assets/status-switch.png))을 클릭하여 제품에서 사용할 수 있습니다.
      1. (선택 사항) 광고에 대한 설정을 열려면 를 클릭합니다 **[!UICONTROL View Ad]** 광고 옆에 표시됩니다.
   * DSP이 배치에 입찰하지 않은 이유를 확인하려면:
      1. 오른쪽 상단에서 **[!UICONTROL Non Bids]**.
      1. (선택 사항) 날짜 범위를 변경하려면 날짜 필드를 클릭하고 다른 날짜 또는 날짜 범위를 선택합니다.

<!-- Later, add link to >* Definitions for NBRs (Reading No Bid Reports (NBRs)) -->

>[!MORELIKETHIS]
>
>* [플랫폼 내 보고서 정보](campaign-reports-about.md)
>* [배치 설정](/help/dsp/campaign-management/placements/placement-settings.md)

