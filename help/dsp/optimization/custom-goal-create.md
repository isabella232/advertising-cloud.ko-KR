---
title: 사용자 지정 목표 만들기
description: 사용자 지정 목표 만들기
feature: DSP Optimization
exl-id: 440ded21-92d3-41ad-839f-ebc8376aa932
source-git-commit: 8aea9eb1358e23a5b25e0353ced80c1550fa0057
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 0%

---

# 사용자 지정 목표 만들기

사용자 지정 목표를 *목표* Advertising Cloud Search 내에서 사용할 수 있습니다.

사용자 지정 목표를 만들려면 Advertising Cloud DSP 계정이 [!DNL Search] 내에서 동일한 Adobe Experience Cloud 조직 ID를 사용하는 계정 [!DNL Search] 클라이언트 설정. DSP 계정이 [!DNL Search] 계정, [!DNL Adobe] 계정 팀입니다.

>[!TIP]
>
>자세한 내용은 [사용자 지정 목표 생성에 대한 우수 사례](custom-goal-best-practices.md) 를 참조하십시오.

1. Advertising Cloud Search에 로그인(미국 회사) [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) 또는 (기타 모든 국가의 회사) [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com).
1. 목표에 포함할 지표가 추적되고, 제품에서 사용할 수 있으며, 표시 이름을 포함하는지 확인합니다.
   1. 주 메뉴에서 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Transaction Properties]**.
   1. 지표를 찾아 확인합니다 **[!UICONTROL Show in UI and Reports]** 이 지표에 대해 활성화되어 있습니다.
   1. 지표에 **[!UICONTROL Display Name]** 열에서 셀을 클릭하고 표시 이름을 입력한 다음 를 클릭합니다 **[!UICONTROL Apply].**
1. 사용자 지정 목표를 *목표*:
   1. 주 메뉴에서 **[!UICONTROL Search]> [!UICONTROL Optimization] >[!UICONTROL Objectives]**.
   1. 도구 모음에서 **[!UICONTROL Create objective].**
   1. 목표 설정을 입력합니다.
      1. 에서 **[!UICONTROL Change Objective Name]** 필드에서 목표 이름을 입력합니다.

         목표 이름은 [!UICONTROL Custom Goals] Advertising Cloud DSP 패키지 설정의 목록 .

      1. 속성과 목표 연결:

         >[!NOTE]
         >
         > 광고주에 대해 추적된 모든 거래 속성은 기본적으로 [!UICONTROL Available Properties] 목록.

         * 속성 및 가중치가 있는 CSV 파일을 가져오려면 **[!UICONTROL Import]** 가져올 파일을 찾습니다.

            가져온 속성은 광고주용으로 이미 있어야 합니다. 이름은 대/소문자를 구분하지 않습니다.

            가져온 속성은 지정된 기존 속성을 대체합니다.

         * 기본 가중치(1)로 첫 번째 속성을 수동으로 지정하려면 광고주용으로 추적된 모든 거래 속성 목록에서 를 선택합니다.

         * 기본 가중치(1)로 다른 속성을 수동으로 추가하려면 **[!UICONTROL +]** .

            >[!TIP]
            >
            > 목록에서 속성을 검색하려면 속성 이름 내의 아무 곳에나 문자열을 입력합니다.

         * 여러 속성을 수동으로 추가하려면 **[!UICONTROL Add Multiple Properties].** 추가할 각 속성에 대해 [!UICONTROL Available Properties] 열을 끌어서 [!UICONTROL Added Properties] 열. 속성 추가를 마치면 를 클릭합니다. **[!UICONTROL Add]**.

            >[!TIP]
            >
            >* 목록에서 속성을 검색하려면 입력 필드의 속성 이름 내 아무 곳에나 문자열을 입력합니다.
            >* 보고서에서 제외된 속성을 제외하도록 목록을 필터링하려면 옵션을 선택합니다 **[!UICONTROL Hide properties excluded from reports].**


         * 목표에 여러 속성이 포함된 경우) 대상의 다른 속성에 상대적인 속성의 가중치를 변경하려면 **[!UICONTROL Weight]** 필드.
      1. 설정 아래쪽에서 **[!UICONTROL Save]**.


일단 목표를 만들면, 최적화 목표가 &quot; &quot;일 때 Advertising Cloud DSP 패키지에 사용자 지정 목표로 할당할 수 있습니다.[!UICONTROL Highest ROAS - Custom Goal]&quot; 또는 &quot;[!UICONTROL Lowest CPA - Custom Goal].&quot;

>[!TIP]
>
>최적의 성능을 위해 사용자 지정 목표(목표)에 있는 결합된 지표는 하루에 최소 10개의 전환을 완료해야 합니다. 코드가 포함되어 있지 않으면 제품 페이지나 애플리케이션이 시작되는 등의 지원 이벤트(트랜잭션 속성)를 목표에 추가하는 것이 좋습니다. 자세한 내용은 [사용자 지정 목표 구축에 대한 우수 사례](custom-goal-best-practices.md) 참조하십시오.

>[!MORELIKETHIS]
>
>* [사용자 지정 목표](custom-goal-about.md)
>* [사용자 지정 목표 구축에 대한 우수 사례](custom-goal-best-practices.md)
>* [최적화 목표 및 사용 방법](optimization-goals.md)
>* [패키지 설정](/help/dsp/campaign-management/packages/package-settings.md)
> * [DSP이 캠페인을 최적화하는 방법](optimization-how-dsp-optimizes-campaigns.md)

