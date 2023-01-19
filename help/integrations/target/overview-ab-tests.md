---
title: Adobe Target에서 Adobe 광고 광고에 대한 A/B 테스트 구성
description: 에서 A/B 테스트를 설정하는 방법을 알아봅니다 [!DNL Target] DSP 및 [!DNL Search] 광고.
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '1647'
ht-degree: 0%

---

# Adobe Target for Advertising DSP 및 [!DNL Advertising Search] 광고

<!-- Add [!UICONTROL and [!DNL tags throughout as needed. -->

<!-- Break into sub-files, or just leave as one? -->

*Advertising DSP만 사용하는 광고주*

Adobe 광고 및 Adobe Target을 사용하면 마케터가 유료 미디어 및 온사이트 메시징 간에 개인화되고 연결된 경험을 보다 쉽게 제공할 수 있습니다. 제품 간에 신호를 공유하여 다음 작업을 수행할 수 있습니다.

* DSP 캠페인에서 고객의 광고 노출을 온사이트 경험에 연결하여 사이트 폴스루 비율을 줄입니다.

* Adobe Audience Manager 노출 데이터 및 클릭-투-피드 Target 대상을 사용하여 광고 메시징으로 온사이트 경험을 미러링하여 A/B 테스트를 설정합니다.

* Adobe Analytics에서 간단한 시각화를 통해 온사이트 목표 상승도에 대한 통합 메시징이 미치는 영향을 측정합니다. [!DNL Target].

클릭스루 및 뷰스루 추적을 설정하고, DSP과 간 신호 공유를 구현하기 위한 사전 요구 사항 및 지침은 다음 섹션을 참조하십시오 [!DNL Target] A/B 테스트 활동을 설정하고, [!DNL Analytics] Analysis Workspace 를 클릭하여 테스트 데이터를 확인합니다.

추가 질문 사항은 adcloud_support@adobe.com으로 문의하십시오.

## 전제 조건

이 사용 사례를 사용하려면 다음 제품 및 통합이 필요합니다.

* [!DNL Target]

* [[!DNL Analytics] 광고](/help/integrations/analytics/overview.md) 통합<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] 대상 [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) 통합

* Audience Manager(뷰스루 테스트에만 필요)

## 1단계: 클릭스루 프레임워크 설정 {#click-through-framework}

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

![클릭스루 프레임워크](/help/integrations/assets/target-ct-framework.png)

클릭스루 URL(사용자가 광고를 클릭하여 랜딩 페이지에 도달하면 표시되는 URL)에 DSP 매크로를 추가하면 DSP은 을 포함하여 자동으로 배치 키를 캡처합니다 ```${TM_PLACEMENT_ID}``` ( 클릭스루 URL) 아래에 그룹화됩니다. 이 매크로는 숫자 배치 ID가 아니라 영숫자 배치 키를 캡처합니다.

![랜딩 페이지 URL에 추가된 클릭스루 URL입니다](/help/integrations/assets/target-ct-url.jpg)

### (DSP만 해당) 클릭스루 URL에 DSP 매크로 추가

<!-- If we ever write instructions for ads on other ad servers (such as Sizmek ads in DCO), then work that into the following section. -->

Flash 대화 또는 Google Campaign Manager 360 내에서 AMO ID 변수를 캡처하는 데 필요한 매크로를 포함하도록 각 광고의 클릭스루 URL을 수동으로 업데이트합니다. AMO ID 변수는 클릭 데이터를 Adobe Analytics으로 보내고 A/B 테스트를 위한 배치 키를 공유하는 데 사용됩니다. 지침이 필요하면 다음 페이지를 참조하십시오.

* [추가 [!DNL Analytics for Advertising] 매크로 [!DNL Flashtalking] 광고 태그](/help/integrations/analytics/macros-flashtalking.md)

* [추가 [!DNL Analytics for Advertising] 매크로 [!DNL Google Campaign Manager 360] 광고 태그](/help/integrations/analytics/macros-google-campaign-manager.md)

필요한 배치 키를 검색하고 설정을 완료하고 각 클릭스루 URL이 배치 키로 채워졌는지 확인하려면 DSP 계정 팀 및 광고 솔루션 그룹(aac-advertising-solutions-group@adobe.com)에 문의하십시오.

## 2단계: Audience Manager을 사용하여 뷰스루 프레임워크 설정 {#view-through-framework}

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

![뷰스루 프레임워크](/help/integrations/assets/targetr-vt-framework.png)

광고 태그 및 배치 설정에서 Audience Manager 노출 이벤트 픽셀을 추가하여 추가 뷰스루 테스트 기회를 위한 테스트 세그먼트를 만들 수 있습니다.

1. 광고 태그 및 DSP 배치 설정에서 Audience Manager 노출 이벤트 픽셀을 구현합니다.

   자세한 내용은 &quot;[Advertising DSP 캠페인에서 미디어 노출 데이터 수집](/help/integrations/audience-manager/media-data-integration/collect.md).&quot;

   추가 [DSP 매크로](/help/dsp/campaign-management/macros.md) 노출 이벤트 픽셀이 전달할 모든 데이터를 캡처하려면 다음을 포함합니다 `${TM_PLACEMENT_ID_NUM}` 를 입력합니다.

   >[!NOTE]
   >
   >클릭 추적 URL에는 다음이 포함됩니다 `${TM_PLACEMENT_ID}` 매크로 대신 영숫자 배치 키를 사용합니다. `${TM_PLACEMENT_ID_NUM}` 를 입력합니다.

1. DSP 노출 데이터에서 Audience Manager 세그먼트를 구성합니다.

   1. 이동 **Audience Manager** > **대상 데이터** > **신호**, 그런 다음 을(를) 선택합니다 **검색** 왼쪽 상단에 있는 탭입니다.

   1. 을(를) 입력합니다. **키** 및 **값** 는 세그먼트 사용자를 그룹화하는 수준을 결정하는 신호에 대해 입니다. 다음 작업 [지원되는 키](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html?lang=en) Audience Manager 노출 이벤트 픽셀에 추가한 매크로에 해당하는 값을 사용하여 값을 만듭니다.

      예를 들어 특정 배치에 대해 사용자를 그룹화하려면 `d_placement` 키. 값은 DSP 매크로에서 캡처된 실제 숫자 배치 ID(예: 위의 스크린샷에서 2501853)을 사용합니다 `${TM_PLACEMENT_ID_NUM}`. <!-- Explain where to find the placement ID, other than in a custom report. -->

      [총 카운트] 필드에 키-값 쌍에 대한 사용자 수가 표시됩니다. 이는 픽셀이 올바르게 배치되고 데이터가 흐르고 있음을 나타냅니다. 다음 단계를 계속 진행할 수 있습니다.
   ![신호 검색](/help/integrations/assets/target-am-signals.png)

1. [규칙 기반 트레이트 만들기](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) Audience Manager에서 세그먼트 생성을 위해 사용됩니다.

   1. 테스트 활동 내에서 쉽게 식별할 수 있도록 트레이트의 이름을 지정합니다. 원하는 폴더에 트레이트를 저장합니다.

   1. 에서 **데이터 소스** 드롭다운 메뉴에서 **Ad Cloud**.

   1. 표현식 빌더 내에서 를 추가합니다 ```d_event``` 키 필드에서 ```imp``` 에서 **값** 필드, 선택 **규칙 추가**, 그런 다음 트레이트를 저장합니다.

   ![규칙 기반 트레이트의 스크린샷](/help/integrations/assets/target-am-trait.png)

1. Audience Manager에서 테스트 세그먼트를 설정합니다.

   1. 페이지 상단에서 다음 위치로 이동합니다. **대상 데이터** > **트레이트** 전체 트레이트 이름을 검색합니다. 트레이트 이름 옆에 있는 확인란을 선택한 다음 를 클릭합니다 **세그먼트 만들기**.

   1. 세그먼트 이름을 지정하고 을 선택합니다. `Ad Cloud` 로서의 **데이터 소스**, 그런 다음 세그먼트를 저장합니다.

      Audience Manager은 세그먼트를 표준 랜딩 페이지 경험을 수신하는 제어 그룹과 개인화된 온사이트 경험을 받은 테스트 그룹으로 자동으로 분할합니다.
   ![테스트 세그먼트의 스크린샷](/help/integrations/assets/target-am-segment.png)

## 3단계: Target에서 &quot;A/B 테스트&quot; 활동 설정

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

다음 지침은 DSP 사용 사례와 관련된 정보를 강조 표시합니다. 전체 지침은 &quot;[A/B 테스트 만들기](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html)

1. [Adobe Target에 로그인](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. 에서 **활동** 목록, **활동 만들기** > **A/B 테스트**.

   ![A/B 테스트 활동 만들기](/help/integrations/assets/target-create-ab.png)

1. 에서 **활동 URL 입력*** 필드에서 테스트의 랜딩 페이지 URL을 입력합니다.

   ![활동 URL 필드 입력](/help/integrations/assets/target-create-ab-url.png)

   >[!NOTE]
   >
   >여러 URL을 사용하여 뷰스루 사이트 항목을 테스트할 수 있습니다. 자세한 내용은 &quot;[다중 페이지 활동](https://experienceleague.adobe.com/docs/target/using/experiences/vec/multipage-activity.html).&quot; 페이지 URL별로 최상위 항목을 만들기 위해 [사이트 시작 보고서](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/integrations/ad-cloud/create-advertising-cloud-site-entry-reports.html) 참조하십시오.

1. 에서 **목표** 필드에서 테스트에 대한 성공 지표를 입력합니다.

   >[!NOTE]
   >
   >확인 [!DNL Analytics] 는 내에서 데이터 소스로 활성화됩니다 [!DNL Target], 그리고 올바른 보고서 세트를 선택하는지 확인합니다.

1. 설정 **우선순위** to `High` 또는 `999` 테스트 세그먼트의 사용자가 사이트에서 잘못된 경험을 받을 때 충돌이 발생하지 않도록 합니다.

1. 내 **보고 설정**&#x200B;에서 을(를) 선택합니다. **회사 이름** 및 **보고서 세트** DSP 계정에 연결되었습니다.

   추가 보고 팁은 &quot;[보고 우수 사례 및 문제 해결](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html).&quot;

1. 에서 **날짜 범위** 필드에서 테스트에 대한 적절한 시작 및 종료 날짜를 입력합니다.

1. 활동에 대상 추가:

   1. 을(를) 선택합니다 [뷰스루 대상을 테스트하기 위해 Audience Manager에서 이전에 만든 세그먼트](#view-through-framework).

      ![활동에 대상 추가](/help/integrations/assets/target-create-ab-audiences.png)

   1. 선택 **사이트 페이지** > **랜딩 페이지** > **쿼리**&#x200B;를 입력한 다음, **값** 클릭스루 대상에 Target 쿼리 문자열 매개 변수를 사용하는 필드입니다.

      ![타겟 클릭 대상의 스크린샷](/help/integrations/assets/target-click-audience.jpg)

1. 대상 **트래픽 할당 방법**, 선택 **수동(기본값)** 대상자를 50/50.

1. 활동을 저장합니다.

1. 사용 [!DNL Target] [시각적 경험 작성기](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) A/B 테스트 랜딩 페이지 템플릿을 디자인하기 위해

   * 경험 A: 개인화 없이 기본/제어 랜딩 페이지 경험이므로 편집하지 마십시오.

   * 경험 B: 를 사용하십시오 [!DNL Target] 사용자 인터페이스를 사용하여 테스트에 포함된 자산(예: 제목, 복사, 단추 배치 및 크리에이티브)을 기반으로 랜딩 페이지 템플릿을 사용자 지정할 수 있습니다.
   >[!NOTE]
   >
   >예를 들어 크리에이티브 테스트에 대한 크리에이티브 테스트 사용 사례는 계정 팀에 문의하십시오.

## 4단계: 설정 [!DNL Analytics for Target] Analysis Workspace의 [!DNL Analytics]

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

[!DNL Analytics for Target] (A4T)는 광고주가 만들 수 있는 솔루션 간 통합입니다 [!DNL Target] 활동 기반 [!DNL Analytics] 전환 지표 및 대상 세그먼트를 사용한 다음 [!DNL Analytics] 를 보고 소스로 사용 해당 활동에 대한 모든 보고 및 세그멘테이션은 [!DNL Analytics] 데이터 수집.

에 대한 자세한 정보 [!DNL Analytics for Target]구현 지침에 대한 링크를 포함하여, 다음을 참조하십시오.[Adobe Target용 보고 소스로서의 Adobe Analytics(A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)&quot;.

### 설정 [!DNL Analytics for Target] 패널

Analysis Workspace에서 [!DNL Analytics for Target panel] 분석을 위해 [!DNL Target] 활동 및 경험. 보고서에 대한 다음의 중요한 정보와 정보를 기억하십시오.

#### 지표

* 테스트가 실행된 Adobe 광고 캠페인, 패키지 또는 배치와 관련된 작업 공간 내에서 패널을 만듭니다. 요약 시각화를 사용하여 Target 테스트 성과와 동일한 보고서에 Adobe 광고 지표를 표시할 수 있습니다.

* 온사이트 지표(방문 및 전환 등)를 사용하여 성능을 측정하는 데 우선 순위를 지정합니다.

* Adobe 광고(예: 노출 횟수, 클릭 수 및 비용)에서 집계된 미디어 지표는 Target 지표과 일치할 수 없음을 이해합니다.

#### Dimension

다음 차원은 [!DNL Analytics for Target]:

* **Target 활동**: A/B 테스트의 이름

* **Target 경험**: 활동 내에 사용된 랜딩 페이지 경험의 이름

* **Target 활동** > **경험**: 활동 이름과 경험 이름이 같은 행에 있습니다

### Analytics 문제 해결 [!DNL Target] 데이터

Analysis Workspace 내에서 활동 및 경험 데이터가 최소한으로 채워지지 않고 있는 것을 발견하면 다음을 수행하십시오.

* Target과 Analytics 모두에 동일한 SDID(Supplemental Data ID)가 사용되는지 확인합니다. 를 사용하여 SDID 값을 확인할 수 있습니다 [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html) 사용자를 유도하는 캠페인이 포함된 랜딩 페이지에서 을 클릭합니다.

[Adobe 디버거의 SDID(Supplemental Data ID) 값](/help/integrations/assets/target-troubleshooting-sdid.png)

* 동일한 랜딩 페이지에서 a) 솔루션 > Target 아래의 Adobe 디버거에 표시된 호스트 이름이 b)에 표시된 추적 서버와 일치하는지 확인합니다. [!DNL Target] 활동에 대해(목표 및 설정 > 보고 설정에서).

   [!DNL Analytics For Target] 를 사용하려면 [!DNL Analytics] 호출에서 전송할 추적 서버 [!DNL Target] 변환 후 [!DNL Modstats] analytics용 데이터 수집 서버.&lt;!— &quot;Analytics로&quot;>

[Adobe 디버거의 호스트 이름 값](/help/integrations/assets/target-troubleshooting-hostname.png)

[Target의 추적 서버 값](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## 추가 읽기

* [Analytics와 Target 통합](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html)- Analysis Workspace에서 Target 보고를 설정하는 방법을 설명합니다.
* [A/B 테스트 개요](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) - DSP 광고에 사용할 수 있는 A/B 테스트 활동에 대해 설명합니다.
* [경험 및 오퍼](https://experienceleague.adobe.com/docs/target/using/experiences/experiences.html) - 설명 [!DNL Target] DSP 테스트 사용자가 노출되는 온사이트 콘텐츠를 결정하는 도구입니다.
* [신호, 트레이트 및 세그먼트](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html) - DSP 뷰스루 테스트에 도움이 되는 Audience Manager 도구 중 일부를 정의합니다.
* [Analytics for Advertising 개요](/help/integrations/analytics/overview.md) - Analytics for Advertising을 도입하여 Analytics 인스턴스에서 클릭스루 및 뷰스루 사이트 상호 작용을 추적할 수 있습니다.

<!-- 
>[!MORELIKETHIS]
>
>* 
-->
