---
title: 광고주 계정 설정
description: 사용 가능한 광고주 설정에 대한 설명을 참조하십시오.
source-git-commit: ee5621329aacf54777d28fa1c1f3d50949824cee
workflow-type: tm+mt
source-wordcount: '968'
ht-degree: 0%

---

# 광고주 계정 설정

*읽기 전용 사용자는 사용할 수 없음*

## [!UICONTROL General] 설정

**[!UICONTROL Advertiser Name]:** 광고주 이름입니다.

**[!UICONTROL Category]:** 광고주의 사업이 작동하는 카테고리입니다. 카테고리는 인벤토리로 입찰할 때 게시자에게 전달됩니다. 광고에 맞는 카테고리를 선택하거나 게시자가 광고를 거부할 수 있는지 확인합니다.

>[!NOTE]
>
>선택하는 경우 *[!UICONTROL Other]*&#x200B;로 설정되면 광고주가 DSP에 액세스할 수 없습니다 [!DNL On Demand Inventory].

**[!UICONTROL Advertiser URL]:** 광고주의 홈 페이지 또는 기본 웹 사이트 URL(시작 `http://` 또는 `https://`).

**[!UICONTROL Share all private exchange feeds into this advertiser]:** (새 광고주 계정만 해당) 조직의 DSP 계정에 대해 구성된 모든 비공개 Exchange 피드를 광고주가 사용할 수 있도록 합니다.

### [!UICONTROL Adobe IMS IDs]

추가 Adobe Experience Cloud 제품을 사용하는 광고주는 회사의 고유한 이름을 사용하여 일부 제품에서 데이터를 공유할 수 있습니다 [!DNL Organization ID] Experience Cloud. 에서 특정 제품 통합을 구성할 수 있습니다 [!UICONTROL Integrations] 섹션을 참조하십시오.

**[!UICONTROL Account IMS org and ID]:** (여러 광고주가 있는 Experience Cloud 계정을 통해 라이선스가 부여된 추가 Experience Cloud 제품이 있는 광고주) (선택 사항) 계정의 Experience Cloud [!DNL Organization ID].

**[!UICONTROL Advertiser IMS org and ID]:** (추가 Experience Cloud 제품에 대한 직접적인 라이선스가 있는 광고주) 선택 사항) 광고주의 Experience Cloud [!DNL Organization ID].

### [!UICONTROL Integrations]

(선택 사항) DSP 계정에 연결된 추가 Experience Cloud 제품. 제품은 동일한 Experience Cloud과 연결되어 있어야 합니다 [!DNL Organization ID] 에서 제공 [!UICONTROL Adobe IMS IDs] 섹션을 참조하십시오.

**[!UICONTROL Adobe Media Optimizer]:** (Advertising Cloud Search이 있거나 Advertising Cloud 변환 픽셀을 사용하는 광고주) A [!DNL Search] DSP에서 속성 데이터를 교환할 계정.

**[!UICONTROL Adobe Device Co-op or 3rd Party Graph]:** (Advertising Cloud 변환 픽셀을 사용하는 광고주) (선택 사항) Advertising Cloud Search에서 광고주 계정 설정에서 개인 기반 속성 측정에 장치 그래프를 사용할 수 있습니다.

>[!NOTE]
>
> * 장치 속성은 Adobe Analytics에서 추적한 전환이 아니라 Advertising Cloud 전환 추적 서비스를 사용하여 추적된 전환에만 사용할 수 있습니다.
> * 또한 에서 장치 간 타깃팅 및 빈도 관리를 위한 개인 기반 장치 그래프를 선택할 수도 있습니다 [캠페인 수준](/help/dsp/campaign-management/campaigns/campaign-settings.md). 그런 다음 에서 교차 장치 타깃팅을 설정할 수 있습니다 [배치 수준](/help/dsp/campaign-management/placements/placement-settings.md) 그리고 추가 주파수 캡은 [패키지 수준](/help/dsp/campaign-management/packages/package-settings.md) 및 [배치 수준](/help/dsp/campaign-management/placements/placement-settings.md). 교차 장치 타깃팅 및 빈도 관리에는 광고주 수준 기여도 분석이 필요하지 않습니다. 대신 캠페인 설정에 지정된 장치 그래프로 작동합니다.


