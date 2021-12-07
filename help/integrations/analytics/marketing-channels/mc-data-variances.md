---
title: Advertising Cloud과 채널 간에 채널 데이터가 다를 수 있는 이유 [!DNL Marketing Channels]
description: AMO ID로 추적된 채널 데이터가 [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
source-git-commit: 1ae45d0ceee2efc4fc52b86fd6737d4c7467a6ca
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---

# Advertising Cloud과 채널 간에 채널 데이터가 다를 수 있는 이유 [!DNL Marketing Channels]

*Advertising Cloud-Adobe Analytics 통합만 있는 광고주*

Advertising Cloud 및 의 통합에 대해 학습하는 사용자로부터의 일반적인 질문 [!DNL Marketing Channels] 데이터 세트는 &quot;AMO ID와 데이터 간의 차이가 발생하는 원인 [!DNL Marketing Channels]? 또는 &quot;왜 데이터가 손상되었나요? 보고서에서 일치시키려면 모든 지표가 필요합니다.&quot; 다행스럽게도 불일치가 데이터가 &quot;손상됨&quot;임을 나타내지 않으며 불일치가 예상되며 원하는 경우도 있습니다. 통합이 왜 이렇게 설계되었는지 살펴보겠습니다.

두 데이터 세트의 기본 사용 사례는 서로 다릅니다.

* [!DNL Marketing Channels]: 에 대한 기본 사용 사례 [!DNL Marketing Channels] 는 여러 채널 간의 데이터를 일반적인 속성 모델과 비교하는 것입니다. 분석가들은 [!UICONTROL Marketing Channel] 차원 을 참조하십시오. 이러한 인사이트를 통해 각 채널에 투자하는 방법에 대한 거시적 수준의 결정을 내리고 각 채널의 방문자가 웹 사이트와 상호 작용하는 방법에 대한 통찰력을 얻을 수 있습니다.

   다음 [!DNL Analytics] [!UICONTROL Marketing Channel] 따라서 차원은 모든 채널을 캡처하고 추적하도록 구성됩니다. [!DNL Marketing Channels] 또한 Advertising Cloud DSP 뷰스루 및 클릭스루를 캡처하도록 구성할 수 있으며, 다른 마케팅 채널과 관련해서 구성될 수도 있습니다.

* Advertising Cloud AMO ID: Advertising Cloud AMO ID 데이터의 기본 사용 사례는 Advertising Cloud의 고급 기능을 제공하는 것입니다 [!DNL Adobe Sensei]-강력한 입찰 알고리즘. 알고리즘은 광고 비용을 극대화하고 목표를 달성하기 위해 매일 수천 개의 마이크로 수준 입찰 결정을 자동으로 수행합니다 [!DNL DSP] 캠페인 또는 [!DNL Search] 포트폴리오. 알고리즘이 캠페인을 연결할 수 있는 전환 데이터가 많을수록 알고리즘이 이러한 입찰 결정을 더 잘 내릴 수 있습니다.

   이 데이터를 수집하려면 [!DNL Analytics for Advertising Cloud] 통합은 사용자 지정 변수(eVar) 또는 예약된 변수(rVar)로 저장된 Adobe Analytics의 AMO ID 차원에서 클릭스루 및 뷰스루 추적 코드로 변환할 수 있는 원시 AMO ID를 전달합니다. 다른 채널에 대한 클릭스루가 AMO ID 차원에서 설정되지 않으므로 AMO ID 차원은 이러한 다른 채널의 항목을 추적할 수 없습니다. 그 결과 AMO ID가 [!DNL Marketing Channes]l 시작 지점.

Advertising Cloud에서 추적한 데이터와 [!DNL Analytics]-추적된 데이터는 다음을 참조하십시오.[다음 사이 예상되는 데이터 분산 [!DNL Analytics] 및 Advertising Cloud](../data-variances.md).&quot;

>[!MORELIKETHIS]
>
>* [다음 사이 예상되는 데이터 분산 [!DNL Analytics] 및 Advertising Cloud](/help/integrations/analytics/data-variances.md)
>* [기본 사항 [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Advertising Cloud ID를 사용하여 만들기 [!DNL Marketing Channels] 처리 규칙](mc-ids.md)
>* [사용 [!DNL Analytics Marketing Channels] Advertising Cloud 데이터 사용](mc-ac-data.md)
>* [비디오: Advertising Cloud을 사용한 보고 [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)

