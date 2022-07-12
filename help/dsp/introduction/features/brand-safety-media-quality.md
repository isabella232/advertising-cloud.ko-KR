---
title: 브랜드 안전 및 미디어 품질
description: 브랜드 안전 및 미디어 품질 기능에 대해 자세히 알아보십시오.
feature: DSP Introduction
exl-id: df5be5d4-490e-479f-b76d-4fda4acd4201
source-git-commit: b436936e3a0edcb78497fadb6f3c4086412baaa5
workflow-type: tm+mt
source-wordcount: '1365'
ht-degree: 0%

---

# 브랜드 안전 및 미디어 품질

<!-- Check on logo sizes in staging environment -- I made them all 100 pixels high except for DoubleVerify, which is 150 (harder to see at 100), but some instances look larger in VS Code. -->

Advertising Cloud DSP은 각 캠페인이 브랜드에 안전한 환경에서 실제 사용자에게 도달하도록 하는 브랜드 보호 기능 세트를 제공합니다.

Adobe의 사기 감시 팀은 [!DNL Interactive Advertising Bureau], [!DNL Trust and Accountability Group] [!DNL (TAG)], 및 [!DNL WhiteOps]을 입력하여 플랫폼에서 인벤토리를 신중하게 조정할 수 있습니다. DSP은 Adobe의 서비스 사전 관리를 통해 플랫폼의 모든 광고주가 인간이 아닌 트래픽(보트, 크롤러, 데이터 센터 트래픽 및 사기)으로부터 보호되고 안전한 컨텍스트에서만 게재되도록 합니다.

중앙 품질 관리를 제공하는 것 외에도 광고주가 자신의 브랜드에 맞는 컨트롤을 디자인할 수 있도록 권한을 부여하는 것이 좋습니다. Adobe Advertising Cloud은 과의 통합을 제공합니다 [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], [!DNL Oracle Data Cloud], 및 [!DNL Peer39]를 사용하여 각 광고주가 원하는 수준의 사기 방지, 상황별 필터링 및 키워드 타깃팅을 선택할 수 있도록 합니다.

## Advertising Cloud DSP 품질 이니셔티브

### 재고 확인 [!DNL Ads.txt] 지원

