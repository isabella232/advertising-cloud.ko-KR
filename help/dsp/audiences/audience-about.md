---
title: Advertising Cloud DSP의 대상 관리 정보
description: 고객 관리 기능에 대해 알아봅니다.
feature: Audiences, Segments
exl-id: 624d2211-59a2-4791-b8f1-a9a5cecd0b8e
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '1026'
ht-degree: 0%

---

# Advertising Cloud DSP의 대상 관리 정보

Advertising Cloud DSP에서 배치 대상으로 사용할 수 있는 대상 세그먼트 및 대상 세트를 만들고 관리할 수 있습니다.

* 세그먼트를 만들고 구현하여 자신의 자사 대상 데이터를 수집할 수 있습니다. 나중에 광고를 사용하여 세그먼트의 사용자를 다시 타겟팅하거나 세그먼트의 사용자가 광고를 받지 못하도록 할 수 있습니다. 다음 유형의 세그먼트를 만들 수 있습니다.

   * [사용자 ](/help/dsp/audiences/custom-segment-create.md) 지정 세그먼트 를 사용하여 a) 데스크탑, 모바일 및 CTV 장치에서 광고에 노출되는 사용자 및 b) 특정 웹 페이지를 방문하는 사용자.

   * [CCPA(](/help/dsp/audiences/ccpa-opt-out-segment-create.md) California Consumer Privacy Act)에 따라 웹 사이트의 소비자 판매 중지 요청에서 사용자 ID를 추적하기 위한 판매 중지 세그먼트입니다. 판매 중지 요청에서 사용자 ID의 월별 보고서를 검색할 수 있습니다.

      CCPA 판매 중지 요청에 대한 Advertising Cloud 지원에 대한 자세한 내용은 [캘리포니아 소비자 개인 정보 보호법 Adobe Advertising Cloud 지원 을 참조하십시오. 소비자 옵트아웃 지원](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html).

* [재사용 가능한 대상](/help/dsp/audiences/reusable-audience-create.md)의 대상 라이브러리를 만들 수 있습니다. 저장된 대상은 사용 가능한 대상 세그먼트와 다른 저장된 대상으로 구성됩니다. 저장된 대상에 대한 모든 변경 사항은 대상을 타깃팅하거나 제외하는 모든 배치와 저장된 대상을 포함하는 다른 모든 대상에 자동으로 적용됩니다.

   저장된 대상을 사용하면 미디어 플래너가 복잡한 부울 논리를 사용하여 여러 세그먼트를 포함하거나 제외하여 필요에 따라 대상을 그룹화할 수 있습니다. 대상을 작성할 때 각 개별 세그먼트의 크기와 총 대상 크기가 표시됩니다. 그런 다음 캠페인 실행자는 각 배치에 대한 대상 대상을 수동으로 구성하는 대신 저장된 대상을 배치 타겟으로 한 개 이상 선택하면 됩니다.

추가적인 대상 유형도 배치 타깃팅에 사용할 수 있습니다.

## 자사 및 타사 데이터 세그먼트 가져오기

Advertising Cloud DSP은 DMP(데이터 관리 플랫폼)에서 자사 데이터 세그먼트를 가져와서 필요에 따라 모든 광고주에게 제공할 수 있습니다.

Advertising Cloud DSP은 타사 세그먼트의 복잡한 조합을 포함하여 사용자 지정 타사 세그먼트를 가져올 수도 있습니다. 필요에 따라 모든 광고주 세트에 세그먼트를 제공할 수 있습니다.

자세한 내용은 계정 관리자에게 문의하십시오.

## 배치 Target으로 사용할 수 있는 대상

배치를 다음 모든 유형의 대상으로 타깃팅할 수 있습니다.

* Advertising Cloud DSP에 저장된 사용자가 만든 모든 대상 세트입니다.

* Advertising Cloud DSP에서 만들어진 모든 사용자가 만든 대상 세그먼트:

   * 특정 웹 페이지를 방문한 사용자와 특정 광고의 노출에 노출된 사용자를 위한 사용자 지정 세그먼트입니다.

   * CCPA(California Consumer Privacy Act)에 따라 웹 사이트에서 판매 중지 요청을 제출한 사용자를 위한 CCPA 판매 중지 대상 세그먼트.

* 가져온 모든 자사 데이터 세그먼트입니다.

* 가져온 모든 사용자 지정 타사 데이터 세그먼트입니다.

* (미국만 타깃팅하는 배치) [Advertising Cloud DSP 고객이 사용할 수 있는 모든 타사 데이터 세그먼트로서, 여기에는 [!DNL Acxiom], [!DNL Datalogix], [!DNL eXelate]([!DNL Nielsen]), [!DNL Lotame], [!DNL Oracle], [!DNL Quantcast] 등이 포함됩니다.](/help/dsp/audiences/third-party-data-providers.md)

   대상 데이터를 기반으로 사용자를 타깃팅하는 특정 세그먼트를 타깃팅할 수 있습니다(예: 특정 인구 통계, 관심 또는 의도를 갖는 사용자 및/또는 행동 프로필). 데이터 제공업체 및 카테고리별로 찾아보고, 이름 또는 세그먼트 ID별로 세그먼트를 검색하거나, 데이터 제공업체, 총 세그먼트 크기, 웹 브라우저 수 또는 장치 수로 결과를 필터링할 수 있습니다.

   타사 세그먼트는 각 세그먼트 이름 옆에 표시되는 추가 비용을 발생시킵니다.

