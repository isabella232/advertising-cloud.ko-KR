---
title: 배치 설정
description: 사용 가능한 배치 설정에 대한 설명을 참조하십시오.
feature: DSP Placements
exl-id: 36097132-e589-4d49-bf86-54f61eae5b67
source-git-commit: c8077a2f9cec1dab08f6635024b3b2d5a4a1c90e
workflow-type: tm+mt
source-wordcount: '3422'
ht-degree: 0%

---

# 배치 설정

## [!UICONTROL Basics]

**[!UICONTROL Placement name]** 배치 이름입니다.

>[!TIP]
>상황에 맞는 명명 규칙을 사용하십시오. 하나의 권장 이름 지정 규칙은 &quot;*\&lt;campaign name=&quot;&quot;>: \&lt;ad unit=&quot;&quot;>: \&lt;duration>: \&lt;targeting>*.&quot;

**[!UICONTROL Status]:** 배치 상태: *[!UICONTROL Active]* (기본값) 또는 *[!UICONTROL Paused]*.

>[!TIP]
>가장 좋은 방법은 배치를 실행할 준비가 될 때까지 배치를 일시 중지하는 것입니다.

**[!UICONTROL Details]:** (읽기 전용) 적용 가능한 광고 유형, 배치를 만들거나 만드는 계정 및 상위 캠페인입니다. 자세한 내용을 보려면 **[!UICONTROL Show more]**.

**[!UICONTROL Templates]:** 기존 배치 템플릿 목록을 엽니다. 템플릿에서 타깃팅 설정을 자동으로 채우려면 다음을 수행합니다.

1. 다음 중 하나를 수행합니다.

   * 템플릿에서 모든 대상을 재사용하려면 템플릿 이름 옆에 있는 확인란을 선택합니다.

   * 템플릿에서 개별 대상 유형을 재사용하려면 템플릿 이름을 확장하고 재사용할 대상 유형 옆의 확인란을 선택합니다.

1. 클릭 **[!UICONTROL Apply]**.

**[!UICONTROL Ad specs for forecast]:** (비디오 광고 형식만 해당) 오른쪽에 있는 예측 투영을 계산하는 데 사용되는 광고 기간 및/또는 광고 사양입니다. 필드는 광고 유형에 따라 다릅니다.

**[!UICONTROL Environment]:** (범용 비디오 광고 형식만 해당) 배치에 대상으로 포함할 장치 환경(데스크탑, 모바일, 연결된 TV)입니다

**[!UICONTROL Placement tags]:** (선택 사항) 이 배치를 찾는 데 도움이 되는 키워드 또는 별명입니다.

## 목표

**[!UICONTROL Package]:** (선택 사항) 배치가 지정된 패키지입니다. 클릭 ![편집](/help/dsp/assets/edit.png) 를 클릭하여 기존 패키지를 선택하거나 새 패키지를 만듭니다. 패키지에 배치를 할당하면 [!UICONTROL Goals] 섹션이 패키지의 플라이트 날짜, 게재 목표 및 예산으로 업데이트됩니다.

**[!UICONTROL Flight Dates]:** 배치의 시작 날짜 및 종료 날짜입니다. 승인된 광고는 게시가 활성 상태이고 활성 패키지 또는 캠페인에 지정된 경우 비행 중에 실행할 수 있습니다.

패키지(해당되는 경우) 또는 캠페인의 날짜는 기본적으로 자동으로 채워집니다.

>[!NOTE]
>
>* 비행 날짜는 캠페인 비행 날짜와 패키지 비행 날짜 내에 포함되어야 합니다.


### 패키지 수준 게시가 있는 패키지에 지정된 배치

**[!UICONTROL Placement Funding]:** 배치에 대한 예산 책정 방법:

* *[!UICONTROL Optimize based on performance]:* 패키지 수준에서 예산을 제어합니다.
* *[!UICONTROL Set a fixed budget cap]:* 일별, 주별, 월별 또는 모든 시간 배치 예산을 설정할 수 있습니다. 값 및 기간 입력(*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Max Bid]:** 노출 1,000개에 대한 최대 비용.

**[!UICONTROL Placement Pre-bid Filters]:** 입찰이 발생하기 위해 충족해야 하는 최대 5개의 KPI 임계값(최소 뷰가능 지표 또는 클릭스루 비율 등)입니다. 사전 입찰 필터를 최적화 전술로 사용할 수 있지만 각 규칙이 이 게재에 입찰할 수 있는 기회를 제한할 수 있음을 이해합니다. 필터를 추가하거나 편집하려면:

1. 클릭 ![편집](/help/dsp/assets/edit.png).
1. 다음 중 하나를 수행합니다.
   * 필터를 추가하려면 다음을 수행하십시오.
      1. 클릭 **[!UICONTROL Add Filter]**.
      1. 다음 **[!UICONTROL Only bid if]**&#x200B;를 클릭하고 지표를 선택한 다음 값을 입력합니다.
   * 필터를 제거하려면 **[!UICONTROL X]** 를 클릭합니다.
1. 클릭 **[!UICONTROL Save]**.

다음 위치에서 각 사전 입찰 필터에 대한 설명을 참조하십시오.[배치 수준 사전 입찰 필터 및 사용 방법](/help/dsp/optimization/optimization-pre-bid-filters.md).&quot;

