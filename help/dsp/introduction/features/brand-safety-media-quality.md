---
title: 브랜드 안전 및 미디어 품질
description: 브랜드 안전 및 미디어 품질 기능에 대해 자세히 알아보십시오.
feature: Introduction
exl-id: df5be5d4-490e-479f-b76d-4fda4acd4201
source-git-commit: e2ee41c7e3e195f062ad1cc67080ed913d6d3d06
workflow-type: tm+mt
source-wordcount: '1266'
ht-degree: 0%

---

# 브랜드 안전 및 미디어 품질

<!-- Check on logo sizes in staging environment -- I made them all 100 pixels high except for DoubleVerify, which is 150 (harder to see at 100), but some instances look larger in VS Code. -->

Advertising Cloud DSP은 각 캠페인이 브랜드에 안전한 환경에서 실제 사용자에게 도달하도록 하는 브랜드 보호 기능 세트를 제공합니다.

Adobe의 사기 감시 팀은 [!DNL Interactive Advertising Bureau], [!DNL Trust and Accountability Group] [!DNL (TAG)] 및 [!DNL WhiteOps]와 같은 업계 선도적인 파트너와 긴밀히 협력하여 플랫폼에서 인벤토리를 신중하게 조정하고 있습니다. DSP은 Adobe의 서비스 사전 관리를 통해 플랫폼의 모든 광고주가 인간이 아닌 트래픽(보트, 크롤러, 데이터 센터 트래픽 및 사기)으로부터 보호되고 안전한 컨텍스트에서만 게재되도록 합니다.

중앙 품질 관리를 제공하는 것 외에도 광고주가 자신의 브랜드에 맞는 컨트롤을 디자인할 수 있도록 권한을 부여하는 것이 좋습니다. Adobe Advertising Cloud은 [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], [!DNL Oracle Data Cloud] 및 [!DNL Peer39]와의 통합을 제공하여 각 광고주가 원하는 수준의 사기 방지, 상황별 필터링 및 키워드 타깃팅을 선택할 수 있도록 합니다.

## Advertising Cloud DSP 품질 이니셔티브

### [!DNL Ads.txt] 지원을 통해 인벤토리 확인

