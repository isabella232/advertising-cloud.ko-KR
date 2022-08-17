---
title: 광고 타깃팅용 Adobe Audience Manager 세그먼트 가져오기
description: 을(를) 가져오는 방법을 알아봅니다 [!DNL Adobe] Adobe Audience Manager을 사용하여 Advertising Cloud DSP으로 대상 전환 및 검색
feature: Integration with Adobe Audience Manager
source-git-commit: 9593400e48f5918850447daacfbdaaa9015e94cd
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 광고 타깃팅용 Adobe Audience Manager 세그먼트 가져오기

Advertising Cloud DSP과 Advertising Cloud Search은 각각 광고주 또는 에이전시의 모든 대상에 대한 메타데이터, 계층 데이터 및 고유한 대상 데이터를 가져올 수 있습니다 [!DNL Adobe] 대상자<!-- segments or audiences? Standardize terms per AAM's docs -->. 여기에는 다음에 대한 데이터가 포함됩니다.

* Adobe Audience Manager 세그먼트

* Adobe Experience Cloud에 게시된 Adobe Analytics 세그먼트

* Adobe Experience Cloud에서 [!DNL People core service]

* Adobe Experience Platform에서 만들어지고 Audience Manager을 통해 Advertising Cloud으로 전송되는 세그먼트

에 액세스하려면 [!DNL Adobe] DSP 또는 [!DNL Creative]를 채울 때는 대상을 DSP으로 가져와야 합니다. 에 액세스하려면 [!DNL Adobe] 대상 [!DNL Search]로 대상을 가져와야 합니다. [!DNL Search].

## 전제 조건

* 광고주는 다음을 구현해야 합니다 [a [!DNL Adobe Experience Cloud Identity (ECID) Service]](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) 버전 2.0 이상 다음 [!DNL Identity Service] 은 Experience Cloud의 모든 솔루션에서 방문자를 식별하는 범용 영구 ID를 제공합니다.

   구현에는 [!DNL Identity service] 광고주 사이트의 각 웹 페이지에 코드를 추가합니다.

* 조직은 [Experience Cloud 서비스에 대해 활성화됨](https://experienceleague.adobe.com/docs/core-services/interface/services/core-services.html) 그리고 Experience Cloud 있음 [!DNL Organization ID] (이전에는 [!DNL IMS org ID]).

   다음 [!UICONTROL Organization ID] 여러 Adobe Experience Cloud 제품이 있는 조직이 일부 제품 간에 데이터를 공유할 수 있도록 해줍니다.

* (광고 그룹 [!DNL Analytics]) 광고주는 [구현 [!DNL Analytics] 사용 `appMeasurement.js`](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html) 버전 1.6.4 이상.

* 광고주의 웹 사이트 방문자는 [!DNL Apple Safari] 사용자 참조.

* (광고주가 Audience Manager과 [!DNL Analytics]) 각 웹 페이지에 대한 호출을 줄이려면 기존 Audience Manager을 제거합니다 [!DNL Data Integration Library] 각 데이터 수집에 대한 코드 및 서버측 전달 활성화 [!DNL Analytics] 보고서 세트를 대신 사용할 수 있습니다. 자세한 내용은 &quot;[서버 측 전달 개요](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

* (권장) 일치율이 높은 경우 자사 웹 사이트 데이터만 Advertising Cloud에 보냅니다. 광고주가 고객 관계 관리 시스템에서 타사 데이터 또는 오프라인 데이터를 번들로 제공하는 경우 데이터 누출로 일치율이 낮아질 수 있습니다.

## DSP에 Audience Manager 대상 가져오기

### 대상을 DSP에 가져오는 단계

다음 [!DNL Adobe] 계정 및 데이터 작업 팀은 다음 단계를 수행합니다.

1. 다음 [!DNL Adobe] 계정 팀은 advertiser-level 설정을 구성해야 합니다.[!UICONTROL Adobe Analytics Cloud].&quot;

1. 다음 [!DNL Adobe] 계정 팀은 요청을 제출해야 합니다.<!-- Submit a request as a JIRA task? --> 데이터 작업 팀에<!-- implementation team? --> Advertising Cloud DSP 기본 API 통합을 사용하여 조직의 Audience Manager 세그먼트를 가져올 수 있습니다.

### Audience Manager의 결과물은 무엇입니까?

API는 자동으로 다음을 수행합니다.

* Audience Manager에서 두 개의 DSP 대상을 만듭니다.

   * **[!UICONTROL Adobe Ad Cloud Cross-Channel (real-time)]**

   * **[!UICONTROL Adobe AdCloud Cross-Channel (batch)])**

* 두 대상을 모든 Audience Manager 세그먼트에 매핑하여 Audience Manager이 동일한 Experience Cloud과 연결된 DSP 광고주 계정과 세그먼트를 공유할 수 있습니다 [!DNL Organization ID] Audience Manager에 사용됩니다. <!-- Verify -->

   조직에서 선택적으로 Audience Manager 내의 대상에서 불필요한 세그먼트를 제거할 수 있습니다.

* 다음 exchange 쿠키 동기화 픽셀을 조직의 Audience Manager 컨테이너에 추가하여 고객 캠페인의 범위를 개선합니다.

   * Adobe AdCloud: 411(표준 및 의 일부로 자동 제공) [!DNL Identity Service] 버전 2.0. 조직 [!DNL Identity Service] 2.0 이하 버전은 이 픽셀을 Audience Manager 컨테이너에 추가해야 합니다.

## 대상 Audience Manager 가져오기 [!DNL Search]

### 대상 가져오기에 대한 단계 [!DNL Search]

[!DNL Adobe] 담당자는 다음 단계 중 대부분 또는 전부를 수행합니다.

1. 다음 [!DNL Adobe] 계정 팀은 데이터 작업 팀에 요청하여 두 팀 간의 통합을 설정해야 합니다. [!DNL Search] 및 Audience Manager. 내보낼 Audience Manager 세그먼트의 이름을 포함합니다 [!DNL Search].

1. Audience Manager 내에서 대상 구성 [!DNL Search]:

   1. 두 개의 새 대상 만들기: `[!UICONTROL Adobe Media Optimizer (HTTP)]` 및 `[!UICONTROL Adobe Media Optimizer Batch Destination]`.

      [!DNL Media Optimizer] 은 의 이전 이름입니다. [!DNL Search].

   1. 각 대상에 대한 세그먼트를 지정합니다.

      사용 [!UICONTROL Automatically map all current and future segments] 선택 사항을 선택하면 모든 세그먼트가 매일 매핑되고 동기화됩니다.

      다음 [!UICONTROL Manually map segments] 옵션을 사용하면 세그먼트를 수동으로 매핑하여 배치 대상(`[!UICONTROL Adobe Media Optimizer Batch Destination]`). HTTP 대상에 수동으로 매핑할 필요는 없습니다.

1. 내 [!DNL Search]다음 중 한 [!DNL Search] 구현 팀이나 직접 액세스 클라이언트 관리자 역할을 가진 사용자는 다음에서 가져오기를 시작해야 합니다 [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Audience Manager Setup].

   조직의 Experience Cloud을 입력해야 합니다 [!DNL Organization ID] ([!DNL IMS org ID]). ID는 조직의 Audience Manager 계정에 사용된 ID와 동일해야 합니다.

### Audience Manager의 결과물은 무엇입니까?

조직은 두 개를 보게 됩니다 [!DNL Search] Audience Manager 대상:

* **[!UICONTROL Adobe Media Optimizer (HTTP)]**
* **[!UICONTROL Adobe Media Optimizer Batch Destination])**

