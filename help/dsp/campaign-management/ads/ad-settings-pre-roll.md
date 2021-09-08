---
title: 프리롤 광고 설정
description: 프리롤 광고에 사용할 수 있는 광고 설정에 대한 설명을 참조하십시오.
feature: Ads
exl-id: 638d5a3d-3dff-40b6-a3ba-7ab3f08282b9
source-git-commit: e2ee41c7e3e195f062ad1cc67080ed913d6d3d06
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 프리롤 광고 설정

## [!UICONTROL Upload or Select Creative]

*새 광고만*

**[!UICONTROL Transcode to]:** (권한에 따라 일부 사용자) (선택 사항) 게시자가 특정 크리에이티브 파일 요구 사항이 있을 때 VAST 태그에 포함할 형식을 지정합니다. 대부분의 게시자가 수락하는 형식은 기본적으로 선택됩니다.

**[!UICONTROL Custom Transcode]:** (베타 사용자만 해당) 세로 비디오를 선택한 경우 사용할 수 없음 ) 비디오가 사용자 지정 코드 변환을 사용함을 나타냅니다. 이 옵션을 선택하는 경우 최대 3개의 사용자 지정 코드 버전에 대한 파일 형식, 비디오 비트율, 확대/축소 및 차원을 지정합니다.

**[!UICONTROL XTrader]:** (권한에 따라 일부 사용자) 비디오가 하나 이상의 피드를 사용함을  [!DNL X_TRADER] 나타냅니다.

**[!UICONTROL Upload Video]** : 원시 자산을 DSP에 업로드하려면 이 옵션을 선택하면 다음 작업을 수행합니다.

1. **[!UICONTROL Choose File]** 을 클릭하고 장치 또는 네트워크에서 파일을 찾습니다.
1. [!UICONTROL Ads] 보기 및 보고서에 사용할 파일의 제목을 입력합니다.
1. 클릭 **[!UICONTROL Upload]**.

**[!UICONTROL Use Existing Video]** : 이전에 업로드한 모든 크리에이티브를 계정 내에서 올바른 형식으로 선택하려면 다음을 수행하십시오.

**[!UICONTROL Advanced: VAST Tag URL]:** (일부 광고 유형) 크리에이티브 자산 및 추적 픽셀을 포함하는 타사 VAST 태그를 입력하려면 다음을 수행하십시오.

1. **[!UICONTROL Advanced: VAST Tag URL]** 옆의 ![화살표](/help/dsp/assets/compressed.png)를 클릭합니다.
1. **[!UICONTROL URL]** 필드에 VAST 태그 URL을 입력합니다.
1. [!UICONTROL Ads] 보기 및 보고서에 사용할 파일에 대해 **[!UICONTROL Title]**&#x200B;을 입력합니다.

>[!TIP]
>
> VAST 태그의 유효성을 확인하려면 브라우저에 붙여 넣은 다음 **[!UICONTROL Enter]** 키를 누릅니다. 태그가 유효하면 맨 위에 `<VAST>`이 포함된 XML 파일이 표시됩니다.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (읽기 전용) 만들고 있는 광고 유형으로, 광고를 첨부할 수 있는 배치 유형에 해당합니다.

**[!UICONTROL Ad Name]:** 광고 이름입니다. 자산 제목은 기본적으로 사용되지만 이름을 변경할 수 있습니다.

>[!TIP]
>
> 광고를 게재할 때 [!UICONTROL Ads] 보기 및 보고서에서 쉽게 찾을 수 있는 이름을 사용하십시오. 예를 들어, 장치 유형과 일부 주요 속성(예: 휴일 제품 미리 보기)을 설명합니다. 30초 프리롤&quot;)

**[!UICONTROL Width]|  [!UICONTROL Ad Unit Width]:**  (표준 및 코드 조각 가능한 프리롤 광고만 해당) 전체 광고 단위의 너비입니다. 선택한 광고 단위 유형에 따라 이 옵션이 잠길 수 있습니다.

