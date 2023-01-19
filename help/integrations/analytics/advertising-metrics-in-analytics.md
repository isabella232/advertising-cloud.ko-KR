---
title: Analysis Workspace의 광고 지표 Adobe
description: Analysis Workspace의 광고 지표 Adobe
feature: Integration with Adobe Analytics
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---

# Analysis Workspace의 광고 지표 Adobe

*Adobe Advertising-Adobe Analytics 통합 전용 광고주*

>[!NOTE]
>
>* Adobe 광고는 트래픽 지표 및 차원을 [!DNL Analytics] 매일.
>* [!DNL Analytics] 은(는) Adobe 광고 클릭스루 및 뷰스루를 실시간으로 캡처합니다.


## Adobe 광고의 트래픽 지표

>[!NOTE]
>
>의 모든 Adobe 광고 트래픽 지표 [!DNL Analytics] &quot;AMO&quot;로 시작합니다.

| 트래픽 지표 | 설명 |
| -------------- | ----------- |
| [!UICONTROL AMO Impressions] | Adobe 광고 노출 횟수. |
| [!UICONTROL AMO Clicks] | 총 Adobe 광고 클릭 수입니다. |
| [!UICONTROL AMO Cost] | Adobe 광고 비용은 보고서 세트의 통화로 표시됩니다. |
| [!UICONTROL AMO ID Instance] | Adobe 광고 ID가 설정된 횟수입니다. |
| [!UICONTROL AMO Minutes Viewed] | Adobe 광고 비디오를 본 시간(분)입니다. |
| [!UICONTROL AMO Views] | 광고에 대한 보기 수입니다. 보기는 뷰어가 Adobe 광고 비디오를 시작할 때 카운트됩니다. |
| [!UICONTROL AMO Views 25% Complete] | Adobe 광고 비디오의 25% 이상을 시청한 보기 수입니다. |
| [!UICONTROL AMO Views 50% Complete] | Adobe 광고 비디오의 50% 이상을 시청한 보기 수입니다. |
| [!UICONTROL AMO Views 75% Complete] | Adobe 광고 비디오의 75% 이상을 시청한 보기 수입니다. |
| [!UICONTROL AMO Views 100% Complete] | Adobe 광고 비디오를 100% 시청한 보기 수입니다. |
| [!UICONTROL AMO Viewable Impressions] | 배치 구성에 따라 볼 수 있도록 측정된 노출 횟수입니다. |
| [!UICONTROL AMO Not Viewable Impressions] | 볼 수 없음으로 확인된 노출 수입니다. 이 값은 ([!UICONTROL AMO Measurable Impressions] - [!UICONTROL AMO Viewable ]). |
| [!UICONTROL AMO Measurable Impressions] | 뷰기능 계기가 성공적으로 초기화된 제공된 노출 횟수. 이 값은 (계측된 노출 횟수 - 측정되지 않은 노출 횟수)로 계산됩니다. |

## Adobe 광고를 위한 유용한 사용자 지정 계산된 지표

Adobe 광고 데이터에 대해 다음 지표를 만드는 것이 좋습니다.

* 랜딩 페이지 인스턴스 클릭 수([!UICONTROL AMO ID Instances] / [!UICONTROL AMO Clicks]): 광고를 클릭하여 랜딩 페이지로 만든 사용자의 백분율입니다.
* 측정 가능 비율([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Impressions] * 100)
* 볼 수 있는 노출 비율([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Measureable Impressions] * 100)
* 뷰당 비용 ([!UICONTROL AMO Cost] / [!UICONTROL AMO Views])
* 클릭당 비용 ([!UICONTROL AMO Cost] / [!UICONTROL AMO Clicks])

## Adobe 광고 Dimension

>[!NOTE]
>
>의 모든 Adobe 광고 차원 [!DNL Analytics] 뒤에 &quot;(AMO ID)가 옵니다.

| Dimension | 적용 가능한 Adobe 광고 데이터 | 설명 |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP] 및 [!DNL Search] 데이터 | Advertising DSP 또는 검색 엔진 이름 |
| [!UICONTROL Account (AMO ID] | [!DNL DSP] 및 [!DNL Search] 데이터 | 계정 이름입니다. |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP] 및 [!DNL Search] 데이터 | RTB ([!DNL DSP]) 또는 광고 네트워크 이름([!DNL Search]) |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP] 및 [!DNL Search] 데이터 | 캠페인 이름. |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP] 및 [!DNL Search] 데이터 | 패키지([!DNL DSP]) 또는 포트폴리오([!DNL Search]) 이름. |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] 데이터 | 배치 이름입니다. |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search] 데이터 | 광고 그룹 이름입니다. |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search] 데이터 | 키워드입니다. |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search] 데이터 | 검색 일치 유형입니다. |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search] 데이터 | 키워드 및 일치 유형입니다. |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP] 및 [!DNL Search] 데이터 | 광고 유형(예: ) `text`, `video`, `display`, 또는 `native`. |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP] 및 [!DNL Search] 데이터 | 광고 유형([!DNL DSP]) 또는 광고 제목( )[!DNL Search]). |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP] 및 [!DNL Search] 데이터 | 광고 설명([!DNL DSP]) 또는 광고 본문([!DNL Search]). |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search] 데이터 | 광고에 표시되는 URL입니다. |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search] 데이터 | 광고의 대상 URL입니다. |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP] 및 [!DNL Search] 데이터 | 랜딩 페이지 항목이 뷰스루인지 클릭스루인지 여부. |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search] 데이터 | 제품 목록 광고에 대한 제품 타겟. |

>[!MORELIKETHIS]
>
>* [개요 [!DNL Analytics for Advertising]](overview.md)
>* [[!DNL Analytics] Adobe 광고의 데이터](/help/integrations/analytics/analytics-data-in-advertising.md)

