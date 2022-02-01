---
title: '[!UICONTROL Simple Ad Serving] 거래 설정'
description: 에 사용 가능한 설정에 대해 알아보기 [!UICONTROL Simple Ad Serving] 거래.
feature: DSP Simple Ad Serving
source-git-commit: b40c6f08b94e546e5fc068c46b279292a4d8a14f
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 0%

---

# [!UICONTROL Simple Ad Serving] 거래 설정

## 새로 만들기 [!UICONTROL Simple Ad Serving] 딜

### [!UICONTROL Select Ad Source]

| 매개 변수 | 설명 |
|-----------|-------------|
| **[!UICONTROL Serving Type]** | 이 거래의 미디어 유형: *[!UICONTROL Video],* *[!UICONTROL Display],* 또는 *[!UICONTROL Audio].* |
| **[!UICONTROL Publisher Site Served On]** | 이 인벤토리를 판매하는 게시자의 이름입니다. 이름에 처음 두 문자 이상을 입력하여 게시자를 검색합니다. 목록에 없는 게시자를 추가하려면 [!DNL Adobe] 계정 팀입니다. |
| **[!UICONTROL Advertiser]** | 이 거래에 액세스할 수 있는 계정의 단일 광고주입니다. 또한 캠페인과 거래를 사용할 수 있는 패키지를 선택합니다(선택적). |
| **[!UICONTROL Media Quality Assessment?]** | (일부 사용자) 타사 확인을 위해 다른 DSP에서 광고를 실행할 수 있도록 합니다. <!-- Who can select this? It's disabled for me. Need to see if there are additional fields when this is enabled. --> |
| **[!UICONTROL Ad Source]** | 유일한 옵션은 다음과 같습니다 *[!UICONTROL Site Serve (Event Pixels)]*. |
| **[!UICONTROL Ad Creation]** | (새 거래만 해당) 다음 중 어느 것을 수행할 것인지 여부:<ul><li>*[!UICONTROL Create New]:* 이 거래에 대한 광고를 만들려면</li><li>*[!UICONTROL Select Ads]:* 이 거래에 기존 광고를 사용하려면</li></ul> |
| **[!UICONTROL Ad Type]** | 이 거래의 광고 유형입니다. 거래에 대한 새 광고를 만들려면 요청된 대로 광고 크기나 기간을 포함하십시오. 사용 가능한 옵션은 미디어 유형에 따라 다릅니다. |

{style=&quot;table-layout:auto&quot;}

### [!UICONTROL Select Ad(s)]

(기존 광고를 사용하는 경우) 거래에 포함할 광고입니다. 포함할 각 광고 옆에 있는 확인란을 선택합니다.

### [!UICONTROL Select & Upload [Media Type]]

(새 광고만 해당) 새 광고를 만드는 화면 [자사 광고](/help/dsp/campaign-management/ads/ad-create.md) 또는 [타사 광고](/help/dsp/campaign-management/ads/ad-create-third-party.md).

### [!UICONTROL Feed Details]