**[!UICONTROL Height]|  [!UICONTROL Ad Unit Height]:**  (표준 및 코드 조각 가능한 프리롤 광고만 해당) 전체 광고 단위의 높이입니다. 선택한 광고 단위 유형에 따라 이 옵션이 잠길 수 있습니다.

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

**[!UICONTROL Wmode]:** (대화형 프리롤 전용) 창 모드:  *[!UICONTROL window]*,  *[!UICONTROL transparent]* 또는  *[!UICONTROL opaque]*.

**[!UICONTROL Video Format]:** (대화형 프리롤 전용) 잠재적 인벤토리를 위한 광고 플레이어의 형식입니다.  *[!UICONTROL VPAID]* 또는  *[!UICONTROL VPAID & VAST]*. 뷰가능 여부는 항상 VPAID에 대해 측정되지만, VPAID 및 VAST에는 뷰가능 측정을 허용하지 않는 인벤토리가 포함됩니다. 보기 가능 지표가 캠페인에 중요한 경우 이를 염두에 두십시오.

**[!UICONTROL Clock Number]**: (대화형 프리롤 전용) 오직 영국에서만 사용됨. 권한이 있는 사용자만 사용할 수 있음) 올바른 광고가 브로드캐스트되도록 하는 데 사용되는 고유한 식별자입니다. 이 설정을 적용할 수 없으면 비워 둡니다.

### [!UICONTROL Companion]

*DSP에서 제공하는 광고만*

광고와 함께 최대 3개의 컴패니언 배너를 선택적으로 첨부할 수 있습니다. 가장 좋은 방법은 가능한 경우 컴패니언 배너를 추가하는 것입니다.

>[!NOTE]
>
> 모든 게시자가 컴패니언 배너를 허용하는 것은 아닙니다. 컴패니언 배너를 허용하는 게시자는 컴패니언 배너에 대한 인상을 보장하지 않습니다.
> 타사 광고 태그의 컴패니언 배너를 미리 보기용으로 항상 사용할 수는 없습니다.

**\[Check Box\]:** 지정한 컴패니언 배너와 광고를 포함합니다. 확인란이 비활성화되면 컴패니언 배너가 포함되지 않습니다.

**\[배너 크기\]:** 컴패니언 배너 크기:  *[!UICONTROL 300x600 (Skyscraper)]*;  *[!UICONTROL 300x250 (Medium Rectangle)]*: 가장 일반적인 광고 크기이며 모든 광고에 권장됩니다.  *[!UICONTROL 300x60 (Small Banner)]*; 또는  *[!UICONTROL 728x90 (Leaderboard)]*: 덜 일반적인 광고 크기입니다.

**\[Source\]:** 나만의 컴패니언 배너 자산을 업로드하는지 또는 타사 태그를 사용하는지 여부.

**자산:** (원시 자산만 해당) 컴패니언 배너 자산입니다. **[!UICONTROL Browse]** 을 클릭하고 장치 또는 네트워크에서 파일을 찾은 다음 **[!UICONTROL Upload]** 를 클릭합니다.

