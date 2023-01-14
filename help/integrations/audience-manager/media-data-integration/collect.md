---
title: Advertising DSP 캠페인에서 클릭 및 노출 데이터 수집
description: Audience Manager 픽셀을 사용하여 Advertising DSP 광고에서 쿠키 기반 노출 및 클릭 이벤트를 캡처하는 방법을 알아봅니다
feature: Integration with Adobe Audience Manager
exl-id: eb717148-00ab-428a-97b9-e8396a5c47b0
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '1055'
ht-degree: 0%

---

# Advertising DSP 캠페인에서 미디어 노출 데이터 수집

*Advertising DSP만 사용하는 광고주*

*Adobe Advertising-Adobe Audience Manager 통합 전용 광고주*

이 문서에서는 Audience Manager 픽셀을 사용하여 쿠키 기반 노출을 캡처하고 클릭 이벤트를 캡처하도록 Advertising DSP 광고에 태그를 지정하는 방법 및 데이터를 사용하는 데 필요한 추가 작업을 설명합니다.

이벤트 픽셀은 모바일 앱 및 연결된 TV(CTV)와 같이 쿠키가 없는 환경에서 발생하는 이벤트를 캡처하지 않습니다.

## 1단계: Audience Manager에서 데이터 소스 설정 {#set-up-data-source}