* (Advertising Cloud JavaScript 변환 태그만 사용하는 Adobe Experience Cloud, Adobe Audience Manager 또는 Adobe Analytics이 있는 광고주) Adobe Experience Cloud에서 만들어진, Audience Manager에서 만들었거나, Audience Manager 또는 [!DNL Analytics]에서 Adobe Experience Cloud에 게시된 모든 사용 가능한 자사, 보조 또는 타사 대상 세그먼트.

   세그먼트 사용에 대한 가격은 미리 협상되며 Advertising Cloud에서 볼 수 없습니다.  <!-- Verify -->

   Adobe Experience Cloud에서 세그먼트를 만들거나 게시한 후 약 1시간 후에 Adobe Experience Cloud의 세그먼트를 사용할 수 있습니다. Audience Manager에서 직접 오는 세그먼트는 만든 후 약 24시간 후에 사용할 수 있습니다. <!-- Verify all -->

   >[!NOTE]
   >
   >해당 솔루션의 세그먼트에 대한 데이터를 설정하고 수집하는 방법에 대한 자세한 내용은 [Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html), [Analytics](https://experienceleague.adobe.com/docs/analytics/landing/home.html) 및 [Adobe Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html)에 대한 설명서를 참조하십시오.

## 대상 크기 데이터

저장된 대상 설정 및 배치 설정 내에서 자세한 대상 크기 데이터를 볼 수 있습니다.

* 선택한 모든 세그먼트와 저장된 대상에 대한 총 및 활성 중복 제거된 대상 크기가 표시되며, 장치 유형(브라우저, 모바일 또는 연결된 TV)별로 세부 사항을 볼 수 있습니다.

   ![결합된 대상 크기](/help/dsp/assets/audience-size.png)

* 개별 세그먼트 및 저장된 대상의 경우, 세그먼트 이름 옆에 총 대상 크기 및 CPM(해당되는 경우)이 표시됩니다. 장치 유형(브라우저, 모바일 또는 연결된 TV)별 크기를 포함하여 세그먼트에 대한 자세한 내용을 볼 수 있습니다. 저장된 대상의 경우, 총 크기는 중복 제거된 합계입니다.

   ![개별 세그먼트 크기](/help/dsp/assets/audience-size-segment.png)

## 대상 보기

### 모든 대상 보기

[!UICONTROL All Audiences] 보기 또는 대상 라이브러리에서는 대상 세그먼트 그룹과 다른 저장된 대상을 포함하는 재사용 가능한 대상을 저장하고 관리할 수 있습니다. 대상을 여러 배치의 타겟으로 사용할 수 있습니다. 각 대상이 사용되는 배치 수는 배치 이름 옆에 표시됩니다.

대상을 편집, 복제, 삭제, 내보내기 또는 공유할 수 있습니다.

### 세그먼트 보기

[!UICONTROL Segments] 보기에서 모든 사용자가 추가 사용자 지정 세그먼트를 만들 수 있습니다.

[!UICONTROL Segments] 보기에는 다음 세그먼트 유형이 나열됩니다.

* 사용자가 만든 모든 사용자 지정 세그먼트를 사용자가 사용할 수 있습니다.

   만든 사용자 지정 세그먼트에 대한 추적 태그를 보고 이러한 세그먼트를 다른 사용자와 공유할 수 있습니다. 만든 사용자 지정 세그먼트를 편집하거나 삭제할 수도 있습니다.

   다른 사용자가 사용자와 공유한 사용자 지정 세그먼트를 편집하거나 공유할 수 없습니다.

* 사용자가 사용할 수 있는 가져온 모든 자사 세그먼트.

   사용자와 공유된 자사 세그먼트는 편집하거나 공유할 수 없습니다. 추가 사용자와 자사 세그먼트를 공유해야 하는 경우 계정 관리자에게 문의하십시오.

* 사용자가 사용할 수 있는 모든 사용자 지정 타사 세그먼트.

   사용자와 공유된 타사 세그먼트는 편집하거나 공유할 수 없습니다. 추가 사용자와 타사 세그먼트를 공유해야 하는 경우 계정 관리자에게 문의하십시오.

>[!MORELIKETHIS]
>
>* [재사용 가능한 대상 만들기](reusable-audience-create.md)
>* [대상 설정](audience-settings.md)
>* [대상 세그먼트 논리 구문](audience-segment-logic-syntax.md)
>* [사용자 지정 세그먼트 만들기 및 구현](custom-segment-create.md)
>* [세그먼트 만들기 및  [!UICONTROL CCPA Opt-Out-of-Sale] 구현](ccpa-opt-out-segment-create.md)
>* [사용 가능한 타사 데이터 공급자](third-party-data-providers.md)
>* [배치 설정](/help/dsp/campaign-management/placements/placement-settings.md)