[[!DNL Ads.txt], which stands for [!DNL Authorized Digital Sellers]](https://iabtechlab.com/ads-txt) 이 계획은  [!DNL Interactive Advertising Bureau] ([!DNL IAB])가 2017년 6월에 공개 시장에서의 적절한 재고 표현을 용이하게 함으로써 불법 트래픽 및 도메인 스푸핑과 싸울 수 있도록 하기 위해 개시된다. 참여하는 게시자 및 배포자는 도메인 최상위 수준(예: `example.com/ads.txt`)에서 `ads.txt` 페이지를 유지 관리하여 디지털 인벤토리를 판매할 수 있는 회사 및 이러한 관계의 특성을 공개적으로 선언합니다.

DSP은 각 게시자의 `ads.txt` 파일을 읽고 확인된 [!DNL ads.txt] 판매자에서만 구매할 수 있는 옵션을 제공하여 [!DNL ads.txt] 을 지원합니다. 예를 들어, `nytimes.com` 액세스를 New York Times의 `ads.txt` 파일에 액세스하는 판매자와 일치시킴으로써 우리는 어느 것이 합법적인지, 그리고 어떤 것이 아닌지를 식별할 수 있고, 배치가 검증된 판매자만을 구매하도록 구성된 경우 위반자를 차단합니다. <!-- can we actually mention NY Times? -->

각 광고주에 대해 기본 [!DNL ads.txt] 컨트롤을 설정한 다음 선택적으로 [각 배치](/help/dsp/campaign-management/placements/placement-settings.md)에 대한 설정을 다음 위치로 사용자 지정할 수 있습니다.<!-- [default ads.txt controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->

* 도메인의 승인된 직접 판매자에서만 인벤토리 구매

* 도메인의 공인 직접 판매자 및 리셀러에서만 인벤토리 구매

* 도메인의 공인 직접 판매자 및 리셀러로부터 인벤토리 구매 우선 순위 지정

* 모든 판매자에서 재고 구매

### 플랫폼 사기 감시

DSP은 Adobe 플랫폼 전반에서 사기를 관리하기 위한 강력한 내부 도구 및 시스템을 구축했으며, [!DNL Whiteops] 및 [!DNL Integral Ad Science] 과 같은 주요 업계 공급업체와 파트너 관계를 맺고 있습니다.

또한 Adobe은 [!DNL IAB] 및 [!DNL TAG]과 밀접하게 연동하여 Adobe의 광고주를 보호하기 위해 [!DNL ads.txt](이전 섹션 참조), [!DNL IAB] 보트 및 스파이더 목록, [!DNL TAG] 데이터 센터 IP 목록과 같은 도구를 활용합니다.

품질에 대한 다차원 접근 방식을 통해 우리 팀은 예외 항목과 잘못된 트래픽 패턴을 모니터링하여 보호된 인벤토리에서 잘못된 트래픽을 3% 미만으로 보장합니다. 특정 도메인 또는 특정 게시자나 판매자의 인벤토리를 포함하여 의심스러운 모든 인벤토리는 플랫폼 전체에서 즉시 차단됩니다.

### 인벤토리 매핑, 계층화 및 분류

인벤토리 매핑은 플랫폼에 추가되기 전에 모든 새로운 인벤토리에 필요한 세부 검토 및 온보딩 프로세스입니다. 이 프로세스는 DSP에 있는 모든 인벤토리의 안전과 품질을 보장하기 위해 설계되었습니다.

* **매핑:** 재고 팀은 다음과 같은 측면을 평가하면서 각 도메인을 신중하게 검토합니다.

   * 브랜드 안전

   * 광고 유형 확인

   * 일반 컨텐츠, 중복 도메인 및 가짜 광고 서비스 제공

* **계층화:** 전체 에코시스템의 브랜드 존재를 전체적으로 검사하여 여러 계층 간에 인벤토리를 분류합니다. [배치를 이러한 계층에 타겟팅하여 원하는 도달 범위를 지정할 수 있습니다.](/help/dsp/campaign-management/placements/placement-settings.md)

   * **[!UICONTROL T1]** - 브랜드 이름, 국제적으로 인식 가능한 사이트

   * **[!UICONTROL T2]** - 사용자가 생성한 컨텐츠 없이 최신 컨텐츠로, 일반적으로 글로벌 인식이 부족한 멋진 웹 사이트

   * **[!UICONTROL T3]** - 사용자가 생성한 콘텐츠와 니치 컨텐츠

* **사이트 분류:** 쉬운 컨텐츠 타깃팅 및 차단을 위해 Adobe에서는 각 속성에 대한 컨텐츠를 기반으로 Advertising Cloud 정의 사이트 카테고리로 태그를 지정합니다. 배치 목표를 기준으로 각 배치에 대해 [이러한 사이트 카테고리를 타깃팅하거나 제외할 수 있습니다](/help/dsp/campaign-management/placements/placement-settings.md).

### 사이트 차단에 대한 종합적인 지원

Advertising Cloud DSP은 전역적으로 차단된 사이트 목록과 광고주 및 계정에 대해 사용자 지정 차단 사이트 목록을 만드는 옵션을 제공합니다.

#### Advertising Cloud DSP 전역 차단 사이트 목록

Advertising Cloud DSP은 광고를 실행하기에 안전하지 않다고 간주되는 사이트의 전역적으로 차단된 사이트 목록을 유지 관리합니다. 이 목록에는 불쾌한 콘텐츠(예: 증오 또는 테러)와 보트, 유사 프리롤, 일치하지 않는 도메인 및 기타 부정 행위가 감염된 사이트가 있는 사이트가 포함되어 있습니다.

광고주를 사취한 활동을 근절하기 위한 Brand Safety 이니셔티브의 일환으로, 차트로 차단된 사이트 목록에서 모든 사이트들이 그 조치를 사용하여 차단됩니다. 브랜드 안전 검사를 통과하지 않는 모든 사이트는 전역 차단 사이트 목록에 추가됩니다. Advertising Cloud DSP은 이 목록을 동적으로 관리하므로 최신 브랜드 안전 분석을 기반으로 사이트에서 언제든지 목록 위 또는 아래로 이동할 수 있습니다.

전역적으로 차단된 사이트 목록에 사이트를 배치 대상으로 포함시키면 사이트가 빨간색 느낌표(!)로 플래그가 지정됩니다. 플래그가 지정된 사이트에서 광고가 실행되지 않음을 나타냅니다.

#### 계정 수준 및 광고주 수준의 차단된 사이트 목록

또한 사용자는 모든 배치에 자동으로 사용되는 계정 수준 및 광고주 수준의 차단된 사이트 목록<!-- [account-level and advertiser-level blocked sites lists](/help/dsp/admin/blocked-sites-list-edit.md) -->을 유지할 수 있습니다. 전역 차단 사이트 목록 외에 하위 차단 사이트 목록이 적용됩니다.

## 타사 통합

### 컨텍스트 기반 필터링

컨텍스트 기반 필터링을 사용하면 광고가 제공하는 페이지의 컨텍스트에 따라 광고 기회를 타깃팅하거나 차단할 수 있습니다. Adobe은 업계 선도적인 공급업체와의 통합을 통해 컨텍스트 기반의 필터링을 제공합니다. [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] 및 [!DNL Peer39]. 현재 필터의 예로는 [!UICONTROL Adult Content], [!UICONTROL Natural Disasters], [!UICONTROL Legal Drinking Age], [!UICONTROL MANGA], [!UICONTROL Epidemics] 및 [!UICONTROL G-rated Sites]가 있습니다.

각 광고주에 대한 기본 컨텍스트 필터 컨트롤을 설정한 다음 선택적으로 [각 배치](/help/dsp/campaign-management/placements/placement-settings.md)에 대한 설정을 사용자 지정할 수 있습니다. <!-- [default contextual filter controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> 이 기능을 사용하는 경우 추가 비용이 발생할 수 있습니다.

![Comscore ](/help/dsp/assets/comscore-logo.png) ![로고DoubleVerify ](/help/dsp/assets/doubleverify-logo.png) ![로고Integral Ad Science ](/help/dsp/assets/ias-logo.png) ![로고Peer39 로고](/help/dsp/assets/peer39-logo.png)

### 입찰 전 사기 차단

[!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] 및 [!DNL Peer39]와의 타사 통합을 활용하여 캠페인에서 비인적 트래픽을 차단하십시오. 이러한 통합은 캠페인에서 업계 선도적인 입찰 전 차단 기능을 제공하여 캠페인에서 일반적이고 복잡한 잘못된 트래픽(GVT 및 SIVT)을 모두 최소화합니다.

각 광고주에 대한 기본 입찰 전 차단 컨트롤을 설정한 다음 선택적으로 [각 배치](/help/dsp/campaign-management/placements/placement-settings.md)에 대한 설정을 사용자 지정할 수 있습니다. <!-- [default pre-bid fraud blocking controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> 이 기능을 사용하는 경우 추가 비용이 발생할 수 있습니다.

기능에 대한 자세한 내용은 원하는 공급업체에 직접 문의하거나 Adobe 계정 관리자에게 문의하십시오.

![Comscore ](/help/dsp/assets/comscore-logo.png) ![로고DoubleVerify ](/help/dsp/assets/doubleverify-logo.png) ![로고Integral Ad Science ](/help/dsp/assets/ias-logo.png) ![로고Peer39 로고](/help/dsp/assets/peer39-logo.png)

### 사전 입찰 뷰가능 {#pre-bid-viewability}

업계 선도적인 파트너 [!DNL DoubleVerify], [!DNL Oracle Advertising]([!DNL Moat]) 및 [!DNL Integral Ad Science]에서 제공하는 사전 입찰 뷰가능 필터를 통해 광고주가 비디오 및 디스플레이 인벤토리에서 원하는 뷰가능 성능 목표를 달성하도록 할 수 있습니다.

각 광고주에 대한 기본 보기 가능 필터를 설정한 다음 선택적으로 [각 배치](/help/dsp/campaign-management/placements/placement-settings.md)에 대한 설정을 사용자 지정할 수 있습니다. <!-- [default pre-viewability filters for each advertiser](/help/dsp/admin/advertiser-settings.md) --> 이 기능을 사용하는 경우 추가 비용이 발생할 수 있습니다.

![DoubleVerify ](/help/dsp/assets/doubleverify-logo.png) ![로고Oracle Advertising ](/help/dsp/assets/oracle-advertising-logo.png) ![로고Integral Ad Science 로고](/help/dsp/assets/ias-logo.png)

### 항목 타깃팅

DSP 주제 타깃팅을 사용하면 업계를 선도하는 컨텍스트 파트너 [!DNL Comscore] 및 [!DNL Oracle Data Cloud]([!DNL Grapeshot])를 활용하여 키워드 목록을 타깃팅하거나 차단할 수 있습니다.

주제 타깃팅은 유해 컨텐츠를 차단하거나 더 큰 성과를 보장하는 컨텍스트에서 비용을 보장하는 등 브랜드에 맞는 환경에서 광고가 항상 제공되도록 하는 데 도움이 됩니다.

주제 타깃팅을 사용하려면 [!DNL Comscore] 또는 [!DNL Grapeshot]([!DNL Oracle Data Cloud] 사용)로 직접 주제 세그먼트를 만들어야 합니다. 파트너 플랫폼에서 만들어진 후에는 각 배치](/help/dsp/campaign-management/placements/placement-settings.md)에 대해 [섹션에서 세그먼트 ID를 타깃팅하거나 제외할 수 있습니다. [!UICONTROL  Audience Targeting] 이 기능에 대한 추가 비용이 발생할 수 있습니다.

시작하려면 선호하는 공급업체 또는 Adobe 계정 관리자에게 문의하십시오.

![Comscore ](/help/dsp/assets/comscore-logo.png) ![로고그래픽 핫 로고](/help/dsp/assets/oracle-grapeshot-logo.png)

### [!DNL DoubleVerify Authentic Brand Safety]

DSP은 [!DNL DoubleVerify]과 파트너 관계를 맺고 [!DNL Authentic Brand Safety] 타겟팅 솔루션을 제공합니다. 이를 통해 모든 구매 플랫폼에서 일관성을 위해 중앙 집중식 브랜드 안전 요구 사항 세트를 만들 수 있습니다.

필요한 타깃팅으로 [!DNL DoubleVerify] 브랜드 안전 세그먼트를 구축한 후에는 DSP 내에서 사용하여 웹 환경에서 사전 입찰로 입찰 후 블록 규칙을 복제할 수 있습니다.

각 광고주<!-- [specify a DoubleVerify segment ID for each advertiser](/help/dsp/admin/advertiser-settings.md) -->에 대해 [!DNL DoubleVerify] 세그먼트 ID를 지정한 다음, 원할 경우 [각 배치에 대해 [!UICONTROL Authentic Brand Safety]을 활성화하거나 비활성화할 수 있습니다](/help/dsp/campaign-management/placements/placement-settings.md). DSP에서는 세그먼트 ID에 대한 사용을 위해 계정에 청구합니다.

기능에 대한 자세한 내용은 [!DNL DoubleVerify] 직접 문의하거나 Adobe 계정 관리자에게 문의하십시오.

![DoubleVerify 로고](/help/dsp/assets/doubleverify-logo.png)

>[!MORELIKETHIS]
>
>* [배치 설정](/help/dsp/campaign-management/placements/placement-settings.md)

<!-- >* [Advertiser Account Settings](/help/dsp/admin/advertiser-settings.md) -->
