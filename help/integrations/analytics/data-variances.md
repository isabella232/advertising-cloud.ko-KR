---
title: ' [!DNL Analytics] 과 Advertising Cloud 간의 예상 데이터 분산'
description: ' [!DNL Analytics] 과 Advertising Cloud 간의 예상 데이터 분산'
feature: Integration with Adobe Analytics
exl-id: 34685e04-d4f9-4e27-b83e-b56164244b2b
source-git-commit: 185fc7d79798a0a3a9ad5829b701aeb53a4a47c1
workflow-type: tm+mt
source-wordcount: '3285'
ht-degree: 0%

---

# [!DNL Analytics] 과 Advertising Cloud 간의 예상 데이터 분산

*Advertising Cloud-Adobe Analytics 통합만 있는 광고주*

[!DNL Analytics for Advertising Cloud] <!-- (A4AdC) --> 통합 추적을 사용하는 광고주는 Advertising Cloud 및 Adobe Analytics을 통해 유료 광고를 추적합니다. 여러 시스템을 통해 미디어, 캠페인 및 채널을 추적할 때 서로 다른 시스템의 동일한 데이터 세트가 거의 일치하지 않습니다. 이 문서에서는 Advertising Cloud을 통해 인신매매되는 미디어에 대한 데이터를 [!DNL Analytics] 내에서 미디어가 추적되는 다른 시스템의 데이터와 비교하는 방법을 설명합니다.

>[!NOTE]
>
>이 문서는 Advertising Cloud 및 Analytics에 중점을 두지만, 많은 주요 사항도 다른 추적 솔루션으로 전송할 수 있습니다.

## 유사한 보고서의 속성 차이

### 잠재적으로 다른 전환 확인 기간 및 속성 모델

[!DNL Analytics for Advertising Cloud] 통합에서는 두 개의 변수(eVars 또는 rVars \[예약된 eVars]\)를 사용하여 [EF ID 및 AMO ID](ids.md)를 캡처합니다. 이러한 변수는 단일 전환 확인 기간(클릭스루 및 뷰스루가 귀속되는 시간) 및 속성 모델로 구성됩니다. 별도로 지정하지 않는 한, 변수는 Advertising Cloud의 기본, 광고주 수준 클릭 전환 확인 기간 및 속성 모델과 일치하도록 구성됩니다.

하지만 전환 확인 기간 및 속성 모델은 Analytics(eVar를 통해)와 Advertising Cloud 모두에서 구성할 수 있습니다. 또한 Advertising Cloud에서 속성 모델은 광고주 수준(입찰 최적화를 위해)에서만 구성할 수 있을 뿐만 아니라 개별 데이터 보기 및 보고서 내에서도(보고 목적으로만) 구성할 수 있습니다. 예를 들어, 조직은 최적화를 위해 짝수 배포 속성 모델을 사용하지만 Advertising Cloud DSP 또는 [!DNL Search]의 보고서에 대한 마지막 터치 속성을 사용할 수 있습니다. 속성 모델을 변경하면 속성 전환 수가 변경됩니다.

보고 전환 확인 기간 또는 속성 모델이 한 제품에서 수정되고 다른 제품이 아닌 경우, 각 시스템의 동일한 보고서에 고유한 데이터가 표시됩니다.

* **서로 다른 전환 확인 기간으로 인한 불일치 예:**

   Advertising Cloud에 60일 클릭 전환 확인 창이 있고 [!DNL Analytics]에 30일 전환 확인 창이 있다고 가정해 봅시다. 사용자가 Advertising Cloud 추적된 광고를 통해 사이트를 방문한 다음 45일에 재방문한 다음 전환한다고 가정합니다. Advertising Cloud은 60일 전환 확인 기간 내에서 전환이 발생했기 때문에 초기 방문으로 전환을 기여하게 됩니다. [!DNL Analytics]그러나 30일 전환 확인 기간이 만료된 후 전환이 발생했으므로 이 전환을 초기 방문으로 간주할 수 없습니다. 이 예에서 Advertising Cloud은 [!DNL Analytics]보다 더 많은 전환 수를 보고합니다.

   ![Advertising Cloud에서 귀속되는 전환의 예  [!DNL Analytics]](/help/integrations/assets/a4adc-lookback-example.png)

