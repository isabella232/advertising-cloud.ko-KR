---
title: 플랫폼 내 보고서 정보
description: 캠페인 관리 보기에 포함된 보고서 데이터에 대해 알아봅니다.
feature: DSP Campaign Data Views
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '940'
ht-degree: 0%

---

# 플랫폼 내 보고서 정보

<!-- rename "About Performance Reports in Campaign Management Views?" -->
캠페인 관리 보기에는 포괄적인 보고서 데이터가 포함됩니다. 사용 가능한 보고서는 성과가 좋은 패키지 및 배치와 주의가 필요한 배치를 식별하는 데 도움이 됩니다. 빠른 작업 버튼을 사용하면 생산성을 높일 수 있습니다.

## 모든 캠페인 보기

다음 [!UICONTROL Campaigns] 계정 내의 모든 캠페인 목록과 성능 데이터 차트 세트가 열립니다.

### 차트 보기 {#chart-view}

다음을 수행할 수 있습니다 [시계열 트렌드 차트 사용자 지정](campaign-data-visualization-manage.md) 3개의 지표를 사용하여 모든 캠페인에서 사용 기본적으로 데이터 [!UICONTROL Net Spend], [!UICONTROL Impressions], 및 [!UICONTROL Net CPM] 별개의 차트(trellis 차트)에 포함됩니다. 지표를 선택적으로 변경할 수 있습니다. 시계열 트렌드 차트에서 시간별 데이터를 활성화하려면 날짜 선택을 하루([!UICONTROL Today], [!UICONTROL Yesterday], 또는 특정 날짜 ).

![세 개의 지표에 대한 개별 트렌드 차트](/help/dsp/assets/trend-chart-separate.png)

또한 3개의 지표를 오버레이하여 예외 항목을 쉽게 감지하고 비율이나 성능을 향상시킬 수도 있습니다.

![오버레이가 있는 트렌드 차트](/help/dsp/assets/trend-chart.png)

### 테이블 보기

![캠페인 목록](/help/dsp/assets/campaigns-list.png)

기본적으로 각 캠페인 행에는 게재 지표와 게재 간격이 포함됩니다. 게재 지표에는 다음이 포함됩니다 [!UICONTROL Gross Spend (Lifetime)]에는 캠페인의 모든 패키지에서 실제 타겟 소비와 예상되는 타겟 내 지출의 지표가 포함되어 있으므로 성과가 낮은 캠페인을 한 눈에 식별할 수 있습니다. 원할 경우 [열 보기 변경](column-view-change.md) 또는 [사용자 지정 열 보기 만들기](column-view-create.md).

추가 작업을 수행할 수 있습니다 [데이터 테이블 사용자 지정](campaign-data-views-about.md) 추가적인 방법 및 [표시된 데이터 필터링](campaign-data-filter.md).

캠페인을 자세히 보려면 캠페인 이름을 클릭합니다.

## 단일 캠페인 보고 {#single-campaign-reporting}

캠페인 내에서 캠페인 엔터티를 기반으로 데이터를 필터링할 수 있습니다. [!UICONTROL Packages], [!UICONTROL Placements], 및 [!UICONTROL Ads]. 추가 작업을 수행할 수 있습니다 [표시된 데이터 필터링](campaign-data-filter.md) 표시하려는 패키지, 배치 또는 광고만 포함하려면,

![캠페인 엔티티 탭](/help/dsp/assets/campaign-subtabs.png)

### 차트 보기

각 캠페인에 대해 다음을 수행할 수 있습니다 [시계열 트렌드 차트 사용자 지정](campaign-data-visualization-manage.md) 각 엔티티 보기에서 사용할 수 있는 세 개의 지표가 있습니다. 동일한 지표가 캠페인의 모든 트렌드 차트에서 유지됩니다.

자세한 내용은 [교차 캠페인 지표에 대한 &quot;차트 보기&quot; 섹션](#chart-view) 추가 정보.

### 테이블 보기

각 엔티티 탭에서 각 행에는 기본적으로 게재 및 게재 지표가 포함되어 있지만, 다음을 수행할 수 있습니다 [열 보기 변경](column-view-change.md) 또는 [사용자 지정 열 보기 만들기](column-view-create.md) 을 눌러 캠페인에 대한 모든 하위 탭에서 을 적용합니다. 추가 작업을 수행할 수 있습니다 [데이터 테이블 사용자 지정](campaign-data-views-about.md) 추가 방법. 각 데이터 테이블에는 [!UICONTROL Subtotals] 행 - 표시되는 모든 행에 있는 각 지표의 합계 또는 평균 값을 표시합니다.

### 배치 [!UICONTROL Inspector] {#placement-inspector}

각 배치에 대해 다음을 수행할 수 있습니다 [(세부 사항 보기) 열기 [!UICONTROL Inspector])](placement-details-view.md)에는 다음 깊이 데이터가 포함됩니다.

* **[!UICONTROL Sites]:** 배치에 있는 모든 사이트에 노출이 있습니다.

   다음 [!UICONTROL Sites] 탭에는 검색 및 필터 기능, 기본 페이지에서 사용할 수 있는 것과 동일한 표준 및 사용자 지정 열 보기 옵션, 및 [!UICONTROL Exclude] 배치에서 사이트를 빠르게 제외할 수 있도록 각 행에 있는 버튼.