### 기타 모든 배치

**[!UICONTROL Budget Goal]:** 총 예산 상한 및 예산 간격(*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Gross Budget Goal]:** (마진 관리만 있는 캠페인에서 배치) 총 예산 상한 및 예산 간격(*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Optimization Goal]:**  패키지에 대한 최적화 목표입니다. 에서 각 최적화 목표에 대한 설명을 참조하십시오.[최적화 목표 및 사용 방법](/help/dsp/optimization/optimization-goals.md)&quot;.

**[!UICONTROL Target Goal]:** 성과를 추적하는 데 사용되는 타겟 목표입니다.

>[!NOTE]
>
>이 필드는 벤치마크일 뿐이며 의사 결정에 사용되지 않습니다.

**[!UICONTROL Pace on]:** 게재 시 기반이 되는 항목:

* **[!UICONTROL Budget goal]:** (기본값) 이 옵션은 할당된 예산 내에서 가능한 한 많은 노출 횟수를 제공합니다.

* **[!UICONTROL Impressions]:** 이 옵션은 지정된 간격에 지정된 수량에 도달할 때까지 노출 횟수를 전달합니다. 이 옵션을 선택하면 노출 횟수 및 간격을 지정합니다. *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* 또는 *[!UICONTROL Weekly]*.

**[!UICONTROL Max Bid]:** 노출 1,000개에 대한 최대 비용.

**[!UICONTROL Flight pacing]:** (배치 수준 게재 전용인 배치) 광고 게재 속도를 높이는 방법:

* *[!UICONTROL Even]:* (기본값) 게재를 각 비행 내내 균일하게 지연시키며, 첫 번째 비행 시 게재 목표의 50%가 됩니다.

* *[!UICONTROL Slightly Ahead]:* (기본값) 55-65%가 비행 기간의 절반을 완료하도록 게재를 가속화합니다.

* *[!UICONTROL Frontload]:* 배송을 가속화하여 65-75%가 비행 중간에 완료됩니다.

* *[!UICONTROL Aggressive Frontload]:* 배송을 가속화하여 75-85%가 비행 중간에 완료됩니다.

**[!UICONTROL Intraday pacing]:** (배치 수준 게재 전용인 배치) 플라이트 내에서 각 날에 걸쳐 광고 전달을 페이스로 지정하는 방법:

* *[!UICONTROL Even]:* (기본값) 재고 가용성에 따라 배달을 조정합니다. 일반적으로 경매 부피가 더 높은 낮 시간 동안 더 많은 광고가 게재되고 아침이나 저녁으로 더 적은 광고가 게재됩니다.

* *[!UICONTROL ASAP]:* (기본값) 게재를 속도가 2배 빠릅니다 *짝수*.

   >[!CAUTION]
   >
   >이 옵션은 성능에 부정적인 영향을 줄 수 있습니다. 전달 우선 순위 지정과 성능 최적화에 대한 비용 지출을 완전히 결정하는 경우에만 사용하십시오.

**[!UICONTROL Placement Pre-bid Filters]:** (선택 사항) 입찰이 발생하기 위해 충족해야 하는 최대 5개의 필터입니다. 입찰 전 필터를 최적화 전술로 사용할 수 있지만 각 규칙은 이 게재에 입찰할 수 있는 기회를 제한할 수 있습니다. 필터를 추가하거나 편집하려면:

1. 클릭 ![편집](/help/dsp/assets/edit.png).
1. 다음 중 하나를 수행합니다.
   * 필터를 추가하려면 다음을 수행하십시오.
      1. 클릭 **[!UICONTROL Add Filter]**.
      1. 다음 **[!UICONTROL Only bid if]**&#x200B;를 클릭하고 지표를 선택한 다음 값을 입력합니다.
   * 필터를 제거하려면 **[!UICONTROL X]** 를 클릭합니다.
1. 클릭 **[!UICONTROL Save]**.

## [!UICONTROL Geo-Targeting]

**[!UICONTROL Audience Location]:** (선택 사항) 배치에 광고를 포함하거나 제외할 특정 위치. 위치를 지정하지 않으면 모든 위치가 타깃팅됩니다.

>[!NOTE]
>
>도시 및 DMA 위치는 Roku 배치에 사용할 수 없습니다.

위치를 지정하려면

1. 클릭 ![편집](/help/dsp/assets/edit.png).
1. 다음 중 하나를 수행합니다.
   * 국가, 주, 도시, DMA, 연방 입법 지구 또는 주 입법 지구를 포함하거나 제외하려면,
      1. 왼쪽 열에서 위치 유형을 선택합니다.
      1. (필요한 경우) 위치를 클릭하여 확장합니다.
      1. 위치 옆에 있는 *[!UICONTROL Include]* 이것을 타겟 또는 *[!UICONTROL Exclude]* 를 타겟으로 제외하는 중입니다.
   * 우편 번호를 검색하고 선택한 모든 결과를 포함하거나 제외하려면,
      1. 클릭 **[!UICONTROL Search Postal Code]**.
      1. 국가를 선택합니다.
      1. 도시 이름을 입력한 다음 ![편집](/help/dsp/assets/search.png).
      1. 올바른 검색 결과를 클릭합니다.
      1. 클릭 *[!UICONTROL Include All]* 모든 위치를 타겟으로 포함하거나 *[!UICONTROL Exclude All]* 모든 위치를 타겟으로 제외하려면 다음을 수행하십시오.
   * 우편 번호를 입력하거나 붙여넣고, 모두 포함하거나 제외하려면:
      1. 클릭 **[!UICONTROL Paste Postal Code]**.
      1. 국가를 선택합니다.
      1. 최대 1000개의 우편 번호를 입력하거나 붙여넣습니다.
