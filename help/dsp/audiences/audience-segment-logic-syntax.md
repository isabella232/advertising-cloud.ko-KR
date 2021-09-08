---
title: 대상 세그먼트 논리 구문
description: 대상 세그먼트에 대한 논리를 정의하는 데 사용할 수 있는 구문을 참조합니다.
feature: Audiences
exl-id: 3a51b1b5-1eef-453b-9be5-0694e27491a8
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# 대상 세그먼트 논리 구문

재사용 가능한 대상을 만들 때 영숫자 세그먼트 ID와 다음 구문을 사용하여 세그먼트 논리를 수동으로 정의할 수 있습니다.

* () 그룹을 나타냅니다.
* `||` 대상  [!DNL OR] <!-- || escaped with backticks so Jenkins doesn't think it's a Markdown table -->
* [!DNL AND]에 대해 &amp;&amp;
* ! [!DNL NOT]에 대해(제외)

>[!NOTE]
>
>* 지정된 세그먼트 그룹은 앞에 오는 경우가 아니면 모두 포함됩니다! (제외됨)


예를 들어 다음 논리가 있습니다.

```
(X5vUk1cNvZxvBJ3jMjTt) || (sfvXrmQkk77PL5OtHpLH) && !(SMWSjTZFiy9hR1bKm1vw || x08UReA0IcP9HAJdcGVe)
```

mean(일반 영어)

```
[!DNL INCLUDE] Segment ID X5vUk1cNvZxvBJ3jMjTt [!DNL OR] INCLUDE Segment ID sfvXrmQkk77PL5OtHpLH [!DNL AND EXCLUDE] (Segment ID SMWSjTZFiy9hR1bKm1vw AND Segment ID x08UReA0IcP9HAJdcGVe)
```

>[!NOTE]
>
>배치 설정에서 저장된 대상을 대상으로 사용하여 명시적으로 타깃팅하거나 타깃팅에서 제외할 별도의 대상으로 사용할 수 있습니다. 세그먼트 로직이 대상을 사용할 목적을 반영하는지 확인하십시오.

>[!MORELIKETHIS]
>
>* [대상자 관리 기본 정보](audience-about.md)
>* [재사용 가능한 대상 만들기](reusable-audience-create.md)
>* [대상 설정](audience-settings.md)
>* [사용 가능한 타사 데이터 공급자](third-party-data-providers.md)