* **서로 다른 속성 모델에 의한 불일치의 예:**

   사용자가 매출 을 전환 유형으로 사용하여 전환하기 전에 세 개의 다른 Advertising Cloud 광고과 상호 작용한다고 가정합니다. Advertising Cloud 보고서가 속성에 짝수 배포 모델을 사용하는 경우 모든 광고에 균등하게 매출을 기여합니다. 그러나 [!DNL Analytics] 이 마지막 터치 속성 모델을 사용하는 경우 매출을 마지막 광고에 연결합니다. 다음 예에서는 Advertising Cloud이 각 3개의 광고에 캡처된 30USD 매출 중 10USD도 차지하는 반면 [!DNL Analytics] 는 사용자가 본 마지막 광고에 30USD의 매출을 모두 기여합니다. Advertising Cloud과 [!DNL Analytics]의 보고서를 비교할 때 속성 차이가 미치는 영향을 예상할 수 있습니다.

   ![Advertising Cloud으로 인한 서로 다른 수입이며, 서로 다른 속성 모델 [!DNL Analytics] 을 기반으로 한 다양한 수입입니다](/help/integrations/assets/a4adc-attribution-example.png)

>[!IMPORTANT]
>
>가장 좋은 방법은 Advertising Cloud과 [!DNL Analytics] 모두에서 동일한 전환 확인 기간과 속성 모델을 사용하는 것입니다. 현재 설정을 식별하고 구성을 계속 동기화하는 데 필요한 Adobe 계정 관리자와 함께 작업할 수 있습니다.

이러한 동일한 개념은 서로 다른 전환 확인 기간 또는 속성 모델을 사용하는 다른 채널과 유사한 모든 채널에 적용됩니다.

#### 뷰스루 추적을 위한 다른 전환 창 {#impression-lookback}

Advertising Cloud에서 속성은 클릭 및 노출을 기반으로 하며 클릭 및 노출을 위해 서로 다른 전환 확인 기간을 구성할 수 있습니다. 그러나 [!DNL Analytics]에서 속성은 클릭스루 및 뷰스루를 기반으로 하며 클릭스루 및 뷰스루에 대해 서로 다른 속성 창을 설정할 수 있는 선택 사항이 없습니다. 각 시작에 대한 추적은 초기 사이트 방문에서 시작됩니다. 노출은 뷰스루가 발생하기 하루 또는 여러 날 전에 발생할 수 있으며, 이 경우 각 시스템에서 속성 창이 시작되는 위치에 영향을 줄 수 있습니다.

일반적으로 뷰스루 전환의 대부분은 두 시스템 모두 크레딧을 받을 만큼 빠르게 발생합니다. 그러나 일부 전환은 Advertising Cloud 노출 전환 확인 기간 외부와 [!DNL Analytics] 전환 확인 기간 내에 발생할 수 있습니다. 이러한 전환은 [!DNL Analytics]의 뷰스루에 귀속되지만 Advertising Cloud의 노출에는 귀속되지 않습니다.

다음 예에서는 방문자가 1일에 광고를 제공하고, 2일에 광고를 클릭하지 않고, 방문자가 뷰스루 방문(즉, 이전에 광고를 클릭하지 않고 광고의 랜딩 페이지를 방문)을 수행하고, 45일에 전환되었다고 가정합니다. 이 경우 Advertising Cloud은 1~14일(14일 전환 확인 사용)에서 사용자를 추적하고, [!DNL Analytics]은 2일~61일(60일 전환 확인 사용)에서 사용자를 추적하며, 45일의 전환은 [!DNL Analytics] 내에 있는 광고에 귀속되지만 Advertising Cloud 내에서는 추적되지 않습니다.

![Advertising Cloud에 귀속되는 뷰스루 전환 [!DNL Analytics] 의 예](/help/integrations/assets/a4adc-viewthrough-example.png)

