---
title: Advertising Cloud DSP 매크로
description: 일반 추적에 사용할 수 있는 매크로를 참조하고 타사 디스플레이 광고의 클릭 수를 추적하십시오.
feature: DSP Ads
exl-id: e31cc2e5-ad1f-4555-a87b-0e4c3731fe5f
source-git-commit: fbadd81a34c375f00fa3e420ea3c46fc9143daf8
workflow-type: tm+mt
source-wordcount: '931'
ht-degree: 0%

---

# Advertising Cloud DSP 매크로

매크로는 간단한 명령 또는 명령 축약이며 일반적으로 형식을 따릅니다 `${MACRO_NAME}`. 크리에이티브 코드 또는 클릭스루 URL에 포함된 매크로는 광고 서버가 이해할 수 있는 더 긴 코드 문자열로 확장됩니다. Advertising Cloud DSP 광고 서버는 광고가 제공되거나 클릭될 때 매크로를 실행합니다.

광고 서버 매크로는 DSP 또는 타사 광고 서버에 중요한 정보를 전달하는 데 유용합니다. 매크로는 타사 및 사용자 지정 크리에이티브 코드 또는 메타데이터(예: 타사 픽셀)를 매매하는 동안 가장 일반적으로 사용됩니다.

VAST 태그, URL 또는 DSP 또는 타사 이벤트 픽셀과 같이 어디서나 매크로를 수동으로 삽입할 수 있습니다. 그러나 각 DSP 클라이언트와 파트너는 다른 광고 태그 형식을 가지므로 그에 따라 태그의 다른 지점에 매크로를 삽입해야 합니다. 새 클라이언트나 파트너를 사용할 때마다 DSP 트래픽이 발생하는 광고 태그에 매크로를 삽입할 위치에 대한 설명서를 요청합니다.

## 일반 추적 매크로

모든 광고 및 태그 유형에 대한 일반 추적 매크로를 사용하여 필요에 따라 특정 데이터를 다시 전달합니다.

| 매크로 | 교체 설명 | 유형 |
| ----- | ----------------------- | ---- |
| `${TM_ACCOUNT_ID}` | 계정 ID입니다. | 정수 |
| `${TM_AD_ID}` | 광고 키(adKey)입니다. | string |
| `${TM_AD_ID_NUM}` | 광고 ID입니다. | 정수 |
| `${TM_ADVERTISER_ID}` | 광고주 ID. | 정수 |
| `${TM_CAMPAIGN_ID}` | 캠페인 키. | string |
| `${TM_CAMPAIGN_ID_NUM}` | 캠페인 ID. | 정수 |
| ` ${TM_CLICK_URL}` | 광고 서버가 광고 클릭 수를 추적하고 카운트할 수 있는 리디렉션 URL입니다. 광고가 제공되면 사용자가 광고를 클릭하면 매크로가 활성화되고 보고를 위해 클릭이 기록되고 계산됩니다. | string |
| ` ${TM_CLICK_URL_URLENC}` | 광고 서버가 광고 클릭 수를 추적하고 카운트할 수 있는 인코딩된 리디렉션 URL입니다. 광고가 제공되면 사용자가 광고를 클릭하면 매크로가 활성화되고 보고를 위해 클릭이 기록되고 계산됩니다. 타사 광고를 만들고 공급업체에서 URL 인코딩을 필요로 하지 않는 한 이 매크로를 사용하지 마십시오. | string |
| `${TM_FEED_ID}` | 미디어 배치 키(feedKey)입니다. | string |
| `${TM_FEED_ID_NUM}` | 미디어 배치에 대한 ID입니다. | 정수 |
| ` ${TM_MACRO_PLACEMENT_SITE_KEY` | 배치에 대한 사이트 키입니다. 에 필요 [!DNL AppsFlyer] 모바일 앱 설치 광고용 추적기 를 클릭합니다.<!-- should map to placement_site_key column of placement_site table --> | string |
| `${TM_PLACEMENT_ID}` | 배치 키(cpKey)입니다. | string |
| `${TM_PLACEMENT_ID_NUM}` | 배치 ID입니다. | 정수 |
| `${TM_RANDOM}` | 캐시 버스터: 1에서 1000000 사이의 난수입니다. | 장기간 |
| `${TM_SESSION_ID}` | 광고 태그의 단일 검색에 해당하는 세션의 ID입니다. | string |
| `${TM_SITE_DOMAIN_URLENC}` | 입찰 요청의 URL에서 구문 분석된 페이지 하위 도메인입니다. URL로 인코딩되었습니다. 인배너, 클릭 투 재생 광고에 대해서는 지원되지 않습니다. | string |
| ` ${TM_SITE_NAME}` | 배치의 사이트 이름입니다. | string |
| `${TM_SITE_URL_URLENC}` | 입찰 요청에서 전달된 URL; URL로 인코딩되었습니다. 인배너, 클릭 투 재생 광고에 대해서는 지원되지 않습니다. | string |
| `${TM_SITE_ID_NUM}` | 배치에 대한 사이트 ID입니다. | 정수 |
| `${TM_TIMESTAMP}` | 1970년 1월 1일 자정(00:00 UTC) 이후 경과된 초 수를 나타내는 Unix 타임스탬프입니다. | 장기간 |
| ` ${TM_VIDEO_DURATION}` | 광고 비디오의 지속 시간(초)입니다. | 정수 |