**[!UICONTROL Adobe Analytics]:** (Adobe Analytics을 사용하는 광고주) 선택 사항; 다음을 포함하는 Advertising Cloud 전환 추적 태그를 사용하여 수집된 데이터에만 적용 가능 [!DNL EF Redirect] 및 토큰만) 하나 이상 [!DNL Analytics] DSP이 게시자 및 공급측 파트너에서 수집하는 데이터를 전송할 보고서 세트입니다. 또한 Analytics는 클라이언트의 사이트에서 수집한 데이터를 DSP으로 보냅니다.

데이터가 보고서 세트에 표시되려면 [!DNL Search] advertiser 수준 설정을 &quot;(으)로 설정[!UICONTROL Enable tracking for SAINT feeds]&quot;을(를) 활성화해야 합니다. 또한 광고주는 [!DNL Analytics] Advertising Cloud에서 데이터를 수신하려면 계정을 구성해야 합니다. <!-- from Advertising Cloud or DSP in particular? Add cross-reference to file in Integrations section. -->

>[!WARNING]
>
>이전에 연결된 보고서 세트를 제거하면 DSP이 더 이상 해당 세트와 데이터를 교환하지 않습니다. 데이터 변동이 예상됩니다. <!-- Fluctuations where? Clarify -->

**[!UICONTROL Adobe Analytics Cloud]:** (Adobe Audience Manager 또는 Adobe Analytics을 사용하는 광고주) 선택 사항) Audience Manager 또는 [!DNL Analytics] DSP에서 모든 광고주의 Adobe 대상에 대한 세그먼트 메타데이터, 계층 데이터 및 고유한 대상 데이터를 가져오는 계정입니다. 여기에는 다음에 대한 데이터가 포함됩니다.

* Audience Manager 세그먼트
* [!DNL Analytics] Adobe Experience Cloud에 게시된 세그먼트
* Adobe Experience Cloud에서 [!DNL People core service]
* Adobe Experience Platform에서 만들어지고 Audience Manager을 통해 Advertising Cloud으로 전송되는 세그먼트

초기 동기화는 24시간 정도 걸립니다. 그 후 데이터는 1~2초 지연을 사용하여 실시간으로 동기화됩니다.
<!-- I don't think this is true anymore:
Segment membership data is sent to Advertising Cloud only after one of the following:

* The segment is targeted in an Advertising Cloud placement or audience library
* The segment is added to the Advertising Cloud batch and real-time destinations within the Audience Manager user interface
-->

## [!UICONTROL Targeting] 설정

광고주의 새 배치에 대한 기본 대상을 선택적으로 구성할 수 있습니다. 사용자는 모든 새 배치에 대한 기본 대상을 재정의할 수 있습니다.

### [!UICONTROL Geo-targeting]

**[!UICONTROL Countries]:** 각 배치의 지역 타깃팅에 대한 기본 국가입니다. 사용자는 각 배치에 대해 국가를 변경하고 보다 구체적인 지역 타깃팅을 구성할 수 있습니다.

### [!UICONTROL Audience Targeting]

**[!UICONTROL Audiences to exclude]:** 기본적으로 제외할 대상 또는 세그먼트. 사용자는 각 배치에 대한 제외를 변경할 수 있습니다.

### [!UICONTROL Media Quality]

#### [!UICONTROL Contextual Filtering]

유형 [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], 및 [!DNL Peer39] 적용할 상황별 필터. 에서 광고주 수준 설정을 재정의할 수 있습니다 [배치 수준](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-context}

**[!UICONTROL Block sites that are]:** (선택 사항) 기본적으로 차단할 하나 이상의 유형의 재고 컨텍스트. 추가 비용이 발생할 수 있습니다.

##### [!UICONTROL Peer 39] {#peer39-context}

**[!UICONTROL Target sites that are]:** (선택 사항) 기본적으로 타깃팅할 하나 이상의 유형의 재고 속성입니다. 추가 비용이 발생할 수 있습니다.

##### [!UICONTROL ComScore]

**[!UICONTROL Block sites that are]:** (선택 사항) 기본적으로 차단할 하나 이상의 유형의 재고 속성입니다. 추가 비용이 발생할 수 있습니다.

##### [!UICONTROL Integral Ad Science] {#ias-context}

**[!UICONTROL Adult Content]:** (선택 사항) 기본적으로 광고를 차단할 성인물 콘텐츠의 정도입니다. *[!UICONTROL Do Not Block]* (기본값), *[!UICONTROL Standard]*, 또는 *[!UICONTROL Strict]*. 추가 비용이 발생할 수 있습니다.

**[!UICONTROL Alcohol Content]:** (선택 사항) 기본적으로 광고를 차단하는 알코올 도입니다. *[!UICONTROL Do Not Block]* (기본값), *[!UICONTROL Standard]*, 또는 *[!UICONTROL Strict]*. 추가 비용이 발생할 수 있습니다.