불일치의 추가적인 원인은 Advertising Cloud에서 클릭 기반 전환으로 인한 가중치에 상대적인 사용자 지정 *뷰스루 가중치*&#x200B;에 대한 뷰스루 전환을 지정할 수 있다는 것입니다. 기본 뷰스루 가중치는 40%입니다. 즉, 뷰스루 전환이 클릭 기반 전환 값의 40%로 계산됩니다. [!DNL Analytics] 에서는 뷰스루 전환 가중치를 제공하지 않습니다. 따라서 예를 들어, 기본 뷰스루 가중치(60USD)를 사용하는 경우 [!DNL Analytics]에 캡처한 100USD의 수입 주문은 Advertising Cloud에서 40USD로 할인됩니다.

Advertising Cloud과 [!DNL Analytics] 보고서 간의 뷰스루 전환을 비교할 때에는 이러한 차이점을 고려하십시오.

#### 사용 가능한 속성 모델

| Advertising Cloud 속성 | [!DNL Analytics] 속성 | eVar/rVar 할당 |
|--- |--- |--- |
| [!UICONTROL Last Event] | [!UICONTROL Last Touch] | [!UICONTROL Most Recent] |
| [!UICONTROL First Event] | [!UICONTROL First Touch] | [!UICONTROL Original Value] |
| [!UICONTROL Weight First Event More] | n/a | n/a |
| [!UICONTROL Even Distribution] | [!UICONTROL Linear] | [!UICONTROL Linear]<br><br>사용하지 않음* |
| [!UICONTROL Weight Last Event More] | n/a | n/a |
| [!UICONTROL U-Shaped] | [!UICONTROL U-Shaped] | n/a |
| n/a | [!UICONTROL J-Shaped] | n/a |
| n/a | [!UICONTROL Inverse-J] | n/a |
| n/a | [!UICONTROL Custom] | n/a |
| n/a | [!UICONTROL Participation] | n/a |
| n/a | [!UICONTROL Algorithmic] | n/a |

>[!NOTE]
>
>선형 할당의 경우 [!DNL Analytics] 은 단일 방문 내의 모든 eVar 값에 균일하게 성공 이벤트를 기여하므로, &quot;방문&quot; eVar 만료과 함께 선형 할당을 사용하십시오. 그러나 광고의 경우 선형 속성을 사용하면 실제로 선형적이지 않고 덜 이상적인 보고에 대한 할당이 발생합니다. 예를 들어 방문자가 세 개의 별도 방문에서 전환하기 전에 세 개의 광고와 상호 작용하는 경우 마지막 방문에서 본 광고만 세 개의 광고 모두가 아닌 전환으로 인한 것입니다.
>
>또한 전환 할당을 &quot;선형&quot;으로 또는 반대로 전환하면 내역 데이터가 표시되지 않으므로 보고서에 잘못 지정된 데이터가 나타날 수 있습니다. 예를 들어 선형 할당은 여러 다른 eVar 값으로 매출을 분할할 수 있습니다. 할당을 &quot;가장 최근&quot;으로 변경하면 해당 수입의 100%가 가장 최근 단일 값과 연결됩니다. 이러한 연관성이 잘못된 결론에 도달할 수 있습니다.
>
>혼동을 방지하기 위해 [!DNL Analytics]은(는) 보고 인터페이스에서 이전 데이터를 사용할 수 없게 합니다. 내역 데이터에 액세스하려면 eVar 할당 설정을 변경해서는 안 되지만, eVar을 다시 초기 할당 설정으로 변경하면 내역 데이터를 볼 수 있습니다. Adobe은 이미 상당한 양의 내역 데이터가 있는 eVar에 대한 할당 설정을 변경하는 대신 이미 기록되고 있는 데이터에 새 할당 설정을 적용하려면 새 eVar을 사용하는 것이 좋습니다.

[!DNL Analytics] 속성 모델 목록과 해당 정의를 [https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html)에서 참조하십시오.