행당 하나의 우편 번호를 포함하거나, 쉼표나 탭으로 구분된 여러 값을 입력합니다.
      1. 클릭 *[!UICONTROL Include All]* 모든 위치를 타겟으로 포함하거나 *[!UICONTROL Exclude All]* 모든 위치를 타겟으로 제외하려면 다음을 수행하십시오.
   * 에서 위치를 제거하려면 [!UICONTROL Included] 또는 [!UICONTROL Excluded] 목록, **[!UICONTROL X]** 오른쪽 열의 위치 옆에 있습니다.
1. 클릭 **[!UICONTROL Done]**.

>[!NOTE]
>
>* 모든 국가가 주, 도시 또는 우편 번호 위치를 가지고 있는 것은 아닙니다.
>* DMA(지정 시장 지역), 연방 입법 지구 및 주 입법 구역은 미국 지역에만 사용할 수 있습니다.


## [!UICONTROL Inventory Targeting]

**[!UICONTROL Inventory Sources]:** 대상으로 포함하거나 제외할 재고 출처. 대부분의 배치 유형의 경우, 모든 재고 유형 및 각 유형의 모든 소스가 기본적으로 포함됩니다. 대상 [!DNL Roku] 배치, 재고 유형 및 소스를 지정해야 합니다. 다음 유형의 인벤토리 중에서 선택할 수 있습니다.

* [!UICONTROL Public]: (Roku를 제외한 모든 배치 유형) Advertising Cloud이 액세스할 수 있는 모든 열린 Exchange 인벤토리입니다. 공개 인벤토리를 포함 및 제외할 수 있습니다.

   소스 또는 피드별로 목록을 볼 수 있습니다. 피드별로 목록을 볼 때 피드 이름, 피드 키 또는 선택한 특성 태그로 검색할 수 있습니다.

* [!UICONTROL Private] | [!UICONTROL Roku Private]: 기존 개인 거래(또는 기존 개인 거래) [!DNL Roku] 거래 [!DNL Roku] 배치)를 사용하도록 설정합니다. 공용 인벤토리를 포함할 수 있지만 제외하지는 않습니다.

   키워드, 키, 거래 ID 또는 사용자 지정 태그로 목록을 검색할 수 있습니다.

* [!UICONTROL On Demand] | [!UICONTROL Roku On Demand]: 모두 [premium, 보장되지 않음 [!UICONTROL On Demand] 인벤토리](/help/dsp/inventory/on-demand-inventory-about.md) 또는 [!UICONTROL On Demand] [!DNL] Roku는 [!DNL Roku] 로그인한 배치) [!DNL DSP]. 포함 및 제외할 수 있습니다 [!UICONTROL On Demand] 인벤토리

   소스 또는 피드별로 목록을 볼 수 있습니다. 피드별 목록을 볼 때 피드 이름, 피드 키 또는 선택한 게시자 영역, 카테고리 태그 또는 특성 태그별로 검색할 수 있습니다.

재고 타깃팅을 지정하려면

* 재고 유형을 제외하려면 이름 옆에 있는 확인란의 선택을 취소합니다.
* 재고 유형을 타깃팅하려면
   1. 재고 유형 이름 옆에 있는 확인란을 선택합니다.
   1. (선택 사항) 소스를 다음과 같이 변경합니다.
      1. 클릭 ![편집](/help/dsp/assets/edit.png).
      1. ([!UICONTROL Public] 및 [!UICONTROL On Demand] inventory) *[!UICONTROL *View by Source]** 또는 **[!UICONTROL View by Feed]** 소스의 목록 방식을 변경하려면
      1. (해당되는 경우) 필요에 따라 인벤토리를 필터링합니다.
      1. 포함 및 제외할 소스를 지정합니다.
         * 다음을 포함합니다 [!UICONTROL Public] 또는 [!UICONTROL On Demand] 소스 **[!UICONTROL Include]** 소스 이름 옆에 표시됩니다.
         * 포함하려면 [!UICONTROL Private] 소스:
            * 거래에 모든 인벤토리를 포함하려면 **[!UICONTROL Include all]** 를 클릭합니다.
            * 개별 재고 출처를 포함하려면 거래 이름을 확장한 다음 출처 이름 옆에 있는 확인란을 클릭합니다.
         * 를 제외하려면 [!UICONTROL Public] 또는 [!UICONTROL On ] 소스 **[!UICONTROL Exclude]** 소스 이름 옆에 표시됩니다.
   1. (선택 사항) 타깃팅 정보가 있는 CSV 파일을 브라우저의 다운로드 위치에 다운로드하려면 를 클릭합니다 **[!UICONTROL Save & Export]**.
   1. 클릭 **[!UICONTROL Save]**.

