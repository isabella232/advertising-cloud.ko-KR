---
title: 오디오 광고 설정
description: 오디오 광고에 사용할 수 있는 광고 설정에 대한 설명을 참조하십시오.
feature: Ads
exl-id: 746b6f40-ff59-4bbe-bfc0-3579d4461e4a
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 오디오 광고 설정

## [!UICONTROL Upload or Select Creative]

*새 광고만*

**[!UICONTROL Upload Audio]** : 원시 자산을 DSP에 업로드하려면 이 옵션을 선택하면 다음 작업을 수행합니다.

1. **[!UICONTROL Choose File]** 을 클릭하고 장치 또는 네트워크에서 파일을 찾습니다.
1. [!UICONTROL Ads] 보기 및 보고서에 사용할 파일의 제목을 입력합니다.
1. 클릭 **[!UICONTROL Upload]**.

**[!UICONTROL Use Existing Audio]** : 이전에 업로드한 모든 크리에이티브를 계정 내에서 올바른 형식으로 선택하려면 다음을 수행하십시오.

**[!UICONTROL Advanced: VAST Tag URL]** : 크리에이티브 자산 및 추적 픽셀을 포함하는 타사 VAST 태그를 입력하려면 다음을 수행하십시오.

1. **[!UICONTROL Advanced: VAST Tag URL]** 옆의 ![화살표](/help/dsp/assets/compressed.png)를 클릭합니다.
1. **[!UICONTROL URL]** 필드에 VAST 태그 URL을 입력합니다.
1. [!UICONTROL Ads] 보기 및 보고서에 사용할 파일에 대해 **[!UICONTROL Title]**&#x200B;을 입력합니다.

>[!TIP]
>
> VAST 태그의 유효성을 확인하려면 브라우저에 붙여 넣은 다음 **[!UICONTROL Enter]** 키를 누릅니다. 태그가 유효하면 맨 위에 `<VAST>`이 포함된 XML 파일이 표시됩니다.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (읽기 전용) 만들고 있는 광고 유형으로, 광고를 첨부할 수 있는 배치 유형에 해당합니다. 기본값은 *[!UICONTROL Audio]*&#x200B;입니다.

**[!UICONTROL Ad Name]:** 광고 이름입니다. 자산 제목은 기본적으로 사용되지만 이름을 변경할 수 있습니다.

>[!TIP]
>
> 광고를 게재할 때 [!UICONTROL Ads] 보기 및 보고서에서 쉽게 찾을 수 있는 이름을 사용하십시오. 예를 들어, 장치 유형과 일부 주요 속성(예: 휴일 제품 미리 보기)을 설명합니다. 30초 오디오&quot;)

**[!UICONTROL Ad Duration]:** 오디오 파일의 길이입니다. 선택한 광고 단위에 따라 자동으로 [!UICONTROL 15] 또는 [!UICONTROL 30] 로 설정됩니다.

이 필드는 계정 권한에 따라 표시될 수도 있고 표시되지 않을 수도 있습니다.

**[!UICONTROL Click URL]:** (원시 자산을 사용하고 디스플레이 배너만 사용하는 광고) (선택 사항) 광고와 함께 표시되는 디스플레이 배너를 클릭할 때 표시되는 URL입니다.

**[!UICONTROL Final Click URL]:** (원시 자산을 사용하고 디스플레이 배너만 사용하는 광고) 읽기 전용) 필요한  [!UICONTROL Click URL] Advertising Cloud DSP 추적  [ ](/help/dsp/campaign-management/macros.md) 매크로가 삽입된 경우,

**[!UICONTROL VAST Tag]**  : (VAST 태그만 사용하는 광고) 타사 광고 소스용 URL입니다. VAST 태그에 오디오 미디어 파일만 포함되어 있는지 확인합니다.

**[!UICONTROL Final VAST Tag]** : (VAST 태그를 사용하는 광고만 해당) 필요한  [Advertising Cloud DSP 추적 매크로가 삽입된 타사 광고 소스의 ](/help/dsp/campaign-management/macros.md) URL입니다(해당하는 경우).

**[!UICONTROL Select Rate]:** (권한이 있는 사용자만 해당) Adobe을 통해 청구되는 사전 협상된 비율 또는 협상한 비율 중 하나이며 공급업체를 통해 청구됩니다. 비율을 추가하려면 Adobe 계정 관리자에게 문의하십시오.

