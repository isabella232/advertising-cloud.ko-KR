---
title: 에서 사용하는 Advertising Cloud ID [!DNL Analytics]
description: 에서 사용하는 Advertising Cloud ID [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ed1aab7b-9bd0-4d42-9bfb-9c6fa6db76bc
source-git-commit: 525bc48104f928ccf9a3bb792b7e33c7e590cf4a
workflow-type: tm+mt
source-wordcount: '1194'
ht-degree: 0%

---

# 에서 사용하는 Advertising Cloud ID [!DNL Analytics]

*Advertising Cloud-Adobe Analytics 통합만 있는 광고주*

*Advertising Cloud DSP 및 Advertising Cloud Search에 적용 가능*

Advertising Cloud은 온사이트 성능 추적에 두 개의 ID를 사용합니다. a *EF ID* 그리고 *AMO ID*.

광고 노출이 발생하면 Advertising Cloud에서 AMO ID 및 EF ID 값을 만들어 저장합니다. 광고를 본 방문자가 광고를 클릭하지 않고 사이트에 들어오면, [!DNL Analytics] 는 Advertising Cloud에서 을 통해 이러한 값을 호출합니다 [!DNL Analytics for Advertising Cloud] JavaScript 코드. 뷰스루 트래픽의 경우, [!DNL Analytics] 는 보충 ID(`SDID`)을 클릭하여 EF ID와 AMO ID를 [!DNL Analytics]. 클릭스루 트래픽의 경우 이러한 ID는 `s_kwcid` 및 `ef_id` 쿼리 문자열 매개 변수.

Advertising Cloud은 다음 기준을 사용하여 웹 사이트에 대한 클릭스루 또는 뷰스루 항목을 구별합니다.

* 사용자가 광고를 보고 사이트를 방문하지만 클릭하지 않은 경우 뷰스루 항목이 캡처됩니다. [!DNL Analytics] 두 가지 조건이 충족되는 경우 뷰스루를 기록합니다.
   * 방문자에 대한 클릭스루가 없습니다 [!DNL DSP] 또는 [!DNL Search] 다음 기간 동안 광고 [전환 확인 기간 을 클릭합니다.](#lookback-a4adc).
   * 방문자가 적어도 한 명을 보았습니다 [!DNL DSP] 다음 기간 동안 광고 [노출 횟수 전환 확인 기간](#lookback-a4adc). 마지막 노출이 뷰스루로 전달됩니다.
* 사이트 방문자가 사이트로 들어오기 전에 광고를 클릭하면 클릭스루 항목이 캡처됩니다. [!DNL Analytics] 다음 조건 중 하나가 발생하면 클릭스루를 캡처합니다.
   * 이 URL에는 Advertising Cloud이 랜딩 페이지 URL에 추가한 EF ID와 AMO ID가 포함되어 있습니다.
   * URL에 추적 코드가 포함되어 있지 않지만, Advertising Cloud JavaScript 코드는 지난 2분 내에 클릭 수를 감지합니다.

![Advertising Cloud 보기 기반 [!DNL Analytics] 통합](/help/integrations/assets/a4adc-view-through-process.png)

*그림 1: Advertising Cloud 보기 기반 [!DNL Analytics] 통합*

![Advertising Cloud 클릭 URL 기반 [!DNL Analytics] 통합](/help/integrations/assets/a4adc-click-through-process.png)

*그림 2: Advertising Cloud 클릭 URL 기반 [!DNL Analytics] 통합*

## Advertising Cloud EF ID

EF ID는 Advertising Cloud에서 활동을 온라인 클릭 또는 광고 노출과 연결하는 데 사용하는 고유한 토큰입니다. EF ID는 [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) 또는 Var(예약된 eVar) 차원(Advertising Cloud EF ID)을 추적하고 개별 브라우저 또는 장치 수준에서 각 광고 클릭이나 노출을 추적합니다. EF ID는 주로 전송 키로 작동합니다 [!DNL Analytics] Advertising Cloud 내에서 보고 및 입찰 최적화를 위해 Advertising Cloud에 데이터를 보냅니다.

### EF ID 형식

>[!NOTE]
>
>EF ID는 대/소문자를 구분합니다. 다음과 같은 경우 [!DNL Analytics] 구현에서는 URL 추적을 소문자로 강제 적용하면 Advertising Cloud에서 EF ID를 인식하지 못합니다. 이 경우 Advertising Cloud 입찰 및 보고에 영향을 주지만 내에서 Advertising Cloud 보고에 영향을 주지 않습니다 [!DNL Analytics].

#### [!DNL Google Ads] 검색 광고

```{gclid}:G:s```

위치:

* `gclid` 은 [!DNL Google Click ID] (GCLID).
* `s` 은 네트워크 유형(&quot;s&quot; for search)입니다.

#### Microsoft 광고 검색 광고

```{msclkid}:G:s```

위치:

* `msclkid` 은 [!DNL Microsoft Click ID] (MSCLKID).
* `s` 은 네트워크 유형(&quot;s&quot; for search)입니다.

#### 다른 검색 엔진에 광고 및 검색 광고를 표시합니다

```<Advertising Cloud visitor ID>:<timestamp>:<channel type>```

<!-- <*Advertising Cloud visitor ID*>:<*timestamp*>:<*channel type*> -->

위치:

* &lt;*Advertising Cloud 방문자 ID*> 은 방문자당 고유한 ID(예: UhKVaAABCkJ0mDt)입니다. 또한 *서퍼 ID*.

* &lt;*timestamp*>은(는) YYYYMMDDHHMSS 형식의 시간입니다(예: 2019년 20190821192533, 월 08일, 21일, 시간 19:25:3)

* &lt;*채널 유형*> 은 클릭 또는 노출을 담당하는 채널 유형입니다.

   * `d` DSP 디스플레이 광고를 클릭하는 경우(클릭스루 표시)
   * `i` DSP 디스플레이 광고 노출(디스플레이 뷰스루)
   * `s` 검색 광고(검색 클릭스루)를 클릭합니다.

예 `EF `ID: WcmibgAAAHJK1RyY:1551968087687:d

### 의 EF ID Dimension [!DNL Analytics]

in [!DNL Analytics] 보고서에서 EF ID 데이터를 검색할 수 있습니다 [!UICONTROL EF ID] 차원 및 사용 [!UICONTROL EF ID Instance] 지표.

EF ID는 Analysis Workspace에서 50만 개의 고유 식별자 제한을 받습니다. 50만 값에 도달하면 모든 새 추적 코드가 1라인 항목 제목 아래에 보고됩니다.[!UICONTROL Low Traffic].&quot; 보고 정확도가 누락될 수 있으므로 EF ID는 분류되지 않으므로 세그먼트나 보고에 이러한 ID를 사용해서는 안 됩니다 [!DNL Analytics].

## Advertising Cloud AMO ID

AMO ID는 덜 세분화된 수준에서 각 고유 광고 조합을 추적하며 [!DNL Analytics] Advertising Cloud의 광고 지표(노출 횟수, 클릭 수 및 비용 등)에 대한 데이터 분류 및 섭취. AMO ID는에 저장됩니다. [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) 또는 rVar 차원(AMO ID)이며,에서 보고에만 사용됩니다 [!DNL Analytics].

AMO ID를 `s_kwcid`: 때로 &quot;[!DNL the squid].&quot;

### AMO ID 형식 [!DNL DSP]

```<Channel ID>!<Ad ID>!<Placement ID>```

위치:

* &lt;*채널 ID*>은(는) 다음 경우에 사용할 수 있습니다.

   * `AC` = Advertising Cloud DSP
   * `AL` Advertising Cloud Search

* &lt;*광고 ID*> 은 광고에 Advertising Cloud에서 생성한 고유 식별자를 사용합니다. Advertising Cloud 엔티티 메타데이터를 읽을 수 있도록 변환하는 키 역할을 합니다 [!DNL Analytics] 차원.

* &lt;*배치 ID*> 은 배치에 대해 Advertising Cloud에서 생성한 고유 식별자입니다. Advertising Cloud 엔티티 메타데이터를 읽을 수 있도록 변환하는 키 역할을 합니다 [!DNL Analytics] 차원.

<!-- <*Channel ID*>!<*Ad ID*>!<*Placement ID*>

where:

* <*Channel ID*> may be:

    * `AC` = Advertising Cloud DSP
    * `AL` for Advertising Cloud Search

* <*Ad ID*> is used an Advertising Cloud-generated unique identifier for an ad. It serves as a key for translating Advertising Cloud entity metadata into readable [!DNL Analytics] dimensions.

* <*Placement ID*> is an Advertising Cloud-generated unique identifier for an placement. It serves as a key for translating Advertising Cloud entity metadata into readable [!DNL Analytics] dimensions.
 -->

AMO ID 예: AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

### AMO ID 형식 [!DNL Search]

용 AMO ID [!DNL Search] 각 검색 엔진에 대해 고유한 형식을 따릅니다. 모든 검색 엔진의 형식은 다음과 같이 시작합니다.

```AL!{userid}!{sid}```

위치:

* `AL` 은 검색 채널의 채널 ID입니다.
* `{userid}` 는 Advertising Cloud이 광고주에 할당하는 고유한 숫자 사용자 ID입니다.
* `{sid}` Advertising Cloud이 지정된 검색 엔진에 사용하는 숫자 ID입니다(예: ) `3` 대상 [!DNL Google Ads] 또는 `10` 대상 [!DNL Microsoft Advertising].

다음은 두 개의 검색 엔진에 대한 전체 AMO ID 형식입니다. 다른 검색 엔진에 대한 AMO ID 형식은 [!DNL Adobe] 계정 팀입니다.

AMO ID 형식 [!DNL Google Ads]:

```AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}```

위치:

* `{creative}` 은 [!DNL Google Ads] 문안 ID입니다.
* `{matchtype}` 는 광고를 트리거한 키워드의 일치 유형입니다. `e` 정확히 말하면 `p` 또는 `b` 광범위한
* `{placement}` 은 광고를 클릭한 웹 사이트의 도메인 이름입니다. 값은 배치 타겟팅된 캠페인의 광고와 콘텐츠 사이트에 표시되는 키워드 타겟팅 캠페인의 광고에 사용할 수 있습니다.
* `{network}` 클릭이 발생한 네트워크를 나타냅니다.  `g` 대상 [!DNL Google] 검색(키워드 타깃팅된 광고만 해당), `s` 검색 파트너(키워드 타깃팅된 광고만 해당) 또는 `d` 디스플레이 네트워크(키워드 타깃팅되거나 배치 타깃팅된 광고의 경우)에 사용됩니다.
* `{keyword}` 은 광고를 트리거하는 특정 키워드(검색 사이트에서)나 가장 일치하는 키워드(콘텐츠 사이트에서)입니다.

AMO ID 형식 [!DNL Microsoft Advertising]:

```AL!{userid}!{sid}!{AdId}!{OrderItemId}```

위치:

* `{AdId}` 은 [!DNL Microsoft Advertising] 문안 ID입니다.
* `{OrderItemId}` 은 [!DNL Microsoft Advertising] 키워드의 숫자 ID입니다.

### 의 AMO ID Dimension [!DNL Analytics]

Analytics 보고서에서 [!UICONTROL AMO ID] 차원 및 사용 [!UICONTROL AMO ID Instance] 지표. 다음 [!UICONTROL AMO ID] 차원은 캡처된 모든 AMO ID 값을 포함하지만, [!UICONTROL AMO ID Instance] 지표는 사이트에서 AMO ID 값을 캡처한 빈도를 나타냅니다. 예를 들어 동일한 검색 광고를 4번 클릭했지만 Analytics가 7개의 사이트 항목을 추적한 경우 [!UICONTROL AMO ID Instance] 7과 [!UICONTROL Clicks] 4는 (4)입니다.

내 모든 보고 또는 감사 [!DNL Analytics]를 설정하는 것이 좋습니다. 해당 인스턴스와 함께 AMO ID를 사용하는 것이 좋습니다. 자세한 내용은 &quot;[에 대한 데이터 유효성 검사 [!DNL Analytics for Advertising Cloud]](data-variances.md#data-validation)&quot;(다음 사이 의 예상되는 데이터 분산) [!DNL Analytics] 그리고 Advertising Cloud.&quot;

## Analytics 분류 정보

in [!DNL Analytics], [분류](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) 는 계정, 캠페인 또는 광고와 같은 주어진 추적 코드에 대한 메타데이터의 일부입니다. Advertising Cloud은 보고서를 생성할 때 데이터를 다양한 방법(예: 광고 유형 또는 캠페인)으로 표시할 수 있도록 분류를 사용하여 원시 Advertising Cloud 데이터를 분류합니다. 분류는 의 Advertising Cloud 보고 기준을 형성합니다 [!DNL Analytics] 와 같은 AMO 지표와 함께 사용할 수 있습니다. [!UICONTROL AMO Cost], [!UICONTROL AMO Impressions], 및 [!UICONTROL AMO Clicks]와 같은 사용자 지정 및 표준 온사이트 이벤트 포함 [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders], 및 [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [개요 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [다음 사이 예상되는 데이터 분산 [!DNL Analytics] 및 Advertising Cloud](data-variances.md)