>[!TIP]
>
>구독한 경우 [!UICONTROL On Demand] 인벤토리를 작성했지만 타겟팅할 게시자나 거래를 찾을 수 없는 경우 거래 상태를 확인합니다. 상태에 대한 자세한 내용은 [정보 [!DNL On Demand] Premium 인벤토리](/help/dsp/inventory/on-demand-inventory-about.md).

**[!UICONTROL Exclude out-stream]:** (비디오 배치만 해당) 아웃스트림 트래픽을 제외합니다.

아웃바운드 스트림 광고는 일반적으로 비디오 플레이어에 있는 일반 비디오 광고보다 컨텐츠 위에 팝업 또는 컨텐츠(기본 경험에서)로 채워져 표시됩니다.

## [!UICONTROL Site Targeting]

**[!UICONTROL Traffic type]:** 타깃팅할 트래픽 유형입니다. 옵션은 다음과 같습니다 **[!UICONTROL Websites]** 및 **[!UICONTROL Apps]**.

**[!UICONTROL Site tier]:** (사용 가능한 경우 **[!UICONTROL Paste list of targeted sites]** is *[!UICONTROL Off]*) 타깃팅할 사이트의 품질입니다. 계층 1-3은 모두 브랜드에 안전하며 DSP 매핑 팀에서 조사 및 승인되었습니다.

* *[!UICONTROL Tier 1]:* 전국적으로 인식할 수 있는 프리미엄 사이트 및 애플리케이션입니다.
* *[!UICONTROL Tier 2]:* Target 계층 1은 물론 Tier 1보다 널리 알려지지 않은 품질 사이트 및 애플리케이션까지 제공됩니다.
* *[!UICONTROL Tier 3]:* Target 계층 1-2뿐만 아니라 틈새 대상에 맞는 합법적이고 안전한 사이트 및 애플리케이션을 제공합니다. 도달 범위 또는 데이터 타겟팅 구매를 위해 계층 3을 사용합니다.
* *[!UICONTROL All Sites]:* Target 계층 1-3과, 검색 또는 분류되지 않은 신규 인벤토리로, 도달 범위를 위해 사용할 수 있습니다.

>[!NOTE]
>
>재고는 배치의 광고 단위에만 적용됩니다.

>[!TIP]
>
>성능 캠페인의 경우, 가장 좋은 방법은 *[!UICONTROL All Sites]*.

**[!UICONTROL Site Categories]:** (선택 사항) 사용 가능한 경우 **[!UICONTROL Paste list of targeted sites]** is *[!UICONTROL Off]*) 타깃으로 포함 또는 제외(둘 다 제외)할 선택한 사이트 계층 내의 사이트 카테고리입니다. Advertising Cloud이 사이트 제목을 기반으로 매핑한 세로 사이트 목록 중에서 선택합니다.

1. 클릭 ![편집](/help/dsp/assets/edit.png).
1. 포함 또는 제외할 사이트 카테고리를 지정합니다.
   * 사이트 카테고리를 포함하려면 다음을 수행합니다.
      1. 클릭 **[!UICONTROL Include categories]**.
      1. 타깃팅할 각 카테고리 옆에 있는 확인란을 선택합니다.
   * 사이트 카테고리를 제외하려면 다음을 수행합니다.
      1. 클릭 **[!UICONTROL Exclude categories]**.
      1. 제외할 각 카테고리 옆에 있는 확인란을 선택합니다.
1. (선택 사항) 타깃팅 정보가 있는 CSV 파일을 브라우저의 다운로드 위치에 다운로드하려면 를 클릭합니다 **[!UICONTROL Export]**.
1. 클릭 **[!UICONTROL Save]**.

**[!UICONTROL Exclude Sites]:** (선택 사항) 사용 가능한 경우 **[!UICONTROL Paste list of targeted sites]** is *[!UICONTROL Off]*) 제외할 사이트. 사이트를 검색하고 선택하거나 도메인 이름을 입력하거나 붙여넣을 수 있습니다.

1. 클릭 ![편집](/help/dsp/assets/edit.png).
1. 사이트를 지정합니다.
   * 사이트를 검색하려면 다음을 수행하십시오.
      1. 클릭 **[!UICONTROL Search]**.
      1. 키워드를 입력하고 사이트 계층을 선택하거나 사이트 카테고리를 선택합니다.
      1. 검색 결과에서 제외할 사이트를 선택합니다.
         * 개별 사이트를 제외하려면 해당 사이트 옆의 확인란을 선택합니다.
         * (결과가 50개 이상인 경우) 처음 50개의 결과를 제외하려면 **[!UICONTROL Exclude these 50]**. 모든 검색 결과를 제외하려면 **[!UICONTROL Exclude these \<*NN *\>]**.
   * 도메인 이름을 입력하려면
      1. 클릭 **[!UICONTROL Paste]**.
      1. 별도의 줄에 하나 이상의 도메인 이름을 입력합니다.
      1. 클릭 **[!UICONTROL Exclude All]**.
1. 클릭 **[!UICONTROL Done]** 다 끝나면

>[!NOTE]
>
>* 계정 수준 및 광고주 수준의 차단된 사이트 목록도 Advertising Cloud DSP 외에도 적용됩니다 [전역 차단 사이트 목록](/help/dsp/introduction/features/brand-safety-media-quality.md): 광고에는 안전하지 않다고 간주되는 사이트가 포함됩니다.
>* 차단된 사이트 목록은 항상 타깃팅된 사이트 목록을 무시합니다. 배치가 둘 다 제외되고 광고에 대해 동일한 타겟을 포함하는 경우 대상이 제외됩니다.


