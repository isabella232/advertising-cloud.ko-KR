---
title: Adobe Audience Manager와의 Adobe 광고 통합
description: Adobe 광고에서 Adobe Audience Manager과 데이터를 교환할 수 있는 다양한 방법에 대해 알아봅니다.
feature: Integration with Adobe Audience Manager
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---

# Adobe Audience Manager와의 Adobe 광고 통합

다음과 같은 방법으로 Adobe 광고를 Audience Manager과 통합할 수 있습니다.

## Audience Manager 및 기타 동기화 [!DNL Adobe] 광고 타깃팅용 세그먼트

[!DNL Search] 및 DSP은 광고주 또는 기관의 Audience Manager 및 기타 모든 대상에 대한 메타데이터, 계층 데이터 및 고유한 대상 데이터를 가져올 수 있습니다 [!DNL Adobe] 대상. 이 고유한 연결은 Adobe 광고를 사용하는 마케터만 사용할 수 있습니다. 참조:[광고 타깃팅용 Adobe Audience Manager 세그먼트 가져오기](/help/integrations/audience-manager/import-audiences.md).&quot;

### Audience Manager 및 기타 사용 [!DNL Adobe] 만들 세그먼트 [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*옵트인 광고주 [!DNL Advertising Search] 전용*

[!DNL 내 [!DNL Search]], [!DNL Google Ads] Google 고객 일치 타겟팅 [!UICONTROL Adobe Media Optimizer (HTTP)] 및 [!UICONTROL Adobe Media Optimizer Batch Destination] 를 대상으로 사용할 수 있습니다. ([!DNL Media Optimizer] 는 [!DNL의 이전 이름입니다. [!DNL Search]참조). 여기에는 Adobe Experience Cloud에 게시된 Adobe Analytics 세그먼트와 [!DNL People core service]. 자세한 내용은 [!DNL 내의 제품 내 도움말을 참조하십시오 [!DNL Search]]

[사용자 ID의 고객 일치 대상](https://support.google.com/google-ads/answer/9199250) 웹 사이트 태그 기반 대상처럼 작동하지만, 비PII ID는 표준 고객 일치 및 웹 사이트 태그 기반 대상자보다 고유한 이점을 위해 고유 대상 구성원에게 할당됩니다.

필요한 사용자 ID를 만들려면 Adobe 광고 JavaScript 태그를 사용해야 합니다 <!-- with a user ID parameter -->클릭합니다. [!DNL에 문의 [!DNL Search]] 계정 팀에서 자세한 내용을 확인하십시오.

![세그먼트 생성 프로세스](/help/integrations/assets/ad_search_user_id_pic.png)

대상자를 만들면 여기에서 대상자를 사용할 수 있습니다. [!DNL Google Ads] 캠페인 [캠페인 수준 또는 광고 그룹 수준 타겟 또는 제외](#audience-manager-targets).

### Audience Manager 및 기타 사용 [!DNL Adobe] Target 또는 제외시킬 세그먼트 {#audience-manager-targets}

* ([!DNL 사용 시 옵트인 광고주) [!DNL Search]]) 모든 [!DNL Google Ads] 대상 [다음을 사용하여 생성 [!DNL Adobe] 세그먼트](#audience-manager-google-audiences) 캠페인 수준 또는 광고 그룹 수준 타겟 또는 제외 [!DNL Google Ads] 캠페인.

* (DSP을 사용하는 광고주) 기존 [!DNL Adobe] 세그먼트를 광고 배치 대상으로 사용할 수 있습니다. 선택적으로 재사용 가능한 대상에 세그먼트를 포함할 수 있습니다. 이 세그먼트를 여러 배치에 대한 타겟 또는 제외로 사용할 수 있습니다.

* (Advertising Creative를 사용하는 광고주) 기존 [!DNL Adobe] 세그먼트를 광고 경험에서 특정 크리에이티브를 위한 타겟으로 사용할 수 있습니다.

>[!NOTE]
>
>Audience Manager 및 Experience Cloud에서 대상을 만드는 방법에 대한 자세한 정보 [!DNL Audience Library] 인터페이스 및 다양한 대상 유형에 대한 일반적인 사용 사례는 &quot;[대상 만들기 옵션](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html).&quot;

## DSP Media Exposure 데이터를 Audience Manager에 전송

*DSP만 사용하는 광고주*

Adobe Audience Manager을 사용하는 DSP 고객은 Audience Manager에 대한 픽셀 호출을 사용하여 광고 캠페인에서 데이터를 캡처할 수 있습니다. 그런 다음 캠페인 데이터를 사용하여 규칙 기반 트레이트를 작성할 수 있습니다. 이 트레이트를 사용하면 새로운 세그먼트를 정의하여 고급 세그멘테이션, 빈도 관리, 마케팅 분석 및 보고 통찰력과 같은 다양한 DSP 사용 사례를 활성화할 수 있습니다.

참조:[Adobe Audience Manager에 DSP Media Exposure 데이터 보내기 개요](/help/integrations/audience-manager/media-data-integration/overview.md)&quot;&quot;을 참조하십시오.

## Audience Analytics을 사용하여 사이트 활동에 대한 보다 풍부한 통찰력 얻기

광고 고객 Adobe [[!DNL Adobe][!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) 은 광고 추적 데이터 및 Audience Manager 세그먼트를 모두 [!DNL Analytics] 사이트 활동에 대한 보강된 인사이트를 제공합니다.

자세한 내용은 &quot;[[!DNL Adobe][!DNL Audience Analytics] Adobe 광고 고객용](/help/integrations/audience-manager/audience-analytics.md).&quot;
