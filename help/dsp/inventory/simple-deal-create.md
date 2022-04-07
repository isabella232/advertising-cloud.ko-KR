---
title: '"만들기 [!UICONTROL Simple Ad Serving] 거래"'
description: 에 대한 추적 픽셀을 만드는 방법을 알아봅니다. [!UICONTROL Simple Ad Serving] "그래."
feature: DSP Simple Ad Serving
exl-id: d8de85ec-616c-44ed-9a1a-cc25713ad4a4
source-git-commit: 3eb63e9d7161c354736ce53ee21518882c541884
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# 만들기 [!UICONTROL Simple Ad Serving] 거래

1. 주 메뉴에서 **[!UICONTROL Inventory]> [!UICONTROL Deals].**

1. 데이터 테이블 위에서 **[!UICONTROL Create]**&#x200B;를 선택한 다음 을 선택합니다. **[!UICONTROL Simple Ad Serving]**.

1. 을(를) 입력합니다. [거래 설정](simple-deal-settings.md):

   1. 에서 [!UICONTROL Select Ad Source] 섹션에서 게시자, 광고주, 캠페인 및 광고 유형에 대한 정보를 지정한 다음 를 클릭합니다 **[!UICONTROL Next]**.

   1. 에서 [!UICONTROL Select Ad(s)] 섹션에서 DSP에서 프록시로 사용할 광고를 지정합니다.

      1. 다음 중 하나를 수행합니다.

         * 기존 광고의 경우 사용할 광고를 선택합니다.

         * 새 광고의 경우 프록시를 만듭니다 [타사 광고](/help/dsp/campaign-management/ads/ad-create-multiple.md).
      >[!NOTE]
      > DSP은 사용자가 지정하는 광고를 실제로 제공하지 않습니다. 게시자가 광고를 제공할 것입니다.

      1. 클릭 **[!UICONTROL Next]**.
   1. 피드 세부 정보에서 피드 세부 사항을 편집한 다음 를 클릭합니다 **[!UICONTROL Next]**.

      Advertising Cloud DSP은 자동으로 &quot;SAS Placement - &lt;*거래 이름*>,&quot;로 표시되어야 합니다. 배치에서 거래는 자동으로 [!UICONTROL Inventory Targets] 섹션을 참조하십시오. 다른 모든 타깃팅 선택 사항은 적용할 수 없습니다.



1. 다음 방법 중 하나로 구현을 위해 이벤트 추적 픽셀을 게시자에게 보냅니다.

   * (선택 사항) [!UICONTROL Activate Tag with Publisher] 화면에서 거래 태그를 게시자에게 보냅니다.

      이전 단계를 완료하면 DSP에서 게시자에게 보낼 수 있는 이메일 메시지를 생성합니다. 이 메시지에는 거래 세부 사항, 거래 태그를 검색할 링크 및 링크에 대한 인증 코드가 포함되어 있습니다.

      1. 거래 상세내역을 검토하고 다음 중 하나를 수행합니다.

         * 정보를 장치의 이메일 애플리케이션에 붙여넣으려면 **[!UICONTROL Email & Done]** 이메일 애플리케이션을 선택합니다. 다음 [!UICONTROL CC:] 필드는 [!DNL Adobe] 지원 주소. 그런 다음 게시자를 위한 적절한 담당자에게 메시지를 보낼 수 있습니다.

         * 클립보드에 정보를 복사하려면 **[!UICONTROL Copy Email].** 그런 다음 콘텐츠를 수동으로 전자 메일 메시지에 붙여넣고 게시자를 위한 적절한 연락처로 보낼 수 있습니다. 에 사본(참조:)을 포함해야 합니다 `publisher-support-global@adobe.com`. 메시지 복사를 마치면 를 클릭합니다. **[!UICONTROL Email & Done]**.
      1. (필요한 경우) 게시자와 함께 태그에는 게시자의 광고 서버에서 태그가 작동되도록 적절한 매크로가 포함되어 있는지 확인합니다.
   * (선택 사항) 이벤트 추적 픽셀을 게시자에게 수동으로 전송합니다.

      1. 거래 행에서 [!UICONTROL Deals] 보기, ![옵션 메뉴](/help/dsp/assets/options-menu.png) **>[!UICONTROL show pixel]**.

         이벤트 픽셀에는 [!UICONTROL Clickthrough] 픽셀 및 [!UICONTROL Impression] 픽셀. 비디오 및 오디오 광고에는 사분위별 완료된 이벤트 픽셀(부터)도 포함됩니다. [!UICONTROL 25% Complete] to [!UICONTROL 100% Complete]).

      1. 이벤트 추적 픽셀을 복사하여 게시자에게 제공합니다.



>[!MORELIKETHIS]
>
>* [정보 [!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* [[!UICONTROL Simple Ad Serving] 설정](simple-deal-settings.md)
>* [이벤트 추적 픽셀 보기 [!UICONTROL Simple Ad Serving] 거래](simple-deal-show-pixels.md)