### [!UICONTROL Companion]

*DSP에서 제공하는 광고만*

광고와 함께 최대 3개의 컴패니언 배너를 선택적으로 첨부할 수 있습니다. 가장 좋은 방법은 가능한 경우 컴패니언 배너를 추가하는 것입니다.

>[!NOTE]
>
>* 모든 게시자가 컴패니언 배너를 허용하는 것은 아닙니다. 컴패니언 배너를 허용하는 게시자는 컴패니언 배너에 대한 인상을 보장하지 않습니다.
>* 타사 광고 태그의 컴패니언 배너를 미리 보기용으로 항상 사용할 수는 없습니다.


**\[Check Box\]:** 지정한 컴패니언 배너와 광고를 포함합니다. 확인란이 비활성화되면 컴패니언 배너가 포함되지 않습니다.

**\[배너 크기\]:** 컴패니언 배너 크기:  *[!UICONTROL 300x250]* ( [!DNL iHeartRadio],  [!DNL Spotify],  [!DNL SoundCloud]및  [!DNL TuneIn]에 사용됨),  *[!UICONTROL 640x640]* ( [!DNL Spotify), or *1024x1024]*( [!DNL SoundCloud]에 사용됨)에 사용됩니다.

**\[Source\]:** 컴패니언 배너 자산의 소스입니다.

* *[!UICONTROL Upload My Own Asset]:* 고유한 자산을 업로드합니다.
* *[!UICONTROL Use a Third Party Tag]* : 인증된 타사 광고 서비스 파트너에서 iFrame 또는 스크립트 태그를 입력하려면 다음을 수행하십시오.

타사 컴패니언 배너 노출 횟수를 추적하려면 서드파티 태그를 사용하십시오.

**[!UICONTROL Asset]:** (원시 자산만 해당) 컴패니언 배너 자산(GIF, JPG 또는 PNG 형식)입니다. **[!UICONTROL Browse]** 을 클릭하고 장치 또는 네트워크에서 파일을 찾은 다음 **[!UICONTROL Upload]** 를 클릭합니다.

**[!UICONTROL Click URL]:** (원시 자산만 해당) 뷰어가 광고에 대한 컴패니언 배너를 클릭할 때 표시되는 URL입니다. 타사 클릭 추적 픽셀을 사용하여 클릭 리디렉션을 포함할 수 있습니다.

**[!UICONTROL Final Click URL]:** (원시 자산만) 읽기 전용) 필요한  [Advertising Cloud DSP 추적 매크로가 ](/help/dsp/campaign-management/macros.md) 삽입된 클릭 URL(해당하는 경우)

**[!UICONTROL Ad Tag]**  : (타사 광고 태그를 사용하는 광고) 타사 컴패니언 배너 소스에 대한 iFrame 또는 스크립트 배너 태그입니다. 인증된 타사 광고 서비스 파트너여야 합니다.

**[!UICONTROL Final Ad Tag]**  : (타사 광고 태그만 사용하는 광고) 필요한  [Advertising Cloud DSP 추적 매크로가 삽입된 ](/help/dsp/campaign-management/macros.md) 광고 태그입니다(해당하는 경우).

### 픽셀

배치에 대한 모든 기존 이벤트 추적 픽셀이 자동으로 첨부됩니다. 추적 요구 사항에 따라 기존 픽셀을 분리하고 필요에 따라 새 픽셀을 만들 수 있습니다.

다음 설정은 만들거나 편집하는 각 픽셀에 적용됩니다.

**[!UICONTROL Integration Event]** : 픽셀을 트리거하여 실행하는 이벤트입니다. 이 광고 유형의 경우 *[!UICONTROL Impression]* 또는 *[!UICONTROL Click-through]*&#x200B;에서 실행되는 픽셀을 사용합니다.

**[!UICONTROL Pixel Type]** : 픽셀이  *[!UICONTROL IMG UR]L* (1x1 픽셀 이미지 파일)인지  *[!UICONTROL HTML]*&#x200B;아니면  *[!UICONTROL JavaScript URL]*&#x200B;인지 여부입니다.

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

