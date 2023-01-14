---
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 0%

---
# Adobe 광고를 위한 공동 작업 설명서

제품 간 및 DSP 문서를 포함하여 Adobe 광고를 위한 설명서 저장소입니다. (나중에 검색에 대한 문서가 포함되며(?) (광고 문구)

**참고: 이 페이지는 고객 관련 설명서에 게시되지 않습니다.**

## TOC

+ `TOC.md` 사용 안내서의 루트에 있는 는 안내서에 포함된 주제 구성을 제공합니다.
+ 각 사용 안내서에는 고유한 가 있습니다 `TOC.md`필요한 경우 모든 페이지/주제를 정렬할 수 있습니다.


## 사용 안내서

+ 사용 안내서 소개는 라고 합니다. `overview.md`
+ 사용 안내서의 각 주제에는 고유한 디렉토리가 있습니다.
   + 안내서에 라는 주제가 있으면 *구현*&#x200B;를 지정하는 경우 해당 디렉토리가 입니다. `/implementation`
+ 모든 이미지 자산은에 저장됩니다. `/assets` 를 클릭합니다.
   + 의 모든 이미지 `/assets` 디렉터리가 현지화됩니다.
   + 의 모든 이미지 `/no-localize` 디렉토리가 현지화되지 않습니다. loc 버전에서 특정 자산이 불필요하게 재생되지 않는지 확인하는 데 사용할 수 있습니다.

## 사용 안내서 수준 메타데이터

+ 사용 안내서를 설명하는 메타데이터는 `TOC.md`. 여기에는 다음이 포함됩니다.
   + product - 제품/기능의 이름.
   + cloud - 이 제품이 속한 클라우드.
   + audience - 안내서가 타깃팅된 대상 또는 원형.
   + user-guide - 사용 안내서의 이름.

## 페이지 수준 메타데이터

+ 문서를 설명하는 데 필요한 메타데이터는 각 개별 페이지의 일부로 저장됩니다. 여기에는 다음이 포함됩니다.
   + title - 페이지의 제목
   + 설명 - 페이지 설명
   + seo-title - seo 대체 제목
   + seo-description - SEO 목적의 대체 제목
   + short-title - (선택적 필드)
   + index - yes / no - 페이지가 Adobe의 검색 플랫폼으로 인덱싱됨
   + 번역 - 예 / 아니요 - 이 페이지를 현지화합니까?
   + beta - 제품이 베타 버전입니까?
   + 리디렉션 - 필요한 경우 새 페이지에 대한 참조를 만드는 데 사용할 수 있습니다.
   + doc-type: 참조(기본값) / 문제 해결 / 개발자 / 자습서 / kb / 백서

## 추가 정보

자세한 게시 지침, 스타일 안내서, 샘플 및 기타 리소스는 다음을 참조하십시오.

+ [기여 작성자 지침 **Adobe 광고용**](https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=EfficientFrontier&amp;title=Contributing+Author+Guidelines+for+Advertising+Cloud+Help)
+ [모든 Adobe 작성자를 위한 공동 작성](https://experienceleague.adobe.com/docs/authoring-guide-exl/using/home.html)

다음을 참조하십시오.

+ contributing.md 설명서 기여 방법에 대한 개요입니다.

<!-- * guidelines.md For an overview on what is expected in contributions and how to compose your documentation contributions. -->
+ code-of-conduct.md 이 설명서 프로젝트에 기여할 때 저희 팀에서 기대하는 활동 표준에 대한 개요입니다.
