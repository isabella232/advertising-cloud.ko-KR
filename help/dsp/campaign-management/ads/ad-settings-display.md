---
title: 광고 설정 표시
description: 디스플레이 광고에 사용할 수 있는 광고 설정에 대한 설명을 참조하십시오.
feature: DSP Ads
exl-id: ae88dfab-0b0c-42ab-9135-422b20a4b6cd
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 0%

---

# 광고 설정 표시

다음 설정은 표준 디스플레이 광고입니다. 디스플레이 광고에 클릭-투-재생 비디오 광고를 제공할 수도 있지만, 이를 지원하는 게시자는 많지 않으므로 그렇게 하지 않는 것이 좋습니다.

## [!UICONTROL Ad Options]

### 기본

**[!UICONTROL Ad Type]:** (읽기 전용) 만들고 있는 광고 유형으로, 광고를 첨부할 수 있는 배치 유형에 해당합니다. 기본값은 *[!UICONTROL Display]*&#x200B;입니다.

**[!UICONTROL Ad Name]:** 광고 이름입니다. 자산 제목은 기본적으로 사용되지만 이름을 변경할 수 있습니다.

>[!TIP]
>
> 광고를 게재할 때 [!UICONTROL Ads] 보기 및 보고서에서 쉽게 찾을 수 있는 이름을 사용하십시오. 예를 들어, 장치 유형과 일부 주요 속성(예: 휴일 제품 미리 보기)을 설명합니다. 300x250 게이머&quot;)

**\[광고 소스\]**: Advertising Cloud DSP이 광고(*[!UICONTROL Adobe served]*)를 제공하고 있는지 아니면 타사 광고 서버(*[!UICONTROL 3rd party]*)를 사용하고 있는지 여부.

**[!UICONTROL This is an expandable Banner]**  : (타사 광고만 해당) 광고가 확장 가능한 배너 광고임을 나타냅니다. 관련 확장 설정은 구매할 인벤토리를 결정하므로 광고 동작을 반영하는지 확인합니다.

**[!UICONTROL Expansion Method]:** (타사 확장 가능한 배너 광고만 해당) 배너를 확장할 것인지  *[!UICONTROL Click]* 아니면  *[!UICONTROL Rollover]*&#x200B;확장할 것인지 여부입니다.

**[!UICONTROL Expansion Directions]:** (타사 확장 가능한 배너 광고만 해당) 광고가 확장하는 방향입니다.  *[!UICONTROL Up]*,  *[!UICONTROL Down]*,  *[!UICONTROL Left]*&#x200B;또는  *[!UICONTROL Right]*.

**[!UICONTROL Certified Vendors]:** (타사 확장 가능한 배너 광고만 해당) 광고를 사용할 수 있는 인증된 공급업체:  *[!UICONTROL DCM]* ([!DNL Google DoubleClick for Advertisers]),  *[!UICONTROL Flashtalking]*,  *[!UICONTROL Sizmek]*&#x200B;또는  *[!UICONTROL Jivox]*.

**[!UICONTROL Display Code]** : (타사 광고만 해당) 타사 광고 자산의 URL입니다. 모든 [타임스탬프] 및 [[timestamp]] 매개 변수는 실제 값으로 대체됩니다.

**[!UICONTROL Final Display Code]:** (타사 광고만 해당) 필요한  [Advertising Cloud DSP 추적 매크로가 삽입된 타사 크리에이티브 자산의 ](/help/dsp/campaign-management/macros.md) URL입니다(해당하는 경우).

**[!UICONTROL Creative type]** : (Adobe이 제공되는 광고만) 자산이 자산인지  *[!UICONTROL Image]* 아니면  *[!UICONTROL HTML5]* 자산인지 여부.

**[!UICONTROL Asset]|  [!UICONTROL HTML5 Asset]:** (Adobe 제공 광고만 해당) 광고 유형에 따라 업로드할 이미지 파일 또는 압축된 HTML5 자산입니다. **[!UICONTROL Browse]** 을 클릭하고 장치 또는 네트워크에서 파일을 찾은 다음 **[!UICONTROL Upload]** 또는 **[!UICONTROL Upload Image]** 를 클릭합니다.

**[!UICONTROL Ad Size]** : 광고의 폭과 높이입니다. 이 값은 [지원되는 표준 디스플레이 광고 크기](/help/dsp/assets/ad-specs.pdf)여야 합니다. 광고를 업로드하기 전에 수동으로 광고 크기를 입력하거나 [!UICONTROL Display Code]을 입력할 수 있습니다. 광고 크기를 입력하지 않으면 업로드된 광고 또는 광고 태그의 차원이 자동으로 읽기 전용으로 입력됩니다. 차원이 표준 디스플레이(예: 300x250 광고 크기 대신 301x250)에 없는 경우 디스플레이 광고가 저장되지 않습니다.

>[!IMPORTANT]
>
> 너비 및 높이 필드에 선언된 광고 크기가 들어오는 입찰 요청과 일치합니다. 광고 차원이 선언된 광고 크기와 일치하지 않는 경우 게재 문제가 발생할 수 있습니다.

**[!UICONTROL Click URL]**  : (Adobe 제공 광고만 해당) 뷰어가 광고를 클릭할 때 표시되는 URL입니다.

**[!UICONTROL Final Click URL]:** (Adobe 제공 광고만 해당) 읽기 전용) 필요한  [!UICONTROL Click URL] Advertising Cloud DSP 추적  [ ](/help/dsp/campaign-management/macros.md) 매크로가 삽입된 경우,

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
>* [광고와 연결된 배치 나열](ad-list-placements.md)
>* [사용 가능한 광고 유형](ad-types.md)
>* [광고 사양](/help/dsp/assets/ad-specs.pdf)
>* [Advertising Cloud DSP 매크로](/help/dsp/campaign-management/macros.md)

