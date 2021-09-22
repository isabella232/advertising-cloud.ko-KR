---
title: 플랫폼 내 보고서 정보
description: 캠페인 관리 보기에 포함된 보고서 데이터에 대해 알아봅니다.
feature: DSP Campaign Data Views
exl-id: e9f7dafe-e0db-4fec-bf5b-858cbcfdde45
source-git-commit: c1441fb6fddf56a0f0346a967da49efa0fb602ff
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 플랫폼 내 보고서 정보

<!-- rename "About Performance Reports in Campaign Management Views?" -->
캠페인 관리 보기에는 포괄적인 보고서 데이터가 포함됩니다. 사용 가능한 보고서는 성과가 좋은 패키지 및 배치와 주의가 필요한 배치를 식별하는 데 도움이 됩니다. 빠른 작업 버튼을 사용하면 생산성을 높일 수 있습니다.

## 모든 캠페인 목록

계정 내의 모든 캠페인 목록이 [!UICONTROL Campaigns] 보기에 열립니다. [!UICONTROL Subtotals] 행은 표시된 모든 행에 있는 각 지표의 합계 또는 평균 값을 보여줍니다.

![캠페인 목록](/help/dsp/assets/campaigns-list.png)

기본적으로 각 캠페인 행에는 게재 지표와 게재 간격이 포함됩니다. 게재 지표에는 캠페인의 모든 패키지에서 실제 타겟 소비와 예상되는 타겟 내 지출의 측정이 포함된 [!UICONTROL Gross Spend (Lifetime)]이 포함되어 있으므로 성과가 낮은 캠페인을 한 눈에 식별할 수 있습니다. 선택적으로 [열 보기를 변경하거나 ](column-view-change.md)사용자 지정 열 보기를 만들 수도 있습니다](column-view-create.md).[

추가 방법으로는 [데이터 테이블](campaign-data-views-about.md)을 사용자 지정하고 [보이는 데이터](campaign-data-filter.md)를 필터링할 수 있습니다.

캠페인을 자세히 보려면 캠페인 이름을 클릭합니다.

## 단일 캠페인 보고

캠페인 내에서 캠페인 엔터티를 기반으로 데이터를 필터링할 수 있습니다. [!UICONTROL Packages], [!UICONTROL Placements] 및 [!UICONTROL Ads] 표시하려는 패키지, 배치 또는 광고만 포함하도록 표시되는 데이터](campaign-data-filter.md)를 더 필터링할 수 있습니다.[

![캠페인 엔티티 탭](/help/dsp/assets/campaign-subtabs.png)

각 엔티티 탭에서 각 행에는 기본적으로 게재 및 게재 지표가 포함되어 있지만, [열 보기](column-view-change.md)를 변경하거나 [를 만들어 캠페인에 대한 모든 하위 탭에 적용할 수 있습니다. ](column-view-create.md) 추가 방법으로 [데이터 테이블](campaign-data-views-about.md)을 사용자 지정할 수 있습니다. 각 데이터 테이블에는 표시되는 모든 행에 대해 각 지표의 합계 또는 평균 값을 표시하는 [!UICONTROL Subtotals] 행이 있습니다.

각 캠페인에 대해 각 엔티티 보기에서 사용할 수 있는 3개의 지표로 시계열 트렌드 차트를 사용자 지정할 수도 있습니다. 기본적으로 [!UICONTROL Net Spend], [!UICONTROL Impressions] 및 [!UICONTROL Net CPM]의 데이터는 별도의 차트(트렐리스 차트)에 포함됩니다. 지표를 선택적으로 변경할 수 있습니다.

![세 개의 지표에 대한 개별 트렌드 차트](/help/dsp/assets/trend-chart-separate.png)

또한 3개의 지표를 오버레이하여 예외 항목을 쉽게 감지하고 비율이나 성능을 향상시킬 수도 있습니다.

![오버레이가 있는 트렌드 차트](/help/dsp/assets/trend-chart.png)

[캠페인별로 트렌드 차트](campaign-data-visualization-manage.md)를 사용자 지정할 수 있으며, 동일한 지표가 캠페인의 모든 트렌드 차트에서 유지됩니다.

### 배치 관리자

각 배치에 대해 다음 깊이 데이터가 포함된 (세부 보기 [!UICONTROL Inspector])](placement-details-view.md)를 [열 수 있습니다.

* **[!UICONTROL Sites]** : 배치에 있는 모든 사이트에 대한 노출 횟수.

   [!UICONTROL Sites] 탭에는 검색 및 필터 기능, 기본 페이지에서 사용할 수 있는 것과 동일한 표준 및 사용자 지정 열 보기 옵션, 배치에서 사이트를 빠르게 제외할 수 있는 각 행의 [!UICONTROL Exclude] 단추가 포함되어 있습니다.

* **[!UICONTROL Ads]** : 배치의 모든 광고.

   [!UICONTROL Ads] 탭에는 검색 및 필터 기능, 기본 페이지에서 사용할 수 있는 동일한 표준 및 사용자 지정 열 보기 옵션, [!UICONTROL Pause] 등의 각 행에 있는 빠른 작업 버튼이 포함되어 있으므로 광고를 빠르게 일시 중지할 수 있습니다.

* **[!UICONTROL Frequency]:** 다음을 포함하여 배치에 대한 각 광고 빈도 수준에 대한 데이터:
   * 광고 빈도 수준(사용자가 광고를 한 번 본 모든 인스턴스에 대해 &quot;1&quot; 등)
   * 지정된 빈도 수준에서 노출 횟수를 수신한 장치/브라우저 또는 사람(배치에 대해 지정된 [!UICONTROL Cross Device Level]에 따라 다름)의 예상 고유 수입니다
   * 지정된 빈도 수준의 예상 노출 횟수
   * 지정된 빈도 수준에 대한 예상 평균 빈도입니다. 이 값은 (예상 노출 수)/(예상 고유 수)와 같습니다.

* **[!UICONTROL Inventory]** : 단일 보기에서 배치에 의해 타깃팅된 모든 거래의 정보입니다.

재고 탭에는 검색 및 필터 기능, 기본 페이지에서 사용할 수 있는 것과 동일한 표준 및 사용자 지정 열 보기 옵션, 편집 및 보고서 보기와 같은 각 행의 빠른 작업 버튼이 포함되어 있습니다. 재고 탭은 경매, 입찰, 승률 등과 같은 성능 상태를 표시하여 빠른 문제 해결에 도움이 됩니다.

# 인벤토리 문제 해결

| 문제 | 가능한 원인 | 수행할 작업 |
| -----------| ---------- | ---------- |
| [!UICONTROL Zero Auctions] | 게시자가 입찰 요청 전송을 시작하지 않았습니다. | 거래를 활성화하려면 게시자에게 문의하십시오 |
|  | 잘못된 외부 거래 ID 입력 등과 같은 거래 설정 문제. | 거래 세부 사항을 확인하고 거래를 편집합니다 |
| [!UICONTROL Non-zero Auctions but no Bids] | 배치 타겟팅이 거래의 들어오는 입찰 요청과 일치하지 않습니다. <br><br> 예를 들어, 게재는 계약에 따라 필요한 지역과 다른 지역을 타겟팅할 수 있습니다 | 거래와 일치하지 않는 타깃팅을 방지하기 위해 배치 설정을 적절히 편집합니다 |
|  | 게재에 활성 광고가 없거나 거래에 필요한 올바른 미디어 유형이 없습니다 | 배치에 올바른 미디어 유형을 사용하여 광고 만들기/첨부 |
|  | 배치에 충분한 예산이 없습니다 | 들어오는 요청에 대한 입찰을 허용하기에 적합한 배치 예산 편집 |
|  | 배치 플라이트 날짜는 거래에 따른 노출 배달 날짜와 겹치지 않습니다 | 배치에 대한 플라이트 날짜 편집 |
| [!UICONTROL Low Win Rate] | 배치 시 최대 입찰은 거래에 필요한 최소(바닥 또는 고정)보다 낮게 설정됩니다 | 배치에서 최대 입찰 편집을 적절히 적합 |
|  | 이 배치에서는 제한하는 사전 입찰 필터를 사용합니다 | 입찰 전 필터의 임계값을 줄여 더 많은 입찰을 허용합니다 |
|  | 배치 시 대상 타깃팅이 너무 제한적입니다 | 지정된 대상 타겟에 충분한 활성 사용자가 있는지 확인하고 가능한 경우 대상을 확장합니다 |

![배치 검사자](/help/dsp/assets/placement-inspector-sites.png)

[!UICONTROL Sites], [!UICONTROL Ads] 또는 [!UICONTROL Frequency] 탭의 데이터를 XLSM 형식의 보고서로 브라우저의 기본 다운로드 폴더로 내보낼 수 있습니다.

### 기타 유형의 캠페인 수준 보고

다른 데이터 분류의 경우 [!UICONTROL Campaigns Classic]에서 [기존 캠페인 수준 보고 페이지](/help/dsp/campaign-management/campaigns/campaign-view-report.md)를 보십시오. 기존 보고서에는 [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability] 및 [!UICONTROL Audience Performance] 데이터의 섹션이 포함됩니다.

>[!MORELIKETHIS]
>
>* [배치에 대한 사이트, 광고 및 빈도 세부 사항 보기](placement-details-view.md)
>* [Campaign 데이터 보기 정보](campaign-data-views-about.md)
>* [사용자 지정 열 보기 만들기](column-view-create.md)
>* [열 보기 변경](column-view-change.md)
>* [데이터 시각화 관리](campaign-data-visualization-manage.md)
>* [캠페인 관리 보기에서 데이터 내보내기](campaign-export-data.md)
>* [캠페인에 대한 세부 보고서 보기](/help/dsp/campaign-management/campaigns/campaign-view-report.md)

