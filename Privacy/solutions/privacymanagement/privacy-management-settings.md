---
title: 개인 정보 관리 설정 구성
f1.keywords:
- CSH
ms.author: v-jgriffee
author: jmgriffee
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
ms.collection:
- M365-security-compliance
- M365-privacy-management
search.appverid:
- MOE150
- MET150
description: 개인 정보 관리를 위한 전역 설정 옵션에 대해 자세히 알아보습니다.
ms.openlocfilehash: 662a3979a0b4fed87beb364fd658569bd6aab074
ms.sourcegitcommit: 85e085eb17af8b4efd1f45207445e1b3c3679600
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/19/2021
ms.locfileid: "60478332"
---
# <a name="configure-privacy-management-settings"></a>개인 정보 관리 설정 구성

화면의 오른쪽 위 모서리에 있는 기어 아이콘을 선택하여 개인 정보 관리에 대한 설정을 관리할 수 있습니다. 여기서 옵션을 사용하면 높은 수준의 기본 설정을 설정하고 주요 속성을 사용자 지정할 수 있습니다. 이 페이지에서는 기본 범주에 대한 설정 제공합니다.

## <a name="anonymization"></a>Anonymization

이 기능을 사용하면 개인 정보 관리 기능 내에서 특정 역할의 사용자에게 사용자 이름의 비동기화된 버전을 표시하는 데 사용할 수 있습니다. 중요한 데이터를 검토하는 동안 사용자의 ID를 마스킹할 수 있도록 식별 가능한 표시 이름을 일반 레이블로 대체합니다. 이 옵션은 주체 권한 요청 모듈에는 적용되지 않습니다.

## <a name="user-notification-emails"></a>사용자 알림 전자 메일  

개인 정보 관리의 정책을 사용하면 사용자 환경에서 잠재적인 개인 정보 위험을 평가하기 위한 매개 변수를 설정할 수 있습니다. 정책 일치가 감지되면 개인 정보 보호 관리에서 취할 수정 작업에 대한 권장 사항과 개인 정보 보호 교육 링크가 있는 전자 메일을 사용자에게 보낼 수 있습니다. 이 설정 개인 정보 관리의 전자 메일 알림 기능을 전체적으로 활성화 또는 비활성화할 수 있습니다. 전자 메일에서 알림 기능이 설정 모든 전자 메일이 사용하지 않도록 설정됩니다. 정책에 대한 자세한 내용은 정책 만들기 [및 관리를 참조합니다.](privacy-management-policies.md)

## <a name="teams-collaboration"></a>Teams 공동 작업  

개인 Microsoft Teams 기능을 통합하여 이해 관계자와의 공동 작업을 향상합니다. 주체 권한 요청을 만들 때마다 연결된 팀이 Teams. 사용자는 요청의 공동 작업자 탭에서 팀에 추가할 수 있습니다. 주체 권한 요청에 대한 자세한 내용은 주체 권한 요청 [관리를 참조합니다.](privacy-management-subject-rights-requests.md)

## <a name="data-matching"></a>데이터 일치  

이 섹션에서는 데이터 주체의 특성을 설명하는 데이터 스마마를 업로드할 수 있습니다. 이렇게 하면 데이터 주체 환경 내에서 개인 데이터를 검색할 때 올바른 데이터 주체가 식별될 Microsoft 365 있습니다. Schemas 및 규칙 패키지는 XML 형식으로 만들어 업로드됩니다. 개인 데이터 업로드에서 제공된 SCHEMA와 일치하는 개인 데이터를 제출할 수도 있습니다. 직접 파일을 만들고 업로드하거나 Azure에서 개인 데이터를 업로드할 수 있습니다. 주체 권한 요청에 대한 자세한 내용은 주체 권한 요청 [관리를 참조합니다.](privacy-management-subject-rights-requests.md)

## <a name="data-retention-periods"></a>데이터 보존 기간

이 설정은 주체 권한 요청과 관련이 있습니다. 요청을 닫은 후 생성한 수집된 데이터 및 보고서를 보존하려는 기간에 대한 기본 설정을 제어할 수 있습니다. 이 설정은 30일 또는 90일로 설정할 수 있습니다. 이러한 데이터 보존 기간이 정책 및 법적 의무를 준수하는지 확인하시기 바랍니다. 주체 권한 요청에 대한 자세한 내용은 주체 권한 요청 [관리를 참조합니다.](privacy-management-subject-rights-requests.md)

## <a name="data-review-tags"></a>데이터 검토 태그

주체 권한 요청에서 검색된 파일을 표시하는 데 사용할 태그를 관리합니다. 이러한 태그를 사용하여 수동으로 삭제해야 할 수 있는 콘텐츠와 같이 추가 주의가 필요한 콘텐츠를 나타낼 수 있습니다. 이 설정 섹션에서는 사용자 지정 태그의 이름과 설명을 편집할 수 있습니다. 시스템에서 제공하는 기본 제공 태그에 대한 태그 설명을 편집할 수도 있습니다. 시스템 태그의 이름은 변경할 수 없습니다. 주체 권한 요청에 대한 자세한 내용은 주체 권한 요청에 대한 데이터 검토 및 [공동 작업을 참조합니다.](privacy-management-subject-rights-requests-review.md#step-3-review-data)
