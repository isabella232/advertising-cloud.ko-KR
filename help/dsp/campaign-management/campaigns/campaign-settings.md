---
title: 캠페인 설정
description: 사용 가능한 캠페인 설정에 대한 설명을 참조하십시오.
feature: Campaigns
exl-id: ff2e22ff-8073-4532-884b-36e0c1f22641
source-git-commit: e2ee41c7e3e195f062ad1cc67080ed913d6d3d06
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 캠페인 설정

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]:** 캠페인 이름입니다.

**[!UICONTROL Advertiser]:** (기존 캠페인의 읽기 전용) 해당 광고주(브랜드)입니다. 기존 광고주를 선택하거나 새 광고주를 만듭니다.

**[!UICONTROL Advertiser URL]:** 광고주의 공식 페이지입니다. 이 필드는 인벤토리 파트너와 함께 광고 승인 프로세스를 가속화합니다.

**[!UICONTROL Timezone]:** (기존 캠페인의 읽기 전용) 보고 및 입찰의 시간대입니다.

**[!UICONTROL Customer PO]:**  (선택 사항) 삽입 주문/구매 발주를 위한 고객 구매 발주입니다.

**[캠페인 날짜]:** 캠페인 시작 및 종료 날짜입니다.

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]:** 캠페인의 여백을 관리할지 여부:  *[!UICONTROL Yes]* 또는  *[!UICONTROL No]* (기본값)

*[!UICONTROL Yes],*&#x200B;을 선택하는 경우 여백 유형 및 금액을 지정합니다.

* **[!UICONTROL Margin Type]:** 여백의 유형입니다. 여백 관리를 활성화하고 캠페인을 저장한 후에는 여백 유형을 변경할 수 없습니다.

   * *[!UICONTROL Fixed]:* (기본값) Advertising Cloud DSP에서 페이지의 고정된 여백률을 기반으로 하여 지출을 자동 계산하고 제한할 수  [!UICONTROL Gross Budget]있습니다.

   * *[!UICONTROL Dynamic]:* 캠페인에서 각 패키지 및 배치에 대해 별도의  [!UICONTROL Budget Reserve %] 및 [!UICONTROL Gross Budget] 를 지정하여 여백을 배치 수준까지 관리할 수 있습니다. Advertising Cloud DSP은 특정 여백을 보장하지 않고 각 배치의 재무 효율성을 기반으로 최적화합니다. 고정 비율로 고정 수량 또는 단위 유형을 제공하기로 동의한 여러 라인 항목으로 구성된 삽입 주문에 사용합니다.

* **[!UICONTROL Fixed Margin %]:** (여백이 고정된 캠페인 전용) 각 삽입 순서에 대한 기본 마크업 <!-- impression? -->을 백분율로 표시합니다. 이 금액은 [!UICONTROL Gross Budget]에서 공제되어 순 캠페인 예산을 정의합니다.

