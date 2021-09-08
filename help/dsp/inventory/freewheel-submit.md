---
title: PG 거래에 대한 광고를 [!DNL FreeWheel]에 제출합니다.
description: FreeWheel의 게시자와 프로그래밍 방식으로 보장되는 거래를 위한 광고 승인을 요청하는 방법을 알아봅니다.
feature: Private Inventory, Deal IDs
exl-id: null
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# FreeWheel에 프로그램 방식으로 보장되는 거래를 위한 광고 제출

*프로그래밍  [!DNL FreeWheel] 보증 권한만 있는 계정*

광고를 선택하고 거래에 사용할 프로그래밍 방식으로 보장되는 기본 배치를 만드는 것을 포함하여 [FreeWheel](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox)에 있는 게시자와 프로그래밍 방식으로 보장되는 거래를 수락하면, 승인을 위해 FreeWheel에 광고를 제출해야 합니다.

>[!PREREQUISITES]
>
>Adobe 계정 팀과 협력하여 [!DNL DSP] 계정에 [!DNL FreeWheel] 프로그래밍 방식 보장 워크플로우를 사용할 수 있는 권한이 있는지 확인합니다.

1. FreeWheel 거래와 함께 사용되는 광고의 광고 키를 복사합니다.

   1. 캠페인 이름을 클릭합니다.

   1. 하위 메뉴에서 **[!UICONTROL Ads]** 을 클릭합니다.

   1. 광고 이름 옆에 있는 **[!UICONTROL ...]>[!UICONTROL Edit]** 를 클릭합니다.

   1. 광고 설정이 열리면 브라우저의 주소 표시줄에 표시되는 URL에 영숫자 광고 키를 복사합니다.

      예를 들어 다음 URL에서 광고 키는 `3NtNC5ZbaGZtqbei8jD3`입니다

      `https://advertising.adobe.com/configurator/ad/3NtNC5ZbaGZtqbei8jD3?referrer=/playtime/ads`

1. FreeWheel에 광고를 제출합니다.

   1. [!UICONTROL Deals] 보기에서 거래를 찾습니다.

   1. 거래 행에서 ![옵션 메뉴](/help/dsp/assets/options-menu.png) **[!UICONTROL submit to [!DNL FreeWheel]]**&#x200B;를 클릭합니다.

   1. 거래 ID를 확인하고 1단계에서 복사한 **[!UICONTROL Ad Key]** 을 입력한 다음 **[!UICONTROL Submit]** 를 클릭합니다.

   광고가 실행되기 전에 광고를 제출하고 승인해야 합니다.

1. [광고 제출 상태를 확인합니다](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [FreeWheel에서 프로그래밍 방식 보장 거래 설정 개요](freewheel-overview.md)
>* [거래 ID 받은 편지함에서 거래 수락](deal-id-inbox-accept.md)
>* [프로그램 보장 거래에 대한 광고  [!DNL FreeWheel] 상태 확인](freewheel-check-status.md)
>* [FreeWheel 광고 제출 오류 코드](freewheel-error-codes.md)