**[!UICONTROL Language]:** (선택 사항) 타깃팅할 단일 언어입니다.

**[!UICONTROL Site List Preview]:** (읽기 전용) 배치에 대한 모든 타깃팅된 사이트와 차단된 사이트입니다.

선택적으로 타깃팅되고 차단된 사이트 목록을 쉼표로 구분된 값(CSV) 파일로 내보낼 수 있습니다. 목록을 내보내려면 **[!UICONTROL Export full site list]**&#x200B;를 입력한 다음 브라우저의 일반 절차에 따라 파일을 열거나 저장합니다.

**[!UICONTROL Allow unscreened sites]:** (표준 디스플레이 배치만 해당) 감사되지 않은 사이트에서 광고 전달을 활성화합니다. 배치가 비공개 인벤토리를 타깃팅하는 경우 이 옵션은 차단된 사이트에 광고를 게재할 수 있습니다.

**[!UICONTROL Paste list of targeted sites]:** 특정 사이트만 타깃팅할 수 있습니다. 이 옵션을 활성화하면 다른 사이트 타깃팅 옵션이 비활성화됩니다.

**[!UICONTROL Sites]:** (사용 가능한 경우 **[!UICONTROL Paste list of targeted sites]** is *[!UICONTROL On]*) 타겟팅할 사이트 사이트를 검색하고 선택하거나 도메인 이름을 입력하거나 붙여넣을 수 있습니다.

1. 클릭 ![편집](/help/dsp/assets/edit.png).
1. 사이트를 지정합니다.
   * 사이트를 검색하려면 다음을 수행하십시오.
      1. 클릭 **[!UICONTROL Search]**.
      1. 키워드를 입력하고 사이트 계층을 선택하거나 사이트 카테고리를 선택합니다.
      1. 검색 결과에서 포함할 사이트를 선택합니다.
         * 개별 사이트를 제외하려면 해당 사이트 옆의 확인란을 선택합니다.
         * (50개 이상의 결과를 사용할 수 있는 경우) 처음 50개의 결과를 포함하려면 **[!UICONTROL Include these 50]**. 모든 검색 결과를 포함하려면 **[!UICONTROL Include these \<*NN *\>]**.
   * 도메인 이름을 입력하려면
      1. click **[!UICONTROL Paste]**.
      1. 별도의 줄에 하나 이상의 도메인 이름을 입력합니다.
      1. 클릭 **[!UICONTROL Include All]**.
1. 클릭 **[!UICONTROL Done]**.

## [!UICONTROL Audience Targeting]

**[!UICONTROL Included Audiences]:** 을 포함한 배치의 모든 대상 타겟 [타사 세그먼트, 퍼스트 파티 세그먼트, Adobe 세그먼트, 사용자 지정 세그먼트 및 저장된 대상](/help/dsp/audiences/audience-settings.md). 선택한 모든 세그먼트 및 저장된 대상에 대한 총 및 활성 중복 제거된 대상 크기도 표시됩니다. 기존 대상을 선택하거나, 나중에 다시 사용할 수 있는 새 대상을 만들거나, 특정 대상 세그먼트를 선택할 수 있습니다.

* 기존 대상자를 선택하려면 ![선택](/help/dsp/assets/chevron-down.png) 다음 [!UICONTROL Included Audiences], 그런 다음 대상자를 선택합니다.
* 새 대상을 만들려면 ![선택](/help/dsp/assets/chevron-down.png) 다음 [!UICONTROL Included Audiences]를 선택한 다음 을 선택합니다. **[!UICONTROL + Create Audience]**. 자세한 내용은 [재사용 가능한 대상 만들기](/help/dsp/audiences/reusable-audience-create.md), 3단계부터
* 특정 대상 세그먼트를 선택하려면 **[!UICONTROL Select segments for this placement only]**. 세그먼트 논리를 선택합니다. 지침은 &quot;[재사용 가능한 대상 만들기](/help/dsp/audiences/reusable-audience-create.md).&quot; 완료되면 을(를) 클릭합니다. **저장**.

**[!UICONTROL Excluded Audiences]:** 을 사용하는 대상을 포함하여 배치에 대해 제외할 모든 대상 [타사 세그먼트, 퍼스트 파티 세그먼트, Adobe 세그먼트, 사용자 지정 세그먼트 및 저장된 대상](/help/dsp/audiences/audience-settings.md). 제외된 모든 대상에 대한 총 및 활성 중복 제거된 대상 크기도 표시됩니다. 기존 대상자를 선택하거나 나중에 다시 사용할 수 있는 새 대상자를 만들 수 있습니다.

* 기존 대상자를 선택하려면 ![선택](/help/dsp/assets/chevron-down.png) 다음 [!UICONTROL Excluded Audiences], 그런 다음 대상자를 선택합니다.
* 새 대상을 만들려면 ![선택](/help/dsp/assets/chevron-down.png) 다음 [!UICONTROL Excluded Audiences]를 선택한 다음 을 선택합니다. **+ 대상 만들기**. 자세한 내용은 [재사용 가능한 대상 만들기](/help/dsp/audiences/reusable-audience-create.md), 3단계부터

