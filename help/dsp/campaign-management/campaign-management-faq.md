---
title: Campaign Management에 대한 FAQ
description: 변경 지연 기간 및 비행 중 예산 변경 시 발생하는 사항 등 캠페인 관리에 대해 자세히 알아보십시오.
feature: DSP Packages, DSP Placements
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---

# Campaign Management에 대한 FAQ

<!-- Most of this information should be moved into the relevant topics (especially editing topics). -->

## 설정 변경 지연

* 배치 또는 패키지 설정을 변경할 때 변경 사항은 언제 적용됩니까?

   설정 변경 사항은 일반적으로 즉시 적용되지만 최대 12시간이 걸릴 수 있습니다.

   배달이 마지막 날이라면, DSP이 그 변경을 기반으로 패키지를 재구성할 시간이 충분하도록 일찍 변경하세요. 예를 들어, 게재 간격 게재 간격 게재 시간에서까지 변경할 경우, DSP은 나머지 비행 동안 지출을 분배하는 방법을 재평가해야 합니다. 마지막 날 배달할 시간이 1시간 밖에 남지 않았다면 그런 종류의 변경을 하지 마세요.

## 중간 비행 예산 갱신

* 배치를 변경할 때 DSP이 패키지 예산을 재할당하는 데 얼마나 걸립니까?

   예산 할당은 배치 성과를 기반으로 하며, 14일 평균을 사용하여 평가됩니다. 배치를 변경하면 예산 할당이 14일 평균 동안 성과 변화를 일으킬 때만 변경됩니다.

   성능 변경 사항이 발생하면 DSP은 캠페인의 시간대에서 자정(00:00)에 발생하는 다음 예산 최적화 주기 동안 그에 따라 배치 중 패키지 예산을 재할당합니다.

* 패키지에서 배치를 제거하고 다른 패키지에 추가할 때 예산이 어떻게 재할당됩니까?

   배치의 전체 지출 내역이 배치에 첨부되어 패키지에서 패키지로 이동합니다.

   패키지에서 배치를 제거해도 패키지에 배치 지출 내역이 더 이상 없습니다. 패키지 예산은 (패키지 예산 - 제거된 배치 예산) / 비행 중 남은 시간 간격이 됩니다. 그런 다음 패키지 예산이 패키지에 남아 있는 배치에 할당됩니다.

   마찬가지로, 동일한 배치를 다른 패키지에 추가하는 경우 DSP은 새 패키지의 모든 배치에 대한 예산을 할당할 때 배치의 지출 내역을 고려합니다.

* 비행기 마지막 날 소포가 어떻게 달라지나요?

   비행기 마지막 날에, 패키지 예산이 초과되지 않도록 24시간에서 23시간으로 단축됩니다. 또한 패키지의 간격 채우기 전략은 자동으로 &quot;[!UICONTROL Frontload],&quot;로 설정되어 있어도[!UICONTROL even].&quot; 하루 평균 65%의 예산이 오전 11시 30분까지 배달된다는 뜻이다.

>[!MORELIKETHIS]
>
>* [패키지 설정](/help/dsp/campaign-management/packages/package-settings.md)
>* [배치 설정](/help/dsp/campaign-management/placements/placement-settings.md)
>* [성능 캠페인 설정에 대한 우수 사례](/help/dsp/optimization/campaign-best-practices-performance.md)