* **[!UICONTROL Ads]:** 게재의 모든 광고.

   다음 [!UICONTROL Ads] 탭에는 검색 및 필터 기능, 기본 페이지에서 사용할 수 있는 것과 동일한 표준 및 사용자 지정 열 보기 옵션, 각 행의 빠른 작업 버튼이 포함되어 있습니다 [!UICONTROL Pause] (따라서 광고를 빠르게 일시 중지할 수 있습니다.)

* **[!UICONTROL Frequency]:** 다음을 포함하여 배치에 대한 각 광고 빈도 수준에 대한 데이터:
   * 광고 빈도 수준(사용자가 광고를 한 번 본 모든 인스턴스에 대해 &quot;1&quot; 등)
   * 장치/브라우저 또는 사람의 예상 고유 수(지정된 [!UICONTROL Cross Device Level] 지정된 빈도 수준에서 노출 횟수를 수신한( 캠페인)
   * 지정된 빈도 수준의 예상 노출 횟수
   * 지정된 빈도 수준에 대한 예상 평균 빈도입니다. 이 값은 (예상 노출 수)/(예상 고유 수)와 같습니다.

* **[!UICONTROL Inventory]:** 배치에서 타겟팅한 모든 거래에 대한 정보입니다.

   다음 [!UICONTROL Inventory] 탭에서는 성능 통계를 표시하여 신속한 문제 해결을 수행할 수 있습니다. 예를 들면 다음과 같습니다 [!UICONTROL Auctions], [!UICONTROL Bids], 및 [!UICONTROL Win Rate]. 탭에는 검색 및 필터 기능, 기본 페이지에서 사용할 수 있는 것과 동일한 표준 및 사용자 지정 열 보기 옵션, 그리고 각 행의 빠른 작업 버튼이 포함되어 있습니다 [!UICONTROL Edit], [!UICONTROL View Report], 및 [[!UICONTROL Auction Insights] 추가 문제 해결](/help/dsp/inventory/private-deal-auction-insights.md).

#### 인벤토리 문제 해결

| 문제 | 가능한 원인 | 수행할 작업 |
| -----------| ---------- | ---------- |
| [!UICONTROL Zero Auctions] | 게시자가 입찰 요청을 보내지 않았습니다. | 거래를 활성화하려면 게시자에게 문의하십시오. |
|  | 잘못된 외부 거래 ID를 입력하는 등의 방식으로 거래가 잘못 설정되었습니다. | 거래 세부 사항을 확인하고 거래를 편집합니다. |
| [!UICONTROL Auctions but no Bids] | 배치 타겟팅이 거래에 대해 들어오는 입찰 요청과 일치하지 않습니다. <br><br> 예를 들어, 게재는 해당 거래에 적합하지 않은 지역을 타겟팅하는 것일 수 있습니다. | 타깃팅 불일치를 방지하기 위해 필요에 따라 배치 대상을 편집합니다. |
|  | 배치에 거래에 필요한 미디어 유형이 있는 활성 광고가 없습니다. | 배치에 올바른 미디어 유형을 사용하는 광고를 만들고 첨부합니다. |
|  | 그 배치에는 충분한 예산이 없다. | 들어오는 요청에 대한 입찰을 허용하도록 배치 예산을 늘립니다. |
|  | 배치 플라이트 날짜는 거래에 대한 노출 배달 날짜와 겹치지 않습니다. | 필요에 따라 배치의 플라이트 날짜를 편집합니다. |
| [!UICONTROL Low Win Rate] | 배치의 최대 입찰(바닥 또는 고정)은 거래에 필요한 최소 입찰보다 낮습니다. | 배치 증가 [!UICONTROL Max Bid] 필요한 경우. |
|  | 게재는 입찰을 제한하는 사전 입찰 필터를 사용합니다. | 입찰 전 필터의 임계값을 낮추어 더 많은 입찰을 허용합니다. |
|  | 배치에 대한 대상 타깃팅이 너무 제한적입니다. | 지정된 대상 타겟에 활성 사용자가 충분한지 확인하고, 가능한 경우 대상을 확장합니다. |

![배치 검사자](/help/dsp/assets/placement-inspector.png)

에서 데이터를 내보낼 수 있습니다 [!UICONTROL Sites], [!UICONTROL Ads], 또는 [!UICONTROL Frequency] XLSM 형식의 보고서로 브라우저의 기본 다운로드 폴더에 탭으로 이동합니다.

### 기타 유형의 캠페인 수준 보고

기타 데이터 분류의 경우 [캠페인 수준 보고 페이지](/help/dsp/campaign-management/campaigns/campaign-view-report.md). 다음 <!--legacy --> 보고서에 섹션 포함 [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability], 및 [!UICONTROL Audience Performance] 데이터.

>[!MORELIKETHIS]
>
>* [배치에 대한 사이트, 광고 및 빈도 세부 사항 보기](placement-details-view.md)
>* [Campaign 데이터 보기 정보](campaign-data-views-about.md)
>* [사용자 지정 열 보기 만들기](column-view-create.md)
>* [열 보기 변경](column-view-change.md)
>* [데이터 시각화 관리](campaign-data-visualization-manage.md)
>* [Campaign Management 보기에서 데이터 내보내기](campaign-export-data.md)
>* [캠페인에 대한 세부 보고서 보기](/help/dsp/campaign-management/campaigns/campaign-view-report.md)

