---
title: Advertising Cloud ID를 사용하여 규칙 만들기 [!DNL Marketing Channels] 규칙
description: Advertising Cloud ID를 사용하여 [!DNL Analytics Marketing Channels]에 대한 처리 규칙을 만드는 방법을 알아봅니다.
feature: Integration with Adobe Analytics
exl-id: null
source-git-commit: 5224d891d665b901d076ff6a203e9ff3bab80f85
workflow-type: tm+mt
source-wordcount: '766'
ht-degree: 0%

---

# Advertising Cloud ID를 사용하여 [!DNL Marketing Channels] 처리 규칙 만들기

*Advertising Cloud-Adobe Analytics 통합만 있는 광고주*

Advertising Cloud ID([AMO ID 및 EF ID](../ids.md))를 사용하여 Adobe Analytics에서 [!DNL Marketing Channels] 처리 규칙을 구성할 수 있습니다. Advertising Cloud 캠페인 관련 규칙에 Advertising Cloud ID를 사용합니다.

## 처리 규칙의 AMO ID입니다

AMO ID는 [!DNL Analytics] 내에서 Advertising Cloud 데이터를 보고하는 데 사용되는 기본 추적 코드입니다. AMO ID는 [!DNL Analytics] 내에서 세부적인 보고를 제공하기 위해 Adobe이 관리하는 동적 값의 연결입니다. [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) 또는 rVar 차원(AMO ID)에 저장됩니다. AMO ID는 두 가지 방법으로 [!DNL Analytics]에서 설정할 수 있습니다.

* 클릭스루 추적: Advertising Cloud은 링크에 `s_kwcid` 쿼리 문자열 매개 변수를 설정하고 [!DNL Analytics] 은 클릭스루가 발생할 때 랜딩 페이지 URL에서 매개 변수를 선택합니다.
* 뷰스루 추적([!DNL DSP]만): 마지막 이벤트 서비스는 서버 측에서 뷰스루를 감지하여 AMO ID를 [!DNL Analytics]에 보냅니다. 이 경우 URL에 `s_kwcid` 매개 변수가 없습니다.

AMO ID 내의 동적 값은 추적된 마케팅 채널을 나타냅니다.

* AMO ID의 접두사는 [!DNL Marketing Channels] 내에서 최상위 채널을 식별하는 데 사용할 수 있습니다.

* AMO ID 본문의 문자 구문은 더 구체적인 캠페인 유형을 나타냅니다.

* 접미사 &quot;vt&quot;는 [!DNL DSP] 뷰스루 트래픽에 대해 존재하며 별도의 클릭스루 및 뷰스루 [!DNL DSP] 채널을 만드는 데 사용할 수 있습니다.

나머지 AMO ID는 무시할 수 있습니다.

| AMO ID | 채널 | 규칙 논리 |
|--------|---------|--------------------|
| 알! (접두사) | [!UICONTROL Paid Search] | 다음으로 시작 |
| AC! (접두사) | [!UICONTROL DSP] | 다음으로 시작 |
| ! (본문) | [!UICONTROL Google Search] | 다음 포함 |
| !s! (본문) | [!UICONTROL Search Partner] | 다음 포함 |
| ! (본문) | [!UICONTROL Display Network] | 다음 포함 |
| ! (본문) | [!UICONTROL Smart Shopping Campaign] | 다음 포함 |
| ! (본문) | [!UICONTROL YouTube Video Ad] | 다음 포함 |
| ! (본문) | [!UICONTROL YouTube Search Ad] | 다음 포함 |
| ! (본문) | [!UICONTROL Google Video Partners] | 다음 포함 |
| !vt(접미사) | [!UICONTROL DSP View-through] | 종료 문자 |

### AMO ID를 사용하는 처리 규칙의 예

[!UICONTROL Paid Search] 채널에 대한 [!DNL Marketing Channels] 처리 규칙은 다음과 같습니다.

![규칙의  [!UICONTROL Paid Search] 예](/help/integrations/assets/a4adc-mc-rule-paidsearch.png)

[!UICONTROL YouTube Video Ads] 채널에 대한 [!DNL Marketing Channels] 처리 규칙은 다음과 같습니다.

