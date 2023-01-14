---
title: 범용 비디오 광고 설정
description: 범용 비디오 광고에 사용할 수 있는 광고 설정에 대한 설명을 참조하십시오.
feature: DSP Ads
exl-id: 0be86b84-78f9-4429-a8b7-8195891875ca
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 0%

---

# 범용 비디오 광고 설정

*베타 기능 열기*

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
> 광고를 게재의 [!UICONTROL Ads] 및 를 보고서 세트에 표시합니다. 예를 들어, 장치 유형과 일부 주요 속성(예: 휴일 제품 미리 보기)을 설명합니다. 30초 Universal Video&quot;)

**[!UICONTROL Show Controls]:** 광고에 대한 비디오 컨트롤을 포함할 위치: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]*, 또는 *[!UICONTROL None]* (기본값)

**[!UICONTROL Preserve Aspect Ratio]:** 비디오의 폭과 높이 비율을 유지하는지 여부(*[!UICONTROL Yes]*) 또는 비디오를 확장하여 사용 가능한 공간을 채우거나(*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (VAST 태그만 사용하는 광고) 읽기 전용) 광고 소스로 입력한 타사 VAST 태그입니다.

**[!UICONTROL Final VAST Tag]:** (VAST 태그만 사용하는 광고) 읽기 전용) 필요한 를 사용하여 광고 소스로 입력한 타사 VAST 태그입니다 [Advertising DSP 추적 매크로](/help/dsp/campaign-management/macros.md) 삽입됨, 해당하는 경우

**[!UICONTROL Wmode]:** 창 모드: *[!UICONTROL window]*, *[!UICONTROL transparent]*, 또는 *[!UICONTROL opaque]*. 이 설정을 적용할 수 없으면 비워 둡니다.

**[!UICONTROL Video Format]:** 잠재적 인벤토리에 대한 광고 플레이어의 형식: *[!UICONTROL VPAID]*, *[!UICONTROL VPAID & VAST]*, 또는 *[!UICONTROL VAST]*. 뷰가능 여부에 대해서는 항상 을 측정합니다 [!UICONTROL VPAID]하지만 [!UICONTROL VPAID & VAST] 뷰가능 측정을 허용하지 않는 인벤토리를 포함합니다. 보기 가능 지표가 캠페인에 중요한 경우 이 구분을 고려하십시오.

사용 *[!UICONTROL VAST]*&#x200B;에서는 뷰가능 측정이 허용되지 않는 로서, VAST 형식만 엄격하게 필요로 하는 연결된 TV나 인벤토리를 타겟팅할 때(일반적으로 Google Ad Manager, Appnexus, SpotX 및 Freewheel과 같은 공급 소스에서).

**[!UICONTROL Clock Number]**: (영국에서만 사용) 권한이 있는 사용자만 사용할 수 있음) 올바른 광고가 브로드캐스트되도록 하는 데 사용되는 고유한 식별자입니다. 이 설정을 적용할 수 없으면 비워 둡니다.

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
>* [DSP 매크로](/help/dsp/campaign-management/macros.md)

