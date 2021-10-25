---
title: Advertising Cloud DSP의 새로운 기능
description: 이 페이지에서는 Advertising Cloud DSP의 새로운 기능과 최근에 변경된 기능에 대해 설명합니다.
cloud: Experience Cloud
product: advertising cloud
index: true
exl-id: d4b67393-e8c5-4170-92eb-bcf643ba3ec3
source-git-commit: 1c59de261bb9ffcb382009bd1e988124ad5aa2f0
workflow-type: tm+mt
source-wordcount: '1066'
ht-degree: 0%

---

# 새로운 기능

다음 기능은 새로운 기능 또는 최근에 변경되었습니다.

<!-- | 19  October 2021 | The [!UICONTROL Deal ID] settings and other places in the user interface reflect new branding for [!DNL Magnite] SSP:<ul><li>The SSP "[!DNL Tremor]" ([!DNL Telaria]) is now "[!DNL Magnite CTV]."</li><li>[!DNL Rubicon]" is now "[!DNL Magnite DV+]," where [!DNL DV+] stands for display, video, and other formats such as audio.</li></ul> | See "[SSP Partners](/help/dsp/inventory/ssp-partners.md)." | -->

| 날짜 | 기능 | 설명 | 추가 정보 |
| ---- | ------- | ----------- | -------------------- |
| 2021년 10월 7일 | 도움말 | 모두 [DSP 및 기타 Advertising Cloud 설명서](https://experienceleague.adobe.com/docs/advertising-cloud.html) on [!DNL Experience League] 이제 모든 언어로 번역된 기계입니다. 표시된 언어를 변경하려면 페이지의 왼쪽 하단에 있는 &quot;언어 변경&quot; 메뉴를 사용합니다.<br>![언어 변경](/help/dsp/assets/change-language.png) |
| 2021년 9월 30일 | 브랜드 안전 | (22 9월 릴리스) [!DNL DoubleVerify] 브랜드 안전 사전 입찰 제품이 [!DNL Brand Suitability Tiers]: 광고주가 특정 항목의 모든 인스턴스를 피하지 않고 특정 세그먼트에 대해 세 가지 위험 수준(낮음, 중간, 높음) 중에서 선택할 수 있도록 합니다. 이전에는 세그먼트에 허용치 레벨이 포함되지 않았습니다.<br><br>새 [!DNL DoubleVerify] 세그먼트 구조, DSP에서 기존 브랜드 안전 세그먼트를 새롭고 권장되는 세그먼트로 마이그레이션했습니다. *중간*-level 세그먼트. 선택적으로 세그먼트 계층을 *낮음* 또는 *높음*.<br><br>**참고:** 작은 세그먼트 목록에는 계층이 없지만 &quot;Incentized/Spyware/Malware,Warz&quot; > Incentized/Malware/Clutter&quot;와 같은 새로운 이름이 있습니다. | — |
|  | 최적화 | 다음 최적화 목표 및 사전 입찰 필터는 더 이상 사용되지 않습니다.<ul><li>최적화 목표:<ul><li>[!UICONTROL Always Max Bid & Highest Viewability Rate (Moat – GroupM)]</li><li>[!UICONTROL Always Max Bid & Highest Viewability Rate (Moat – MRC)]</li></ul><li>사전 입찰 필터 목표:<ul><li>[!UICONTROL Viewability IAS]</li><li>[!UICONTROL Viewability Moat]</li></ul></ul> | 참조:[최적화 목표 및 사용 방법](/help/dsp/optimization/optimization-goals.md)&quot; 및 &quot;[배치 수준 사전 입찰 필터 및 사용 방법](/help/dsp/optimization/optimization-pre-bid-filters.md).&quot; |
| 2021년 9월 28일 | 캠페인 관리 보기 | A &quot;[!UICONTROL Creation date]&quot; 열은 이제 의 사용자 지정 열 세트에서 사용할 수 있습니다 [!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements], 및 [!UICONTROL Ads] 보기. 을(를) 필터링할 수도 있습니다 [!UICONTROL Placements] 및 [!UICONTROL Ads] 보기 기준 [!UICONTROL Creation date]. | 참조:[사용자 지정 열 보기 만들기](/help/dsp/campaign-management/reports/column-view-create.md)&quot; 및 &quot;[캠페인 데이터 필터링](/help/dsp/campaign-management/reports/campaign-data-filter.md).&quot; |
|  | 프로그램 방식의 보장 거래 | (8월 릴리스) 이제 [!UICONTROL Max Bid] 프로그램 보증(PG) 거래에 대한 기본 배치입니다. 그러나 PG 계약에는 항상 고정된 CPM이 있으므로 국제 클라이언트만 [!UICONTROL Max Bid] 통화료를 고려하다. | — |
|  |  | (8월 릴리스) &quot;[!DNL FreeWheel Programmatic Guaranteed]&quot; 사용 권한에 대한 광고를 이제 [!DNL FreeWheel Programmatic Creative API] 에서 [!UICONTROL Ads] 보기 또는 [!UICONTROL Placements] 보기. 에서 광고를 제출할 수 있습니다. [!UICONTROL Deals] 보기. | —<!-- Add link to page on submitting ads to Freewheel once it's edited. --> |
| 2021년 8월 11일 | 사전 입찰 뷰가능 | 입찰 전 뷰가능 필터 [!DNL Oracle Advertising (Moat)] 이제 배치에 대해 사용할 수 있습니다. | 자세한 내용 [입찰 전 뷰가능 여부를 위한 타사 통합](/help/dsp/introduction/features/brand-safety-media-quality.md#pre-bid-viewability) 및 &quot;[배치 수준 사전 입찰 필터 및 사용 방법](/help/dsp/optimization/optimization-pre-bid-filters.md).&quot; |
| 7월 15일 | 도움말 | Advertising Cloud DSP에서 미디어 및 서비스 구매를 위해 고객이 계정을 처리하는 방법에 대한 세부 사항이 추가되었습니다. | 참조:[계정 자금조달](/help/dsp/introduction/billing/account-funding.md).&quot; |
| 2021년 6월 12일 | 도움말 | 광고 정책이 업데이트되었습니다. | 참조:[Adobe Advertising Cloud 광고 요구 사항 정책](/help/policies/ad-requirements-policy.md).&quot; |
| 2021년 6월 7일 | 도움말 | 지침은 [!DNL FreeWheel]. | 참조:[프로그램 보장 거래 설정 개요 [!DNL FreeWheel]](/help/dsp/inventory/freewheel-overview.md),&quot; &quot;[프로그래밍 방식의 보장 거래에 대한 광고를 제출합니다. [!DNL FreeWheel]](/help/dsp/inventory/freewheel-submit.md),&quot; &quot;[광고 상태 확인 [!DNL Freewheel] 프로그램 방식의 보장 거래](/help/dsp/inventory/freewheel-check-status.md),&quot; 및 &quot;[에 대한 오류 코드 [!DNL FreeWheel] 광고 제출](/help/dsp/inventory/freewheel-error-codes.md).&quot; |
| 2021년 5월 27일 | 도움말 | 이 지침은 건강 관련 대상 세그먼트를 타깃팅하는 대체 요소로 사용할 수 있는 건강 관련 대상 세그먼트 및 전술에서 사용할 수 있습니다. | 참조:[허용 가능한 상태 세그먼트 지침](/help/policies/health-segment-guidelines.md).&quot; |
| 2021년 5월 26일 | 도움말 | Adobe Experience Cloud와의 통합 장은 이제 [Advertising Cloud 설명서 홈페이지](https://experienceleague.adobe.com/docs/advertising-cloud.html). 새 안내서에는 &quot;작업 중&quot;에 대한 새 하위 장이 포함되어 있습니다 [!DNL Analytics Marketing Channels].&quot;<br>이 DSP 안내서의 목차 에는 새 안내서에 대한 링크가 포함되어 있습니다. | 참조:[Adobe Experience Cloud과 통합](/help/integrations/home.md).&quot; |
| 2021년 5월 24일 | 도움말 | &quot;캠페인 관리&quot; 장에서는 Excel QA 스프레드시트를 사용하여 캠페인에 대한 주요 배치 설정을 검토 및 편집하는 방법에 대한 새 주제를 사용할 수 있습니다. | 참조:[스프레드시트를 사용하여 캠페인에 대한 배치 설정 수정 정보](/help/dsp/campaign-management/qa/qa-about.md), &quot;[캠페인에 대한 배치 설정 다운로드](/help/dsp/campaign-management/qa/qa-sheet-download.md),&quot; &quot;[캠페인에 대한 배치 설정 업로드](/help/dsp/campaign-management/qa/qa-sheet-upload.md), 및 &quot;[다운로드/업로드된 스프레드시트의 열](/help/dsp/campaign-management/qa/qa-sheet-columns.md). |
| 2021년 5월 5일 | 패키지 설정 | 새로운 간격 채우기 전략 옵션인 &#39;약간 앞으로&#39;가 사용 가능하며, 새 패키지의 기본값입니다. 이 전략은 55-65%가 비행 기간의 절반을 완수하도록 전송을 가속화합니다. | 참조:[패키지 설정](/help/dsp/campaign-management/packages/package-settings.md).&quot; |
| 2021년 3월 17일 | 도움말 | 더 많은 절차와 참조를 포함하도록 &quot;캠페인 관리&quot; 장을 확장했습니다. | 목차에서 &quot;캠페인 관리&quot; 장 및 하위 섹션을 엽니다. |
| 2021년 3월 10일 | 인벤토리 | 더 이상 만들 수 없습니다 [!UICONTROL Smart Ad Serving] 은 VAST 태그를 사용하는 것을 다룹니다. 대신, 거래 ID를 통해 개인 거래를 실행할 수 있는지 게시자에게 문의하십시오. 를 사용하여 게시자에서 직접 거래 ID를 가져올 수 있습니다. [!UICONTROL Deal ID inbox] 또는 수동으로 거래 세부 사항을 입력합니다.<br><br>기존의 스마트 광고 서비스 제공은 여전히 이용 가능하지만, 올해 말 종료될 예정입니다. | 참조:[정보 [!UICONTROL Deal ID inbox]](/help/dsp/inventory/deal-id-inbox-about.md)&quot; 및 &quot;[수동으로 만들기 [!UICONTROL Deal ID] 세부 사항](/help/dsp/inventory/deal-id-create.md)&quot; |
| 2021년 2월 25일 | 도움말 | 설명서 [!DNL Analytics for Advertising Cloud]Adobe Analytics과 Adobe Advertising Cloud을 통합하는 를 사용할 수 있습니다. | 통합에 대한 개요는 &quot;[개요 [!DNL Analytics for Advertising Cloud]](/help/integrations/analytics/overview.md).&quot; 전체 설명서는 &quot;Adobe Experience Cloud과 통합&quot; > &quot;에 있는 장을 참조하십시오.[!DNL Analytics for Advertising Cloud].&quot; |
| 2020년 10월 28일 | 새 도움말 | 기존 도움말은 업데이트된 페이지로 대체되었으며, 이 도움말은 의 도움말 링크에서 사용할 수 있습니다. [!DNL DSP] 기본 메뉴 및 [https://experienceleague.adobe.com/docs/advertising-cloud/dsp/home.html](https://experienceleague.adobe.com/docs/advertising-cloud/dsp/home.html). | — |
|  | 캠페인 | 이전 [!UICONTROL Campaigns Beta] 보기는 이제 기본값입니다 [!UICONTROL Campaigns] 보기 횟수, 더 빠른 통찰력, 간소화된 워크플로우 및 사용자 정의된 보기 수.<br><br>새로운 [!UICONTROL Campaigns] 보기는 다음과 같습니다.<ul><li>새 탐색. 계정 내의 모든 캠페인 목록을 볼 수 있습니다. 캠페인 내에서 캠페인 엔터티를 기반으로 데이터를 필터링할 수 있습니다. [!UICONTROL Packages], [!UICONTROL Placements], 및 [!UICONTROL Ads].<br><br>![캠페인 엔티티 탭](/help/dsp/assets/campaign-subtabs.png)</li><li>최대 3개의 지표를 비교할 수 있는 데이터 시각화.<br><br>![세 개의 지표에 대한 개별 트렌드 차트](/help/dsp/assets/trend-chart-separate.png)</li><li>사전 정의된 사용자 지정 열 보기를 만들고 관리하는 기능 [!UICONTROL Pacing] 및 [!UICONTROL Performance] 보기.<br><br>![열 보기 선택기](/help/dsp/assets/column-view-selector.png)</li><li>검색 및 필터링을 업그레이드했습니다.</li></ul><br>기존 [!UICONTROL Campaigns Classic] 오른쪽 상단의 프로필 메뉴에서 보기를 계속 사용할 수 있습니다. 를 열려면 [!UICONTROL Campaigns Classic] 보기, **[!UICONTROL Switch to Campaigns Classic]**.<br><br>![링크 대상 [!UICONTROL Campaigns Classic]](/help/dsp/assets/switch-campaigns-classic.png)<br><br>로 돌아가려면 [!UICONTROL Campaigns] 홈에서 **[!UICONTROL Exit Classic]**. | 참조:[플랫폼 내 보고서 정보](/help/dsp/campaign-management/reports/campaign-reports-about.md).&quot;<br><br>참조: &quot;[Campaign 데이터 보기 정보](/help/dsp/campaign-management/reports/campaign-data-views-about.md).&quot; |
|  | 배치 | 수동 입찰 규칙을 포함하는 옵션이 제거되어 DSP 최적화가 작업을 수행할 수 있습니다. 이제 최신성을 기반으로 한 모든 기존 최대 입찰이 자동으로 최적화됩니다. | — |
|  |  | 전반적인 성능을 향상시키기 위해 더 이상 뷰어의 시간대를 기준으로 방송 시간 분할을 할 수 없습니다. 대신, 모든 방송 시간 분할은 이제 캠페인의 시간대를 기반으로 &#x200B; 합니다. | 참조:[배치 설정](/help/dsp/campaign-management/placements/placement-settings.md).&quot; |
| 2020년 10월 15일 | 비공개 인벤토리 | 이제 모든 사용자는 기존 버전의 간소화된 새로운 거래 ID 양식을 사용하여 거래 ID 세부 사항을 설정하고 편집할 수 있습니다 [!UICONTROL Smart Ad Serving] 양식. 새 거래 ID 세부 사항을 설정하려면 다음 위치로 이동하십시오. [!UICONTROL Inventory] > [!UICONTROL Deals]를 클릭합니다. [!UICONTROL Create]를 클릭한 다음 [!UICONTROL Deal ID Beta]. | 참조:[수동으로 거래 ID 상세내역 생성](/help/dsp/inventory/deal-id-create.md)&quot; 및 &quot;[수동 거래 ID 설정](/help/dsp/inventory/deal-id-settings.md).&quot; |
|  | 배치 예측 | 배치 수준 게재 간격이 있는 배치의 경우, [!UICONTROL Forecast] 배치 설정의 섹션에는 새 항목이 포함됩니다 [!UICONTROL Estimated Maximums] 섹션을 참조하십시오. | — |
| 2020년 9월 2일 | 보고서 | 여러 DSP 계정이 있는 모든 조직은 조직의 요구 사항에 따라 사용자 지정 보고서에서 교차 계정 데이터를 선택적으로 활성화할 수 있습니다. | &quot;의 &quot;계정 간 보고&quot; 섹션을 참조하십시오.[사용자 지정 보고서 정보](/help/dsp/reports/report-about.md#cross-account-reporting).&quot; |
