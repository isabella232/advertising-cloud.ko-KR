---
title: 배치 수준 사전 입찰 필터 및 사용 방법
description: 사용 가능한 배치 수준 사전 입찰 필터를 참조하여 사용 방법을 확인합니다.
feature: DSP Optimization
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 0%

---

# 배치 수준 사전 입찰 필터 및 사용 방법

| 사전 입찰 필터 | 설명 | 이 필터를 사용해야 하는 경우 |
| ---------------| ----------- | ---------------------- |
| [!UICONTROL Click Through Rate] | 경매가 클릭스루로 이어질 가능성에 대한 최소 예측 임계값을 설정합니다. 예를 들어 임계값을 0.1%로 설정하면, 클릭 예상 확률이 0.1%보다 크거나 같은 경우가 아니면 경매에 입찰하지 않습니다.<br><br><b>참고:</b> 최적화 목표 전에 필터가 적용됩니다. 따라서 매우 엄격한 필터가 비용을 방지할 수 있습니다. | CTR(클릭스루 비율)에 대한 최소 KPI 목표가 있고 CTR이 임계값 미만인 경우 예산을 지출하지 않으려는 경우에 사용합니다. 이 필터는 매우 제한적일 수 있으므로 실제 목표를 설정하는 것이 중요합니다. 배치에 대한 다른 제한 사항에 따라 .03-.07%의 목표는 일반적으로 좋은 시작점입니다. 지표를 향상시키는 데 도움이 되는 필요에 따라 사이트 수준에서 최적화할 수 있습니다.<br><br>최소 CTR과 가장 적합한 CPM을 달성하는 것이 목표라면, 권장되는 설정은 를 결합하는 것입니다 [!UICONTROL Click Through Rate] 최적화 목표 &quot; 를 사용하여 필터링[!UICONTROL Lowest CPM].&quot; 목표가 초과 달성하는 데 실제 이점이 없는 최대 CPM이고 최소 CTR인 경우 를 페어링합니다 [!UICONTROL Click Through Rate] 최적화 목표 &quot; 를 사용하여 필터링[!UICONTROL Always Max Bid + Highest CTR]&quot;가 더 적절할 수 있습니다. |
| [!UICONTROL 100% Completion Rate] | 노출에 입찰하기 전에 충족해야 하는 필수 최소 완료율을 설정합니다. | 캠페인의 기본 목표가 완료율일 때 이 필터를 사용하십시오. 다른 타깃팅 매개 변수의 계수는 65%이지만 권장되는 시작 비율은 65%입니다. |
| [!UICONTROL Player Size - Adobe] | DSP의 데이터를 사용하여 필요한 최소 플레이어 크기를 설정합니다. 당신은 이 [!UICONTROL Player Size] 임계값이 충족됩니다. | DSP의 데이터를 사용하여 전체 에피소드 플레이어 인벤토리를 게재할 때 사용합니다. |
| [!UICONTROL Player Size 3rdParty (Moat/IAS)] | 의 데이터를 사용하여 필요한 최소 플레이어 크기를 설정합니다. [!DNL Moat] 또는 [!DNL Integral Ad Science] ([!DNL IAS]). 당신은 이 [!UICONTROL Player Size] 임계값이 충족됩니다. | 플랫폼 전체를 사용하여 전체 에피소드 플레이어 인벤토리를 게재하고 있는지 확인하려면 을 사용하십시오 [!DNL Moat] 또는 [!DNL IAS] 데이터.<br><br><b>참고:</b> 이 필터는 캠페인이 [!DNL Moat] 또는 [!DNL IAS] 데이터. |
| [!UICONTROL Viewability Adobe (MRC or [!DNL GroupM])] | DSP 뷰가능 번호 및 측정을 사용하여 필요한 최소 뷰가능 비율을 설정합니다. 지정된 임계값이 충족되면 노출에 입찰합니다.<br><br><b>참고:</b><ul><li>캠페인이 [!UICONTROL Viewability Sensitivity] 설정[!UICONTROL Standard (50% of ad in view for 2 consecutive seconds)],&quot; [!DNL Media Rating Council] (MRC) 뷰성 측정 표준이 캠페인에 사용됩니다. 만약 [!UICONTROL Viewability Sensitivity] 설정[!UICONTROL Strict (100% of ad in view & audio on for 50% duration)],&quot; [!DNL GroupM] 캠페인에 뷰기능 측정 표준이 사용됩니다.</li><li>Adobe 측정 정의가 타사 정의와 다르므로 타사 데이터와 약간 일치하지 않을 수 있습니다.</li></ul> | 가장 좋은 방법은 최적화 목표 및 모든 사전 입찰 필터 설정을 캠페인의 설정과 일치시키는 것입니다 [!UICONTROL Viewability Sensitivity] 설정 |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [DSP이 캠페인을 최적화하는 방법](optimization-how-dsp-optimizes-campaigns.md)
>* [패키지 설정](/help/dsp/campaign-management/packages/package-settings.md)
>* [배치 설정](/help/dsp/campaign-management/placements/placement-settings.md)
>* [캠페인 설정](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [최적화 목표 및 사용 방법](optimization-goals.md)

