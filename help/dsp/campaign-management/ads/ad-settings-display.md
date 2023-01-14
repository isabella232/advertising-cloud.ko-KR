---
title: 광고 설정 표시
description: 디스플레이 광고에 사용할 수 있는 광고 설정에 대한 설명을 참조하십시오.
feature: DSP Ads
exl-id: ae88dfab-0b0c-42ab-9135-422b20a4b6cd
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 0%

---

# 광고 설정 표시

다음 설정은 표준 디스플레이 광고입니다.

## [!UICONTROL Ad Options]

### 기본

**[!UICONTROL Ad Type]:** (읽기 전용) 만들고 있는 광고 유형으로, 광고를 첨부할 수 있는 배치 유형에 해당합니다. 기본값은 입니다. *[!UICONTROL Display]*.

**[!UICONTROL Ad Name]:** 광고 이름. 자산 제목은 기본적으로 사용되지만 이름을 변경할 수 있습니다.

>[!TIP]
>
> 광고를 게재의 [!UICONTROL Ads] 및 를 보고서 세트에 표시합니다. 예를 들어, 장치 유형과 일부 주요 속성(예: 휴일 제품 미리 보기)을 설명합니다. 300x250 게이머&quot;)

**\[광고 소스\]**: (읽기 전용) *[!UICONTROL 3rd party]*.

**[!UICONTROL This is an expandable Banner]:** (타사 광고만 해당) 광고가 확장 가능한 배너 광고임을 나타냅니다. 관련 확장 설정은 구매할 인벤토리를 결정하므로 광고 동작을 반영하는지 확인합니다.

**[!UICONTROL Expansion Method]:** (타사 확장 가능한 배너 광고만 해당) 배너가 *[!UICONTROL Click]* 또는 *[!UICONTROL Rollover]*.

**[!UICONTROL Expansion Directions]:** (타사 확장 가능한 배너 광고만 해당) 광고가 확장하는 방향입니다. *[!UICONTROL Up]*, *[!UICONTROL Down]*, *[!UICONTROL Left]*, 또는 *[!UICONTROL Right]*.

**[!UICONTROL Certified Vendors]:** (타사 확장 가능한 배너 광고만 해당) 광고를 사용할 수 있는 인증된 공급업체: *[!UICONTROL DCM]* ([!DNL Google DoubleClick for Advertisers]), *[!UICONTROL Flashtalking]*, *[!UICONTROL Sizmek]*, 또는 *[!UICONTROL Jivox]*.

**[!UICONTROL Display Code]:** (타사 광고만 해당) 타사 광고 자산의 URL입니다. 임의 [timestamp] 및 [[timestamp]] 매개 변수는 실제 값으로 대체됩니다.

**[!UICONTROL Final Display Code]:** (타사 광고만 해당) 필요한 경우 타사 크리에이티브 자산의 URL입니다 [Advertising DSP 추적 매크로](/help/dsp/campaign-management/macros.md) 삽입됨, 해당하는 경우

**[!UICONTROL Ad Size]:** 광고의 폭과 높이입니다. 이것은 [지원되는 표준 디스플레이 광고 크기](ad-specs.md). 광고를 업로드하거나 을 입력하기 전에 수동으로 광고 크기를 입력할 수 있습니다 [!UICONTROL Display Code]. 광고 크기를 입력하지 않으면 업로드된 광고 또는 광고 태그의 차원이 자동으로 읽기 전용으로 입력됩니다. 차원이 표준 디스플레이(예: 300x250 광고 크기 대신 301x250)에 없는 경우 디스플레이 광고가 저장되지 않습니다.

>[!IMPORTANT]
>
> 너비 및 높이 필드에 선언된 광고 크기가 들어오는 입찰 요청과 일치합니다. 광고 차원이 선언된 광고 크기와 일치하지 않는 경우 게재 문제가 발생할 수 있습니다.

### [!UICONTROL Pixel]

배치에 대한 모든 기존 이벤트 추적 픽셀이 자동으로 첨부됩니다. 개별 광고에 대한 추적 요구 사항에 따라 기존 픽셀을 분리하고 필요에 따라 새 픽셀을 만들 수 있습니다.

다음 설정은 만들거나 편집하는 각 픽셀에 적용됩니다.

**[!UICONTROL Integration Event]:** 픽셀을 트리거하여 실행하는 이벤트입니다. 이 광고 유형의 경우, *[!UICONTROL Impression]* 또는 *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** 픽셀이 *[!UICONTROL IMG URL]* (1x1 픽셀 이미지 파일), *[!UICONTROL HTML]*, 또는 *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** 픽셀 이미지의 URL을 지정된 [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** 픽셀 이름입니다. 픽셀을 쉽게 식별하는 데 도움이 되는 이름을 사용하십시오.

**[!UICONTROL Pixel Provider]:** 픽셀 공급자: *[!UICONTROL None]*, *[!UICONTROL Nielsen]*, 또는 *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [광고 관리](ad-about.md)
>* [단일 광고 만들기](ad-create.md)
>* [광고와 연결된 배치 나열](ad-list-placements.md)
>* [광고 사양](ad-specs.md)
>* [DSP 매크로](/help/dsp/campaign-management/macros.md)

