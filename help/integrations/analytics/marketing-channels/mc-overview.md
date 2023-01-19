---
title: 기본 사항 [!DNL Marketing Channels]
description: 에 대한 주요 정보 알아보기 [!DNL Analytics Marketing Channels] 그게 [!DNL Analytics for Advertising] 사용자는 이를 이해해야 합니다.
feature: Integration with Adobe Analytics
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 0%

---

# 기본 사항 [!DNL Analytics Marketing Channels]

*Adobe Advertising-Adobe Analytics 통합 전용 광고주*

이 페이지에서는 다음에 대한 주요 정보를 설명합니다. [!DNL Analytics Marketing Channels] 그게 [!DNL Analytics for Advertising] 사용자는 이해해야 합니다.

에 대한 전체 설명서는 [!DNL Marketing Channels]를 참조하십시오.[시작하기 [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/c-getting-started-mchannel.html).&quot;

## 개요 [!DNL Marketing Channels]

[!DNL Marketing Channels] 는 Adobe Analytics의 주요 기능입니다. [!DNL Marketing Channels] 보고서는 고객이 보고 기간을 통해 웹 사이트에 도착하는 방법과 각 채널이 매출 또는 온사이트 행동에 미치는 영향을 보여줍니다.

다음 방문 간 여정 예를 생각해 보십시오. 웹 사이트에 대한 각 방문은 방문자가 입력한 마케팅 채널로 표시됩니다. 첫 번째 터치 채널이라고도 하는 첫 번째 방문은 이메일입니다. 방문 시 표시 2 는 참여하는 채널이며, 자연어 검색은 마지막 터치 채널로 간주됩니다. 만약 [!UICONTROL Last Touch Attribution] within [!UICONTROL Attribution IQ], 자연어 검색은 $250 전환 이벤트에 대한 전체 크레딧을 받습니다. Experience Cloud ID 서비스를 사용하여 이러한 개별 방문을 함께 연결하여 단일 방문자에 의한 하나의 여정을 표시할 수 있습니다.

![마케팅 채널에서의 방문 간 전환 여정 예](/help/integrations/assets/a4adc-mc-sample-journey.png)

사용 [!UICONTROL Marketing Channels] 처리 규칙 을 사용하면 논리 세트를 만들어 트래픽을 유도하는 채널을 결정하고 사용자가 사이트를 방문할 때 각 채널을 추적할 수 있습니다. 예: [!UICONTROL Email] 채널은 클릭 시 생성된 고유한 추적 코드로 표시되는데, 이 경우 Adobe Analytics에 의해 기록되면 방문을 이메일 마케팅 캠페인에서 시작된 방문으로 분류합니다.

## 처리 규칙 및 마케팅 채널 설정 방법

사용자가 웹 사이트를 방문할 때마다 사용자는 주소 표시줄에 직접 입력하거나 클릭한 URL을 통해 주소를 입력합니다. 사용자가 웹 사이트에 들어오면, [!DNL Analytics] 방문을 유도한 채널을 파악하는 데 사용할 수 있는 정보를 추적합니다.

마케터는 종종 쿼리 문자열 매개 변수 추적 코드를 채널 URL에 추가하여 채널이 사이트에서 미치는 영향을 추적합니다. 다음을 구성할 수 있습니다 [!DNL Marketing Channels] 특정 추적 매개 변수 및 값을 수신하여 추가 추적 없이 채널을 결정하는 처리 규칙. 예를 들어 모든 이메일 캠페인 URL이 형식을 따르는 경우 `www.adobe.com?cid=email…` (URL에 쿼리 문자열 매개 변수와 값이 포함되어 있는 경우) `cid=email`)를 채울 규칙을 만들어 이 추적 코드를 수신하고 의 방문을 버킷할 수 있습니다 [!UICONTROL Email] 채널.

다른 채널에는 추적 가능한 URL 경로가 없으며 식별을 위한 추가 논리가 필요합니다. 예, [!UICONTROL Earned Social]는 사용자가 소셜 네트워크에서 유기적으로 공유한 링크를 클릭하는 중요한 채널입니다. 그러나 마케팅 담당자는 쿼리 문자열 매개 변수 추적 코드를 공유된 URL에 추가할 수 없습니다. 이 경우 처리 규칙을 만들어 관심 있는 소셜 네트워크의 참조 도메인과 유료 추적 코드가 없는 을 수신하여 채널을 결정할 수 있습니다. 이러한 요구 사항을 충족하는 방문자는 마케팅 채널 보고서 내에서 얻은 소셜로 추적됩니다.

Adobe은 analytics 팀과 함께 포괄적인 일련의 [!DNL Marketing Channels] 처리 규칙을 사용하여 비즈니스에 관련된 모든 채널을 추적합니다. 이를 통해 강력한 속성 보고를 만들 수 있습니다.

Adobe 광고가 사용자 지정 마케팅 채널을 만드는 데 필요한 신호에 기여할 수 있는 방법을 이해하려면 &quot;[광고 ID를 사용하여 만들기 [!DNL Marketing Channels] 규칙](mc-ids.md).&quot;

>[!MORELIKETHIS]
>
>* [Adobe 광고 ID를 사용하여 만들기 [!DNL Marketing Channels] 처리 규칙](mc-ids.md)
>* [Adobe 광고과 광고 사이에 채널 데이터가 다를 수 있는 이유 [!DNL Marketing Channels]](mc-data-variances.md)
>* [사용 [!DNL Analytics Marketing Channels] 광고 데이터 Adobe 사용](mc-ac-data.md)
>* [비디오: 사용 [!DNL Marketing Channels] Adobe 광고 보고용](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [개요 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)

