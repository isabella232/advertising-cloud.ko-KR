---
title: Advertising Cloud DSP 매크로
description: 일반 추적에 사용할 수 있는 매크로를 참조하고 타사 디스플레이 광고의 클릭 수를 추적하십시오.
feature: DSP Ads
exl-id: e31cc2e5-ad1f-4555-a87b-0e4c3731fe5f
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 0%

---

# Advertising Cloud DSP 매크로

매크로는 명령의 짧은 명령 또는 축약이며 일반적으로 `${MACRO_NAME}` 형식을 따릅니다. Advertising Cloud DSP 광고 서버는 광고가 제공되거나 클릭될 때 매크로를 실행합니다.

매크로는 타사 및 사용자 지정 크리에이티브 코드 또는 메타데이터(예: 타사 픽셀)를 매매하는 동안 가장 일반적으로 사용됩니다.

## 일반 추적 매크로

모든 광고 및 태그 유형에 대한 일반 추적 매크로를 사용하여 필요에 따라 특정 데이터를 다시 전달합니다.

| 매크로 | 설명 |
| --------------- | ---------------------- |
| `${USER_ID}` | 모든 장치 유형에 대한 사용자 식별자입니다. |
| `${TM_RANDOM}` | 캐시 버스터: 1에서 1000000 사이의 난수 |
| `${TM_PLACEMENT_ID_NUM}` | 배치 ID |
| `${TM_SITE_URL_URLENC}` | 입찰 요청에서 전달된 URL; URL 인코딩 |
| `${TM_SITE_DOMAIN_URLENC}` | 입찰 요청의 URL에서 구문 분석된 페이지 하위 도메인입니다. URL 인코딩 |

{style=&quot;table-layout:auto&quot;}

## 타사 디스플레이 광고에 대한 매크로 를 클릭합니다

타사 디스플레이 태그를 사용하여 광고 클릭을 정확하게 추적하려면 DSP에 디스플레이 클릭 매크로가 필요합니다. 매크로 버전은 하나만 필요합니다. 관련 매크로는 태그 유형에 따라 다릅니다.

| 매크로 | 설명 |
| --------------- | ---------------------- |
| `${TM_CLICK_URL}` | 광고 서버가 플랫폼에서 광고 클릭 수를 추적하고 카운트할 수 있는 리디렉션 URL |
| `${TM_CLICK_URL_URLENC}` | 플랫폼에서 광고 클릭 수를 추적하고 계산하기 위해 URL 인코딩이 필요한 광고 서버를 활성화하는 리디렉션 URL |

{style=&quot;table-layout:auto&quot;}

DSP에서는 다음과 같은 경우 디스플레이 태그에 표시 클릭 매크로를 자동으로 삽입합니다.

* Advertising Cloud 광고 서버 파트너 <!-- [Needs PM confirmation.] -->에서 광고 태그를 내보냅니다.
* DSP에서 직접 [!DNL Flashtalking] 또는 [!DNL Google DoubleClick for Advertisers] 광고 태그를 벌크 업로드합니다

디스플레이 광고를 작성할 때 클릭 매크로가 누락된 경우 태그의 올바른 영역에 해당 표시 클릭 매크로를 수동으로 삽입하라는 경고 메시지가 DSP에 표시됩니다.

>[!MORELIKETHIS]
>
>* [오디오 광고 설정](/help/dsp/campaign-management/ads/ad-settings-audio.md)
>* [연결된 TV 광고 설정](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)
>* [광고 설정 표시](/help/dsp/campaign-management/ads/ad-settings-display.md)
>* [모바일 광고 설정](/help/dsp/campaign-management/ads/ad-settings-mobile.md)
>* [기본 광고 설정](/help/dsp/campaign-management/ads/ad-settings-native.md)
>* [프리롤 광고 설정](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)