Advertising Cloud에 로그인되어 있는 경우에는 의 속성 모델 목록을 찾을 수 있습니다.
[https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm](https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

#### Advertising Cloud의 이벤트 날짜 속성

Advertising Cloud에서는 연결된 클릭 날짜/이벤트 날짜(클릭 또는 노출 이벤트의 날짜) 또는 트랜잭션 날짜(전환 날짜)별로 전환 데이터를 보고할 수 있습니다. 클릭/이벤트 날짜 보고 개념이 [!DNL Analytics]에 없습니다. [!DNL Analytics]에서 추적된 모든 전환은 트랜잭션 날짜별로 보고됩니다. 따라서 Advertising Cloud 및 [!DNL Analytics]에 있는 다른 날짜에 동일한 전환이 보고될 수 있습니다. 예를 들어, 1월 1일에 광고를 클릭하고 1월 5일에 전환하는 사용자를 생각해 보십시오. Advertising Cloud에서 이벤트 날짜별로 전환 데이터를 보고 있다면 클릭이 발생한 1월 1일에 전환이 보고됩니다. [!DNL Analytics]에서 동일한 전환이 1월 5일에 보고됩니다.

![다른 날짜에 속하는 전환의 예](/help/integrations/assets/a4adc-conversions-based-on.png)

## [!DNL Analytics Marketing Channels]의 속성

[[!DNL Analytics Marketing Channels] ](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/marketing-channels-admin.html) 보고 기능을 사용하면 히트 정보의 고유한 측면을 기반으로 다른 마케팅 채널을 식별하도록 규칙을 구성할 수 있습니다. `ef_id` 쿼리 문자열 매개 변수를 사용하여 Advertising Cloud 추적된 채널([!UICONTROL Display Click Through], [!UICONTROL Display View Through] 및 [!UICONTROL Paid Search])을 [!DNL Marketing Channels]로 추적할 수 있습니다. <!-- Move most of the above text to "Marketing Channels" chapter once it's created, and add link here. --> 하지만 보고서에서  [!DNL Marketing Channels] Advertising Cloud 채널을 추적할 수 있지만, 몇 가지 이유로 데이터가 Advertising Cloud 보고서와 일치하지 않을 수 있습니다. 자세한 내용은 다음 섹션을 참조하십시오.

>[!NOTE]
>
> 다음 핵심 개념은 [`campaign`](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/campaign.html) 변수(&quot;추적 코드&quot; Dimension 또는 &quot;eVar 0&quot;이라고도 함) 및 사용자 지정 eVar 추적과 같이, Advertising Cloud에서 추적되지 않은 캠페인을 포함하는 모든 다중 채널 추적에도 적용됩니다.

### [!DNL Marketing Channels]에 있는 잠재적으로 다른 속성 모델

대부분의 [!DNL Marketing Channels] 보고서는 [!UICONTROL Last Touch] 속성으로 구성되며, 여기서 마지막으로 감지된 마케팅 채널은 전환 값의 100%가 할당됩니다. [!DNL Marketing Channels] 보고서 및 Advertising Cloud 보고서에 서로 다른 속성 모델을 사용하면 속성 전환이 일치하지 않습니다.

### [!DNL Marketing Channels]에 있을 수 있는 다른 전환 확인 기간

[!DNL Marketing Channels]에 대한 전환 확인 기간을 사용자 지정할 수 있습니다. Advertising Cloud에서 고정된 60일 창이 일반적이지만 클릭 전환 확인 기간은 구성할 수 있습니다. 두 제품이 서로 다른 전환 확인 기간을 사용하는 경우 데이터 불일치를 예상할 수 있습니다.

### [!DNL Marketing Channels]의 다른 채널 속성

Advertising Cloud 보고서는 Advertising Cloud(Advertising Cloud Search 광고에 대한 유료 검색 및 Advertising Cloud DSP 광고에 대한 표시)를 통해 인신매매된 유료 미디어만 캡처하지만, [!DNL Marketing Channels] 보고서는 모든 디지털 채널을 추적할 수 있습니다. 이로 인해 전환이 귀속되는 채널에서 불일치가 발생할 수 있습니다.

예를 들어 유료 검색 및 자연어 검색 채널은 종종 각 채널이 다른 채널을 지원하는 공생 관계를 갖습니다. [!DNL Marketing Channels] 보고서는 자연어 검색을 추적하지 않으므로 Advertising Cloud이 추적하지 않을 일부 전환을 자연어 검색에 표시합니다.

디스플레이 광고를 보고, 유료 검색 광고를 클릭하고, 이메일 메시지 내부를 클릭한 다음, 30USD 주문을 게재하는 고객을 고려합니다. Advertising Cloud과 [!DNL Marketing Channels] 둘 다 마지막 터치 속성 모델을 사용하더라도 전환은 여전히 각각 다르게 계산됩니다. Advertising Cloud은 [!UICONTROL Email] 채널에 액세스할 수 없으므로 전환을 위한 유료 검색을 크레딧합니다. [!DNL Marketing Channels]그러나 은 세 가지 채널 모두에 액세스할 수 있으므로 전환을  [!UICONTROL Email] 위해 크레딧을 받습니다.

![Advertising Cloud과 비교하여 다른 전환 속성의 예  [!DNL Analytics Marketing Channels]](/help/integrations/assets/a4adc-channel-example.png)

지표가 다양한 이유에 대한 자세한 내용은 &quot;[Advertising Cloud과 [!DNL Marketing Channels]](marketing-channels/mc-data-variances.md) 간에 채널 데이터가 달라질 수 있는 이유&quot;를 참조하십시오.

## Adobe Analytics [!DNL Paid Search Detection]의 데이터 차이점

[!DNL Analytics]의 [기존 [!DNL Paid Search Detection]](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/paid-search-detection.html) 기능을 사용하면 회사는 [규칙을 정의하여 지정된 검색 엔진에 대한 유료 및 유기 검색 트래픽을 추적할 수 있습니다.](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/t-paid-search-detection.html) [!DNL Paid Search Detection] 규칙은 쿼리 문자열과 참조 도메인을 모두 사용하여 유료 검색과 자연어 검색 트래픽을 식별합니다. [!DNL Paid Search Detection] 보고서는 지정된 이벤트(예: 장바구니 체크아웃)가 발생하거나 방문이 종료될 때 만료되는 더 큰 [검색 방법](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/finding-methods.html) 보고서 그룹의 일부입니다.

다음은 [!DNL Paid Search Detection] 규칙 세트를 만드는 인터페이스입니다.

![에 설정된 유료 검색 감지 규칙의 예  [!DNL Analytics]](/help/integrations/assets/a4adc-paid-search-detection.png)

결과 [!DNL Paid Search Detection] 보고서에는 [!UICONTROL Paid Search Engine], [!UICONTROL Paid Search Keywords], [!UICONTROL Natural Search Engine] 및 [!UICONTROL Natural Search Keywords] 보고서가 포함됩니다.

[!DNL Paid Search Detection] 보고서의 데이터에 대해 다음의 두 가지 제한 사항을 참고하십시오.

* [!UICONTROL Paid Search Keywords] 및 [!UICONTROL Natural Search Keywords] 보고서는 사용자가 입찰하는 키워드가 아니라 참조 URL로 식별되는 검색 쿼리를 보여줍니다. Advertising Cloud 및 [!DNL Analytics] 보고서에는 실제 키워드가 표시되므로 [!DNL Paid Search Detection] 키워드 보고서에 일치하지는 마십시오.

* 원래 [!DNL Paid Search Detection] 기능이 만들어지면 원래 검색 쿼리(사용자가 검색 엔진의 검색 표시줄에 입력한 문자 문자열)가 참조 URL을 통해 광고주가 보다 쉽게 사용할 수 있었습니다. 현재 검색 엔진은 검색 쿼리를 대부분 난독화하므로 [!DNL Paid Search Detection] 키워드 보고서는 대부분의 쿼리 데이터가 &quot;지정되지 않음&quot;에 속하므로 값이 제한됩니다.

   [!DNL Analytics for Advertising Cloud]을 사용하는 광고주는 여전히 [!DNL Analytics]에서 유료 키워드를 추적할 수 있습니다. 참조 도메인은 트래픽을 유도한 검색 엔진을 엔진 보고서에 알려줍니다. 광고주별 계정 정보가 참조 도메인에 연결되어 있지 않으므로 모든 트래픽이 검색 엔진 아래에 나열됩니다. 동일한 검색 엔진에 여러 계정이 있는 광고주는 계정별 보고를 위해 Advertising Cloud 또는 [!DNL Analytics] 보고를 참조해야 합니다.

### [!DNL Paid Search Detection]을 구성하는 이유

[!DNL Paid Search Detection] 보고서를 사용하면 [[!DNL Analytics Marketing Channels] reports](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/marketing-channels-admin.html)에서 자연어 검색 트래픽을 식별할 수 있습니다. 유료 검색 트래픽과 자연어 검색 트래픽을 분리하는 것은 자연어 검색이 전체 마케팅 에코시스템에 가져오는 값을 이해하는 좋은 방법입니다.

## [!DNL Analytics for Advertising Cloud]에 대한 클릭스루 데이터 유효성 검사 {#data-validation}

통합의 경우 클릭스루 데이터의 유효성을 검사하여 사이트의 모든 페이지가 클릭스루를 올바르게 추적하는지 확인해야 합니다.

[!DNL Analytics]에서 [!DNL Analytics for Advertising Cloud] 추적을 확인하는 가장 쉬운 방법 중 하나는 다음과 같이 계산되는 &quot;AMO ID 인스턴스에 클릭 수&quot; 계산된 지표를 사용하여 클릭을 인스턴스와 비교하는 것입니다.

```Clicks to AMO ID Instances = (AMO ID Instances / AMO Clicks)```

[!UICONTROL AMO ID Instances] 사이트에서 AMO ID(`s_kwcid`  매개 변수)를 추적한 횟수를 나타냅니다. 광고를 클릭할 때마다 `s_kwcid` 매개 변수가 랜딩 페이지 URL에 추가됩니다. 따라서 [!UICONTROL AMO ID Instances] 수는 클릭 수와 유사하며 실제 광고 클릭에 대해 유효성을 검사할 수 있습니다. 일반적으로 [!DNL Search]에 대한 80% 일치율과 [!DNL DSP] 트래픽에 대한 30% 일치율이 표시됩니다(클릭스루 [!UICONTROL AMO ID Instances]만 포함하도록 필터링된 경우). 검색과 디스플레이 간의 예상 차이는 예상되는 트래픽 동작으로 설명할 수 있습니다. 검색은 의도를 캡처하며, 따라서 일반적으로 사용자가 쿼리의 검색 결과를 클릭합니다. 그러나 디스플레이 또는 온라인 비디오 광고를 보는 사용자는 실수로 광고를 클릭한 다음, 사이트에서 바운스 또는 페이지 활동이 추적되기 전에 로드되는 새 창을 포기할 가능성이 높습니다.

Advertising Cloud 보고서에서는 클릭을 [!UICONTROL AMO ID Instances] 대신 &quot;[!UICONTROL ef_id_instances]&quot; 지표를 사용하여 인스턴스와 유사하게 비교할 수 있습니다.

```Clicks to [!UICONTROL EF ID Instances] = (ef_id_instances / Clicks)```

AMO ID와 EF ID 간의 일치율이 높을 것으로 예상해야 하지만 AMO ID와 EF ID가 기본적으로 다른 데이터를 추적하므로 100% 패리티를 기대하지 마십시오. 이 차이로 인해 총 [!UICONTROL AMO ID Instances] 및 [!UICONTROL EF ID Instances]에 약간의 차이가 발생할 수 있습니다. [!DNL Analytics]의 총 [!UICONTROL AMO ID Instances]이 Advertising Cloud의 [!UICONTROL EF ID Instances]와 1% 이상 다른 경우 Adobe 계정 관리자에게 문의하여 지원을 받으십시오.

AMO ID 및 EF ID에 대한 자세한 내용은 Analytics에서 사용하는 [Advertising Cloud ID](ids.md)를 참조하십시오.

다음은 인스턴스 클릭 수를 추적하는 작업 공간의 예입니다.

![인스턴스 클릭 수를 추적하는 작업 공간의 예](/help/integrations/assets/a4adc-clicks-to-instances-example.png)

## [!DNL Analytics for Advertising Cloud]의 데이터 세트와 Advertising Cloud의 데이터 세트 비교

[AMO ID](ids.md) (s_kwcid 쿼리 문자열 매개 변수)는 [!DNL Analytics]에서 보고하는 데 사용되며 [EF ID](ids.md)는 Advertising Cloud에서 보고하는 데 사용됩니다. 고유한 값이므로 한 값이 손상되거나 랜딩 페이지에 추가되지 않을 수 있습니다.

예를 들어 다음과 같은 랜딩 페이지가 있다고 가정합니다.

`www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id`

여기서 EF ID는 &quot;`test_ef_id`&quot;이고 AMO ID는 &quot;`test_amo_id`&quot;입니다.

사이트측 리디렉션이 발생하는 경우 URL이 다음과 같이 끝날 수 있습니다.

`www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id#redirectAnchorTag`

여기서 EF ID는 &quot;`test_ef_id`&quot;이고 AMO ID는 &quot;`test_amo_id#redirectAnchorTag`&quot;입니다.

이 예에서 앵커 태그를 추가하면 AMO ID에 예기치 않은 문자가 추가되어 Analytics에서 인식하지 못하는 값이 발생합니다. 이 AMO ID는 분류되지 않으며 연결된 전환은 [!DNL Analytics] 보고서의 &quot;[!UICONTROL unspecified]&quot; 또는 &quot;[!UICONTROL none]&quot;에 속합니다.

다행히도, 이와 같은 문제는 흔한 일이지만, 일반적으로 높은 비율의 불일치를 초래하지는 않습니다. 그러나 [!DNL Analytics]의 AMO ID와 Advertising Cloud의 EF ID 간에 큰 차이가 발생하는 경우 Adobe 계정 관리자에게 문의하여 지원을 받으십시오.

## 기타 지표 고려 사항

### 클릭 수와 방문 횟수 간의 차이점 {#clicks-vs-visits}

이는 유사해 보이지만 클릭 및 방문 수는 다른 데이터를 나타냅니다.

* **클릭:** [!DNL DSP]  또는 검색 엔진은 방문자가 게시자의 웹 사이트에서 광고를 클릭할 때 클릭을 기록합니다.

* **방문:** [!DNL Analytics] 사용자가 30분 동안 활동이  [](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html) 않는 경우와 같은 몇 가지 기준 중 하나에 따라 종료되는 일련의 페이지 보기를 정의합니다.

기본적으로 클릭을 수행하면 여러 방문이 발생할 수 있습니다.

다음 예를 생각해 보십시오. 사용자 1 및 사용자 2 는 모두 Advertising Cloud 광고를 클릭하여 사이트에 액세스합니다. 사용자 1은 4개의 페이지를 열람한 다음 하루를 떠나므로 초기 클릭으로 인해 한 번의 방문이 발생합니다. 사용자 2는 두 페이지를 보고 45분 동안 점심을 먹고 다시 돌아가서 두 페이지를 더 본 다음 나갑니다. 이 경우 초기 클릭으로 인해 두 번의 방문이 발생합니다.

![클릭 수와 방문 횟수 간의 차이점 예](/help/integrations/assets/a4adc-visits-example.png)

### 클릭과 클릭스루의 차이점

<!-- Rob to let me know if we should remove this and add more info. to the section on AMO Instances etc. -->

클릭 수와 클릭스루는 두 개의 서로 다른 지표입니다.

* **클릭:** [!DNL DSP]  또는 검색 엔진은 방문자가 게시자의 웹 사이트에서 광고를 클릭할 때 클릭을 기록합니다.

* **클릭스루:** [!DNL Analytics] 방문자가 대상 웹 사이트에 도달하고, 랜딩 페이지가 로드되고, 페이지 하단에  [!DNL Analytics] 있는 요청이 데이터를 [!DNL Analytics]에 보낼 때 클릭스루를 기록합니다.

클릭과 클릭스루는 우발적 광고 클릭으로 인해 크게 다를 수 있습니다. 디스플레이 광고의 대부분의 클릭이 우발적 클릭이며, 이러한 우발적 방문자가 랜딩 페이지가 로드되기 전에 뒤로 버튼을 히트하므로 [!DNL Analytics]이 클릭스루를 기록할 수 없습니다. 이는 특히 화면을 채우고 페이지를 보기 전에 닫아야 하는 모바일 광고, 비디오 광고 및 광고와 같이 고객이 실수로 클릭할 가능성이 높은 광고에 해당됩니다.

모바일 장치에 로드되는 사이트는 대역폭이 작거나 처리 능력이 향상되어 랜딩 페이지가 로드되는 시간이 오래 걸려서 클릭스루가 발생할 가능성도 낮습니다. 클릭의 50~70%가 클릭스루를 수행하지 않는 것은 일반적이지 않습니다. 모바일 환경에서 이러한 차이는 90%까지 높을 수 있습니다. 왜냐하면 더 느린 브라우저와 사용자가 페이지를 스크롤하거나 광고를 닫으려고 하는 동안 실수로 광고를 클릭할 가능성이 높기 때문입니다.

클릭 데이터는 현재 추적 메커니즘(예: 모바일 앱으로 들어가는 클릭 또는 들어오는 클릭)으로 클릭스루를 기록할 수 없거나 광고주가 하나의 추적 접근 방식(예: 뷰스루 JavaScript 접근 방식을 사용하는 경우 타사 쿠키를 차단하는 브라우저는 클릭스루가 아님)만 배포한 환경에서도 기록됩니다. Adobe이 클릭 URL 추적과 뷰스루 JavaScript 추적 접근 방식을 모두 배포하는 것이 권장되는 주요 이유는 추적 가능한 클릭스루의 범위를 최대화하는 것입니다.

### 비Advertising Cloud Dimension에 Advertising Cloud 트래픽 지표 사용

Advertising Cloud은 DSP 및 Search](advertising-cloud-metrics-in-analytics.md)의 광고 관련 트래픽 지표와 관련 차원을 Analytics에 제공합니다. [ Advertising Cloud에서 제공하는 지표는 지정된 Advertising Cloud 차원에만 적용할 수 있으며 데이터는 [!DNL Analytics]의 다른 차원에는 사용할 수 없습니다.

예를 들어 Advertising Cloud 차원인 계정별 [!UICONTROL AMO Clicks] 및 [!UICONTROL AMO Cost] 지표를 보면 계정별 총 [!UICONTROL AMO Clicks] 및 [!UICONTROL AMO Cost]이 표시됩니다.

![Advertising Cloud 차원을 사용하는 보고서의 Advertising Cloud 지표 예](/help/integrations/assets/a4adc-traffic-supported-dimension.png)

그러나 Advertising Cloud에서 데이터를 제공하지 않는 페이지 내 차원(예: 페이지)으로 [!UICONTROL AMO Clicks] 및 [!UICONTROL AMO Cost] 지표를 보는 경우 각 페이지에 대한 [!UICONTROL AMO Clicks] 및 [!UICONTROL AMO Cost]은 0이 됩니다(0).

![지원되지 않는 차원을 사용하는 보고서의 Advertising Cloud 지표 예](/help/integrations/assets/a4adc-traffic-unsupported-dimension.png)

### Advertising Cloud이 아닌 Dimension에서 클릭 대신 [!UICONTROL AMO ID Instances] 사용

사이트 내 차원과 함께 [!UICONTROL AMO Clicks]을 사용할 수 없으므로 클릭과 동등한 항목을 찾을 수 있습니다. 방문 횟수를 대체로 사용하고 싶을 수 있지만 각 방문자에게 여러 번의 방문이 있을 수 있으므로 이러한 옵션은 가장 적합한 옵션이 아닙니다. ([클릭 수와 방문 횟수](#clicks-vs-visits) 간의 차이를 참조하십시오.) 대신 [!UICONTROL AMO ID Instances] 을 사용하는 것이 좋습니다. 이 값은 AMO ID가 캡처된 횟수입니다. [!UICONTROL AMO ID Instances]이 [!UICONTROL AMO Clicks]과 정확히 일치하지 않지만 사이트에서 클릭 트래픽을 측정하는 데 가장 적합한 옵션입니다. 자세한 내용은 &quot;[데이터 유효성 검사 [!DNL Analytics for Advertising Cloud]](#data-validation)&quot;를 참조하십시오.

![지원되지  [!UICONTROL AMO ID Instances] 않는 차원 [!UICONTROL AMO Clicks] 의 예](/help/integrations/assets/a4adc-amo-id-instances.png)

>[!MORELIKETHIS]
>
>* [개요 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [에서 사용하는 Advertising Cloud ID [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Analysis Workspace의 Advertising Cloud 지표](/help/integrations/analytics/advertising-cloud-metrics-in-analytics.md)
>* [[!DNL Analytics] Advertising Cloud의 데이터](/help/integrations/analytics/analytics-data-in-advertising-cloud.md)
>* [Advertising Cloud과 데이터 간에 데이터가 다를 수 있는 이유 [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)

