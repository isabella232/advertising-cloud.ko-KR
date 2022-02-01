---
title: 수동으로 거래 ID 상세내역 생성
description: 거래 ID에 대한 세부 사항을 수동으로 입력하는 방법을 알아봅니다.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: cd9763a7-99d4-4881-9df9-b4e24c55be0f
source-git-commit: 593bfc03d2dd182b817be9eac4792dfd690132a2
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# 수동으로 거래 ID 상세내역 생성

1. 주 메뉴에서 **[!UICONTROL Inventory]> [!UICONTROL Deals].**

1. 데이터 테이블 위에서 **[!UICONTROL Create]**&#x200B;를 선택한 다음 을 선택합니다. **[!UICONTROL Deal ID]**.

1. 을(를) 입력합니다. [거래 설정](deal-id-settings.md):

   1. 에서 [!UICONTROL Deal ID basics] 섹션에서 거래 세부 사항과 거래에 액세스할 수 있는 광고주를 지정합니다. 보증 거래의 경우 추적 목적으로만 계획된 비행 날짜와 예상 노출 횟수를 지정해야 합니다.

   1. (관리자 사용자만 해당) 선택 사항) [!UICONTROL Technical] 섹션에서 필요에 따라 기본 설정을 편집합니다.

   1. 클릭 **[!UICONTROL Save]**.

1. (보증 계약만) 거래에 사용할 광고를 선택하고 기본 프로그래밍 방식 보장(PG) 배치를 만듭니다.

   기본 PG 배치는 거래가 모든 입찰 요청에 대해 항상 입찰을 반환하도록 합니다. 기본 PG 배치를 만들지 않으면 거래를 타겟팅하는 모든 배치는 올바르게 설정되지 않는 한 입찰을 배치하지 않습니다. 항상 기본 PG 배치를 만들어야 합니다. 에서 [!UICONTROL Placements] 보기, 기본 PG 배치에 [!UICONTROL Sub-type] 열 값: &quot;[!UICONTROL PG Default].&quot;

   원할 경우 추가 배치에서 거래를 재고 타겟으로 사용할 수 있지만, 입찰을 배치하려면 이 거래를 올바로 설정해야 합니다.

   1. 에서 [!UICONTROL Ad & Campaign Selection] 설정에서 거래에 사용할 광고를 선택합니다.

      1. 광고주, 캠페인 및 광고 유형을 선택합니다. 선택적으로 광고를 필터링할 광고 상태를 선택합니다.

      1. 사용 가능한 광고 목록에서 거래에 사용할 각 광고 옆에 있는 확인란을 선택합니다.

      1. 클릭 **[!UICONTROL Apply]**.
   1. 배치 설정 화면에서 다음을 수행합니다.

      1. 배치 이름을 입력합니다.

      1. (선택 사항) [배치 설정](/help/dsp/campaign-management/placements/placement-settings.md)를 덮어쓰는 것을 비롯하여 거래의 CPM 값으로 자동으로 채워지는 기본 입찰을 포함합니다. 날짜 범위 변경 또는 더 많은 광고를 첨부합니다.

      거래는 재고 Target 섹션에서 자동으로 타겟팅됩니다. 다른 모든 타깃팅 선택 사항은 적용할 수 없습니다.

      1. 클릭 **[!UICONTROL Create placement]**.



거래를 생성한 후에는 거래를 여러 배치에 대한 인벤토리 타겟으로 사용할 수 있습니다.

>[!NOTE]
>
> 확인을 위해 거래 태그를 게시자에게 보낼 필요가 없습니다.

>[!TIP]
>
>* 에서 [!UICONTROL Inventory] > [!UICONTROL Deals] 보기, [!UICONTROL Pacing & Budget] 열에는 거래가 지정된 비행 날짜 및 노출 목표까지 걸리는 방식이 표시됩니다.
>
>* 게재 속도가 느려지거나 과게재를 하는 경우, 게재를 통해 보내는 볼륨의 양을 조정하도록 게시자에게 문의하십시오.


>[!MORELIKETHIS]
>
>* [수동 거래 ID 설정](deal-id-settings.md)
>* [프로그래밍 방식 보장 거래 설정](programmatic-guaranteed-set-up.md)
>* [프로그램 방식으로 보장되는 거래를 위한 광고 제출 [!DNL FreeWheel]](freewheel-submit.md)
>* [프로그램 보장 거래 기본 정보](programmatic-guaranteed-about.md)

<!-- >* [Specify Placements and Ads for a Private Deal](deal-id-attach-placements.md)-->