Audience Manager에서 [데이터 소스](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html) DSP 노출에 대해 를 클릭하고 데이터를 클릭합니다. 데이터 소스 ID 포함 [각 이벤트 태그](#implement-dsp-pixels) 추적된 모든 이벤트가 데이터 소스에 귀속됩니다.

>[!NOTE]
> 단일 데이터 소스 내에서 여러 DSP에서 실행되는 광고 캠페인에 대한 모든 노출과 클릭 데이터를 수집할 수 있습니다.

## 2단계: 웹 페이지에서 노출 횟수 구현 및 이벤트 픽셀 클릭 {#implement-dsp-pixels}

광고주는 자체 브랜드에 대한 이벤트 태그를 만들고 구현할 수 있습니다. 필요한 경우 Adobe Audience Manager 컨설턴트나 다음 주소로 문의하십시오 [!DNL Adobe] 계정 관리자가 지원됩니다.

>[!NOTE]
>
>조직에서 [!DNL Analytics] 추적하면 Audience Manager 클릭 추적이 필요하지 않을 수 있습니다. Adobe Analytics은 클릭 신호를 캡처하여 을 통해 Audience Manager으로 전송할 수 있습니다 [서버 측 전달](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

### 픽셀 구문

이벤트 픽셀에는 다음 매개 변수가 포함되어야 합니다.

**노출 추적 픽셀:**

`[Audience Manager customer domain].demdex.net/event?d_event=imp&d_src=[source id]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

with [선택적 추가 매개 변수](#parameters) 접두어 `&`

**클릭 추적 픽셀:**

`[Audience Manager customer domain].demdex.net/event?d_event=click&d_src=[source id]&d_rd=[redirect URL]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

with [선택적 추가 매개 변수](#parameters) 접두어 `&`

위치:

* `[Audience Manager customer domain]` 은 노출이나 클릭 이벤트를 보낼 도메인 이름입니다 [!DNL Adobe].

* `[source id]` 는 의 ID입니다 [데이터 소스](#set-up-data-source) 에서 DSP 노출 횟수를 추적하고 데이터를 클릭합니다.

* `[redirect URL]` 는 이중 인코딩 리디렉션 URL입니다. www.urlencoder.org과 같은 온라인 인코딩 도구를 사용하는 경우 인코더를 통해 문자열을 실행하고 결과를 다시 인코딩합니다.

* `${TM_CAMPAIGN_ID_NUM}` 는 DSP의 숫자 캠페인 ID입니다. DSP 매크로를 사용하지 않고 개별 캠페인 ID를 하드코딩하려면 캠페인 설정에서 ID를 찾습니다.

* 각 [매개 변수](#key-value-pairs) 이 접두사로 `&` 및 는 형식으로 되어 있습니다 `d_parameter=parameter_id`, 위치 `parameter` 는 새 필드에 대한 키-값 쌍으로 대체됩니다. 예: `&d_placement=${TM_PLACEMENT_ID_NUM}`

### 매개 변수를 키-값 쌍으로 {#parameters}

**형식:**  `d_parameter=parameter_id`

    위치:
    
    * 매개 변수 접두사는 &#39;&amp;&#39;입니다.
    
    * &#39;parameter&#39;는 새 필드에 대한 키-값 쌍으로 대체됩니다.
    
    예: &#39;&amp;d_placement=${TM_PLACEMENT_ID_NUM}&#39;

두 픽셀 유형은 모두 추가적인 매개 변수를 다음과 같이 포함할 수 있습니다. *키 값 쌍* 트레이트를 수집하거나 다른 보고서에 캠페인 메타데이터(예: 배치 이름 또는 캠페인 이름)를 제공하기 위해. 키-값 쌍은 다음 두 가지 관련 요소로 구성됩니다. a *key*: 데이터 세트를 정의하는 상수입니다. *value*: 세트에 속하는 변수입니다.

키-값 쌍에서 값 변수는 하드 코딩된 ID 또는 *매크로*: 캠페인 및 사용자 추적을 위해 광고 태그가 로드될 때 해당 값으로 동적으로 대체되는 작은 자체 포함된 코드 단위입니다. 캠페인 관련 매개 변수의 경우 [DSP 매크로](/help/dsp/campaign-management/macros.md) 모든 Audience Manager에서 단일 픽셀을 사용하여 캠페인 속성을 해당 노출과 함께 전송하거나 데이터를 클릭하여 Audience Manager을 이동하는 매크로 대신 이벤트 픽셀에 삽입하는 DSP 매크로는 픽셀 내에 포함하는 키-값 쌍에 적합한 값이어야 합니다. 예를 들어 `d_placement` 키, DSP 매크로를 사용합니다. `${TM_PLACEMENT_ID_NUM}` 광고 Adobe 매크로에서 생성된 배치 ID를 캡처하는 값으로 사용됩니다.

Audience Manager이 노출 이벤트 픽셀에 대해 지원하는 매크로 목록은 &quot;[픽셀 호출을 통해 캠페인 노출 횟수 데이터 캡처](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html#supported-key-value-pairs).&quot;

Audience Manager이 클릭 이벤트 픽셀에 대해 지원하는 매크로 목록은 &quot;[픽셀 호출을 통해 캠페인 클릭 데이터 캡처](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/click-data-pixels.html).&quot;

>[!TIP]
>
>* 캠페인 속성을 사용하여 Audience Manager 특성을 만들 수 있도록 캠페인, 배치, 광고(광고) 및 사이트 ID를 포함하는 것이 가장 좋습니다.
>* Audience Optimization 보고서를 만들려면 추가 매개 변수가 필요합니다.
>* 키-값 쌍에서 값을 관련 값으로 바꿉니다 [DSP 매크로](/help/dsp/campaign-management/macros.md) 따라서 모든 캠페인의 모든 광고에서 단일 픽셀을 사용할 수 있습니다. 예를 들어, `d_campaign=[%campaignID%]`to `d_campaign=${TM_CAMPAIGN_ID_NUM}` 광고 Adobe 매크로에서 생성된 캠페인 ID를 캡처하려면 다음을 수행하십시오.
>* 필요한 경우 하드코딩된 값으로 자신만의 매개 변수를 만들 수 있습니다. 예: `d_DSP=AdCloud`


노출 이벤트 픽셀의 예:

`http://acme.demdex.net/event?d_event=imp&d_src=1052880&d_site=${TM_SITE_ID_NUM}&d_creative=${TM_AD_ID_NUM}&d_placement=${TM_FEED_ID_NUM}&d_campaign=${TM_CAMPAIGN_ID_NUM}&d_DSP=AdCloud&d_bust=${TM_RANDOM}`

### 픽셀을 추가할 위치

#### 노출 추적 픽셀

노출수 이벤트 추적 픽셀을 페이지의 모든 광고에 첨부합니다 [!DNL DSP] 캠페인. 다음 위치 중 하나에서 그렇게 할 수 있습니다.

* 배치 수준에서 픽셀을 배치의 모든 광고에 기본적으로 적용합니다. 배치 설정의 추적 섹션에서 [[!UICONTROL Event pixels] 필드](/help/dsp/campaign-management/placements/placement-settings.md).

* 임의의 배치 수준 이벤트 픽셀을 무시하는 광고 레벨입니다. 광고 설정에서, [에서 이벤트 픽셀 만들기 [!UICONTROL Pixel] 탭](/help/dsp/campaign-management/ads/ad-edit.md).

* (타사 광고 서버의 광고 경우) 광고 서버 내의 광고 수준에서

#### 클릭 추적 픽셀

광고 서버 내에서 일반적으로 광고의 클릭스루 URL을 삽입할 때마다 인코딩된 URL이 추가된 클릭 이벤트 픽셀을 삽입합니다.

## 3단계: 구현 후 작업

이벤트 태그가 구현되면 데이터가 Audience Manager 데이터 수집 서버로 이동합니다. 보고서에서 데이터를 사용하려면 먼저 다음 작업을 완료하십시오.

### 만들기 [!DNL Amazon S3] 버킷 및 데이터 소스

데이터가 Audience Manager 서버에 있으면 [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3]) 버킷 다음 모든 픽셀 데이터를 전송할 데이터 소스입니다. Audience Manager 컨설턴트나 [고객 지원 센터](https://experienceleague.adobe.com/docs/audience-manager/user-guide/help-and-legal/help-legal-contact.html) 지원이 필요한 경우

### Audience Manager 트레이트 및 세그먼트 만들기

이벤트 데이터는 다음과 같이 Audience Manager으로 유입됩니다 [사용되지 않는 신호](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/interactive-and-overlap-reports/unused-signals.html). 수동으로 만들기 [규칙 기반 특성](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) 수집된 데이터에서 만든 다음 [세그먼트](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segments-purpose.html) 보고서에서 데이터를 사용하려면 먼저 이러한 트레이트를 사용하십시오.

DSP의 특정 크리에이티브에 노출된 사용자의 사용자 수준 데이터를 채우는 트레이트의 예:

1. 다음으로 이벤트 식별 `d_event = imp`.
1. DSP 캠페인 내에서 광고 ID를 식별한 다음 트레이트에 `d_creative=[Creative ID]`.

![트레이트 만들기 화면](/help/dsp/assets/aa-trait.png)

>[!MORELIKETHIS]
>
>* [DSP 매크로](/help/dsp/campaign-management/macros.md)
>* [Adobe Audience Manager에 DSP Media Exposure 데이터 보내기 개요](overview.md)
>* [사용 사례](use-cases.md)

