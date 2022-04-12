---
title: 오디오 광고 설정
description: 오디오 광고에 사용할 수 있는 광고 설정에 대한 설명을 참조하십시오.
feature: DSP Ads
exl-id: 746b6f40-ff59-4bbe-bfc0-3579d4461e4a
source-git-commit: bcece4bfec6f8a765cced3ee230fd8cbf3055b7b
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# 오디오 광고 설정

## [!UICONTROL Insert Ad Tag]

*새 광고만*

**[!UICONTROL URL]**: VAST 태그 URL입니다.

**[!UICONTROL Title]**: 에서 사용할 파일의 이름입니다. [!UICONTROL Ads] 보기 및 보고서.

>[!TIP]
>
> VAST 태그의 유효성을 확인하려면 브라우저에 붙여 넣은 다음 **[!UICONTROL Enter]** 키. 태그가 유효하면 `<VAST>` 꼭대기 근처에요

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (읽기 전용) 만들고 있는 광고 유형으로, 광고를 첨부할 수 있는 배치 유형에 해당합니다. 기본값은 입니다. *[!UICONTROL Audio]*.

**[!UICONTROL Ad Name]:** 광고 이름. 자산 제목은 기본적으로 사용되지만 이름을 변경할 수 있습니다.

>[!TIP]
>
> 광고를 게재의 [!UICONTROL Ads] 및 를 보고서 세트에 표시합니다. 예를 들어, 장치 유형과 일부 주요 속성(예: 휴일 제품 미리 보기)을 설명합니다. 30초 오디오&quot;)

**[!UICONTROL Ad Duration]:** 오디오 파일의 길이입니다. 자동으로 다음 중 하나로 설정됩니다. [!UICONTROL 15] 또는 [!UICONTROL 30], 선택한 광고 단위에 따라 달라집니다.

이 필드는 계정 권한에 따라 표시될 수도 있고 표시되지 않을 수도 있습니다.

**[!UICONTROL VAST Tag]:** (VAST 태그만 사용하는 광고) 타사 광고 소스용 URL입니다. VAST 태그에 오디오 미디어 파일만 포함되어 있는지 확인합니다.

**[!UICONTROL Final VAST Tag]:** (VAST 태그만 사용하는 광고) 필요한 타사 광고 소스의 URL입니다 [Advertising Cloud DSP 추적 매크로](/help/dsp/campaign-management/macros.md) 삽입됨, 해당하는 경우

**[!UICONTROL Select Rate]:** (권한이 있는 사용자만 해당) Adobe을 통해 청구되는 사전 협상된 비율 또는 협상한 비율 중 하나이며 공급업체를 통해 청구됩니다. 비율을 추가하려면 [!DNL Adobe] 계정 팀입니다.

### 픽셀

배치에 대한 모든 기존 이벤트 추적 픽셀이 자동으로 첨부됩니다. 개별 광고에 대한 추적 요구 사항에 따라 기존 픽셀을 분리하고 필요에 따라 새 픽셀을 만들 수 있습니다.

다음 설정은 만들거나 편집하는 각 픽셀에 적용됩니다.

**[!UICONTROL Integration Event]:** 픽셀을 트리거하여 실행하는 이벤트입니다. 이 광고 유형의 경우, *[!UICONTROL Impression]* 또는 *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** 픽셀이 *[!UICONTROL IMG UR]L* (1x1 픽셀 이미지 파일), *[!UICONTROL HTML]*, 또는 *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** 픽셀 이미지의 URL(지정된 픽셀 유형에 적합한 형식)입니다.

**[!UICONTROL Pixel Name]:** 픽셀 이름입니다. 픽셀을 쉽게 식별하는 데 도움이 되는 이름을 사용하십시오.

**[!UICONTROL Pixel Provider]:** 픽셀 공급자: *[!UICONTROL None]*, *[!UICONTROL Nielsen]*, 또는 *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [광고 관리](ad-about.md)
>* [단일 광고 만들기](ad-create.md)
>* [광고와 연결된 배치 나열](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [광고 사양](ad-specs.md)
>* [Advertising Cloud DSP 매크로](/help/dsp/campaign-management/macros.md)