**[!UICONTROL Cross Device Targeting]:** 세그먼트 또는 대상을 한 개 이상 선택하고 [campaign은 사람 기반 교차 장치 타깃팅을 위해 구성됩니다](/help/dsp/campaign-management/campaigns/campaign-settings.md). 지정된 세그먼트에 없는 장치라도 개인의 알려진 모든 장치(캠페인 설정에 지정된 장치 그래프에 따라)에 걸쳐 타깃팅을 확장할 수 있습니다. 요금은 캠페인에 대해 지정된 그래프에 따라 적용될 수 있습니다. 장치 그래프 데이터는 현재 북미에서만 사용할 수 있습니다.

**[!UICONTROL Placement Cap]:** (선택 사항) 고유 장치 또는 사람의 횟수입니다(지정된 [!UICONTROL Cross Device Level] 캠페인의 경우)가 배치에서 광고에 제공됩니다. 옵션은 다음과 같습니다 *[!UICONTROL Unlimited]* 또는 일, 주 또는 개월당 특정 금액입니다.

>[!NOTE]
>
> 캠페인, 패키지 및 배치 수준에서 빈도 캡을 설정할 수 있습니다. DSP은 캠페인 계층에서 가장 엄격한 빈도 제한을 준수합니다.

**[!UICONTROL Secondary Cap]:** (선택 사항) 숫자를 포함할 때 사용할 수 있습니다. [!UICONTROL Placement Cap]) 기본 배치 캡의 경계 내에 추가 제한이 있습니다. 노출 횟수 및 기간(예: 12시간당 3시간)을 선택합니다.

**[!UICONTROL Day Parting]:** (선택 사항) 광고가 실행될 수 있는 특정 요일 및 시간입니다. 방송 시간 분할 간격을 지정하려면
1. 클릭 ![편집](/help/dsp/assets/edit.png).
1. 적용 가능한 시간대를 선택합니다.
1. 간격을 지정합니다.
   * 미리 설정된 간격을 선택하려면 간격 단추 중 하나를 클릭합니다. 옵션에는 *[!UICONTROL Weekends]**, *[!UICONTROL Weekdays]*, *[!UICONTROL Morning]*, *[!UICONTROL Lunch]*, *[!UICONTROL Dinner]*, 또는 *[!UICONTROL Prime]* (primetime).
   * 간격을 수동으로 선택하려면 셀 내부를 클릭하고 선택적으로 드래그하여 간격을 선택합니다.
1. 클릭 **[!UICONTROL Save]**.

**[!UICONTROL Topic Targeting]:** (선택 사항) 으로 구성된 광고주 [!DNL Comscore] 및 [!DNL Grapeshot] 세그먼트) 의 특정 세그먼트 이름 또는 ID를 [!DNL Comscore] 및 [!DNL Grapeshot] 을 타겟으로 포함시킵니다. 이 기능에 대한 추가 비용이 발생할 수 있습니다. 이 기능을 활성화하고 주제 세그먼트를 설정하려면 [!DNL Adobe] 계정 팀입니다.

주제 타깃팅을 지정하려면 다음을 수행하십시오.

1. 클릭 ![편집](/help/dsp/assets/edit.png).
1. 타겟팅할 세그먼트 지정:
   1. 왼쪽 열에서 partner (*[!UICONTROL Comscore]* 또는 *[!UICONTROL Grapeshot]*).
   1. 입력 필드에 세그먼트 이름 또는 세그먼트 ID를 입력합니다.
1. (선택 사항) 주제 정보가 포함된 CSV 파일을 브라우저의 다운로드 위치에 다운로드하려면 를 클릭합니다 **[!UICONTROL Export]**.
1. 클릭 **[!UICONTROL Save]**.

>[!TIP]
>
>* 항목 타깃팅은 게재에 입찰할 수 있는 인벤토리를 제한하므로 전체 구매의 소수 비율에 대해서만 항목 타깃팅을 사용합니다.
>
>* 의 세그먼트 내에서 임의 음수 타겟팅 설정 [!DNL Comscore] 또는 [!DNL Grapeshot].


**[!UICONTROL Device Targeting]:** (선택 사항) 타깃으로 포함 및 제외할 장치 유형, 제조업체, 운영 체제, 브라우저 및 연결 유형을 포함한 특정 장치 정보. 장치 타깃팅을 지정하려면 다음을 수행하십시오.

1. 클릭 ![편집](/help/dsp/assets/edit.png).
1. 포함 및 제외할 장치 세부 사항을 지정합니다.
   1. 왼쪽 열에서 카테고리를 선택합니다.
   1. 타겟팅 지정:
      * 값을 포함하려면 **[!UICONTROL Include]** 값 이름 옆에 표시됩니다.
      * 값을 제외하려면 **[!UICONTROL Exclude]** 값 이름 옆에 표시됩니다.
1. (선택 사항) 장치 타깃팅 정보가 있는 CSV 파일을 브라우저의 다운로드 위치에 다운로드하려면 를 클릭합니다 **[!UICONTROL Export]**.
1. 클릭 **[!UICONTROL Save]**.

**[!UICONTROL ISP Targeting]:** (선택 사항) 대상으로 포함 또는 제외(둘 다 제외)할 특정 인터넷 서비스 공급자(ISP)입니다. ISP 타깃팅을 지정하려면