## 데이터 동기화

처음 가져오는 데 24시간 정도 걸립니다. 초기 가져오기 후 데이터는 1~2초 지연으로 실시간으로 동기화됩니다.

<!--
### How DSP Syncs the Data

DSP syncs the data automatically using the [!DNL Adobe Experience Cloud Identity (ECID) Service]. During synchronization, the [!DNL ECID Service] calls Advertising Cloud at [!DNL cm.eversttech.net]. Because Advertising Cloud is a trusted domain, ID syncs take place from parent pages rather than within the destination publishing iframes, as they do with most third-party activation partners. Audience Manager identifies unique users by device IDs, using the [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html#global-device-ids), also called the [!DNL Device ID].
 
![Synchronization of [!DNL Adobe] audiences in DSP](/help/integrations/assets/audience-manager-sync.png)

### How Search Syncs the Data
-->

<!-- 
Segment membership data is sent only after one of the following events occurs:

* (Advertisers with DSP):

  * The segment is targeted in an Advertising Cloud display ad.

  * The segment is added to the [!DNL Adobe AdCloud Cross-Channel] batch and real-time destinations within the Audience Manager user interface.

* (Advertisers with [!DNL Search]):

  * The segment is targeted in an Advertising Cloud search ad.

  * The segment is added to the [!DNL Adobe Media Optimizer] batch and HTTP destinations within the Audience Manager user interface.
 -->
<!-- Is membership data/whatever available in Creative? If so, does it show the same as DSP? -->

## 동기화된 세그먼트를 찾을 위치

### DSP에서

DSP에서 세그먼트 이름은 Audience Manager 분류법에 의해 구성되며 다음의 해당 세그먼트 멤버십 수로 사용할 수 있습니다.

* [배치 설정](https://experienceleague.adobe.com/docs/advertising-cloud/dsp/campaign-management/placements/placement-settings.html?#audience-targeting): 설정 [!UICONTROL Adobe Segments] 의 탭 [!UICONTROL Audience Targeting] 섹션을 참조하십시오.

* in [대상 설정](/help/dsp/audiences/audience-settings.md): 설정 [!UICONTROL Adobe Segments] 탭.

### Advertising Cloud Creative에서

in [!DNL Creative]로 지정하는 경우 대상 노드의 경험 설정에서 세그먼트를 사용할 수 있습니다.

### in [!DNL Search]

in [!DNL Search]를 채울 때는 세그먼트를 [!DNL Google] 대상을 사용하여 [!UICONTROL Data Source] &quot;[!UICONTROL Adobe Audience]&quot; [!UICONTROL Campaigns] > [!UICONTROL Audiences] > [!UICONTROL Library].

각 [!DNL Google] 만드는 대상, [!DNL Google] 대상 크기를 제공합니다.

>[!MORELIKETHIS]
>
>* [Adobe Audience Manager과 Advertising Cloud 통합](/help/integrations/audience-manager/overview.md)

