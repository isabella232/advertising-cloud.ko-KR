---
title: 캠페인 설정
description: 사용 가능한 캠페인 설정에 대한 설명을 참조하십시오.
feature: DSP Campaigns
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '921'
ht-degree: 0%

---

# 캠페인 설정

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]:** 캠페인 이름.

**[!UICONTROL Advertiser]:** (기존 캠페인에 대한 읽기 전용) 해당 광고주(브랜드). 기존 광고주를 선택하거나 새 광고주를 만듭니다.

**[!UICONTROL Advertiser URL]:** 광고주의 공식 페이지입니다. 이 필드는 인벤토리 파트너와 함께 광고 승인 프로세스를 가속화합니다.

**[!UICONTROL Timezone]:** (기존 캠페인에 대한 읽기 전용) 보고 및 입찰을 위한 시간대입니다.

**[!UICONTROL Customer PO]:** (선택 사항) 삽입 주문/구매 발주에 대한 고객 구매 발주.

**[캠페인 날짜]:** 캠페인 시작 및 종료 날짜입니다.

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]:** 캠페인의 여백을 관리할지 여부: *[!UICONTROL Yes]* 또는 *[!UICONTROL No]* (기본값)

선택 시 *[!UICONTROL Yes],* 여백 유형 및 금액을 지정합니다.

* **[!UICONTROL Margin Type]:** 여백의 유형입니다. 여백 관리를 활성화하고 캠페인을 저장한 후에는 여백 유형을 변경할 수 없습니다.

   * *[!UICONTROL Fixed]:* (기본값) DSP에서 [!UICONTROL Gross Budget].

   * *[!UICONTROL Dynamic]:* 여백을 별도의 [!UICONTROL Budget Reserve %] 및 [!UICONTROL Gross Budget] 의 각 패키지 및 캠페인에 배치되는 각각의 경우를 설명합니다. DSP은 특정 여백을 보장하지 않고 각 배치의 재무 효율성을 기반으로 최적화합니다. 고정 비율로 고정 수량 또는 단위 유형을 제공하기로 동의한 여러 라인 항목으로 구성된 삽입 주문에 사용합니다.

* **[!UICONTROL Fixed Margin %]:** (여백이 고정된 캠페인 전용) 각 삽입 순서에 대한 기본 마크업 <!-- impression? -->를 백분율로 제한할 수 있습니다. 이 금액은 [!UICONTROL Gross Budget] 순 캠페인 예산을 정의하기 위해.

* **[!UICONTROL Budget Reserve %]:** (여백이 고정된 캠페인 선택 사항) 지정된 백분율을 예약합니다 [!UICONTROL Gross Budget] 보호 조치로써 이 금액은 [!UICONTROL Gross Budget] 순 캠페인 예산을 정의하기 위해.

**[!UICONTROL Gross Budget]:** (마진 관리만 있는 캠페인) 지정된 한계 조정이 적용되기 전의 총캠페인 예산입니다.

일일, 주별 또는 월별 총 예산을 추가할 수도 있습니다.

1. 클릭 **[!UICONTROL Add an additional Gross Budget]**.

1. 을(를) 입력합니다. **[!UICONTROL Gross Budget]** 그리고 예산 간격을 선택합니다. *[!UICONTROL Daily],* *[!UICONTROL Weekly],* 또는 *[!UICONTROL Monthly]*.

캠페인의 지출 상한인 총 순 예산은 마진 설정을 기반으로 자동으로 계산되며 이 값 아래에 표시됩니다.

**[!UICONTROL Budget]:** (마진 관리 없는 캠페인) 전체 캠페인 예산.

**[!UICONTROL Estimated Tax Withholding]:** Within 은 국가 또는 지방세 계정 수준에서 광고 비용, 광고 서비스 비용 및/또는 데이터 요금에 대한 총 지출의 백분율을 갖습니다. 이율은 예산 및 게재 목적에서 추정치이므로 송장 발행 세율은 다를 수 있습니다.

원천징수할 세금을 추정하려면

1. 클릭 **[!UICONTROL Update rates here]**.

1. 을(를) 지정합니다. **[!UICONTROL Estimated tax rate]**&#x200B;를 백분율로 제한할 수 있습니다.

1. 세금을 보류할 각 요금 유형 옆의 확인란을 선택합니다. 요금 유형은 다음과 같습니다.

   * *[!UICONTROL Include estimated tax - ads fee]:* 캠페인 관리 요금에 대한 세금을 포함한 모든 Advertising DSP 미디어 지출에 적용됩니다.

   * *[!UICONTROL Include estimated tax - ad serving fee]:* 미디어 및 데이터를 제외한 Advertising DSP에 지출하는 모든 비용에 적용됩니다. 이는 캠페인 관리 비용에 대한 세금을 제외합니다

   * *[!UICONTROL Include estimated tax - data fee]:* Advertising DSP에 대한 모든 데이터 지출에 적용됩니다.

1. 클릭 **[!UICONTROL Submit]**.

>[!NOTE]
>
>* 미국에서, 주들은 광고, 광고 서비스 제공 및 데이터에 대한 세금 포함에 따라 다를 수 있습니다. 다른 국가의 조직의 경우 VAT를 계산할 세 가지 세금 범주 모두를 포함합니다.
>
>* 계정의 요금 설정에서 이러한 값을 구성할 수도 있습니다.<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->


