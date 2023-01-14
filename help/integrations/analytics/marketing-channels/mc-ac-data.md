---
title: 사용 [!DNL Marketing Channels] 광고 데이터 Adobe 사용
description: 에서 Adobe 광고 데이터를 사용하는 방법을 알아봅니다. [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: c9403a03-58aa-4633-bb97-51afc30843ad
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '708'
ht-degree: 0%

---

# 사용 [!DNL Analytics Marketing Channels] 광고 데이터 Adobe 사용

*Adobe Advertising-Adobe Analytics 통합 전용 광고주*

Adobe 광고 및 [!DNL Analytics Marketing Channels] 보고서를 사용하면 디지털 미디어가 사이트 활동에 미치는 영향에 대한 중요한 통찰력을 얻을 수 있습니다.

<!-- from video: By using Marketing Channels with your Adobe Advertising data, you can get a more holistic view of how your advertising efforts are affecting site behavior. In particular, you can see the value of your view-through and click-through data, and how your advertising assists or is assisted by other channels. -->

다음 그림은 Adobe 광고 및 [!DNL Marketing Channels] 방문자의 여정을 구성하는 개별 방문을 추적합니다. 의 광고 보고서 Adobe [!DNL Analytics] AMO ID를 사용하여 Adobe 광고를 통해 노출되는 유료 디스플레이, 검색, 소셜 및 상거래 채널 광고만 제한됩니다. 하지만, [!DNL Marketing Channels] 에 구성된 모든 채널을 추적합니다 [!DNL Marketing Channels] 처리 규칙.

![Adobe 광고 및 [!DNL Marketing Channels] 방문자 여정에서 개별 방문 횟수 추적](/help/integrations/assets/a4adc-mc-sample-journey2.png)

첫 번째 방문에서 사용자는 이메일 캠페인을 통해 웹 사이트에 들어갔다가 10개의 페이지 보기를 실행한 다음 나갔습니다. 두 번째 방문에서 사용자는 디스플레이 광고를 통해 사이트에 들어갔다가 10개의 페이지 보기를 실행한 다음 나갔습니다. 세 번째 방문에서 사용자는 자연어 검색을 통해 사이트로 이동하고, 5개의 페이지 보기를 실행하고, $250 전환을 실행한 후 왼쪽으로 이동합니다. 간 추적의 차이점 확인 [!DNL Marketing Channels] 및 Adobe 광고. 이 여정에서 광고 Adobe이 추적하는 유일한 채널은 [!UICONTROL Display]. Adobe 광고 추적 [!UICONTROL Display] 채널 방문 및 은 후속 참여 데이터(예: 페이지 보기 수)와 전환을 해당 광고의 영향에 다시 기여합니다. [!DNL Marketing Channels]반면에 는 모든 채널에 대한 전체 보기를 제공합니다.

AMO ID는 방문자의 여정을 통해 유지되므로 AMO ID 데이터를 사용하여 Adobe 광고가 다른 마케팅 채널에 미치는 영향을 확인할 수 있습니다. AMO ID [기본적으로 60일 동안 지속됩니다](/help/integrations/analytics/overview.md)하지만 필요에 따라 지속성을 구성할 수 있습니다.

## Adobe 광고 및 마케팅 채널 데이터를 결합하여 미디어 성능을 분석하는 방법

내 [!DNL Analytics], 유료 광고 데이터를 지속하는 Adobe 광고 및 [!DNL Marketing Channels] 고객 여정에 더 나은 영향을 줄 수 있도록 미디어 성능을 더 잘 분석하기 위한 포괄적인 방문 데이터.

다음 분석에서는 Adobe 광고 데이터를 사용하여 디스플레이 광고가 사이트 전환에 미치는 영향에 대한 다양한 버전을 표시합니다. 세 열 모두 동일한 전환 지표를 사용하지만, 각 열은 다른 스토리를 나타냅니다.

* 열 1은 방문자의 여정 전체에서 지속되는 AMO ID 데이터를 봅니다. 열 1은 뷰스루 또는 클릭스루 이벤트를 통해 한 시점에서 Adobe 광고 광고에 연결된 641 애플리케이션 시작임을 나타냅니다. 이 보기에서는 다른 보기가 없습니다 [!DNL Marketing Channels] 기여도 분석.

* 에서 [!DNL Marketing Channels] 그러나 데이터 세트, 641 애플리케이션 시작 은 다른 마케팅 채널에 귀속됩니다. 마지막 두 열은 641 응용 프로그램 시작을 가져와 데이터를 로 제한합니다 [!UICONTROL Display Click-Through] 및 [!UICONTROL Display View-Through] 마지막 터치 속성 모델에서 발생하는 전환을 표시하는 채널입니다.

![디스플레이 광고가 사이트 변환에 미치는 영향 예](/help/integrations/assets/a4adc-mc-display-impact.png)

이 분석을 한 단계 더 진행할 수 있습니다. 마케팅 채널별로 광고 Adobe 행을 추가로 분류하여 641 애플리케이션 시작에 대한 Adobe 광고 전환이 어디에서 발생하는지 확인할 수 있습니다. 이미 이러한 전환 5개가 마지막 터치 디스플레이 클릭스루에 귀속되고 19개가 마지막 터치 디스플레이 뷰스루에 귀속된다는 사실을 알고 있습니다. 이렇게 해도 다른 마케팅 채널에 속하는 617 애플리케이션 시작이 남게 됩니다. Advertising DSP 라인 항목 위에 마지막 터치 채널 차원을 끌어다 놓아 나머지 애플리케이션 시작에 대한 채널 속성을 표시하고 디스플레이 채널의 크로스 채널 영향을 표시할 수 있습니다.

![마지막 터치 채널 차원을 추가하는 방법](/help/integrations/assets/a4adc-mc-display-impact-ltc.png)

이제 나머지 응용 프로그램 시작 속성이 어떻게 지정되는지 확인할 수 있습니다. AMO ID가 지속된 357개의 마지막 터치 애플리케이션 시작에 대한 크레딧이 이메일에 제공됩니다. 이러한 유형의 분석을 사용하면 Adobe 광고 디스플레이 광고가 모든 채널에 미치는 영향을 확인할 수 있습니다. 데이터 세트와 속성 모델이 하나만 있으면 이 유형의 인사이트를 사용할 수 없습니다.

![디스플레이 채널의 크로스 채널 영향 예](/help/integrations/assets/a4adc-mc-display-impact-x-channel.png)

시간에 따른 트렌드 데이터를 표시하려면 스택 그래프 세트를 &quot;100% 스택&quot;으로 사용하여 분석을 더 향상시킬 수 있습니다. 이 시각화를 사용하면 디스플레이 마케팅 캠페인의 영향을 가장 많이 받는 마지막 터치 마케팅 채널을 보다 쉽게 모니터링할 수 있습니다.

![디스플레이 채널의 트렌드 크로스 채널 영향의 예](/help/integrations/assets/a4adc-mc-display-impact-x-channel-trend.png)

>[!MORELIKETHIS]
>
>* [기본 사항 [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Adobe 광고 ID를 사용하여 만들기 [!DNL Marketing Channels] 처리 규칙](mc-ids.md)
>* [Adobe 광고과 광고 사이에 채널 데이터가 다를 수 있는 이유 [!DNL Marketing Channels]](mc-data-variances.md)
>* [비디오: 사용 [!DNL Marketing Channels] Adobe 광고 보고용](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [개요 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)

