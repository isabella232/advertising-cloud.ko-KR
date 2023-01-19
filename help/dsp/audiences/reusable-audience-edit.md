---
title: 재사용 가능한 대상 편집
description: 재사용 가능한 대상을 편집하는 방법을 알아봅니다.
feature: DSP Audiences
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# 재사용 가능한 대상 편집

배치나 다른 재사용 가능한 대상에서 사용되는 대상을 편집하면 변경 사항이 해당 배치 및 대상에 즉시 적용됩니다.<!-- verify -->

1. 주 메뉴에서 **[!UICONTROL Audiences]>[!UICONTROL All audiences]**.

1. 대상 행 위에 커서를 놓고 **[!UICONTROL Edit]**.

1. 다음 방법 중 하나로 대상 설정을 편집합니다.

   >[!NOTE]
   >
   >대상 세그먼트 논리를 편집하는 경우 자세히 설명합니다. [대상 크기 데이터](audience-about.md) 이 오른쪽 패널에서 업데이트됩니다.

   * (선택 사항) **[!UICONTROL Audience Name]** click ![편집](/help/dsp/assets/edit.png) 대상 이름 옆에 고유한 대상 이름을 입력한 다음 을 클릭합니다 **[!UICONTROL Apply]**.

   * (선택 사항) [[!UICONTROL Third Party Segments], [!UICONTROL First Party Segments], [!UICONTROL Adobe Segments], [!UICONTROL Custom Segments], 및 [!UICONTROL Saved Audiences] 탭](audience-settings.md)를 눌러 다음을 수행합니다.

      * 기존 세그먼트 그룹에 세그먼트를 추가하려면:
      1. 오른쪽 패널에서 세그먼트 그룹을 클릭합니다.

      1. (선택 사항) 그룹 논리를 (으)로 변경합니다. *[!UICONTROL Include Any]*, *[!UICONTROL Include All]*, 또는 *[!UICONTROL Exclude All]*&#x200B;필요한 경우 ).

         *[!UICONTROL Exclude All]* 첫 번째 세그먼트 그룹에서 사용할 수 없습니다. 제외만 포함하는 대상의 경우, 이 대상을 다음으로 빌드하십시오. *[!UICONTROL Include Any]* 그런 다음 배치 내에서 제외된 대상 메뉴에서 해당 대상자를 선택합니다.

      1. 왼쪽 패널에서 새 세그먼트를 찾아 세그먼트 이름 옆에 있는 확인란을 선택합니다.

         세그먼트 그룹은 자동으로 새 세그먼트로 업데이트됩니다.
   * 새 세그먼트 그룹을 추가하려면:

      1. 클릭 **[!UICONTROL + New Group]** 오른쪽 패널에 표시됩니다.

      1. (선택 사항) 이전 그룹과 새 그룹 간의 논리를 (으)로 변경합니다 *[!UICONTROL And]* 또는 *[!UICONTROL Or]*&#x200B;필요한 경우 ).

      1. 왼쪽 패널에서 새 그룹의 세그먼트를 찾고 세그먼트 이름 옆에 있는 확인란을 선택합니다.

      1. (선택 사항) 그룹 논리를 (으)로 변경합니다. *[!UICONTROL Include Any]*, *[!UICONTROL Include All]*, 또는 *[!UICONTROL Exclude All]*&#x200B;필요한 경우 ).
   * 기존 대상의 세그먼트 로직을 사용하려면

      1. 다음 방법 중 하나로 기존 대상의 세그먼트 논리를 복사합니다.

         * 모든 대상 보기에서 대상 행 위에 커서를 놓고 **[!UICONTROL More]>[!UICONTROL Copy to Clipboard]**.

         * 기존 대상에 대한 설정의 세그먼트 논리 패널 상단에서 을 클릭합니다. **[!UICONTROL More]>[!UICONTROL Copy to Clipboard]**.

         * 텍스트 편집기에서 영숫자 세그먼트 ID와 [부울 구문](audience-segment-logic-syntax.md)를 클립보드에 복사합니다.
      1. 클릭 **[!UICONTROL paste in an audience rule to begin building]**&#x200B;기존 세그먼트 논리를 입력 필드에 붙여 넣은 다음 를 클릭합니다 **[!UICONTROL Apply]**.

         >[!NOTE]
         >
         >대상에 이미 세그먼트 로직이 포함되어 있는 경우 새 세그먼트 로직을 붙여 넣으면 기존 논리를 덮어씁니다.





1. 클릭 **[!UICONTROL Save]**.

1. 확인 메시지에서 **[!UICONTROL Continue]**.

>[!MORELIKETHIS]
>
>* [대상자 관리 기본 정보](audience-about.md)
>* [재사용 가능한 대상 만들기](reusable-audience-create.md)
>* [재사용 가능한 대상 복제](reusable-audience-duplicate.md)
>* [재사용 가능한 대상에 대한 세부 정보 보기](reusable-audience-view-details.md)
>* [재사용 가능한 대상 공유](reusable-audience-share.md)
>* [재사용 가능한 대상 내보내기](reusable-audience-export.md)
>* [재사용 가능한 대상에 대한 세그먼트 키를 클립보드에 복사합니다.](reusable-audience-clipboard.md)
>* [재사용 가능한 대상 삭제](reusable-audience-delete.md)
>* [대상 설정](audience-settings.md)
>* [대상 세그먼트 논리 구문](audience-segment-logic-syntax.md)
>* [사용 가능한 타사 데이터 공급자](third-party-data-providers.md)

