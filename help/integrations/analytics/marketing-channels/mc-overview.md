---
title: ' [!DNL Marketing Channels] 기본 사항'
description: ' [!DNL Analytics Marketing Channels] that [!DNL Analytics for Advertising Cloud] 사용자가 이해해야 하는 주요 정보에 대해 알아봅니다.'
feature: Integration with Adobe Analytics
exl-id: null
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 0%

---

# [!DNL Analytics Marketing Channels] 기본 사항

*Advertising Cloud-Adobe Analytics 통합만 있는 광고주*

이 페이지에서는 [!DNL Analytics for Advertising Cloud] 사용자가 이해해야 하는 [!DNL Analytics Marketing Channels]에 대한 주요 정보를 설명합니다.

[!DNL Marketing Channels]에 대한 전체 설명서는 &quot;[시작하기 [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/c-getting-started-mchannel.html)&quot;를 참조하십시오.

## [!DNL Marketing Channels] 개요

[!DNL Marketing Channels] 는 Adobe Analytics의 주요 기능입니다. [!DNL Marketing Channels] 보고서는 고객이 보고 기간을 통해 웹 사이트에 도착하는 방법과 각 채널이 매출 또는 온사이트 행동에 미치는 영향을 보여줍니다.

다음 방문 간 여정 예를 생각해 보십시오. 웹 사이트에 대한 각 방문은 방문자가 입력한 마케팅 채널로 표시됩니다. 첫 번째 터치 채널이라고도 하는 첫 번째 방문은 이메일입니다. 방문 시 표시 2 는 참여하는 채널이며, 자연어 검색은 마지막 터치 채널로 간주됩니다. [!UICONTROL Attribution IQ] 내에서 [!UICONTROL Last Touch Attribution]을 사용하는 경우, 자연어 검색은 $250 전환 이벤트에 대한 전체 크레딧을 받습니다. Experience Cloud ID 서비스를 사용하여 이러한 개별 방문을 함께 연결하여 단일 방문자에 의한 하나의 여정을 표시할 수 있습니다.

![마케팅 채널에서의 방문 간 전환 여정 예](/help/integrations/assets/a4adc-mc-sample-journey.png)

[!UICONTROL Marketing Channels] 처리 규칙을 사용하여 논리 세트를 만들어 트래픽을 유도하는 채널을 결정하고 사용자가 사이트를 방문할 때 각 채널을 추적할 수 있습니다. 예를 들어 [!UICONTROL Email] 채널은 클릭 시 생성된 고유한 추적 코드로 표시되는데, 이 경우 Adobe Analytics에 의해 기록되면 방문이 이메일 마케팅 캠페인에서 시작된 것으로 분류됩니다.

## 처리 규칙 및 마케팅 채널 설정 방법

사용자가 웹 사이트를 방문할 때마다 사용자는 주소 표시줄에 직접 입력하거나 클릭한 URL을 통해 주소를 입력합니다. 사용자가 웹 사이트에 들어올 때 [!DNL Analytics] 은 방문을 유도한 채널을 결정하는 데 사용할 수 있는 정보를 추적합니다.

마케터는 종종 쿼리 문자열 매개 변수 추적 코드를 채널 URL에 추가하여 채널이 사이트에서 미치는 영향을 추적합니다. 추가 추적 없이 특정 추적 매개 변수 및 값을 수신하도록 [!DNL Marketing Channels] 처리 규칙을 구성하여 채널을 결정할 수 있습니다. 예를 들어 모든 이메일 캠페인 URL이 `www.adobe.com?cid=email…` 형식을 따르는 경우(이 URL에 쿼리 문자열 매개 변수와 값 `cid=email`)에는 이 추적 코드를 수신하고 [!UICONTROL Email] 채널에서 방문을 버킷하는 규칙을 만들 수 있습니다.

다른 채널에는 추적 가능한 URL 경로가 없으며 식별을 위한 추가 논리가 필요합니다. 예를 들어, 다른 사용자가 소셜 네트워크에서 유기적으로 공유한 링크를 클릭하는 [!UICONTROL Earned Social]은 추적해야 할 중요한 채널입니다. 그러나 마케팅 담당자는 쿼리 문자열 매개 변수 추적 코드를 공유된 URL에 추가할 수 없습니다. 이 경우 처리 규칙을 만들어 관심 있는 소셜 네트워크의 참조 도메인과 유료 추적 코드가 없는 을 수신하여 채널을 결정할 수 있습니다. 이러한 요구 사항을 충족하는 방문자는 마케팅 채널 보고서 내에서 얻은 소셜로 추적됩니다.

Adobe은 analytics 팀과 함께 작업과 관련된 모든 채널을 추적하기 위해 포괄적인 [!DNL Marketing Channels] 처리 규칙 세트를 만드는 것이 좋습니다. 이를 통해 강력한 속성 보고를 만들 수 있습니다.

Advertising Cloud이 사용자 지정 마케팅 채널을 만드는 데 필요한 신호에 기여할 수 있는 방법을 이해하려면 &quot;[광고 ID를 사용하여 규칙 만들기 [!DNL Marketing Channels] 규칙 만들기&quot;를 참조하십시오.](mc-ids.md)

>[!MORELIKETHIS]
>
>* [Advertising Cloud ID를 사용하여  [!DNL Marketing Channels] 처리 규칙 만들기](mc-ids.md)
>* [Advertising Cloud과 채널 간에 채널 데이터가 다를 수 있는 이유 [!DNL Marketing Channels]](mc-data-variances.md)
>* [ [!DNL Analytics Marketing Channels] Advertising Cloud 데이터 사용](mc-ac-data.md)
>* [비디오: Advertising Cloud을 사용한 보고 [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [개요 [!DNL Analytics for Advertising Cloud]](/help/integrations/analytics/overview.md)