* **[!UICONTROL Budget Reserve %]:** (고정된 여백 전용 캠페인 (선택 사항) 지정된 백분율을  [!UICONTROL Gross Budget] 세이프가드로서 예약합니다. 이 금액은 [!UICONTROL Gross Budget]에서 공제되어 순 캠페인 예산을 정의합니다.

**[!UICONTROL Gross Budget]:** (마진 관리만 있는 캠페인) 지정된 한계 조정이 적용되기 전의 총 캠페인 예산입니다.

일일, 주별 또는 월별 총 예산을 추가할 수도 있습니다.

1. 클릭 **[!UICONTROL Add an additional Gross Budget]**.

1. **[!UICONTROL Gross Budget]** 을 입력하고 예산 간격을 선택합니다. *[!UICONTROL Daily],* *[!UICONTROL Weekly],* 또는 *[!UICONTROL Monthly]*.

캠페인의 지출 상한인 총 순 예산은 마진 설정을 기반으로 자동으로 계산되며 이 값 아래에 표시됩니다.

**[!UICONTROL Budget]:** (마진 관리 없는 캠페인) 전체 캠페인 예산.

**[!UICONTROL Estimated Tax Withholding]** : 국가 또는 지방세의 계정 수준에서 광고 비용 간 총 지출, 광고 서비스 제공 수수료 및/또는 데이터 수수료의 백분율을 보유합니다. 이율은 예산 및 게재 목적에서 추정치이므로 송장 발행 세율은 다를 수 있습니다.

원천징수할 세금을 추정하려면

1. 클릭 **[!UICONTROL Update rates here]**.

1. **[!UICONTROL Estimated tax rate]** 을 백분율로 지정합니다.

1. 세금을 보류할 각 요금 유형 옆의 확인란을 선택합니다. 요금 유형은 다음과 같습니다.

   * *[!UICONTROL Include estimated tax - ads fee]:* 캠페인 관리 요금에 대한 세금을 포함한 모든 Advertising Cloud DSP 미디어 지출에 적용됩니다.

   * *[!UICONTROL Include estimated tax - ad serving fee]:* 미디어 및 데이터를 제외한 Advertising Cloud DSP의 모든 지출에 적용됩니다. 이는 캠페인 관리 비용에 대한 세금을 제외합니다

   * *[!UICONTROL Include estimated tax - data fee]:* Advertising Cloud DSP의 모든 데이터 지출에 적용됩니다.

1. 클릭 **[!UICONTROL Submit]**.

>[!NOTE]
>
>* 미국에서, 주들은 광고, 광고 서비스 제공 및 데이터에 대한 세금 포함에 따라 다를 수 있습니다. 다른 국가의 조직의 경우 VAT를 계산할 세 가지 세금 범주 모두를 포함합니다.
>
>* 계정의 요금 설정에서 이러한 값을 구성할 수도 있습니다.<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->


**[!UICONTROL Cross Device Level]:**  (2020년 6월 22일 이후에 생성된 기존 캠페인에 대한 읽기 전용) 2020년 6월 22일 이전에 생성된 캠페인에 사용할 수 없음) Advertising Cloud이 광고를 타겟팅하고 빈도 제한을 적용할 레벨입니다.  *동일한* 장치  ** 를 사용하여 장치 또는 사람을 대상으로 하여 알려진 모든 장치에서 사용자를 타깃팅합니다.

**[!UICONTROL Device Graph]:** (기존 캠페인에 대한 읽기 전용) 사람 기반의 교차 장치 타깃팅만 있는 캠페인) 교차 장치 타깃팅 및 빈도 관리에 사용할 장치 그래프입니다.

* *[!UICONTROL LiveRamp - U.S. only]* :  [!DNL LiveRamp] 장치 그래프를 사용하여 전달되는 노출에 대해 $0.35의 교차 장치 타깃팅을 위해 모든 광고주가 사용할 수 있습니다(즉, 타깃팅된 대상 세그먼트 내에 없는 장치의 경우). 배치 수준에서 교차 장치 타깃팅을 설정할 수 있습니다.

   이 옵션은 주파수 관리 및 속성 측정에 대해 비용 없이 모든 광고주에서도 사용할 수 있습니다.

* *[!UICONTROL Adobe Co-op U.S. and Canada only]:* Adobe Experience Cloud 참여자만 추가  [!DNL Device Co-op] 비용 없이 사용할 수 있습니다.

>[!TIP]
>
>광고주가 교차 장치 속성을 사용하는 경우 가장 좋은 방법은 광고주의 교차 장치 속성 설정에 지정된 대로 타깃팅 및 빈도 관리를 위해 동일한 장치 그래프 설정을 사용하는 것입니다. 이 캠페인에 대해 다른 장치 그래프를 선택하는 경우 보고에 불일치가 발생할 수 있습니다.

**[!UICONTROL Frequency Cap]**  : (선택 사항) 캠페인에서 고유 장치 또는 사람(지정된 내용에 따라)이 광고를 제공하는  [!UICONTROL Cross Device Level]횟수입니다. 옵션에는 *[!UICONTROL Unlimited]* 또는 일, 주 또는 개월당 특정 금액이 포함됩니다.

