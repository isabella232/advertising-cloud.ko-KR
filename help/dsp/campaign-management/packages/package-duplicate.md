---
title: 패키지 복제
description: 패키지를 복제하는 방법을 알아봅니다.
feature: DSP Packages
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---

# 패키지 복제

유사한 설정으로 패키지를 만들려면 패키지를 복제합니다. 다음을 수행할 수 있습니다.

* 원래 광고주 및 캠페인 내 또는 다른 광고 내에서 패키지를 복제합니다
* 원할 경우 패키지 내에서 배치를 복제합니다
* (원래 캠페인 내에 중복된 패키지가 있는 경우) 원본 광고와 배치 수준 이벤트 픽셀을 선택적으로 복제합니다
* 새 패키지의 플라이트 날짜 수정

참조:[복제되지 않은 사항](#package-not-duplicated)중복되지 않은 배치 설정 목록입니다.

1. 주 메뉴에서 **[!UICONTROL Campaigns]**.

1. 캠페인 이름을 클릭하여 캠페인 [!UICONTROL Packages] 보기.

1. 패키지 이름 옆의  **[!UICONTROL ...]>[!UICONTROL Duplicate]**.

1. 새 패키지 설정을 지정합니다.

   1. 새 패키지 이름을 입력합니다.

   1. (선택 사항) 기본 설정을 변경합니다.

      기본적으로

      * 새 패키지는 원래 광고주 및 캠페인에 할당됩니다.

      * 새 패키지가 현재 날짜에 활성화됩니다.<!-- and the flight continues for NN  days. -->

      * 원래 패키지 내의 배치는 새 패키지에 복사됩니다.

      * 광고 및 배치 수준 이벤트 픽셀이 새 패키지에 복사되지 않습니다.

1. 클릭 **[!UICONTROL Submit]**.

## 복제되지 않은 사항 {#package-not-duplicated}

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
>* [패키지 관리 정보](package-about.md)
>* [패키지 만들기](package-create.md)
>* [패키지 편집](package-edit.md)
>* [패키지에 대한 변경 로그 보기](package-change-log.md)
>* [패키지 설정](package-settings.md)