{style=&quot;table-layout:auto&quot;}

<!-- Removed because not found in code base:
|` ${TM_MACRO_PROMOTED_AD_KEY}` | The promoted ad key for the placement. Required for [!DNL AppsFlyer] click trackers for mobile app install ads. | string |
 -->

## 모바일 특정 매크로

| 매크로 | 교체 설명 | 유형 |
| ----- | ----------------------- | ---- |
| `${CS_PLATFORM_ID}` | ([!DNL ComScore]) 장치의 운영 체제에 해당하는 플랫폼 ID입니다.<ul><li>`ios` = [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>`other` 플랫폼이 위의 플랫폼이 아닌 경우</li></ul> | varchar(50) |
| `${CS_DEVICE_MODEL}` | ([!DNL ComScore]) 장치 모델 이름, URL로 인코딩됩니다. | string |
| `${CS_IMPLEMENTATION_TYPE}` | ([!DNL ComScore]) 광고가 제공된 환경입니다.<ul><li>`a` = 모바일 애플리케이션</li><li>`b` = 모바일 웹 사이트</li></ul> | 문자열(`a` 또는 `b`) |
| `${NS_PLATFORM_ID}` | ([!DNL Nielsen]) 장치의 운영 체제에 해당하는 플랫폼 ID입니다.<ul><li>`ios`= [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>`other` 플랫폼이 위의 플랫폼이 아닌 경우</li></ul> | string |
| `${NS_DEVICE_GROUPING}` | ([!DNL Nielsen]) 광고가 시청된 장치 유형입니다.<ul><li>`TAB` = 태블릿</li><li>`PHN` = 모바일</li><li>`computer` = 컴퓨터</li></ul> | string |
| `${UOO}` | ([!DNL Nielsen]) 사용자가 광고 추적을 옵트아웃했는지 여부:<ul><li>`1` (DNT 플래그 = 1) = 사용자가 광고 추적을 옵트아웃했습니다</li><li>`0` (DNT 플래그 = 0) = 사용자가 광고 추적을 옵트인했습니다</li></ul> | 정수 (`0` 또는 `1`) |
| `${TM_BUNDLE}` | 다음 [!DNL iOS] 또는 [!DNL Android] 앱스토어 번들 ID입니다. 예: com.zynga.wwf2 free 또는 id804379658 | string |
| `gdpr=${GDPR_ENFORCED}&gdpr_consent=${GDPR_CONSENT}` | `gdpr=${GDPR_ENFORCED}` 입찰 요청이 유럽 연합 출원에서 오고 GDPR 집행이 요구되는지 여부를 입찰자가 결정하는지를 나타냅니다.<ul><li>`1` = GDPR이 적용되어야 함</li><li>`0` = GDPR은 적용하지 않아야 합니다</li></ul>`gdpr_consent=${GDPR_CONSENT}` 은 인바운드 입찰 요청에서 공급 파트너로부터 전달된 동의 값입니다.<ul><li>대부분의 경우 base64url로 인코딩된 동의 문자열 또는 데이지비트입니다(예: BN5lERiOYEdiAKAWXEND1HoSBE6CAFApAMgBkIDIgM0AgOJxAnQA)</li><li>`0` = 동의 없음</li><li>`1` = 동의</li></ul> | 데이지 비트 또는 정수 |

{style=&quot;table-layout:auto&quot;}

## 타사 디스플레이 광고에 대한 매크로 를 클릭합니다

타사 디스플레이 태그를 사용하여 광고 클릭을 정확하게 추적하려면 DSP에 디스플레이 클릭 매크로가 필요합니다. 매크로 버전은 하나만 필요합니다. 관련 매크로는 태그 유형에 따라 다릅니다.

| 매크로 | 교체 설명 | 유형 |
| ----- | ----------------------- | ---- |
| `${TM_CLICK_URL}` | 광고 서버가 플랫폼에서 광고 클릭 수를 추적하고 카운트할 수 있는 리디렉션 URL입니다. | string |
| `${TM_CLICK_URL_URLENC}` | 플랫폼에서 광고 클릭 수를 추적하고 계산하기 위해 URL 인코딩이 필요한 광고 서버를 활성화하는 리디렉션 URL. | string |

{style=&quot;table-layout:auto&quot;}

DSP에서는 다음과 같은 경우 서드파티 디스플레이 태그에 표시 클릭 매크로를 자동으로 삽입합니다.

* Advertising Cloud 광고 서버 파트너에서 광고 태그 내보내기 <!-- [Needs PM confirmation.] -->
* 일괄 업로드 [!DNL Flashtalking] 또는 [!DNL Google DoubleClick for Advertisers] DSP에서 바로 태그 추가

디스플레이 광고를 작성할 때 클릭 매크로가 누락된 경우 태그의 올바른 영역에 해당 표시 클릭 매크로를 수동으로 삽입하라는 경고 메시지가 DSP에 표시됩니다.

## 매크로 오류 문제 해결

코드에 매크로를 추가할 때는 매크로의 정확한 구문을 사용해야 합니다. 매크로를 확인할 때 DSP에서는 매크로가 유효한 매크로 중 하나와 정확히 일치하는지 확인합니다.

매크로 이름의 시작 또는 끝에서 문자가 누락된 경우 오류가 생성됩니다. 예를 들어 다음과 같은 경우 오류 메시지가 표시됩니다.

* 매크로 이름의 시작 부분에서 다음과 같은 문자를 하나 이상 잊어버립니다 `${`. 전체 구문을 포함하지 않으면 항목이 유효한 매크로로 인식되지 않습니다.
* 매크로가 다음과 같은 유효한 문자 집합으로 끝나지 않습니다. `}`.

>[!MORELIKETHIS]
>
>* [오디오 광고 설정](/help/dsp/campaign-management/ads/ad-settings-audio.md)
>* [연결된 TV 광고 설정](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)
>* [광고 설정 표시](/help/dsp/campaign-management/ads/ad-settings-display.md)
>* [모바일 광고 설정](/help/dsp/campaign-management/ads/ad-settings-mobile.md)
>* [기본 광고 설정](/help/dsp/campaign-management/ads/ad-settings-native.md)
>* [프리롤 광고 설정](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)

