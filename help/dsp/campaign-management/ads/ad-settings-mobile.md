---
title: 모바일 광고 설정
description: 모바일 광고에 사용할 수 있는 광고 설정에 대한 설명을 참조하십시오.
feature: DSP Ads
exl-id: f67c4ba0-1011-4ad6-bd36-98c312b81b67
source-git-commit: bcece4bfec6f8a765cced3ee230fd8cbf3055b7b
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 0%

---

# 모바일 광고 설정

## [!UICONTROL Insert Ad Tag]

*새로운 모바일 비디오 광고 형식만*

**[!UICONTROL URL]** 또는 **[!UICONTROL Ad Tag]**: 크리에이티브 자산 및 추적 픽셀을 포함하는 타사 VAST 광고 태그 또는 광고 태그

**[!UICONTROL Ad Title]** 또는 **[!UICONTROL Title]**: 에서 사용되는 광고의 이름입니다 [!UICONTROL Ads] 보기 및 보고서.

>[!TIP]
>
> VAST 태그의 유효성을 확인하려면 브라우저에 붙여 넣은 다음 **[!UICONTROL Enter]** 키. 태그가 유효하면 `<VAST>` 꼭대기 근처에요

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]: 모바일 디스플레이 광고

**[!UICONTROL Ad Type]:** (읽기 전용) 만들고 있는 광고 유형으로, 광고를 첨부할 수 있는 배치 유형에 해당합니다.

**[!UICONTROL Ad Name]:** 광고 이름. 자산 제목은 기본적으로 사용되지만 이름을 변경할 수 있습니다.

>[!TIP]
>
> 광고를 배치, 광고 보기 및 보고서에서 첨부할 때 쉽게 찾을 수 있는 이름을 사용합니다. 예를 들어, 장치 유형과 일부 주요 속성(예: 휴일 제품 미리 보기)을 설명합니다. 300x250 게이머&quot;)

**\[광고 소스\]**: (읽기 전용) *[!UICONTROL 3rd party]*.

**[!UICONTROL Display Code]:** 타사 크리에이티브 자산의 URL입니다. 임의 [timestamp] 및 [[timestamp]] 매개 변수는 실제 값으로 대체됩니다.

**[!UICONTROL Final Display Code]:** 필요한 경우 타사 크리에이티브 자산의 URL입니다 [Advertising Cloud DSP 추적 매크로](/help/dsp/campaign-management/macros.md) 삽입됨, 해당하는 경우

### [!UICONTROL Basic]: 비디오 광고

**[!UICONTROL Ad Type]:** (읽기 전용) 만들고 있는 광고 유형으로, 광고를 첨부할 수 있는 배치 유형에 해당합니다.

**[!UICONTROL Ad Name]:** 광고 이름. 자산 제목은 기본적으로 사용되지만 이름을 변경할 수 있습니다.

>[!TIP]
>
> 광고를 배치, 광고 보기 및 보고서에서 첨부할 때 쉽게 찾을 수 있는 이름을 사용합니다. 예를 들어, 장치 유형과 일부 주요 속성(예: 휴일 제품 미리 보기)을 설명합니다. 30초 전화 프리롤&quot;)

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]:** 전체 광고 단위의 폭입니다. 선택한 광고 단위 유형에 따라 이 옵션이 잠길 수 있습니다.

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]:** 전체 광고 단위의 높이입니다. 선택한 광고 단위 유형에 따라 이 옵션이 잠길 수 있습니다.

**[!UICONTROL Player X]:** 광고 단위에 대한 X 좌표입니다. 기본 설정을 유지합니다.

**[!UICONTROL Player Y]:** 광고 단위에 대한 Y 좌표입니다. 기본 설정을 유지합니다.

**[!UICONTROL Player Width]:** 전체 광고 단위의 폭입니다. 선택한 광고 단위 유형에 따라 이 옵션이 잠길 수 있습니다.

이것은 와 같습니다 **[!UICONTROL Width]** 필드.

**[!UICONTROL Player Height]:** 전체 광고 단위의 높이입니다. 선택한 광고 단위 유형에 따라 이 옵션이 잠길 수 있습니다.

이것은 와 같습니다 **[!UICONTROL Height]** 필드.

**[!UICONTROL Show Controls]:** 광고에 대한 비디오 컨트롤을 포함할 위치: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]*, 또는 *[!UICONTROL None]* (기본값)

**[!UICONTROL Preserve Aspect Ratio]:** 비디오의 폭과 높이 비율을 유지할 것인지 여부(*[!UICONTROL Yes]*) 또는 비디오를 확장하여 사용 가능한 공간을 채우거나(*[!UICONTROL No]*).

**[!UICONTROL Close Button Delay]:** (일부 광고 유형) 닫기 버튼의 모양을 지연하는 초 수입니다.

**[!UICONTROL VAST Tag]:** (VAST 태그만 사용하는 광고) 읽기 전용) 광고 자산으로 입력한 타사 VAST 태그입니다.

**[!UICONTROL Final VAST Tag]:** (VAST 태그만 사용하는 광고) 읽기 전용) 필요한 경우 크리에이티브 자산으로 입력한 타사 VAST 태그 [Advertising Cloud DSP 추적 매크로](/help/dsp/campaign-management/macros.md) 삽입됨, 해당하는 경우

**[!UICONTROL Wmode]:** (일부 광고 유형) 창 모드: *[!UICONTROL window]*, *[!UICONTROL transparent]*, 또는 *[!UICONTROL opaque]*.

### [!UICONTROL Pixel]

배치에 대한 모든 기존 이벤트 추적 픽셀이 자동으로 첨부됩니다. 개별 광고에 대한 추적 요구 사항에 따라 기존 픽셀을 분리하고 필요에 따라 새 픽셀을 만들 수 있습니다.

다음 설정은 만들거나 편집하는 각 픽셀에 적용됩니다.

**[!UICONTROL Integration Event]:** 픽셀을 트리거하여 실행하는 이벤트입니다. 이 광고 유형의 경우, *[!UICONTROL Impression]* 또는 *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** 픽셀이 *[!UICONTROL IMG URL]* (1x1 픽셀 이미지 파일), *[!UICONTROL HTML]*, 또는 *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** 픽셀 이미지의 URL을 지정된 [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** 픽셀 이름입니다. 픽셀을 쉽게 식별하는 데 도움이 되는 이름을 사용하십시오.

**[!UICONTROL Pixel Provider]:** 픽셀 공급자: *[!UICONTROL None]*, *[!UICONTROL Nielsen]*, 또는 *[!UICONTROL Comscore]*.

### [!UICONTROL Sharing]

사용되지 않음

>[!MORELIKETHIS]
>
>* [광고 관리](ad-about.md)
>* [단일 광고 만들기](ad-create.md)
>* [광고와 연결된 배치 나열](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [광고 사양](ad-specs.md)
>* [Advertising Cloud DSP 매크로](/help/dsp/campaign-management/macros.md)