1. 클릭 ![편집](/help/dsp/assets/edit.png).
1. 포함 또는 제외할 ISP를 지정합니다.
   * ISP를 포함하려면:
      1. 클릭 **[!UICONTROL Include ISPs]**.
      1. (선택 사항) 목록을 키워드로 필터링합니다.
      1. 타깃팅할 각 ISP 옆에 있는 확인란을 선택합니다.
   * ISP를 제외하려면 다음을 수행하십시오.
      1. 클릭 **[!UICONTROL Exclude ISPs]**.
      1. (선택 사항) 목록을 키워드로 필터링합니다.
      1. 제외할 각 ISP 옆에 있는 확인란을 선택합니다.
1. (선택 사항) ISP 타깃팅 정보가 있는 CSV 파일을 브라우저의 다운로드 위치에 다운로드하려면 를 클릭합니다 **[!UICONTROL Export]**.
1. 클릭 **[!UICONTROL Save]**.

## [!UICONTROL Brand Safety and Media Targeting]

**[!UICONTROL Contextual filtering]:** 유형 [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], 및 [!DNL Peer39] 적용할 상황별 필터. 새 배치에 대해 광고주 수준 기본값이 선택되지만 설정을 변경할 수 있습니다.

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block sites that are]:** (선택 사항) 기본적으로 차단할 하나 이상의 유형의 재고 컨텍스트. 추가 비용이 발생할 수 있습니다.

* [!UICONTROL Peer 39]:

   * **다음과 같은 Target 사이트:** (선택 사항) 기본적으로 타깃팅할 하나 이상의 유형의 재고 속성입니다. 추가 비용이 발생할 수 있습니다.

* [!UICONTROL ComScore]:

   * **다음을 수행하는 사이트를 차단합니다.** (선택 사항) 기본적으로 차단할 하나 이상의 유형의 재고 속성입니다. 추가 비용이 발생할 수 있습니다.

* [!UICONTROL Integral Ad Science]

   * **[!UICONTROL Adult Content]:** (선택 사항) 기본적으로 광고를 차단할 성인물 콘텐츠의 정도입니다. *[!UICONTROL Do Not Block]* (기본값), *[!UICONTROL Standard]*, 또는 *[!UICONTROL Strict]*. 추가 비용이 발생할 수 있습니다.

   * **[!UICONTROL Alcohol Content]:** (선택 사항) 기본적으로 광고를 차단하는 알코올 도입니다. *[!UICONTROL Do Not Block]* (기본값), *[!UICONTROL Standard]*, 또는 *[!UICONTROL Strict]*. 추가 비용이 발생할 수 있습니다.

**[!UICONTROL Pre-bid fraud blocking]:** 측정된 부정 트래픽과 의심스러운 활동을 기반으로 차단할 사이트 유형 [!DNL DoubleVerify], [!DNL Integral Ad Science], 및 [!DNL Peer39]. 새 배치에 대해 광고주 수준 기본값이 선택되지만 설정을 변경할 수 있습니다.

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** 기본적으로 에서는 새 배치에 대해 강조 표시된 장치의 트래픽을 포함하여 100% 잘못된 트래픽을 모두 차단합니다. 추가 비용이 발생할 수 있습니다.

   * **[!UICONTROL Also block sites with]:** (선택 사항) 기본적으로 DSP에서 광고를 차단하는 추가 사기 및 잘못된 트래픽 수준입니다.  *[!UICONTROL None]* (추가 트래픽을 차단하지 않는 기본값), *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]*, 또는 *[!UICONTROL >25% Average Fraud/IVT levels]*. 추가 비용이 발생할 수 있습니다.

* [!UICONTROL Peer 39]:

   * **[!UICONTROL Block sites that are]:** (선택 사항) DSP에서 기본적으로 광고를 차단하는 하나 이상의 사기 유형입니다. *[!UICONTROL Fraud]* (사기 행위로 모든 사이트를 차단함), *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]*, 및/또는 *[!UICONTROL Fraud: Zero Ads]*. 추가 비용이 발생할 수 있습니다.

* [!UICONTROL Integral Ad Science]:

   * **[!UICONTROL Block sites that are]:** (선택 사항) DSP이 기본적으로 광고를 차단하도록 하는 의심스러운 웹 사이트 또는 앱 활동 유형입니다. *[!UICONTROL None]* (의심스러운 활동을 기반으로 광고를 차단하지 않는 기본값), *[!UICONTROL Suspicious Activity - High Risk]*, 또는 *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. 추가 비용이 발생할 수 있습니다.

**[!UICONTROL Ads.txt filtering]:**

