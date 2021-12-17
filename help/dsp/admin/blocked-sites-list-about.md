---
type: Documentation
cloud: Experience Cloud
solution: Advertising Cloud
product: advertising cloud
title: 계정 수준 및 광고주 수준의 차단된 사이트 목록 정보
description: 계정 수준 및 광고주 수준의 차단된 사이트 목록 정보
source-git-commit: ac35677ef4832177b7a7e735bbbbf24454371496
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---


# 계정 수준 및 광고주 수준의 차단된 사이트 목록 정보

<!-- Can you just add domains for your acct profile or advertiser to which you have access? It doesn't look like you can remove or edit any existing domains. Or can you with a specific syntax? -->

<!-- For domains, sub-domains,...? Specify what is valid. -->
전체 Advertising Cloud 계정에 사용되는 차단된 사이트 목록과 계정의 개별 광고주를 위한 추가 목록을 편집할 수 있습니다.

차단된 사이트 목록은 배치에 대해 제외할 대상 세트를 정의합니다. 각 목록은 최상위 웹 사이트 도메인과 모든 수준으로 구성될 수 있습니다 <!--- verify --> 하위 도메인(예: example.com, my.example.com 또는 my.new.example.com) 및 모바일 앱 이름(예: ???)<!-- package names/app IDs, the full URL in Google Play/iTunes? Specify what is valid. -->.

광고주 수준 목록은 계정 수준 목록을 무시합니다.

>[!NOTE]
>
>* 계정 수준 및 광고주 수준의 차단된 사이트 목록은 Advertising Cloud DSP 외에도 적용됩니다 [전역 차단 사이트 목록](/help/dsp/introduction/features/brand-safety-media-quality.md): 광고에는 안전하지 않다고 간주되는 사이트가 포함됩니다.
>* 사용자는 모든 배치에 타깃팅된 사이트를 추가할 수도 있습니다.
>* 차단된 사이트 목록은 항상 타깃팅된 사이트 목록을 무시합니다. 배치가 둘 다 제외되고 광고에 대해 동일한 타겟을 포함하는 경우 대상이 제외됩니다. <!-- Verify -->


>[!MORELIKETHIS]
<!--
>* [Edit an Account-level or Advertiser-level Blocked Site List](/help/dsp/admin/blocked-sites-list-edit.md)
[Brand Safety and Media Quality](/help/dsp/introduction/features/brand-safety-media-quality.md)
>* [Placement Settings](/help/dsp/campaign-management/placements/placement-settings.md)
-->