![규칙의  [!UICONTROL YouTube Video Ads] 예](/help/integrations/assets/a4adc-mc-rule-youtube-video.png)

>[!IMPORTANT]
>
> 규칙을 특정 순서로 실행해야 합니다. 위의 두 규칙이 순서대로 실행된 경우 AMO ID가 모두 &quot;AL!&quot;으로 시작되므로 [!DNL YouTube] 비디오 광고 트래픽이 모두 [!UICONTROL Paid Search] 채널에 속합니다 &quot;!ytv!&quot;를 포함합니다.

## 처리 규칙의 EF ID

AMO EF ID(EF ID)는 [!DNL Analytics for Advertising Cloud] 통합에 사용되는 두 번째 추적 코드입니다. 기본 목적은 [!DNL Analytics] 이벤트 데이터를 추적하고 Advertising Cloud에 전달하는 것입니다. 클릭스루 또는 뷰스루가 발생할 때마다 동일한 방문자에 대해 정확히 동일한 광고라도 고유 EF ID가 생성됩니다. EF ID는 일반적으로 [!DNL Analytics]의 변수 제한당 500k 고유 값을 초과하므로 보고 시 사용할 수 없으므로 [!DNL Analytics] 보고 사용자 인터페이스에 사용되지 않습니다. Advertising Cloud 지표 및 메타데이터는 EF ID에 적용되지 않습니다. AMO ID에만 적용됩니다. Advertising Cloud의 캠페인 최적화에 대해 추가된 추적 세부 기간이 필요하므로 두 ID가 모두 필요합니다.

EF ID 차원은 [!DNL Analytics] 보고에서 직접 사용되지 않지만 EF ID는 마케팅 채널을 만드는 데 유용할 수 있습니다. EF ID 접미사는 채널(표시 또는 검색)과 방문이 클릭스루에 의해 제어되었는지 아니면 뷰스루에 의해 제어되었는지를 나타냅니다. EF ID의 구분 기호는 AMO ID의 느낌표가 아닌 콜론입니다.

| EF ID 접미사 | 채널 |
|-------|---------|
| : s | [!UICONTROL Paid Search] |
| :d | [!UICONTROL Display Click-through] |
| : i | [!UICONTROL Display View-through] |

### EF ID를 사용하는 처리 규칙의 예

#### 클릭스루 규칙 표시

클릭스루만 캡처하여 디스플레이 클릭스루 마케팅 채널을 만듭니다. AMO ID는 클릭스루와 뷰스루 모두에 대해 동일하므로 이 규칙은 EF ID 변수와 `ef_id` 쿼리 문자열 매개 변수를 사용합니다.

경우에 따라 URL(기본값)을 통해 클릭스루가 추적됩니다. 다른 경우에는 서버 측에서 마지막 이벤트 서비스를 통해 클릭스루가 추적되므로 URL에 `ef_id` 매개 변수가 없습니다. 따라서 규칙은 EF ID 변수 또는 `ef_id` 쿼리 문자열 매개 변수가 &quot;:d&quot;로 끝나는 조건을 확인합니다. 두 조건 중 하나에 대해 이 규칙을 트리거하려면 &quot;`Any`&quot; 연산자를 사용하십시오.

![디스플레이 클릭스루 규칙의 예](/help/integrations/assets/a4adc-mc-rule-display-ct.png)

#### 뷰스루 규칙 표시

디스플레이 뷰스루 채널을 만들려면 EF ID가 &quot;:i&quot;로 끝나는 규칙을 만듭니다. 방문자가 광고를 클릭하지 않았으므로 뷰스루 추적에 `ef_id` 또는 `s_kwcid`이 URL에 포함되지 않습니다. 따라서 한 가지 조건만 필요합니다.

![표시 뷰스루 규칙의 예](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

>[!MORELIKETHIS]
>
>* [기본 사항 [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Advertising Cloud과 채널 간에 채널 데이터가 다를 수 있는 이유 [!DNL Marketing Channels]](mc-data-variances.md)
>* [ [!DNL Analytics Marketing Channels] Advertising Cloud 데이터 사용](mc-ac-data.md)
>* [비디오: Advertising Cloud을 사용한 보고 [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [에서 사용하는 Advertising Cloud ID [!DNL Analytics]](/help/integrations/analytics/ids.md)

