---
title: Advertising Cloud DSP의 광고 관리 정보
description: 광고 관리에 대해 알아봅니다.
feature: DSP Ads
exl-id: 72c8bbef-d09c-4cf4-994d-99578d043d39
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 0%

---

# Advertising Cloud DSP의 광고 관리 정보

<!-- add "The Ads View (Dashboard?)" section -->

Advertising Cloud DSP은 광고를 제공하는 두 가지 방법을 제공합니다.

* Advertising Cloud DSP은 DSP에 직접 자산(예: 디스플레이 배너, 비디오 자산, 오디오 파일 또는 URL)을 업로드할 때 무료로 광고를 제공합니다. DSP에서 제공하는 자산의 경우 오버레이와 같은 추가 기능에 액세스할 수 있습니다.

* 타사 광고 서버(예: Google, Flashtalk 또는 Sizmek)를 사용하는 경우 타사 광고 서비스 태그를 개별적으로 또는 대량으로 DSP에 업로드할 수 있습니다. 벌크 업로드 기능을 사용하려면 a) DoubleClick 및 Flashtalk 태그 시트를 업로드하거나 또는 b) 템플릿을 다운로드하고, 태그를 템플릿에 입력한 다음 템플릿을 다시 업로드해야 합니다.<!-- need a list of all supported third-party ad servers; see file in future-tbd folder -->

광고가 설정되면, 캠페인의 게재 방법을 제어하는 타깃팅 매개 변수(예: 지역, 대상, 장치 및 인벤토리 타깃팅)가 포함된 각 광고를 게재해야 합니다. 단일 광고를 하나 또는 여러 배치에 첨부할 수 있습니다.

## 사용 가능한 광고 유형

* 오디오
* 연결된 TV
* 표시
* 모바일
* 기본
* 프리롤

이러한 광고 유형에 대한 자세한 내용은 [사용 가능한 광고 유형](ad-types.md) 및 전체 [광고 사양](/help/dsp/assets/ad-specs.pdf)을 참조하십시오.

## 특수 광고 기능

다음 기능은 DSP에서 제공하는 광고에만 사용할 수 있습니다.

### 컴패니언 배너

컴패니언 배너는 [프리롤 광고](ad-settings-pre-roll.md) 또는 (일부 게시자와 함께) [오디오 광고](ad-settings-audio.md)와 함께 제공되며, 브랜드 및 메시지 연결을 강화하는 데 도움이 될 수 있습니다.

>[!NOTE]
>
>* 모든 게시자가 컴패니언 배너를 허용하는 것은 아닙니다. 컴패니언 배너를 허용하는 게시자는 컴패니언 배너에 대한 인상을 보장하지 않습니다.
>* 타사 광고 태그의 컴패니언 배너를 미리 보기용으로 항상 사용할 수는 없습니다.


자신의 컴패니언 배너 자산을 업로드하거나 인증된 타사 광고 서비스 파트너에서 타사 iFrame 또는 스크립트 배너 태그를 업로드할 수 있습니다.

### 오버레이

오버레이는 비디오 전체에서 지속적인 브랜딩에 도움이 되며 추가 클릭 수를 유도할 수 있습니다. 오버레이 기능은 [대화형 프리롤 광고](ad-settings-pre-roll.md) 및 [대화형 및 탭하여 재생 형식으로 모바일 광고에 사용할 수 있습니다](ad-settings-mobile.md).

[오버레이 디자인을 위한 우수 사례](/help/dsp/campaign-management/ads/ad-best-practices-overlays.md)를 참조하십시오

### 티저

티저는 시청자에게 광고를 하도록 유혹하는 눈길을 끄는 이미지입니다. Teaser는 모바일 탭-재생 광고 형식에만 적용됩니다.

## Advertising Cloud DSP 광고 승인

광고를 만들 때 Advertising Cloud DSP에서 중요한 카테고리에 대해 검토하고, URL 기능을 클릭하고, 렌더링을 미리 봅니다.

처음에는 [!UICONTROL Status] 열에 빨간색 점이 표시됩니다. 검토 프로세스는 일반적으로 24-48시간이 소요됩니다. 그러나 끊어진 광고에는 48시간 이상 보류 중인 상태가 있을 수 있으므로 광고를 거부하기 전에 오류를 수정할 시간이 있습니다. 거부된 광고에는 거부에 대한 이유가 포함되어 있습니다.

DSP이 광고를 승인하면 상태 열에 녹색 점이 표시됩니다.

![열의 승인  [!UICONTROL Status] 표시기](/help/dsp/assets/ad-approval-status.png)

>[!NOTE]
>
>DSP과 SSP가 모두 크리에이티브를 승인한 경우에만 광고가 제공됩니다. 각 SSP에는 자체 승인 요구 사항 및 프로세스가 있습니다.

>[!MORELIKETHIS]
>
>* [광고 만들기](ad-create.md)
>* [여러 타사 광고 만들기](ad-create-third-party.md)
>* [사용 가능한 광고 유형](ad-types.md)
>* [광고 사양](/help/dsp/assets/ad-specs.pdf)

