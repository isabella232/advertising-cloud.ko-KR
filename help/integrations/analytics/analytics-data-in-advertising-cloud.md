---
title: '"[!DNL Analytics] Advertising Cloud의 데이터"'
description: '"[!DNL Analytics] Advertising Cloud의 데이터"'
feature: Integration with Adobe Analytics
exl-id: 79fbc809-9965-41c1-971f-3652cc78fee3
source-git-commit: 2c94b6c02b4e24878639dd9edbc0455e1751f679
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---

# [!DNL Analytics] Advertising Cloud의 데이터

*Advertising Cloud-Adobe Analytics 통합만 있는 광고주*

## Analytics 세그먼트

에서 만들어진 모든 세그먼트 [!DNL Analytics] Experience Cloud에 게시되었습니다.

새 세그먼트는 Advertising Cloud에 표시되는 데 24-48시간이 소요됩니다. 기존 세그먼트에 대한 업데이트는 약 8시간 내에 동기화됩니다.

<!-- I added "metric" to some of the links below, even though it looks redundant, because of syntax limitations: If you use [!DNL] or [!UICONTROL] as the sole text of a link (such as [[!UICONTROL Revenue]], the tag is included in the link text (such as "[!UICONTROL Revenue]") when it's published. -->

## 사이트 참여 지표

>[!NOTE]
>
>* [!DNL Analytics] 은 EF ID eVar에 대한 이벤트를 Advertising Cloud에 전달합니다.  기본 통합은 계산된 지표 또는 다른 차원(eVar)을 Advertising Cloud으로 전송하는 것을 지원하지 않습니다. 하지만 계산된 지표를 사용자 지정 이벤트에서 완전히 캡처할 수 있는 경우 Advertising Cloud이 사용자 지정 이벤트를 수집할 수 있습니다.
>* [!DNL Analytics] 는 데이터를 Advertising Cloud에 시간별로 전달합니다.


* [!UICONTROL Timespent_secs_1stvisit]: 방문자의 첫 방문 동안 사이트에서 보낸 시간(초)입니다.
* [!UICONTROL Timespent_secs_total]: 클릭 전환 확인 기간 내의 모든 방문에서 사이트에서 보낸 총 시간(초)입니다.
* [!UICONTROL Pageviews_1stvisit]: 방문자가 처음 방문하는 동안 사이트에 대한 페이지 보기 수입니다.
* [!UICONTROL Pageviews_total]: 클릭 전환 확인 기간 내의 모든 방문에서 사이트에 대한 총 페이지 보기 수입니다.
* [[!UICONTROL Bounces] 지표](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html)
* [[!UICONTROL Visits] 지표](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html)
* [!UICONTROL ef_id_instances]: 해당 횟수 [!DNL Analytics] 수집한 것 [!UICONTROL EF ID].

## 전환 지표

[!DNL Analytics] 변환 지표를 매일 Advertising Cloud에 전달합니다.

### 표준 전환 지표

* [[!UICONTROL Revenue] 지표](https://experienceleague.adobe.com/docs/analytics/components/metrics/revenue.html)
* [[!UICONTROL Orders] 지표](https://experienceleague.adobe.com/docs/analytics/components/metrics/orders.html)
* [[!UICONTROL Units] 지표](https://experienceleague.adobe.com/docs/analytics/components/metrics/units.html)
* [[!UICONTROL Carts] 지표](https://experienceleague.adobe.com/docs/analytics/components/metrics/carts.html)
* [[!UICONTROL Cart Views] 지표](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-views.html)
* [[!UICONTROL Checkouts] 지표](https://experienceleague.adobe.com/docs/analytics/components/metrics/checkouts.html)
* [[!UICONTROL Cart Additions] 지표](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-additions.html)
* [[!UICONTROL Cart Removals] 지표](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-removals.html)

### 사용자 지정 전환 지표

이러한 지표는 보고서 세트별로 다르므로 사용 가능한 지표는 각 고객 및 보고서 세트에 따라 다릅니다.

### 예약된 전환 지표

이러한 지표는 보고서 세트별로 다르므로 사용 가능한 지표는 각 고객 및 보고서 세트에 따라 다릅니다.

>[!MORELIKETHIS]
>
>* [개요 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Analysis Workspace의 Advertising Cloud 지표](/help/integrations/analytics/advertising-cloud-metrics-in-analytics.md)

