---
title: PG 거래에 대한 광고 제출 대상 [!DNL FreeWheel]
description: 게시자와 프로그래밍 방식으로 보장되는 거래를 위한 광고 승인을 요청하는 방법을 알아봅니다. [!DNL Freewheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 6cb41f3b-29e4-4feb-9c31-578ab40bd4f7
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# 프로그래밍 방식의 보장 거래에 대한 광고를 제출합니다. [!DNL Freewheel]

*을 사용하는 계정 [!DNL FreeWheel] 프로그래밍 방식의 보장 권한만 해당*

일단 [FreeWheel의 게시자와 프로그램 방식으로 보장되는 거래를 수락합니다.](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox)광고를 선택하고 거래에 사용할 프로그래밍 방식으로 보장되는 기본 배치를 만드는 것을 포함하여, 광고에 를 제출해야 합니다. [!DNL Freewheel] 승인용.

>[!PREREQUISITES]
>
>Adobe 계정 팀과 협력하여 [!DNL DSP] 계정에 사용할 수 있는 권한이 있습니다. [!DNL FreeWheel] 프로그래밍 방식으로 보장되는 워크플로우입니다.

1. 와 함께 사용되는 광고의 광고 키를 복사합니다. [!DNL Freewheel] 거래:

   1. 캠페인의 이름을 클릭합니다.

   1. 하위 메뉴에서 **[!UICONTROL Ads]**.

   1. 클릭  **[!UICONTROL ...]>[!UICONTROL Edit]** 광고 이름 옆에 표시됩니다.

   1. 광고 설정이 열리면 브라우저의 주소 표시줄에 표시되는 URL에 영숫자 광고 키를 복사합니다.

      예를 들어 다음 URL에서 광고 키는 다음과 같습니다 `3NtNC5ZbaGZtqbei8jD3`

      `https://advertising.adobe.com/configurator/ad/3NtNC5ZbaGZtqbei8jD3?referrer=/playtime/ads`

1. 에 광고 제출 [!DNL Freewheel]:

   1. 다음 중 하나를 수행합니다.

      * 광고 이름 옆에 있는 를 클릭합니다.  **[!UICONTROL ...]** > **[!UICONTROL submit to FreeWheel]**.

      * 주 메뉴에서 **[!UICONTROL Inventory]** > **[!UICONTROL Deals]**. 거래 행에서 ![옵션 메뉴](/help/dsp/assets/options-menu.png) > **[!UICONTROL submit to FreeWheel]**.
   1. 거래 ID를 확인하고 를 입력합니다. **[!UICONTROL Ad Key]** 1단계에서 복사한 다음 **[!UICONTROL Submit]**.

   광고가 실행되기 전에 광고를 제출하고 승인해야 합니다.

1. [광고 제출 상태를 확인합니다](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [프로그램 보장 거래 설정 개요 [!DNL Freewheel]](freewheel-overview.md)
>* [거래 ID 받은 편지함에서 거래 수락](deal-id-inbox-accept.md)
>* [광고 상태 확인 [!DNL FreeWheel] 프로그램 방식의 보장 거래](freewheel-check-status.md)
>* [에 대한 오류 코드 [!DNL Freewheel] 광고 제출](freewheel-error-codes.md)