>[!NOTE]
>
> 캠페인, 패키지 및 배치 수준에서 빈도 캡을 설정할 수 있습니다. DSP은 캠페인 계층에서 가장 엄격한 빈도 제한을 준수합니다.

**[!UICONTROL Packages]:** 캠페인 [](/help/dsp/campaign-management/packages/package-about.md) 에 패키지를 포함합니다. 기존 패키지를 선택하거나 포함할 패키지를 만듭니다. 패키지를 만드는 경우 자세한 내용은 [패키지 설정](/help/dsp/campaign-management/packages/package-settings.md)에 대한 설명을 참조하십시오.

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>다음 설정은 측정 및 보고 기능만 활성화합니다. 성능 최적화는 패키지 및 배치 수준에서만 실행됩니다.

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]:** (선택 사항) 지정된 설정을  [!DNL IAS] 사용하여 뷰가능, 사기, 브랜드 안전 및 대상 확인을 측정하고 보고할 수 있습니다. 추가 비용이 적용됩니다.

* **[!UICONTROL Measure On]:** 측정할 재고:  *[!UICONTROL Display and VPAID video inventory]* (기본값) 또는  *[!UICONTROL Display, VPAID & VAST video inventory]*.

   >[!NOTE]
   >
   >VPAID 인벤토리에서 비디오 뷰가능 여부를 측정할 수 있습니다.

* **[!UICONTROL IAS Account ID (AnID)]:** (자기의  [!DNL IAS] 계정을 가진 광고주) (선택 사항) 사용을  [!DNL IAS] 위해 직접 청구되 [!DNL IAS] 는 조직의 계정 ID입니다.

* **[!UICONTROL IAS Team ID]:** (자기의  [!DNL IAS] 계정을 가진 광고주) (선택 사항) 조직의  [!DNL IAS] 계정에 대한 팀 ID로, 이 [!DNL IAS] 는 사용을 위해 직접 청구됩니다.  <!-- verify -->

**[!UICONTROL MOAT]:** (선택 사항)  [!DNL MOAT] 뷰가능, 사기, 브랜드 안전 및 대상 검증에 대한 측정 및 보고를 활성화합니다. 추가 비용이 적용됩니다.

#### 대상 확인

**[!UICONTROL Nielsen]:** (선택 사항) 지정된  [!DNL Nielsen] 설정을 사용하여 대상 확인을 측정하고 보고할 수 있습니다. 추가 비용이 적용됩니다.

* **[!UICONTROL Target Gender]:** 타겟팅할 성별:  *[!UICONTROL Both]* (기본값),  *[!UICONTROL Male]*&#x200B;또는  *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** 타깃팅할 연령 범위입니다. 필요에 따라 왼쪽 및 오른쪽 슬라이더를 사용하여 범위를 줄입니다.

* **[!UICONTROL Target Country]:**  (선택 사항) 타깃팅할 국가입니다. [!DNL Nielsen] 은 지원되는 국가에서만 제공되는 노출 횟수를 측정합니다.

**[!UICONTROL comScore vCE]:** (선택 사항) 지정된  [!DNL Comscore validated Campaign Essentials (vCE)] 설정을 사용하여 대상 확인을 측정하고 보고할 수 있습니다. 추가 비용이 적용됩니다.

* **[!UICONTROL Target Gender]:** 타겟팅할 성별:  *[!UICONTROL Both]* (기본값),  *[!UICONTROL Male]*&#x200B;또는  *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** 타깃팅할 연령 범위입니다. 필요에 따라 왼쪽 및 오른쪽 슬라이더를 사용하여 범위를 줄입니다.

* **[!UICONTROL Target Country]:**  (선택 사항) 타깃팅할 국가입니다. [!DNL Comscore] 은 지원되는 국가에서만 제공되는 노출 횟수를 측정합니다.

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]:** 지정된 민감도 수준을 기반으로 기술을 사용하여  [!DNL IAB Open Video Viewability (OpenVV)] 뷰가능 여부를 자사 측정하고 보고할 수 있습니다.

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [Campaign Management 기본 정보](campaign-about.md)
>* [캠페인 만들기](campaign-create.md)
>* [캠페인 편집](campaign-edit.md)

