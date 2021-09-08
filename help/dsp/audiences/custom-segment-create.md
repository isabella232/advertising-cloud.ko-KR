---
title: 사용자 지정 세그먼트 만들기 및 구현
description: 웹 페이지를 방문하는 광고나 사용자에게 노출된 사용자를 추적하기 위해 사용자 지정 세그먼트를 만들고 구현하는 방법을 알아봅니다.
feature: Segments
exl-id: 691903e2-773e-4205-837e-822f435f57a7
source-git-commit: e2ee41c7e3e195f062ad1cc67080ed913d6d3d06
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---

# 사용자 지정 세그먼트 만들기 및 구현

사용자 지정 Advertising Cloud 세그먼트를 만들고 구현하여 자신만의 자사 대상 데이터를 수집할 수 있습니다. 세그먼트를 사용하여 a) 데스크탑, 모바일 및 CTV 장치에서 광고에 노출되는 사용자 및 b) 특정 웹 페이지를 방문하는 사용자를 추적할 수 있습니다. 나중에 추가 광고를 사용하여 세그먼트의 사용자를 재타겟팅하거나 세그먼트의 사용자가 추가 광고를 받지 못하도록 할 수 있습니다.

>[!NOTE]
>
>CCPA(California Consumer Privacy Act)에 따라 웹 사이트의 소비자 판매 중지 요청에서 사용자 ID를 추적하려면 [CCPA 판매 중지 세그먼트](ccpa-opt-out-segment-create.md)를 만듭니다.

1. 세그먼트를 만듭니다.

   1. 주 메뉴에서 **[!UICONTROL Audiences]>[!UICONTROL Segments]** 를 클릭합니다.

   1. 데이터 테이블 위에서 **[!UICONTROL Create]** 을 클릭합니다.

   1. 고유한 **[!UICONTROL Segment Name]** 을 입력합니다.

   1. [!UICONTROL Segment Type]에 대해 **[!UICONTROL Custom]**&#x200B;을 선택합니다.

   1. 세그먼트 창을 입력합니다. 세그먼트 창은 사용자의 쿠키가 세그먼트에 남아 있는 일수입니다.

      기본 창은 45일입니다. 1부터 365까지의 값을 입력합니다.

   1. 클릭 **[!UICONTROL Save]**.

1. 필요에 따라 태그를 복사하여 세그먼트를 추적합니다.

   1. **[!UICONTROL Audiences]>[!UICONTROL Segments]**&#x200B;로 돌아갑니다.

   2. 세그먼트 행 위에 커서를 놓고 **[!UICONTROL Get pixel]** 를 클릭합니다.

      * 데스크탑 및 모바일 웹 페이지 방문자를 추적하려면

         1. &quot;[!UICONTROL Desktop or mobile websites]&quot; 레이블이 지정된 페이지 보기 추적 태그를 복사합니다.

         1. 배포를 위해 광고주 또는 웹 사이트 담당자에게 태그를 제공합니다.

            광고주의 IT 부서나 다른 그룹은 태그 배포를 예약하거나 알려주어야 할 수 있습니다.
      * 데스크탑, 모바일 또는 CTV 장치에서 광고 단위에 노출된 사용자를 추적하려면 다음을 수행하십시오.

         1. &quot;[!UICONTROL Desktop or mobile ads]&quot; 레이블이 지정된 노출 추적 태그를 복사합니다.

         1. 광고에 대한 [!UICONTROL Pixel] 탭에 태그를 추가합니다. <!-- I'll add cross-reference to ad settings later. -->


추적 태그가 구현되면 대상 타겟의 세그먼트를 사용하거나 배치를 위해 제외를 사용할 수 있습니다.

>[!TIP]
>
>사용자가 추적될 때 세그먼트 크기를 추적합니다.

>[!MORELIKETHIS]
>
>* [대상자 관리 기본 정보](audience-about.md)
>* [세그먼트 만들기 및  [!UICONTROL CCPA Opt-Out-of-Sale] 구현](ccpa-opt-out-segment-create.md)
>* [재사용 가능한 대상 만들기](reusable-audience-create.md)
>* [대상 설정](audience-settings.md)
>* [사용 가능한 타사 데이터 공급자](third-party-data-providers.md)
>* [배치 설정](/help/dsp/campaign-management/placements/placement-settings.md)

<!-- I'll add x-ref to ad settings later.-->
