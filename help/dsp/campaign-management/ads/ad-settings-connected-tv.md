---
title: 연결된 TV 광고 설정
description: 연결된 TV 광고에 사용할 수 있는 광고 설정에 대한 설명을 참조하십시오.
feature: Ads
exl-id: 4daae9e4-27eb-4496-9186-f33aebd8daae
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 연결된 TV 광고 설정

## [!UICONTROL Upload or Select Creative]

*새 광고만*

**[!UICONTROL Upload Audio]** : 원시 자산을 DSP에 업로드하려면 이 옵션을 선택하면 다음 작업을 수행합니다.

1. **[!UICONTROL Choose File]** 을 클릭하고 장치 또는 네트워크에서 파일을 찾습니다.
1. [!UICONTROL Ads] 보기 및 보고서에 사용할 파일의 제목을 입력합니다.
1. 클릭 **[!UICONTROL Upload]**.

**[!UICONTROL Use Existing Audio]** : 이전에 업로드한 모든 크리에이티브를 계정 내에서 올바른 형식으로 선택하려면 다음을 수행하십시오.

**[!UICONTROL Advanced: VAST Tag URL]:** (일부 광고 유형) 크리에이티브 자산 및 추적 픽셀을 포함하는 타사 VAST 태그를 입력하려면 다음을 수행하십시오.

1. **[!UICONTROL Advanced: VAST Tag URL]** 옆의 ![화살표](/help/dsp/assets/compressed.png)를 클릭합니다.
1. **[!UICONTROL URL]** 필드에 VAST 태그 URL을 입력합니다.
1. 광고 보기 및 보고서에 사용할 파일에 대해 **[!UICONTROL Title]**&#x200B;을 입력합니다.

>[!TIP]
>
> VAST 태그의 유효성을 확인하려면 브라우저에 붙여 넣은 다음 **[!UICONTROL Enter]** 키를 누릅니다. 태그가 유효하면 맨 위에 `<VAST>`이 포함된 XML 파일이 표시됩니다.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (읽기 전용) 만들고 있는 광고 유형으로, 광고를 첨부할 수 있는 배치 유형에 해당합니다.

**[!UICONTROL Ad Name]:** 광고 이름입니다. 자산 제목은 기본적으로 사용되지만 이름을 변경할 수 있습니다.

>[!TIP]
>
> 광고를 게재할 때 [!UICONTROL Ads] 보기 및 보고서에서 쉽게 찾을 수 있는 이름을 사용하십시오. 예를 들어, 장치 유형과 일부 주요 속성(예: 휴일 제품 미리 보기)을 설명합니다. 30초 CTV&quot;)

**[!UICONTROL Width | Ad Unit Width]:** 전체 광고 단위의 폭입니다. 선택한 광고 단위 유형에 따라 이 옵션이 잠길 수 있습니다.

**[!UICONTROL Height | Ad Unit Height]:** 전체 광고 단위의 높이입니다. 선택한 광고 단위 유형에 따라 이 옵션이 잠길 수 있습니다.

**[!UICONTROL Player X]:** 광고 단위의 X 좌표입니다. 기본 설정을 유지합니다.

**[!UICONTROL Player Y]:** 광고 단위의 Y 좌표입니다. 기본 설정을 유지합니다.

**[!UICONTROL Player Width]:** 전체 광고 단위의 폭입니다. 선택한 광고 단위 유형에 따라 이 옵션이 잠길 수 있습니다.

**[!UICONTROL Width]** 필드와 동일합니다.

**[!UICONTROL Player Height]:** 전체 광고 단위의 높이입니다. 선택한 광고 단위 유형에 따라 이 옵션이 잠길 수 있습니다.

**[!UICONTROL Height]** 필드와 동일합니다.

**[!UICONTROL Show Controls]:** 광고에 대한 비디오 컨트롤을 포함할 위치:  *[!UICONTROL Under]*,  *[!UICONTROL Over]*,  *[!UICONTROL Bottom]* 또는  *[!UICONTROL None]* (기본값).

**[!UICONTROL Preserve Aspect Ratio]** : 비디오의 폭과 높이 비율(*[!UICONTROL Yes]*)을 유지할지 또는 비디오를 확장하여 사용 가능한 공간을 채우지(*[!UICONTROL No]*) 여부.

**[!UICONTROL Click URL]**  : (Adobe 제공 광고만 해당) 뷰어가 광고를 클릭할 때 표시되는 URL입니다.

**[!UICONTROL Final Click URL]:** (Adobe 제공 광고만 해당) 읽기 전용) 필요한  [!UICONTROL Click URL] Advertising Cloud DSP 추적  [ ](/help/dsp/campaign-management/macros.md) 매크로가 삽입된 경우,

**[!UICONTROL VAST Tag]:** (VAST 태그만 사용하는 광고 읽기 전용) 광고 소스로 입력한 타사 VAST 태그입니다.

**[!UICONTROL Final VAST Tag]:** (VAST 태그만 사용하는 광고 읽기 전용) 필요한  [Advertising Cloud DSP 추적 매크로가 ](/help/dsp/campaign-management/macros.md) 삽입된 광고 소스로 입력한 타사 VAST 태그입니다(해당하는 경우).

**[!UICONTROL Clock Number]**: (영국에서만 사용) 권한이 있는 사용자만 사용할 수 있음) 올바른 광고가 브로드캐스트되도록 하는 데 사용되는 고유한 식별자입니다. 이 설정을 적용할 수 없으면 비워 둡니다.

### [!UICONTROL Pixel]

배치에 대한 모든 기존 이벤트 추적 픽셀이 자동으로 첨부됩니다. 추적 요구 사항에 따라 기존 픽셀을 분리하고 필요에 따라 새 픽셀을 만들 수 있습니다.

다음 설정은 만들거나 편집하는 각 픽셀에 적용됩니다.

**[!UICONTROL Integration Event]** : 픽셀을 트리거하여 실행하는 이벤트입니다. 이 광고 유형의 경우 *[!UICONTROL Impression]* 또는 *[!UICONTROL Click-through]*&#x200B;에서 실행되는 픽셀을 사용합니다.

**[!UICONTROL Pixel Type]** : 픽셀이  *[!UICONTROL IMG URL]* (1x1 픽셀 이미지 파일)  *[!UICONTROL HTML]*&#x200B;인지,  *[!UICONTROL JavaScript URL]*&#x200B;인지 여부입니다.

**[!UICONTROL Pixel URL or Code]** : 픽셀 이미지의 URL로서, 지정된 픽셀 유형에 적합한 포맷입니다.

**[!UICONTROL Pixel Name]:** 픽셀 이름입니다. 픽셀을 쉽게 식별하는 데 도움이 되는 이름을 사용하십시오.

**[!UICONTROL Pixel Provider]:** 픽셀 공급자:  *[!UICONTROL None]*,  *[!UICONTROL Nielsen]* 또는  *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [광고 관리](ad-about.md)
>* [광고 만들기](ad-create.md)
>* [광고와 연결된 배치 나열](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [사용 가능한 광고 유형](ad-types.md)
>* [광고 사양](/help/dsp/assets/ad-specs.pdf)
>* [Advertising Cloud DSP 매크로](/help/dsp/campaign-management/macros.md)

