---
title: Advertising Cloud DSP의 캠페인 관리 개요
description: Campaign 관리 계층 및 구성 요소에 대해 알아봅니다.
feature: DSP Packages, DSP Placements, DSP Ads
exl-id: c94e08d0-0dd5-4cf9-8df2-9eb4c591375c
source-git-commit: 19d6a2edf07eecf874537dd9d356737ed9156bd9
workflow-type: tm+mt
source-wordcount: '359'
ht-degree: 0%

---

# Advertising Cloud DSP의 캠페인 관리 개요

Advertising Cloud DSP 캠페인에는 다음 계층이 있습니다.

* 캠페인
   * 패키지
      * 배치
         * 광고
            * 크리에이티브

<!-- Add "Feature: DSP Creatives" once we have other topics on creatives; get Bob to update the feature list. -->
<!-- Do clients think in terms of insertion orders? If yes, then work in the following info.:
In Advertising Cloud DSP, an insertion order is represented as a campaign, and line items are represented as packages. Each package will include placements, which can use different strategies and tactics to deliver the line item requirements.
-->

## [!UICONTROL Campaigns]

[캠페인](/help/dsp/campaign-management/campaigns/campaign-about.md) 는 비행 설정의 중요한 프레임워크입니다. 각 캠페인은 광고주, 시작 및 종료 날짜, 전체 예산, 교차 장치 타깃팅 옵션 및 기본 빈도 상한, 뷰가능, 사기, 브랜드 안전 및 대상 확인을 위한 보고 옵션으로 구성됩니다. 모든 캠페인 수준 설정은 캠페인 내의 각 패키지 및 배치에 자동으로 적용됩니다.

## [!UICONTROL Packages]

각 캠페인에는 하나 이상을 포함할 수 있습니다 [패키지](/help/dsp/campaign-management/packages/package-about.md)각각의 에는 배치 세트가 포함되어 있습니다.

패키지를 사용하여 배달을 위한 배치를 설정된 예산, 성능 목표 및 사용자 지정 간격 전략에 그룹화합니다. DSP은 예산을 패키지에서 가장 성과가 좋은 배치로 전환하여 패키지를 최적화합니다. 배치 형식, 재고 유형, 데이터 공급자, 성향 또는 기타 구별할 수 있는 특성별로 패키지를 구성할 수 있습니다.

패키지는 선택 사항이지만 권장됩니다.

## [!UICONTROL Placements]

A [배치](/help/dsp/campaign-management/placements/placement-about.md) 동일한 광고 유형의 하나 이상의 광고에 대한 타깃팅 매개 변수를 저장합니다. 단일 캠페인이나 패키지에 대한 배치를 만든 다음 해당 캠페인에 광고를 할당할 수 있습니다.

## [!UICONTROL Ads]

[광고](/help/dsp/campaign-management/ads/ad-about.md) 크리에이티브 자산 및 추적 URL을 포함합니다. 크리에이티브 자산을 업로드할 수 있으며 DSP에서 무료로 사용하는 광고를 제공하거나 타사 광고 서비스 태그를 업로드할 수 있습니다.

광고가 설정되면 각 광고를 게재해야 합니다. 하나 이상의 배치에 단일 광고를 첨부할 수 있습니다.

활성 캠페인에서 활성 위치에 있는 활성 상태의 승인된 모든 광고는 배치 타깃팅 매개 변수를 기반으로 실행할 수 있습니다.

## [!UICONTROL Creatives]

지정된 캠페인의 광고에 사용할 오디오 및 비디오 파일을 업로드할 수 있습니다.
<!-- add link to [About Creative Management](/help/dsp/campaign-management/creatives/creative-about.md) when it's available-->

업로드된 크리에이티브를 사용하여 광고를 즉시 만들거나 나중에 크리에이티브 보기 또는 광고 보기에서 광고를 만들 수 있습니다.

>[!MORELIKETHIS]
>
>* [Campaign Management 기본 정보](/help/dsp/campaign-management/campaigns/campaign-about.md)
>* [패키지 관리 정보](/help/dsp/campaign-management/packages/package-about.md)
>* [배치 관리 정보](/help/dsp/campaign-management/placements/placement-about.md)
>* [광고 관리](/help/dsp/campaign-management/ads/ad-about.md)
>* [Campaign Launch 검사 목록](/help/dsp/campaign-management/campaign-launch-checklist.md)
>* [성능 캠페인 설정에 대한 우수 사례](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [플랫폼 내 보고서 정보](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Campaign 데이터 보기 정보](/help/dsp/campaign-management/reports/campaign-data-views-about.md)
>* [비디오: DSP 계정 구조 및 사용자 인터페이스](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/dsp/ui.html)

