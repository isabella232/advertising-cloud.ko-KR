---
title: FAQ
description: xxx
source-git-commit: 2e0395dc1e5aa52adc83c1aaea49793fd5555390
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---

# FAQ xxx

## 제목

https://adobeadcloud.zendesk.com/agent/tickets/14214 기본적으로 Adobe Analytics은 모든 보고서에 캡처된 모든 이벤트를 보고합니다. &quot;[!UICONTROL Unspecified]&quot; 이벤트는 Advertising Cloud에 연결되어 있지 않은 양식 완료 이벤트를 나타냅니다. 예를 들어, 광고 플랫폼 보고서에서 이메일 캠페인에 의해 제어되는 유기 전환 또는 전환은 &quot;지정되지 않음&quot;으로 분류됩니다.

다음 &quot;지정되지 않음(없음) 포함&quot; 옵션으로 확인 표시를 제거하여 보고서에서 지정되지 않은 이벤트를 제거할 수 있습니다. <!-- Not sure if this is in DSP or in Analytics Workspace -->

## 제목

https://adobeadcloud.zendesk.com/agent/tickets/24323 Ad Cloud 픽셀과 동일한 지점에 Analytics 이벤트 태그를 지정하여 XXX가 일치하는지 확인하십시오.

## 제목

https://adobeadcloud.zendesk.com/agent/tickets/24323

Q: 내부 보안 감사 중에 특정 기능은 Ad Cloud을 기존 Adobe Analytics 설치에 통합할 때 활성화한 보안 우려로 플래그가 지정되었습니다.

문제의 통합은 AdCloud와 Adobe Audience Manager입니다. 이 기능은 AdCloud와 Adobe Audience Manager 간 방문자 ID에 대한 일치율을 높입니다. 이 작업은 pagead.l.doubleclick.net, star-mini.c10r.facebook.com 및 pug88000nf.pubmatic.com에 네트워크 요청을 전송하여 활용할 수 있는 방문자를 위한 기존 ID가 있는지 확인합니다. 보안 위험으로 플래그가 지정되고 모든 사이트 방문자에 대해 발생하는 네트워크 요청입니다.

Auditor가 이 기능을 비활성화하도록 요청하고 있습니다. 이러한 네트워크 요청을 차단하면 어떻게 됩니까?

A: Adobe는 제품과 함께 확인했으며, 해당 픽셀은 Ad Cloud, 특정 재고/SSP 파트너(DSP 관련) 및 AAM 간의 쿠키 일치율을 높이기 위한 목적이라고 언급했습니다.  해당 항목이 제거되면 고객은 AAC/AAM과 각 픽셀이 사용되는 인벤토리 파트너 간에 감소된 일치율 수준을 볼 수 있지만 큰 차이가 있을 것으로 예상하지는 않습니다.

Ad Cloud Search의 경우 광고주의 Experience Cloud 조직 ID가 Mattworks에 대해 설정되었지만 제품 팀에서는 Ad Cloud에서 대상을 활성화하기 위한 Mattworks 설정을 보지 않습니다. Ad Cloud Search로 대상을 전송하는 데 Audience Manager Adobe을 사용하고 있습니까? 그렇지 않은 경우 이러한 필드를 제거해도 현재 워크플로우에 영향을 주지 않습니다. AAM 고객 지원 센터에서 이러한 픽셀을 실행하지 않으려면 제거할 수 있습니다.