어느 수준 [Ads.txt](https://iabtechlab.com/ads-txt-about/) 각 게시자의 승인된 디지털 판매자 목록을 활용하여 사용할 사전 입찰 필터링입니다. 새 배치에 대해 광고주 수준 기본값이 선택되지만 설정을 변경할 수 있습니다.

* *[!UICONTROL Opt out of ads.txt (default)]*: 모든 판매자로부터 재고를 구입하기 위해서.
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*: 도메인의 공인 직접 판매자 및 리셀러에서 인벤토리 구매에 우선 순위를 두기
* *[!UICONTROL Ads.txt sellers only]*: 도메인의 공인 직접 판매자와 리셀러에서만 인벤토리를 구매하려면
* *[!UICONTROL Ads.txt sellers only]*: 도메인의 공인 직접 판매자로부터 인벤토리를 구입하기 위해

**[!UICONTROL DoubleVerify Authentic Brand Safety]:** (광고주는 [!UICONTROL DoubleVerify Authentic Brand Safety] 옵션) 사용 [!DNL DoubleVerify Authentic Brand Safety]: 지정된 세그먼트 ID에 대해 구성된 사용자 지정 브랜드 안전 규칙을 사용하여 입찰 후 노출 횟수를 차단합니다. DSP에서는 광고주 설정에 지정된 세그먼트 ID에 대한 사용을 위해 계정에 청구합니다.

## [!UICONTROL Tracking] {#placement-tracking}

>[!NOTE]
>
>([!DNL Roku] 배치) [!DNL Roku] 포함 [!DNL Acxiom], [!DNL comScore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk], 및 [!DNL Research Now].

**[!UICONTROL Event Pixels]:** (선택 사항) 배치의 모든 새 광고에 기본적으로 첨부할 타사 이벤트 추적 픽셀입니다. 이벤트 픽셀을 지정하려면

1. 클릭 ![편집](/help/dsp/assets/edit.png).
1. 다음 중 하나를 수행합니다.
   * 기존 픽셀을 선택하려면 픽셀 행에서 확인란을 선택합니다.
   * 새 픽셀을 만들려면
      1. 클릭 **[!UICONTROL Create]**.
      1. 다음 정보를 입력합니다.
         * **[!UICONTROL Pixel name]:** 픽셀 이름 최대 길이는 500자입니다. 픽셀을 쉽게 식별하는 데 도움이 되는 이름을 사용하십시오.
         * **[!UICONTROL Pixel event fires on]:** 픽셀을 트리거하여 실행하는 이벤트입니다. 사용 가능한 이벤트는 광고 유형에 따라 다릅니다.
         * **[!UICONTROL Pixel type]:** 픽셀이 *[!UICONTROL IMG URL]* (1x1 픽셀 이미지 파일), *[!UICONTROL HTML]*, 또는 *[!UICONTROL JavaScript URL]*.
         * **[!UICONTROL Pixel URL]:** 픽셀 이미지의 URL입니다.
      1. 클릭 **[!UICONTROL Create and attach]**.
   1. 클릭 **[!UICONTROL Save]**.

**[!UICONTROL Conversion Pixels]:** (선택 사항) 배치의 모든 새 광고에 기본적으로 첨부할 변환 추적 픽셀입니다. 변환 픽셀을 지정하려면

1. 클릭 ![편집](/help/dsp/assets/edit.png).
1. 다음 중 하나를 수행합니다.
   * 기존 픽셀을 선택하려면 픽셀 행에서 확인란을 선택합니다.
   * 새 픽셀을 만들려면
      1. 클릭 **[!UICONTROL Create]**.
      1. 다음 정보를 입력합니다.
         * **[!UICONTROL Conversion pixel name]:** 픽셀 이름 최대 길이는 500자입니다. 픽셀을 쉽게 식별하는 데 도움이 되는 이름을 사용하십시오.
         * **[!UICONTROL Conversion category]:** 전환 유형입니다.
         * **[!UICONTROL Impression conversion window]:** 광고 노출이 발생한 후 일 수로, 노출이 전환으로 인한 것일 수 있습니다. 기본값은 30일입니다.
         * **[!UICONTROL Click conversion window]:** 광고 클릭이 발생한 후 클릭이 전환으로 인한 것일 수 있는 일 수입니다. 기본값은 30일입니다.
         * **[!UICONTROL Notes]:** (선택 사항) 픽셀에 대한 설명 또는 기타 정보입니다.
      1. 클릭 **[!UICONTROL Create and attach]**.
      1. 관련 웹 페이지에서 변환 픽셀을 구현합니다.
         1. 주 메뉴에서 **[!UICONTROL Resources]>[!UICONTROL Conversion pixels]**.
         1. 픽셀 행에서 **[!UICONTROL edit]**.
         1. 에서 값을 복사합니다. [!UICONTROL HTML Tag] 및 [!UICONTROL Flash Tag] 광고주 또는 웹 사이트 연락처에 제공하기 위한 필드입니다.

            광고주의 IT 부서나 다른 그룹은 태그 배포를 예약하거나 알려주어야 할 수 있습니다.
   1. 클릭 **[!UICONTROL Save]**.

**[!UICONTROL 3rd-party Fees]:** (선택 사항) 1000개 노출당 청구 가능한 비용으로 추적할 정적, 타사 요금. 적용 가능한 경우 패키지 수준 기본값은 다른 값을 입력하지 않는 한 새 배치에 자동으로 적용됩니다.

>[!NOTE]
>
>청구 가능한 수수료는 [!UICONTROL Net CPM] 지표.

>[!MORELIKETHIS]
>
>* [배치 관리 정보](placement-about.md)
>* [배치 만들기](placement-create.md)
>* [배치 편집](placement-edit.md)
>* [배치에 대한 변경 로그 보기](placement-change-log.md)
>* [키보드 단축키](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [Campaign Management에 대한 FAQ](/help/dsp/campaign-management/campaign-management-faq.md)