| 매개 변수 | 설명 |
|-----------|-------------|
| **[!UICONTROL Media CPM]** | 계약에 대한 비율 카드에 반영되는 천 단위 노출 횟수(CPM)의 비용입니다. 다음 사항에 문의하십시오. [!DNL Adobe] 이 값에 대한 계정 팀입니다. <br><br>거래의 통화도 지정합니다. 모든 사용자는 USD를 선택하거나, SSP가 추가 통화를 지원하는 경우 DSP 계정의 통화를 선택할 수 있습니다. |
| **[!UICONTROL Third Party Billed Fees]** | (선택 사항) 청구 불가능한 원가로 추적되는 정적 타사 수수료 및 거래에 대한 통화입니다.<br><br>모든 사용자는 USD를 선택하거나, SSP가 추가 통화를 지원하는 경우 DSP 계정의 통화를 선택할 수 있습니다. **참고:** 청구 가능한 수수료는 [!UICONTROL Net CPM] 지표. |
| **[!UICONTROL Third Party Fee Description]** | (선택 사항) 타사 요금에 대한 설명입니다. |
| **[!UICONTROL Flight Dates]** | 이 거래를 사용하는 트래픽의 시작 및 종료 날짜입니다. 비행 날짜는 캠페인 비행 날짜 내에 포함되어야 합니다. 광고 태그는 지정된 비행 중에만 응답을 반환합니다.<br><br> 가장 좋은 방법은 1년 동안 지속되는 별도의 간단한 광고 서비스 캠페인을 만들고 그 안에서 추적 픽셀을 빌드하는 것입니다. |
| **[!UICONTROL Impressions]** | (선택 사항) 이 거래를 사용하여 실행할 예상 노출 횟수입니다. 이 값은 추적 목적으로만 사용되며 게재 목표가 충족될 때 플래그를 지정합니다. 게시자가 실제 광고 배달을 제어합니다. 가장 좋은 방법은 많은 노출 횟수를 입력하여 DSP 내에서 태그를 활성화하여 필요한 경우 갱신하거나 연장할 수 있는 것입니다. |
| **[!UICONTROL Deal Name]** | 거래 이름 이름을 입력하거나 *[!UICONTROL Auto Generate Deal Name]* 를 입력하여 DSP에서 거래 세부 사항을 기반으로 이름을 생성할 수 있습니다.<br><br>자동 생성된 이름의 예: `Campaign-desktop_video_preroll_15-24Kitchen-$10_USD-jdoe-SAS` |
| **[!UICONTROL Attached Ads]** | (읽기 전용) 거래의 일부인 광고. 광고를 편집하려면 광고 이름을 클릭합니다. 광고에서 광고를 제거하려면 **[!UICONTROL X]** 광고 이름 옆에 표시됩니다. |

{style=&quot;table-layout:auto&quot;}

<!-- 
## Existing Simple Ad Serving Deals

Changes aren't applied retroactively.
-->

<!-- completely different settings layout, so need a separate section for them -->

<!-- From Abhinav: Editable fields are Name, Start & End date, Impressions & CPM. Changes are not applied retroactively.

But I see:

| Parameter | Description |
|-----------|-------------|

| **[!UICONTROL Are you using Deal ID?] | (Read-only) Whether the deal was set up as a [!UICONTROL Deal ID] (*[!DNL Yes]*)  or a [!UICONTROL Simple Ad Serving] deal (*[!DNL No]*). |
| **[!UICONTROL Inventory Type] | (Read-only) The inventory type for the deal. |
| **[!UICONTROL Feed Name] | The name of the [!UICONTROL Simple Ad Serving] deal. |
| **[!UICONTROL Publisher Ad Server] | (Read-only)  |
| **[!UICONTROL Publisher maximum ad length] | The maximum length of the ad, per the publisher. |
| **[!UICONTROL Publisher minimum ad length] | The minimum length of the ad, per the publisher. |
| **[!UICONTROL Fill Type] | (Read-only)  |
| **[!UICONTROL Contracted CPM] | This field is required if billing through TubeMogul, but enter your CPM in this field to track your actual spend. |
| **[!UICONTROL 3rd party technology CPM] | (Optional)  |
| **[!UICONTROL Planned Flight Dates] | The beginning and end dates for the deal flight. These dates don't control ad delivery but are used to track delivery pacing. **THIS IS CONTRARY TO WHAT THE NEW DEAL SETTINGS ABOVE, FROM ABHINAV, SAY**> |
| **[!UICONTROL Target Impressions] | (Optional) The estimated number of impressions you expect to run using this deal. This value is used for tracking purposes only and to flag when delivery goals are met; the publisher controls actual ad delivery. The best practice is to enter a high number of impressions to keep the tag active within DSP so it can be renewed or extended if needed. |
 -->

>[!MORELIKETHIS]
>
>* [정보 [!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* [만들기 [!UICONTROL Simple Ad Serving] 거래](simple-deal-create.md)
>* [이벤트 추적 픽셀 보기 [!UICONTROL Simple Ad Serving] 거래](simple-deal-show-pixels.md)