**광고 태그]:[!UICONTROL **(VAST 태그만 사용하는 광고) 타사 컴패니언 배너 소스에 대한 URL입니다.

**[!UICONTROL Final Ad Tag]:** (VAST 태그를 사용하는 광고 전용) 필요한  [Advertising Cloud DSP 추적 매크로가 삽입된 타사 컴패니언 배너 소스 소스 소스(해당하는 경우)에 ](/help/dsp/campaign-management/macros.md) 대한 URL입니다.

### [!UICONTROL Overlays]

*DSP에서 제공하는 광고를 위한 대화형 프리롤 및 모바일 인터랙티브한 탭-재생 형식*

다음 설정은 만들거나 편집하는 각 오버레이에 적용됩니다.

**[!UICONTROL Asset]:** (원시 자산만 해당) 오버레이 이미지 자산. 파일은 단일 프레임 GIF, JPG 또는 PNG 형식이어야 하며 최대 이미지 크기는 2MB보다 작아야 합니다. 자산을 업로드하려면 **[!UICONTROL Browse]** 을 클릭하고 장치 또는 네트워크에서 파일을 찾은 다음 **[!UICONTROL Upload]** 를 클릭합니다.

>[!TIP]
>
>[오버레이 디자인을 위한 우수 사례](/help/dsp/campaign-management/ads/ad-best-practices-overlays.md)를 참조하십시오

**[!UICONTROL Click URL]**  : 뷰어가 광고 오버레이를 클릭할 때 표시되는 URL입니다.

**[!UICONTROL X]:** 오버레이의 X 좌표입니다. 오버레이 시작 위치를 선택한 다음 시작 위치의 픽셀 수(예: 중앙으로부터 10px)를 입력합니다. 가장 좋은 방법은 *중앙으로부터*&#x200B;를 사용하는 것입니다. 이 경우 오버레이가 게시자 사이트에서 다른 플레이어 크기를 사용하여 이동하지 못하도록 합니다.

**[!UICONTROL Y]:** 오버레이의 Y 좌표입니다. 오버레이 시작 위치를 선택한 다음 시작 위치의 픽셀 수(예: 위쪽에서 10px)를 입력합니다. 가장 좋은 방법은 오버레이가 광고에 표시될 위치에 따라 *[!UICONTROL From Bottom]* 또는 *[!UICONTROL From Top],* 좌표를 지정하는 것입니다.

**[!UICONTROL Layer]:** 오버레이가 표시될 레이입니다. 비디오와 각 오버레이는 별도의 레이로 표시됩니다.

* *[!UICONTROL 2 through 5]* : 비디오 앞에, 다른 오버레이 뒤에 있습니다.

* *[!UICONTROL 1]* : 비디오 앞에 있습니다.

* *[!UICONTROL 0]* : 비디오와 동일한 레이어에 있습니다. 비디오가 축소되어 나머지 공간을 채웁니다. 대화형 프리롤에는 권장되지 않습니다.

* *[!UICONTROL -1]:* 비디오 뒤.

* *[!UICONTROL -2 through -5]* : 비디오 뒤에서 다른 오버레이 앞에 있습니다.

* *[!UICONTROL Background]:* 비디오 및 기타 오버레이 백그라운드에서 오버레이는 비디오의 전체 너비와 높이로 확장되며 종횡비는 유지되지 않습니다.

### [!UICONTROL Pixel]

배치에 대한 모든 기존 이벤트 추적 픽셀이 자동으로 첨부됩니다. 추적 요구 사항에 따라 기존 픽셀을 분리하고 필요에 따라 새 픽셀을 만들 수 있습니다.

다음 설정은 만들거나 편집하는 각 픽셀에 적용됩니다.

**[!UICONTROL Integration Event]** : 픽셀을 트리거하여 실행하는 이벤트입니다. 이 광고 유형의 경우 *[!UICONTROL Impression]* 또는 *[!UICONTROL Click-through]*&#x200B;에서 실행되는 픽셀을 사용합니다.

**[!UICONTROL Pixel Type]** : 픽셀이  *[!UICONTROL IMG URL]* (1x1 픽셀 이미지 파일)  *[!UICONTROL HTML]*&#x200B;인지,  *[!UICONTROL JavaScript URL]*&#x200B;인지 여부입니다.

**[!UICONTROL Pixel URL or Code]** : 픽셀 이미지의 URL로서, 지정한 형식에 적절한  [!UICONTROL Pixel Type]형식입니다.

**[!UICONTROL Pixel Name]:** 픽셀 이름입니다. 픽셀을 쉽게 식별하는 데 도움이 되는 이름을 사용하십시오.

**[!UICONTROL Pixel Provider]:** 픽셀 공급자:  *[!UICONTROL None]*,  *[!UICONTROL Nielsen]* 또는  *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [광고 관리](ad-about.md)
>* [광고 만들기](ad-create.md)
>* [광고와 연결된 배치 나열](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [사용 가능한 광고 유형](ad-types.md)
>* [광고 사양](/help/dsp/assets/ad-specs.pdf)
>* [오버레이 디자인을 위한 우수 사례](/help/dsp/campaign-management/ads/ad-best-practices-overlays.md)
>* [Advertising Cloud DSP 매크로](/help/dsp/campaign-management/macros.md)