**[!UICONTROL Cross Device Level]:** (2020년 6월 22일 이후 생성된 기존 캠페인에 대한 읽기 전용. DSP에서 광고를 타깃팅하고 빈도 제한 적용 수준: *동일한 장치* 장치 또는 *사람* 의 모든 알려진 장치에서 사용자를 타겟팅합니다.

**[!UICONTROL Device Graph]:** (기존 캠페인에 대한 읽기 전용) 사람 기반의 교차 장치 타깃팅만 있는 캠페인) 교차 장치 타깃팅 및 빈도 관리에 사용할 장치 그래프입니다.

* *[!UICONTROL LiveRamp - U.S. only]:* 모든 광고주가 를 사용하여 전달되는 노출에 대해 0.35CPM으로 교차 장치 타깃팅에 사용할 수 있습니다. [!DNL LiveRamp] 장치 그래프(즉, 타깃팅된 대상 세그먼트 내에 없는 장치의 경우). 배치 수준에서 교차 장치 타깃팅을 설정할 수 있습니다.

   이 옵션은 주파수 관리 및 속성 측정에 대해 비용 없이 모든 광고주에서도 사용할 수 있습니다.

**[!UICONTROL Frequency Cap]:** (선택 사항) 고유 장치 또는 사람의 횟수입니다(지정된 [!UICONTROL Cross Device Level])은 캠페인에서 광고를 제공합니다. 옵션은 다음과 같습니다 *[!UICONTROL Unlimited]* 또는 일, 주 또는 개월당 특정 금액입니다.

>[!NOTE]
>
> 캠페인, 패키지 및 배치 수준에서 빈도 캡을 설정할 수 있습니다. DSP은 캠페인 계층에서 가장 엄격한 빈도 제한을 준수합니다.

**[!UICONTROL Packages]:** 다음 [패키지](/help/dsp/campaign-management/packages/package-about.md) 캠페인에 포함할 수 없습니다. 기존 패키지를 선택하거나 포함할 패키지를 만듭니다. 패키지를 만드는 경우 [패키지 설정](/help/dsp/campaign-management/packages/package-settings.md) 추가 정보.

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>다음 설정은 측정 및 보고 기능만 활성화합니다. 성능 최적화는 패키지 및 배치 수준에서만 실행됩니다.

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]:** (선택 사항) 활성화 [!DNL IAS] 지정된 설정을 사용하여 뷰가능, 사기, 브랜드 안전 및 대상 검증에 대한 측정 및 보고. 추가 비용이 적용됩니다.

* **[!UICONTROL Measure On]:** 측정할 재고: *[!UICONTROL Display and VPAID video inventory]* (기본값) 또는 *[!UICONTROL Display, VPAID & VAST video inventory]*.

   >[!NOTE]
   >
   >VPAID 인벤토리에서 비디오 뷰가능 여부를 측정할 수 있습니다.

* **[!UICONTROL IAS Account ID (AnID)]:** (자체 광고주 [!DNL IAS] 계정; (선택 사항) 조직의 [!DNL IAS] 계정 ID, [!DNL IAS] 사용시 직접 청구됩니다.

* **[!UICONTROL IAS Team ID]:** (자체 광고주 [!DNL IAS] 계정; (선택 사항) 조직의 팀 ID입니다 [!DNL IAS] 계정 [!DNL IAS] 사용시 직접 청구됩니다. <!-- verify -->

**[!UICONTROL MOAT]:** (선택 사항) 활성화 [!DNL MOAT] 뷰가능, 사기, 브랜드 안전 및 고객 검증에 대한 측정 및 보고. 추가 비용이 적용됩니다.

#### 대상 확인

**[!UICONTROL Nielsen]:** (선택 사항) 활성화 [!DNL Nielsen] 지정된 설정을 사용하여 대상 확인에 대한 측정 및 보고. 추가 비용이 적용됩니다.

* **[!UICONTROL Target Gender]:** 타겟팅할 성별: *[!UICONTROL Both]* (기본값), *[!UICONTROL Male]*, 또는 *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** 타깃팅할 연령 범위입니다. 필요에 따라 왼쪽 및 오른쪽 슬라이더를 사용하여 범위를 줄입니다.

* **[!UICONTROL Target Country]:** (선택 사항) 타깃팅할 국가입니다. [!DNL Nielsen] 은 지원되는 국가에서만 제공되는 노출 횟수를 측정합니다.

**[!UICONTROL comScore vCE]:** (선택 사항) 활성화 [!DNL Comscore validated Campaign Essentials (vCE)] 지정된 설정을 사용하여 대상 확인에 대한 측정 및 보고. 추가 비용이 적용됩니다.

* **[!UICONTROL Target Gender]:** 타겟팅할 성별: *[!UICONTROL Both]* (기본값), *[!UICONTROL Male]*, 또는 *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** 타깃팅할 연령 범위입니다. 필요에 따라 왼쪽 및 오른쪽 슬라이더를 사용하여 범위를 줄입니다.

* **[!UICONTROL Target Country]:** (선택 사항) 타깃팅할 국가입니다. [!DNL Comscore] 은 지원되는 국가에서만 제공되는 노출 횟수를 측정합니다.

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]:** 를 사용하여 뷰가능 여부에 대한 자사 측정 및 보고를 활성화합니다 [!DNL IAB Open Video Viewability (OpenVV)] 지정된 민감도 수준을 기반으로 하는 기술:

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [Campaign Management 정보](campaign-about.md)
>* [캠페인 만들기](campaign-create.md)
>* [캠페인 편집](campaign-edit.md)

