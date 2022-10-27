---
title: 중복 배치
description: 하나 이상의 배치를 복제하는 방법을 알아봅니다.
feature: DSP Placements
exl-id: d22a61a8-4f1b-41ee-b4fb-3124bec81a2f
source-git-commit: 5ed402a7c83072a7af6a06757050486c6d7d7080
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# 중복 배치

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

유사한 설정으로 배치를 만들려면 하나 이상의 배치를 복제합니다. 다음을 수행할 수 있습니다.

* 배치의 여러 중복 만들기
* 원래 광고주와 캠페인 내에 또는 다른 광고 내에서 배치가 중복됩니다
* (원래 캠페인 내에 중복된 배치의 경우) 선택적으로 원본 광고를 복제합니다
* 새 배치의 상태 및 플라이트 날짜를 수정합니다

참조:[복제되지 않은 사항](#placement-not-duplicated)중복되지 않은 배치 설정 목록입니다.

1. 주 메뉴에서 **[!UICONTROL Campaigns]**.
1. 캠페인의 이름을 클릭합니다.
1. 하위 메뉴에서 **[!UICONTROL Placements]**.
1. 다음 중 하나를 수행합니다.
   * 한 배치를 복제하려면 를 클릭합니다  **[!UICONTROL ...]>[!UICONTROL Duplicate]** 패키지 이름 옆에 있는 를 클릭합니다.
   * 여러 배치를 복제하려면
      1. 복제할 각 배치 옆에 있는 확인란을 선택합니다.
      1. 벌크 작업 도구 모음에서 **[!UICONTROL Duplicate]**.
1. 새 배치 설정을 지정합니다.
   1. (단일 배치) 새 배치 이름을 입력합니다.
   1. 에서 **[!UICONTROL Choose Package (Required)]** 메뉴에서 상위 패키지 또는 ** 중 하나를 선택합니다[!UICONTROL No package]*.
   1. (선택 사항) 기본 설정을 변경합니다.

   이 설정은 선택한 모든 배치에 적용됩니다.

   기본적으로 새 배치는 원래 광고 유형에 대해 배치되며, 원래 광고주와 캠페인에 할당되며, 현재 날짜에 시작하고, 일시 중지되고, 원래 광고를 포함하지 않는 플라이트 일정을 갖습니다.

   여러 배치를 만들 때 새 배치 이름은 &lt;*original_placement_name #N*>(예: &quot;내 배치 #2&quot;).

1. 클릭 **[!UICONTROL Submit]**.

## 복제되지 않은 사항 {#placement-not-duplicated}

다음을 제외하고 원래 배치의 모든 설정이 복제됩니다.

* 실험 설정
* (플라이트 날짜를 변경하는 경우) 사용자 지정 광고 예약
* (광고를 첨부하지 않는 경우) 사용자 지정 광고 가중치 및 예약
* 의 프로그래밍 방식 보장(PG) 거래 및 배치에 대한 기본 배치 [!UICONTROL Simple Ad Serving] 거래
* (배치를 다른 캠페인에 복사하는 경우):
   * 지역 타겟
   * 이벤트 픽셀
   * 광고
   * 배치 수준 [!DNL DoubleVerify Authentic Brand Safety] 세그먼트(광고주 수준 세그먼트를 재정의하는 세그먼트)

>[!MORELIKETHIS]
>
>* [배치 관리 정보](placement-about.md)
>* [배치 만들기](placement-create.md)
>* [배치 편집](placement-edit.md)
>* [배치에 대한 변경 로그 보기](placement-change-log.md)
>* [배치 설정](placement-settings.md)

