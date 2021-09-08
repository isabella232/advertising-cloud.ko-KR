---
title: Advertising Cloud과 [!DNL Marketing Channels] 간에 채널 데이터가 다를 수 있는 이유는 무엇입니까?
description: AMO ID로 추적된 채널 데이터가 [!DNL Analytics Marketing Channels]에서 추적한 채널 데이터와 다를 수 있는 이유를 알아봅니다.
feature: Integration with Adobe Analytics
exl-id: null
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---

# Advertising Cloud과 [!DNL Marketing Channels] 간에 채널 데이터가 다를 수 있는 이유는 무엇입니까?

*Advertising Cloud-Adobe Analytics 통합만 있는 광고주*

Advertising Cloud과 [!DNL Marketing Channels] 데이터 세트의 통합에 대해 학습하는 사용자에게 일반적인 질문은 &quot;AMO ID와 [!DNL Marketing Channels] 간의 데이터가 왜 차이가 발생합니까?&quot;입니다. 또는 &quot;왜 데이터가 손상되었나요? 보고서에서 일치시키려면 모든 지표가 필요합니다.&quot; 다행스럽게도 불일치가 데이터가 &quot;손상됨&quot;임을 나타내지 않으며 불일치가 예상되며 원하는 경우도 있습니다. 통합이 왜 이렇게 설계되었는지 살펴보겠습니다.

두 데이터 세트의 기본 사용 사례는 서로 다릅니다.

* [!DNL Marketing Channels]: 의 기본 사용 사례 [!DNL Marketing Channels] 는 여러 채널의 데이터를 일반적인 속성 모델과 비교하는 것입니다. 분석가들은 [!UICONTROL Marketing Channel] 차원을 사용하여 채널이 서로 상호 작용하는 방법에 대한 통찰력을 얻을 수 있습니다. 이러한 인사이트를 통해 각 채널에 투자하는 방법에 대한 거시적 수준의 결정을 내리고 각 채널의 방문자가 웹 사이트와 상호 작용하는 방법에 대한 통찰력을 얻을 수 있습니다.

   따라서 [!DNL Analytics] [!UICONTROL Marketing Channel] 차원은 모든 채널을 캡처하고 추적하도록 구성됩니다. [!DNL Marketing Channels] 또한 Advertising Cloud DSP 뷰스루 및 클릭스루를 캡처하도록 구성할 수 있으며, 다른 마케팅 채널과 관련해서 구성될 수도 있습니다.

* Advertising Cloud AMO ID: Advertising Cloud AMO ID 데이터의 기본 사용 사례는 Advertising Cloud의 고급 [!DNL Adobe Sensei] 기반 입찰 알고리즘을 제공하는 것입니다. 알고리즘은 광고 비용을 극대화하고 [!DNL DSP] 캠페인 또는 [!DNL Search] 포트폴리오의 목표를 달성하기 위해 매일 수천 개의 마이크로 수준 입찰 결정을 자동으로 수행합니다. 알고리즘이 캠페인을 연결할 수 있는 전환 데이터가 많을수록 알고리즘이 이러한 입찰 결정을 더 잘 내릴 수 있습니다.

   이 데이터를 수집하기 위해 [!DNL Analytics for Advertising Cloud] 통합은 사용자 지정 변수(eVar) 또는 예약된 변수(rVar)로 저장된 Adobe Analytics의 AMO ID 차원에서 클릭스루 및 뷰스루 추적 코드로 변환할 수 있는 원시 AMO ID를 전달합니다. 다른 채널에 대한 클릭스루가 AMO ID 차원에서 설정되지 않으므로 AMO ID 차원은 이러한 다른 채널의 항목을 추적할 수 없습니다. 그 결과 AMO ID는 [!DNL Marketing Channes]l 시작 지점을 통해 유지됩니다.

Advertising Cloud 추적된 데이터와 [!DNL Analytics]-추적된 데이터 간의 가능한 데이터 차이에 대한 자세한 내용은 &quot;[Advertising Cloud [!DNL Analytics] 간의 예상 데이터 분산&quot;을 참조하십시오.](../data-variances.md)

>[!MORELIKETHIS]
>
>* [Advertising Cloud과  [!DNL Analytics] 간의 예상 데이터 분산](/help/integrations/analytics/data-variances.md)
>* [기본 사항 [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Advertising Cloud ID를 사용하여  [!DNL Marketing Channels] 처리 규칙 만들기](mc-ids.md)
>* [ [!DNL Analytics Marketing Channels] Advertising Cloud 데이터 사용](mc-ac-data.md)
>* [비디오: Advertising Cloud을 사용한 보고 [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)

