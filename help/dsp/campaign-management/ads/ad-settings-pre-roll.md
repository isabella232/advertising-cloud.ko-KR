---
title: 프리롤 광고 설정
description: 프리롤 광고에 사용할 수 있는 광고 설정에 대한 설명을 참조하십시오.
feature: DSP Ads
exl-id: 638d5a3d-3dff-40b6-a3ba-7ab3f08282b9
source-git-commit: bcece4bfec6f8a765cced3ee230fd8cbf3055b7b
workflow-type: tm+mt
source-wordcount: '552'
ht-degree: 0%

---

# 프리롤 광고 설정

## [!UICONTROL Insert Ad Tag]

*새 광고만*

**[!UICONTROL URL]:** VAST 태그 URL입니다.

**[!UICONTROL Title]:** 파일의 제목으로서 [!UICONTROL Ads] 보기 및 보고서.

>[!TIP]
>
> VAST 태그의 유효성을 확인하려면 브라우저에 붙여 넣은 다음 **[!UICONTROL Enter]** 키. 태그가 유효하면 `<VAST>` 꼭대기 근처에요

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (읽기 전용) 만들고 있는 광고 유형으로, 광고를 첨부할 수 있는 배치 유형에 해당합니다.

**[!UICONTROL Ad Name]:** 광고 이름. 자산 제목은 기본적으로 사용되지만 이름을 변경할 수 있습니다.

>[!TIP]
>
> 광고를 게재의 [!UICONTROL Ads] 및 를 보고서 세트에 표시합니다. 예를 들어, 장치 유형과 일부 주요 속성(예: 휴일 제품 미리 보기)을 설명합니다. 30초 프리롤&quot;)

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]:** (표준 및 경사진 프리롤 광고만 해당) 전체 광고 단위의 너비입니다. 선택한 광고 단위 유형에 따라 이 옵션이 잠길 수 있습니다.

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]:** (표준 및 경사진 프리롤 광고만 해당) 전체 광고 단위의 높이입니다. 선택한 광고 단위 유형에 따라 이 옵션이 잠길 수 있습니다.

**[!UICONTROL Player X]:** 광고 단위에 대한 X 좌표입니다. 기본 설정을 유지합니다.

**[!UICONTROL Player Y]:** 광고 단위에 대한 Y 좌표입니다. 기본 설정을 유지합니다.

**[!UICONTROL Player Width]:** 전체 광고 단위의 폭입니다. 선택한 광고 단위 유형에 따라 이 옵션이 잠길 수 있습니다.

이 필드는 다음과 같습니다 **[!UICONTROL Width]** 필드.

**[!UICONTROL Player Height]:** 전체 광고 단위의 높이입니다. 선택한 광고 단위 유형에 따라 이 옵션이 잠길 수 있습니다.

이것은 와 같습니다 **[!UICONTROL Height]** 필드.

**[!UICONTROL Show Controls]:** 광고에 대한 비디오 컨트롤을 포함할 위치: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]*, 또는 *[!UICONTROL None]* (기본값)

**[!UICONTROL Preserve Aspect Ratio]:** 비디오의 폭과 높이 비율을 유지하는지 여부(*[!UICONTROL Yes]*) 또는 비디오를 확장하여 사용 가능한 공간을 채우거나(*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (VAST 태그만 사용하는 광고) 읽기 전용) 광고 소스로 입력한 타사 VAST 태그입니다.

**[!UICONTROL Final VAST Tag]:** (VAST 태그만 사용하는 광고) 읽기 전용) 필요한 를 사용하여 광고 소스로 입력한 타사 VAST 태그입니다 [Advertising Cloud DSP 추적 매크로](/help/dsp/campaign-management/macros.md) 삽입됨, 해당하는 경우

**[!UICONTROL Wmode]:** (대화형 프리롤 전용) 창 모드: *[!UICONTROL window]*, *[!UICONTROL transparent]*, 또는 *[!UICONTROL opaque]*.

**[!UICONTROL Video Format]:** (대화형 프리롤 전용) 잠재적 인벤토리를 위한 광고 플레이어의 형식입니다. *[!UICONTROL VPAID]* 또는 *[!UICONTROL VPAID & VAST]*. 뷰가능 여부는 항상 VPAID에 대해 측정되지만, VPAID 및 VAST에는 뷰가능 측정을 허용하지 않는 인벤토리가 포함됩니다. 보기 가능 지표가 캠페인에 중요한 경우 이 구분을 고려하십시오.

**[!UICONTROL Clock Number]**: (대화형 프리롤 전용) 오직 영국에서만 사용됨. 권한이 있는 사용자만 사용할 수 있음) 올바른 광고가 브로드캐스트되도록 하는 데 사용되는 고유한 식별자입니다. 이 설정을 적용할 수 없으면 비워 둡니다.

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
>* [광고와 연결된 배치 나열](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [광고 사양](ad-specs.md)
>* [Advertising Cloud DSP 매크로](/help/dsp/campaign-management/macros.md)