#### [!UICONTROL Pre-Bid Fraud Blocking]

측정된 부정 트래픽과 의심스러운 활동을 기반으로 차단할 사이트 유형 [!DNL DoubleVerify], [!DNL Integral Ad Science], 및 [!DNL Peer39]. 에서 광고주 수준 설정을 재정의할 수 있습니다 [배치 수준](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-fraud}

**[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** 기본적으로 는 새 배치에 대해 납치된 장치의 트래픽을 포함하여 100% 잘못된 트래픽을 모두 차단합니다. 추가 비용이 발생할 수 있습니다.

**[!UICONTROL Also block sites with]:** (선택 사항) 기본적으로 DSP에서 광고를 차단하는 추가 사기 및 잘못된 트래픽 수준입니다.  *[!UICONTROL None]* (추가 트래픽을 차단하지 않는 기본값), *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]*, 또는 *[!UICONTROL >25% Average Fraud/IVT levels]*. 추가 비용이 발생할 수 있습니다.

##### [!UICONTROL Peer 39] {#peer-39-fraud}

**[!UICONTROL Block sites that are]:** (선택 사항) DSP에서 기본적으로 광고를 차단하는 하나 이상의 사기 유형입니다. *[!UICONTROL Fraud]* (사기 행위로 모든 사이트를 차단함), *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]*, 및/또는 *[!UICONTROL Fraud: Zero Ads]*. 추가 비용이 발생할 수 있습니다.

##### [!UICONTROL Integral Ad Science] {#ias-fraud}

**[!UICONTROL Block sites that are]:** (선택 사항) DSP이 기본적으로 광고를 차단하도록 하는 의심스러운 웹 사이트 또는 앱 활동 유형입니다. *[!UICONTROL None]* (의심스러운 활동을 기반으로 광고를 차단하지 않는 기본값), *[!UICONTROL Suspicious Activity - High Risk]*, 또는 *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. 추가 비용이 발생할 수 있습니다.

#### [!UICONTROL Ads.text]

**[!UICONTROL Ads.txt Filtering]:** 기본적으로 [[!DNL Ads.txt] 입찰 전 필터링](https://iabtechlab.com/ads-txt-about/) 각 게시자의 [!DNL Authorized Digital Sellers] 목록:
* *[!UICONTROL Opt out of ads.txt (default)]*: 모든 판매자로부터 재고를 구입하기 위해서.
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*: 도메인의 공인 직접 판매자 및 리셀러에서 인벤토리 구매에 우선 순위를 두기
* *[!UICONTROL Ads.txt sellers only]*: 도메인의 공인 직접 판매자와 리셀러에서만 인벤토리를 구매하려면
* *[!UICONTROL Ads.txt sellers only]*: 도메인의 공인 직접 판매자로부터 인벤토리를 구입하기 위해

에서 광고주 수준 설정을 재정의할 수 있습니다 [배치 수준](/help/dsp/campaign-management/placements/placement-settings.md).

#### [!UICONTROL Safe Site Block]

**[!UICONTROL Enable Site Safety Block]:** 기본적으로 에서는 광고가 광고주가 타깃팅하는 사이트에서 제공되도록 실시간 입찰 후 필터를 활성화합니다. <!-- Can remove this: Users can enable or disable the feature for each placement. I don't see this option, but I should probably verify. If this can't be edited at placement level, then remove "By default." If it can, say that you can override at placement level. -->

#### [!UICONTROL DoubleVerify Authentic Brand Safety]

**[!UICONTROL DoubleVerify Account]:** ([!DNL DoubleVerify] 고객만 (선택 사항) 조직의 [!DNL DoubleVerify] 계정이 필요합니다.

**[!UICONTROL Enable Authentic Brand Safety]:** (선택 사항) 기본적으로 [!DNL DoubleVerify] 지정된 세그먼트 ID에 대해 구성된 사용자 지정 브랜드 안전 규칙을 사용하여 입찰 후 노출 횟수를 차단하는 인증 브랜드 안전. DSP에서는 세그먼트 ID에 대한 사용을 위해 계정에 청구합니다.

배치 수준에서 광고주 수준 설정을 재정의할 수 있습니다.

>[!MORELIKETHIS]
>
>* [광고주 계정 만들기](/help/dsp/admin/advertiser-create.md)


<!-- >* [View the Advertiser List for the Account](/help/dsp/admin/advertiser-view.md) -->
