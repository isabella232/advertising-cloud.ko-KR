---
title: Adobe 광고 ID를 사용하여 만들기 [!DNL Marketing Channels] 규칙
description: Adobe 광고 ID를 사용하여 처리 규칙을 만드는 방법을 알아봅니다. [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 4fcdd586-e9c5-4405-a6dc-7799d2bac93e
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 0%

---

# Adobe 광고 ID를 사용하여 만들기 [!DNL Marketing Channels] 처리 규칙

*Adobe Advertising-Adobe Analytics 통합 전용 광고주*

Adobe 광고 ID([AMO ID 및 EF ID](../ids.md)) 를 구성합니다. [!DNL Marketing Channels] Adobe Analytics의 처리 규칙. Adobe 광고 캠페인 관련 규칙에 Adobe 광고 ID를 사용합니다.

## 처리 규칙의 AMO ID입니다

AMO ID는 내에서 Adobe 광고 데이터를 보고하는 데 사용되는 기본 추적 코드입니다 [!DNL Analytics]. AMO ID는 내에서 세부적인 보고를 제공하기 위해 Adobe에서 관리하는 동적 값의 연결입니다 [!DNL Analytics]. 이 파일은 [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) 또는 rVar 차원(AMO ID)입니다. AMO ID는에서 설정할 수 있습니다. [!DNL Analytics] 두 가지 방법으로 다음을 수행합니다.

* 클릭스루 추적: Adobe 광고 은 `s_kwcid` 링크의 쿼리 문자열 매개 변수 및 [!DNL Analytics] 클릭스루가 발생할 때 랜딩 페이지 URL에서 매개 변수를 선택합니다.
* 뷰스루 추적([!DNL DSP] (전용): 마지막 이벤트 서비스는 서버 측에서 뷰스루를 감지하여 AMO ID를 로 보냅니다 [!DNL Analytics]. 이 경우 URL에 `s_kwcid` 매개 변수.

AMO ID 내의 동적 값은 추적된 마케팅 채널을 나타냅니다.

* AMO ID의 접두사는 내에서 최상위 채널을 식별하는 데 사용할 수 있습니다 [!DNL Marketing Channels].

* AMO ID 본문의 문자 구문은 더 구체적인 캠페인 유형을 나타냅니다.

* 접미사 &quot;vt&quot;가 [!DNL DSP] 뷰스루 트래픽 및 를 사용하여 별도의 클릭스루 및 뷰스루를 만들 수 있습니다 [!DNL DSP] 채널입니다.

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

다음 [!DNL Marketing Channels] 에 대한 처리 규칙 [!UICONTROL Paid Search] 채널은 다음과 같습니다.

![예 [!UICONTROL Paid Search] 규칙](/help/integrations/assets/a4adc-mc-rule-paidsearch.png)

다음 [!DNL Marketing Channels] 에 대한 처리 규칙 [!UICONTROL YouTube Video Ads] 채널은 다음과 같습니다.

![예 [!UICONTROL YouTube Video Ads] 규칙](/help/integrations/assets/a4adc-mc-rule-youtube-video.png)

>[!IMPORTANT]
>
> 규칙을 특정 순서로 실행해야 합니다. 위의 두 규칙이 순서대로 실행되면, [!DNL YouTube] 비디오 광고 트래픽은 모두 [!UICONTROL Paid Search] AMO ID가 모두 &quot;AL!&quot;로 시작되므로 채널에서 액세스할 수 있습니다. &quot;!ytv!&quot;를 포함합니다.

## 처리 규칙의 EF ID

AMO EF ID(EF ID)는 [!DNL Analytics for Advertising] 통합. 이것의 주요 목적은 추적하고 통과시키는 것이다 [!DNL Analytics] 이벤트 데이터를 Adobe 광고으로 가져옵니다. 클릭스루 또는 뷰스루가 발생할 때마다 동일한 방문자에 대해 정확히 동일한 광고라도 고유 EF ID가 생성됩니다. EF ID는 [!DNL Analytics] 보고 사용자 인터페이스는 일반적으로 변수 제한당 500k 고유 값을 초과하므로 [!DNL Analytics]를 사용 못하여 보고에 사용할 수 없습니다. Adobe 광고 지표 및 메타데이터는 EF ID에 적용되지 않습니다. AMO ID에만 적용됩니다. Adobe 광고의 캠페인 최적화에 추가된 추적 세부 기간이 필요하므로 두 ID가 모두 필요합니다.

EF ID 차원은 [!DNL Analytics] 보고 EF ID는 마케팅 채널을 만드는 데 유용할 수 있습니다. EF ID 접미사는 채널(표시 또는 검색)과 방문이 클릭스루에 의해 제어되었는지 아니면 뷰스루에 의해 제어되었는지를 나타냅니다. EF ID의 구분 기호는 AMO ID의 느낌표가 아닌 콜론입니다.

| EF ID 접미사 | 채널 |
|-------|---------|
| : s | [!UICONTROL Paid Search] |
| :d | [!UICONTROL Display Click-through] |
| : i | [!UICONTROL Display View-through] |

### EF ID를 사용하는 처리 규칙의 예

#### 클릭스루 규칙 표시

클릭스루만 캡처하여 디스플레이 클릭스루 마케팅 채널을 만듭니다. AMO ID는 클릭스루와 뷰스루 모두에 대해 동일하므로 이 규칙은 EF ID 변수와 `ef_id` 쿼리 문자열 매개 변수가 포함된 랜딩 페이지 URL이 있는지 확인합니다.

경우에 따라 URL(기본값)을 통해 클릭스루가 추적됩니다. 다른 경우에는 서버 측에서 마지막 이벤트 서비스를 통해 클릭스루가 추적되므로 URL에 가 포함되어 있지 않습니다 `ef_id` 매개 변수. 따라서 규칙은 EF ID 변수 또는 `ef_id` 쿼리 문자열 매개 변수는 &quot;:d&quot;로 끝납니다. &quot;`Any`&quot; 두 조건 중 하나에 대해 이 규칙을 트리거할 수 있습니다.

![디스플레이 클릭스루 규칙의 예](/help/integrations/assets/a4adc-mc-rule-display-ct.png)

#### 뷰스루 규칙 표시

디스플레이 뷰스루 채널을 만들려면 EF ID가 &quot;:i&quot;로 끝나는 규칙을 만듭니다. 방문자가 광고를 클릭하지 않았으므로 뷰스루 추적에 `ef_id` 또는 `s_kwcid` 를 사용하여 규칙을 만들 수 있습니다.

![표시 뷰스루 규칙의 예](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

>[!MORELIKETHIS]
>
>* [기본 사항 [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Adobe 광고과 광고 사이에 채널 데이터가 다를 수 있는 이유 [!DNL Marketing Channels]](mc-data-variances.md)
>* [사용 [!DNL Analytics Marketing Channels] 광고 데이터 Adobe 사용](mc-ac-data.md)
>* [비디오: 사용 [!DNL Marketing Channels] Adobe 광고 보고용](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Adobe 광고 ID 사용 [!DNL Analytics]](/help/integrations/analytics/ids.md)

