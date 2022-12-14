---
title: 배치 만들기
description: 배치를 만드는 방법을 알아봅니다.
feature: DSP Placements
exl-id: 4e37b571-9af4-4897-bff2-035a5f2600a5
source-git-commit: cb77fd450db1798f190f3b6eb51054553440bac9
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 1%

---

# 배치 만들기

>[!TIP]
>
>특정 캠페인 목표 또는 보고 요구 사항에 따라 배치를 만들 수 있습니다.

1. 주 메뉴에서 **[!UICONTROL Campaigns]**.

1. 배치가 포함될 캠페인의 이름을 클릭합니다.

1. 데이터 테이블 위에서 **[!UICONTROL Create]**. 에서 [!UICONTROL Placement Types] 메뉴의 섹션에서 배치 유형을 클릭합니다.

   배치 유형은 배치에 포함할 수 있는 광고 유형을 결정합니다.

1. 을(를) 입력합니다. [배치 설정](placement-settings.md):

   1. 을(를) 지정합니다. [!UICONTROL Basics] 설정.

   1. 에서 [!UICONTROL Goals] 섹션에서 [!UICONTROL Gross Budget] 추가 배치 목표를 지정할 수도 있습니다.

      일부 필드에는 재정의할 수 있는 기본값이 있습니다.

      배치가 할당된 패키지에 패키지 수준 게시가 있는 경우 목표 및 게재 설정에 패키지 설정이 반영됩니다.

   1. (선택 사항)에서 [!UICONTROL Geo-Targeting] 섹션을 통해 포함 또는 제외된 위치를 좁힙니다.

      특정 위치를 식별하지 않으면 모든 위치가 타깃팅됩니다.

      >[!NOTE]
      >
      >도시 및 DMA 위치는 Roku 배치에 사용할 수 없습니다.

   1. 에서 [!UICONTROL Inventory Targeting] 섹션에서 포함 또는 제외할 재고 소스의 범위를 좁힙니다.

      대부분의 배치 유형의 경우, 모든 재고 유형 및 각 유형의 모든 소스가 기본적으로 포함됩니다. 대상 [!DNL Roku] 배치, 재고 유형 및 소스를 지정해야 합니다.

   1. (선택 사항)에서 [!UICONTROL Site Targeting] 섹션에서 타겟팅할 사이트 범위를 좁히고 제외할 사이트를 모두 지정합니다.

   1. (선택 사항)에서 [!UICONTROL Audience Targeting] 섹션:

      1. 대상자 범위를 좁힙니다. 여기에는 배치 내에서 타겟팅할 대상 세그먼트 선택도 포함됩니다.

         대상 [!DNL] Roku 배치를 활용할 수 있습니다 [DSP 고유 대상 일치 [!DNL Roku]](/help/dsp/inventory/roku-inventory.md) 에 대해 일치시킬 수 있는 하나 이상의 대상 세그먼트를 포함함으로써 [!DNL Roku] (옵트인) 결정적 데이터 세트.
   1. (사람 수준 교차 장치 타겟팅이 있는 캠페인의 경우) 선택 사항) 배치가 하나 이상의 특정 대상을 타깃팅하는 경우 배치에 대해 사용자 기반 교차 장치 타깃팅을 활성화합니다.

      사용자 기반 교차 장치 타깃팅은 [!DNL LiveRamp] 사용. 이 서비스는 모든 광고주가 CPM $0.35로 를 사용하여 게재되는 노출에 사용할 수 있습니다 [!DNL LiveRamp] 장치 그래프(즉, 타깃팅된 대상 세그먼트 내에 없는 장치의 경우).

   1. (선택 사항)에서 [!DNL Brand Safety and Media Targeting] 섹션에서 배치에 대한 브랜드 안전 제한 사항을 적용합니다.

   1. (선택 사항)에서 [!DNL Tracking] 섹션에서 배치에 광고의 타사 이벤트 픽셀 또는 변환 픽셀을 입력합니다.

      >[!NOTE]
      >
      >([!DNL Roku] 배치) [!DNL Roku] 포함 [!DNL Acxiom], [!DNL comScore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk], 및 [!DNL Research Now].