[[!DNL Ads.txt]에 대한 [!DNL Authorized Digital Sellers]](https://iabtechlab.com/ads-txt) 는 [!DNL Interactive Advertising Bureau] ([!DNL IAB])를 만들 수 있습니다. 참여하는 출판사 및 유통업체는 디지털 인벤토리를 판매할 수 있는 회사 및 이러한 관계의 특성을 `ads.txt` 페이지의 도메인 상단 수준(예: `example.com/ads.txt`).

DSP 지원 [!DNL ads.txt] 각 게시자의 `ads.txt` 파일 및 확인된 파일에서만 구매할 수 있는 옵션 제공 [!DNL ads.txt] 판매자. 예를 들어, 표시되는 판매자와 연결하여 `nytimes.com` 뉴욕 타임즈에 `ads.txt` 파일에서는 어떤 것이 합법적이며 그렇지 않은지 식별할 수 있으며, 이 배치가 검증된 판매자만을 구매하도록 구성된 경우 위반자를 차단합니다. <!-- can we actually mention NY Times? -->

기본값을 설정할 수 있습니다 [!DNL ads.txt] 각 광고주에 대한 컨트롤<!-- [default ads.txt controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->, 및 원할 경우 [각 배치에 대한 설정 사용자 정의](/help/dsp/campaign-management/placements/placement-settings.md) 변환:

* 도메인의 승인된 직접 판매자에서만 인벤토리 구매

* 도메인의 공인 직접 판매자 및 리셀러에서만 인벤토리 구매

* 도메인의 공인 직접 판매자 및 리셀러로부터 인벤토리 구매 우선 순위 지정

* 모든 판매자에서 재고 구매

### 플랫폼 사기 감시

DSP은 플랫폼 전반에서 사기를 관리하기 위한 강력한 내부 도구 및 시스템을 구축했으며, 다음과 같은 주요 업계 공급업체와 파트너 관계를 맺고 있습니다 [!DNL Whiteops] 및 [!DNL Integral Ad Science].

또한 Adobe은 [!DNL IAB] 및 [!DNL TAG] 다음과 같은 도구를 활용하여 Adobe의 광고주를 보호하기 위한 강력한 업계 표준 사기 방지 [!DNL ads.txt] (이전 섹션 참조), [!DNL IAB] 보트 및 스파이더 목록, 및 [!DNL TAG] 데이터 센터 IP 목록입니다.

품질에 대한 다차원 접근 방식을 통해 우리 팀은 예외 항목과 잘못된 트래픽 패턴을 모니터링하여 보호된 인벤토리에서 잘못된 트래픽을 3% 미만으로 보장합니다. 특정 도메인 또는 특정 게시자나 판매자의 인벤토리를 포함하여 의심스러운 모든 인벤토리는 플랫폼 전체에서 즉시 차단됩니다.

### 인벤토리 매핑, 계층화 및 분류

인벤토리 매핑은 플랫폼에 추가되기 전에 모든 새로운 인벤토리에 필요한 세부 검토 및 온보딩 프로세스입니다. 이 프로세스는 DSP에 있는 모든 인벤토리의 안전과 품질을 보장하기 위해 설계되었습니다.

* **매핑:** Adobe의 인벤토리 팀은 다음과 같은 측면을 평가하면서 각 도메인을 신중하게 검토합니다.

   * 브랜드 안전

   * 광고 유형 확인

   * 일반 컨텐츠, 중복 도메인 및 가짜 광고 서비스 제공

* **계층화:** 전체 에코시스템의 브랜드 존재를 전체적으로 검사하여 여러 계층 간에 인벤토리를 분류합니다. 다음을 수행할 수 있습니다 [배치 타겟팅](/help/dsp/campaign-management/placements/placement-settings.md) 원하는 도달 범위 동안 다음 계층을 참조하십시오.

   * **[!UICONTROL T1]** - 브랜드 이름, 국제적으로 인식 가능한 사이트

   * **[!UICONTROL T2]** - 사용자가 생성한 컨텐츠 없이 최신 컨텐츠로, 일반적으로 글로벌 인식이 부족한 멋진 웹 사이트

   * **[!UICONTROL T3]** - 사용자가 생성한 콘텐츠와 니치 컨텐츠

* **사이트 분류:** 쉽게 컨텐츠를 타깃팅하고 차단할 수 있도록 Adobe에서는 각 속성에 속성 컨텐츠를 기반으로 Advertising Cloud 정의 사이트 카테고리에 태그를 지정합니다. 다음을 수행할 수 있습니다 [각 배치에 대해 이러한 사이트 카테고리를 타깃팅하거나 제외합니다](/help/dsp/campaign-management/placements/placement-settings.md) 배치 목표를 기반으로 합니다.

### 사이트 차단에 대한 종합적인 지원

Advertising Cloud DSP은 전역적으로 차단된 사이트 목록과 광고주 및 계정에 대해 사용자 지정 차단 사이트 목록을 만드는 옵션을 제공합니다.

#### Advertising Cloud DSP 전역 차단 사이트 목록 {#global-blocked-sites}

Advertising Cloud DSP은 광고를 실행하기에 안전하지 않다고 간주되는 사이트의 전역적으로 차단된 사이트 목록을 유지 관리합니다. 이 목록에는 불쾌한 콘텐츠(예: 증오 또는 테러)와 보트, 유사 프리롤, 일치하지 않는 도메인 및 기타 부정 행위가 감염된 사이트가 있는 사이트가 포함되어 있습니다.

광고주를 사취한 활동을 근절하기 위한 Brand Safety 이니셔티브의 일환으로, 차트로 차단된 사이트 목록에서 모든 사이트들이 그 조치를 사용하여 차단됩니다. 브랜드 안전 검사를 통과하지 않는 모든 사이트는 전역 차단 사이트 목록에 추가됩니다. Advertising Cloud DSP은 이 목록을 동적으로 관리하므로 최신 브랜드 안전 분석을 기반으로 사이트에서 언제든지 목록 위 또는 아래로 이동할 수 있습니다.

전역적으로 차단된 사이트 목록에 사이트를 배치 대상으로 포함시키면 사이트가 빨간색 느낌표(!)로 플래그가 지정됩니다. 플래그가 지정된 사이트에서 광고가 실행되지 않음을 나타냅니다.

>[!NOTE]
>
>&quot;를 활성화하여 신뢰할 수 있는 비공개 거래에 첨부된 표준 디스플레이 광고에 대해 글로벌 차단 사이트 목록을 우회할 수도 있습니다.[!UICONTROL Allow unscreened sites]&quot; 옵션을 선택합니다 [배치 설정](/help/dsp/campaign-management/placements/placement-settings.md). 필요한 경우 [!DNL Adobe] 거래팀은 선택적으로 거래에 대한 게시자 설정에서 공개(경매 수준) 거래에 대한 사이트 차단을 비활성화할 수도 있습니다.

#### 계정 수준 및 광고주 수준의 차단된 사이트 목록

사용자는 계정 수준 및 광고주 수준의 차단된 사이트 목록을 유지 관리할 수도 있습니다<!-- [account-level and advertiser-level blocked sites lists](/help/dsp/admin/blocked-sites-list-edit.md) -->: 모든 배치에 자동으로 사용됩니다. 전역 차단 사이트 목록 외에 하위 차단 사이트 목록이 적용됩니다.

## 타사 통합

### 컨텍스트 기반 필터링

컨텍스트 기반 필터링을 사용하면 광고가 제공하는 페이지의 컨텍스트에 따라 광고 기회를 타깃팅하거나 차단할 수 있습니다. Adobe은 업계 선도적인 공급업체와의 통합을 통해 컨텍스트 기반의 필터링을 제공합니다. [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], 및 [!DNL Peer39]. 현재 필터의 예는 다음과 같습니다 [!UICONTROL Adult Content], [!UICONTROL Natural Disasters], [!UICONTROL Legal Drinking Age], [!UICONTROL MANGA], [!UICONTROL Epidemics], 및 [!UICONTROL G-rated Sites].

각 광고주에 대한 기본 컨텍스트 필터 컨트롤을 설정할 수 있습니다<!-- [default contextual filter controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->, 및 원할 경우 [각 배치에 대한 설정 사용자 정의](/help/dsp/campaign-management/placements/placement-settings.md). 이 기능을 사용하는 경우 추가 비용이 발생할 수 있습니다.

![Comscore 로고](/help/dsp/assets/comscore-logo.png) ![DoubleVerify 로고](/help/dsp/assets/doubleverify-logo.png) ![Integral Ad Science 로고](/help/dsp/assets/ias-logo.png) ![Peer39 로고](/help/dsp/assets/peer39-logo.png)

### 입찰 전 사기 차단

과의 타사 통합 활용 [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], 및 [!DNL Peer39] 캠페인에서 사람이 아닌 트래픽을 차단하려면 다음을 수행하십시오. 이러한 통합은 캠페인에서 업계 선도적인 입찰 전 차단 기능을 제공하여 캠페인에서 일반적이고 복잡한 잘못된 트래픽(GVT 및 SIVT)을 모두 최소화합니다.

각 광고주에 대한 기본 입찰 전 차단 컨트롤을 설정할 수 있습니다<!-- [default pre-bid fraud blocking controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->, 및 원할 경우 [각 배치에 대한 설정 사용자 정의](/help/dsp/campaign-management/placements/placement-settings.md). 이 기능을 사용하는 경우 추가 비용이 발생할 수 있습니다.

기능에 대한 자세한 내용은 원하는 공급업체에 직접 문의하거나 [!DNL Adobe] 계정 팀입니다.

![Comscore 로고](/help/dsp/assets/comscore-logo.png) ![DoubleVerify 로고](/help/dsp/assets/doubleverify-logo.png) ![Integral Ad Science 로고](/help/dsp/assets/ias-logo.png) ![Peer39 로고](/help/dsp/assets/peer39-logo.png)

### 사전 입찰 뷰가능 {#pre-bid-viewability}

업계 선도적인 파트너가 제공하는 사전 입찰 뷰가능 필터 [!DNL DoubleVerify], [!DNL Oracle Advertising] ([!DNL Moat]) 및 [!DNL Integral Ad Science] 광고주가 비디오 및 디스플레이 인벤토리에서 원하는 뷰가능 성과 목표를 캠페인이 충족하도록 할 수 있습니다.

각 광고주에 대한 기본 뷰기능 필터를 설정할 수 있습니다<!-- [default pre-viewability filters for each advertiser](/help/dsp/admin/advertiser-settings.md) -->, 및 원할 경우 [각 배치에 대한 설정 사용자 정의](/help/dsp/campaign-management/placements/placement-settings.md). 이 기능을 사용하는 경우 추가 비용이 발생할 수 있습니다.

![DoubleVerify 로고](/help/dsp/assets/doubleverify-logo.png) ![Oracle 광고 로고](/help/dsp/assets/oracle-advertising-logo.png) ![Integral Ad Science 로고](/help/dsp/assets/ias-logo.png)

### 항목 타깃팅

DSP 주제 타깃팅을 사용하면 업계 선도적인 컨텍스트 파트너를 활용하여 키워드 목록을 타깃팅하거나 차단할 수 있습니다 [!DNL Comscore] 및 [!DNL Oracle Data Cloud] ([!DNL Grapeshot]). 주제 타깃팅은 유해 컨텐츠를 차단하거나 더 큰 성과를 보장하는 컨텍스트에서 비용을 보장하는 등 브랜드에 맞는 환경에서 광고가 항상 제공되도록 하는 데 도움이 됩니다.

주제 타깃팅을 사용하려면 [!DNL Comscore] 또는 [!DNL Grapeshot] (사용 [!DNL Oracle Data Cloud]). 파트너 플랫폼에서 만들고 나면 다음 작업을 수행할 수 있습니다 [에서 세그먼트 ID 타깃팅 또는 제외 [!UICONTROL Audience Targeting] 각 배치의 섹션](/help/dsp/campaign-management/placements/placement-settings.md). 이 기능에 대한 추가 비용이 발생할 수 있습니다.

사용자 지정 주제 세그먼트를 만들려면 다음을 수행하십시오.

* 을(를) 만들려면 [!DNL Comscore] 계정을 설정하고 사용자 지정 세그먼트를 만듭니다. [!DNL Activation Segment Manager] at [https://agents.comscore.com](https://agents.comscore.com). 자세한 내용은 [[!DNL Comscore] 도움말 센터](https://comscoreactivation.zendesk.com/hc/) 을 참조하십시오. 사용자 지정 세그먼트에 대한 요금은 [!DNL Segment Manager] 만들 때

* 시작하려면 [!DNL Oracle Data Cloud], 연락처 [!DNL Oracle Data Cloud] 또는 [!DNL Adobe] 계정 팀입니다.

![Comscore 로고](/help/dsp/assets/comscore-logo.png) ![그래픽 핫 로고](/help/dsp/assets/oracle-grapeshot-logo.png)

### [!DNL DoubleVerify Authentic Brand Safety]

DSP은 [!DNL DoubleVerify] 그것을 제공하다 [!DNL Authentic Brand Safety] 타깃팅 솔루션: 일관성을 위해 모든 구매 플랫폼에서 타겟팅할 중앙 집중식 브랜드 안전 요구 사항 세트를 만들 수 있습니다.

다음을 빌드했으면 [!DNL DoubleVerify] 필요한 타깃팅이 있는 브랜드 안전 세그먼트를 DSP 내에서 사용하여 웹 환경에서 미리 입찰한 상태로 입찰 후 블록 규칙을 복제할 수 있습니다.

을(를) 지정할 수 있습니다 [!DNL DoubleVerify] 각 광고주의 세그먼트 ID<!-- [specify a DoubleVerify segment ID for each advertiser](/help/dsp/admin/advertiser-settings.md) -->, 및 원할 경우 [활성화 또는 비활성화 [!UICONTROL Authentic Brand Safety] 각 배치에 대해](/help/dsp/campaign-management/placements/placement-settings.md). DSP에서는 세그먼트 ID에 대한 사용을 위해 계정에 청구합니다.

기능에 대한 자세한 내용은 [!DNL DoubleVerify] 직접 또는 [!DNL Adobe] 계정 팀입니다.

![DoubleVerify 로고](/help/dsp/assets/doubleverify-logo.png)

>[!MORELIKETHIS]
>
>* [배치 설정](/help/dsp/campaign-management/placements/placement-settings.md)

<!-- >* [Advertiser Account Settings](/help/dsp/admin/advertiser-settings.md) -->
