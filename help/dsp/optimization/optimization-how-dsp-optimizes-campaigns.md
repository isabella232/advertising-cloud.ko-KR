---
title: DSP이 캠페인을 최적화하는 방법
description: DSP이 캠페인에서 패키지를 최적화하는 방법을 알아봅니다.
feature: DSP Optimization
exl-id: 054582ef-b677-4725-b25c-b82bf3e5b43e
source-git-commit: b40c6f08b94e546e5fc068c46b279292a4d8a14f
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# DSP이 캠페인을 최적화하는 방법

이 페이지에서는 다음에 의해 구동되는 Advertising Cloud DSP 최적화 엔진을 간략하게 설명합니다 [!DNL Adobe Sensei]은 캠페인에서 패키지를 최적화합니다. 캠페인을 수동으로 최적화하는 방법에 대한 팁과 트릭은 [!DNL Adobe] 계정 팀입니다. <!-- add link to trading playbook if we add it to help -->

패키지 최적화 목표는 두 가지 수준에서 작동합니다.

* 각 패키지의 경우: DSP은 선택한 KPI에 대한 배치 성과를 기반으로 패키지 내의 각 배치에 예산을 할당합니다.

* 패키지의 각 배치/경매에 대해: DSP은 배치당 각 경매에 대한 실시간 경제적 KPI 값을 계산한 다음 이 값을 사용하여 입찰가를 결정합니다.

   >[!NOTE]
   >
   >즉, 취업이 얼마나 잘 되는지를 기준으로 경제 가치가 지나치게 가중될 수 있다. 배치가 지출 목표보다 늦는다면, 더 낮은 품질의 경매를 구매할 수 있을 것입니다. 배치가 지출 목표에 쉽게 도달한다면, 더 높은 품질 경매에 중점을 둘 것입니다.

## 패키지 최적화

DSP은 특정 성능 목표에 맞게 20개의 변형을 사용하여 두 가지 기본 방법으로 게재를 최적화할 수 있습니다. 다음을 선택할 수 있습니다.

* 성능 비율 우선 순위 지정

* 성능 비율로 비용 효율성을 우선 순위 지정

자세한 내용은 [최적화 목표 및 사용 방법](optimization-goals.md) kpi를 달성하는 데 도움이 되는 최적화 목표를 결정하려면

### 성능 비율을 우선시하는 패키지

성과 비율을 우선시하는 최적화 목표의 경우 DSP은 각 경매의 성과를 예측하고 항상 최대 입찰에서 입찰합니다. 적용 가능한 최적화 목표의 예는 다음과 같습니다 [!UICONTROL Highest Viewability Rate], [!UICONTROL Highest Clickthrough Rate]등

다음 경우 이 최적화 모드가 잘 작동합니다.

* 이미 유효/허용 가능한 CPM 수준(예: 이전 벤치마크)을 알고 있습니다.

* 수동으로 [!UICONTROL Max Bid] 에 대해 크기 조절을 사용하여 문제가 발생하는 경우 각 배치에 대해 설명합니다.

* 효율성보다 스케일을 우선시해야 합니다.

#### 게재 논리 {#pacing-logic-performance}

* 만약 지출이 속도라면, 입찰은 더 선택적이 될 것이고, 그래서 당신은 높은 성과를 낼 것으로 예상되는 경매에만 입찰할 것이다.

* 만약 지출이 속도보다 빠진다면 입찰은 덜 선택적이 될 것이며, 그래서 당신은 게재 목표를 맞추기 위해 가격 인하에 따른 실적을 올리기 위해 낮은 실적을 낼 것으로 예상되는 경매에 입찰할 것이다.

#### 가격/입찰 음영 지우기 {#clearing-price-performance}

간격 논리를 실행한 후 DSP은 정산 가격 예측 모델을 통해 제안된 입찰을 실행합니다. 예측이 낙찰률을 최소화하면서 입찰을 낮출 수 있음을 나타내는 경우 해당 입찰은 예측에 따라 감소합니다.

### 성능 비율로 비용 효율성을 우선시하는 패키지

일부 최적화 목표의 경우 DSP은 각 경매의 성과를 예측하여 배치를 초과하지 않고 입찰 가격을 자동으로 조정합니다 [!UICONTROL Max Bid]. 적용 가능한 최적화 목표의 예는 다음과 같습니다 [!UICONTROL Lowest CPM], [!UICONTROL Lowest CPA], [!UICONTROL Lowest Cost per View], [!UICONTROL Lowest Cost per Click]등

#### 간격 논리 {#pacing-logic-balanced}

* 지출이 속도에따라 DSP은 가격이 더 민감해져 가격 인상으로 시장가격 인하에 따른 경쟁률이 낮아진다.

* 성능 지표도 균형 잡힌 경우(목표를 제외한 모든 목표) [!UICONTROL Lowest CPM])를 클릭한 다음 예측된 KPI를 입찰 금액에 혼합합니다. 따라서 &quot;Cost per&quot;를 기반으로 더 높은 성능을 기대할 수 있는 경매에 대해 높은 입찰을 수행합니다.

* 지출이 속도보다 뒤처지면, DSP은 더 적은 가격 민감성과 입찰이 더 많이 되어, [!UICONTROL Max Bid]이는 게재 간격 계획과 일치된 환율로 교환하기 위한 것이다.

#### 가격/입찰 음영 지우기 {#clearing-price-balanced}

간격 논리를 실행한 후 DSP은 정산 가격 예측 모델을 통해 제안된 입찰을 실행합니다. 예측이 낙찰률을 최소화하면서 입찰을 낮출 수 있음을 나타내는 경우 해당 입찰은 예측에 따라 감소합니다.

## 배치 최적화

입찰 전 필터를 배치하는 것은 강력한 성능을 보장하기 위한 가장 엄격한 방법입니다. DSP은 서로 다른 광고 유형에서 입찰 전 필터를 전략적으로 사용하여 각 패키지 내에서 배치 간에 성능 목표를 달성합니다. 입찰 전 필터를 패키지 수준 최적화와 동시에 사용하거나 독립적으로 사용할 수 있습니다.

>[!NOTE]
>
>사용 가능한 사전 입찰 필터는 광고 유형에 따라 다릅니다. 예를 들어 표준 디스플레이 배치의 경우 클릭스루 비율과 뷰가능 여부에 따라 필터링할 수 있지만 완료율은 필터링할 수 없습니다.

자세한 내용은 [배치 수준 사전 입찰 필터 및 사용 방법](optimization-pre-bid-filters.md) 를 입력하여 KPI를 달성하는 데 도움이 되는 사전 입찰 필터를 결정합니다.

>[!MORELIKETHIS]
>
>* [패키지 설정](/help/dsp/campaign-management/packages/package-settings.md)
>* [배치 설정](/help/dsp/campaign-management/placements/placement-settings.md)
>* [최적화 목표 및 사용 방법](optimization-goals.md)
>* [배치 수준 사전 입찰 필터 및 사용 방법](optimization-pre-bid-filters.md)
>* [성능 문제 해결](/help/dsp/optimization/troubleshooting-performance.md)