1. 클릭 **[!UICONTROL Create Placement]**.

1. (선택 사항) 배치에 광고를 추가합니다.

   1. 클릭 **[!UICONTROL Attach an ad]**.

   1. 다음 중 하나를 수행합니다.
   * 새 광고를 만들려면 다음을 수행하십시오.

      1. 클릭 **[!UICONTROL Create a New Ad].**

      1. 에 대한 광고 설정을 지정합니다 [오디오 광고](/help/dsp/campaign-management/ads/ad-settings-audio.md), [연결된 TV](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md), [디스플레이 광고](/help/dsp/campaign-management/ads/ad-settings-display.md), [모바일 광고](/help/dsp/campaign-management/ads/ad-settings-mobile.md), [기본 광고](/help/dsp/campaign-management/ads/ad-settings-native.md), [프리롤 광고](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md), 또는 [범용 비디오 광고](ad-settings-universal-video.md).

      1. 클릭 **[!UICONTROL Save & Submit for Review]**.

      1. (선택 사항) 배치에 대해 만들려는 각 추가 광고에 대해 를 클릭합니다 **[!UICONTROL Attach Another Ad]**, 그런 다음 1-3단계를 반복합니다.

      1. 기존 광고를 첨부하지 않으려면 **[!UICONTROL I'm done for now]**.
   * 캠페인에 기존 광고를 첨부하려면

      1. 클릭 **[!UICONTROL Select an Ad]**.

      1. 다음 중 하나를 수행합니다.

         * 한 번에 한 개의 광고를 추가하려면:

            1. 광고 이름 옆에 있는 를 클릭합니다. **[!UICONTROL Select].**

            1. (선택 사항) 첨부할 각 추가 광고에 대해 **[!UICONTROL Attach Another Ad]**&#x200B;를 호출한 다음 프로세스를 반복합니다.
         * 한 번에 최대 20개의 광고를 추가하려면:

            1. 광고 목록 위에 있는 확인란을 선택합니다.

            1. 추가할 각 광고 옆에 있는 확인란을 선택합니다.

            1. 클릭 **[!UICONTROL Attach]**.

            1. 광고 이름 옆에 있는 를 클릭합니다. **[!UICONTROL Select]**.
      1. (선택 사항) 배치에서 특정 광고에 대한 기본 플라이트 기간 및 광고 순환을 무시하려면 다음을 수행합니다.

         1. 클릭 **[!UICONTROL Custom Schedule Ads]**.

         1. 다음 중 하나를 수행합니다.

            * 플라이트 추가 **[!UICONTROL Add Flight]**, 그런 다음 시작 날짜 및 종료 날짜를 지정합니다.

            * 기존 플라이트 를 광고에 추가하려면 **[!UICONTROL +]** 를 입력합니다.

            * 광고에서 기존 비행을 제거하려면 **[!UICONTROL x]** 를 입력합니다.

            * (여러 광고에 동일한 플백이 있는 경우) 광고를 균일하지 않게 회전하려면 **[!UICONTROL Even Rotation]** 플라이트 정보에서 각 광고를 회전할 상대적 가중치를 백분율로 입력합니다.

               총 가중치는 100이어야 합니다.
         1. 오른쪽 상단에서 **[!UICONTROL Continue]**.

         1. 플라이트 세부 사항을 검토한 다음 **[!UICONTROL Save & Finish]**.






>[!MORELIKETHIS]
>
>* [배치 관리 정보](placement-about.md)
>* [배치 편집](placement-edit.md)
>* [배치에 대한 광고 일정 편집](placement-edit-ad-schedule.md)
>* [배치 일시 중지 또는 활성화](placement-pause-activate.md)
>* [배치에 대한 변경 로그 보기](placement-change-log.md)
>* [배치 설정](placement-settings.md)
>* [키보드 단축키](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)

   >*[성능 문제 해결](/help/dsp/optimization/troubleshooting-performance.md)
>* [비디오: 표준 디스플레이 배치를 만드는 방법](https://video.tv.adobe.com/v/340454)

