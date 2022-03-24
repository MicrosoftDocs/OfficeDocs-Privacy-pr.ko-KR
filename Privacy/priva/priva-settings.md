---
title: Priva 설정 구성
f1.keywords:
- CSH
ms.author: chvukosw
author: chvukosw
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
ms.collection:
- M365-security-compliance
- M365-priva-subject-rights-requests
- M365-priva-privacy-risk-management
search.appverid:
- MOE150
- MET150
description: Microsoft Priva의 전역 설정 옵션에 대해 자세히 알아보습니다.
ms.openlocfilehash: 1cbb508d8c1dd98dfa846595d81e8aaeecdbaeb4
ms.sourcegitcommit: 02921b2dd438a517191522567908046b136a89e2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63758427"
---
# <a name="configure-priva-settings"></a>Priva 설정 구성

화면의 오른쪽 위 모서리에 있는 기어 아이콘을 선택하여 Microsoft Priva의 설정을 관리할 수 있습니다. 여기서 옵션을 사용하면 높은 수준의 기본 설정을 설정하고 주요 속성을 사용자 지정할 수 있습니다. 이 페이지에서는 기본 범주에 대한 설정 제공합니다.

## <a name="anonymization"></a>Anonymization

개인 정보 보호 위험 관리 기능 내에서 특정 역할의 사용자에게 사용자 이름의 비동기화된 버전을 표시 할 수 있습니다. Anonymization feature replaces identyable display names with a generic label to help mask your users'identities while reviewing sensitive data. 이 옵션은 주체 권한 요청 솔루션에는 적용되지 않습니다.

## <a name="user-notification-emails"></a>사용자 알림 전자 메일  

개인 정보 보호 위험 관리의 정책을 사용하면 사용자 환경에서 잠재적인 개인 정보 위험을 평가하기 위한 매개 변수를 설정할 수 있습니다. 정책 일치가 감지되면 개인 정보 보호 위험 관리는 취할 수정 작업에 대한 권장 사항과 개인 정보 보호 교육 링크가 있는 전자 메일을 사용자에게 보낼 수 있습니다. 이 **설정** 개인 정보 위험 관리의 전자 메일 알림 기능을 전체적으로 활성화 또는 비활성화할 수 있습니다. 알림 기능을 사용하지 않도록 설정한 설정 모든 전자 메일이 사용하지 않도록 설정됩니다. 정책에 대한 자세한 내용은 [Create policies in Privacy Risk Management를 참조합니다](risk-management-policies.md).

## <a name="teams-collaboration"></a>Teams 공동 작업  

사용자 Microsoft Teams 권한 요청과 통합하여 이해 관계자와의 공동 작업을 향상합니다. 주체 권한 요청을 만들 때마다 연결된 팀이 Teams. 사용자는 요청의 공동 작업자 탭에서 팀에 추가할 수 있습니다. 주체 권한 요청에 대한 자세한 내용은 [Priva Subject Rights Requests에 대해 자세히를 참조합니다](subject-rights-requests.md).

## <a name="data-matching"></a>데이터 일치  

이 섹션에서는 데이터 주체의 특성을 설명하는 데이터 스마마를 업로드할 수 있습니다. 이 기능을 통해 데이터 환경 내에서 개인 데이터를 검색할 때 올바른 데이터 주체가 식별될 Microsoft 365 있습니다. Schemas 및 규칙 패키지는 XML 형식으로 만들어 업로드됩니다. 개인 **데이터 업로드에서** 제공된 SCHEMA와 일치하는 개인 데이터를 제출할 수도 있습니다. 직접 파일을 만들고 업로드하거나 Azure에서 개인 데이터를 업로드할 수 있습니다. 주체 권한 요청에 대한 자세한 내용은 [Priva Subject Rights Requests에 대해 자세히를 참조합니다](subject-rights-requests.md).

## <a name="data-retention-periods"></a>데이터 보존 기간

이 설정은 Priva Subject Rights Requests와 관련이 있습니다. 이를 통해 요청이 닫힌 후 수집된 데이터 및 보고서를 보존하려는 기간에 대한 기본 설정을 제어할 수 있습니다. 이 설정은 30일 또는 90일로 설정할 수 있으며 만든 모든 주체 권한 요청에 적용됩니다. 데이터 보존 기간이 조직의 정책 및 법적 의무를 준수하는지 확인하는 것이 좋습니다. 자세한 내용은 주체 권한 [요청에 대한 데이터 보존 설정에 대해 자세히 알아보아야 합니다](subject-rights-requests-reports.md#manage-data-retention).

## <a name="data-review-tags"></a>데이터 검토 태그

데이터 검토 태그를 사용하여 주체 권한 요청에서 검색된 콘텐츠 항목을 표시하는 데 사용할 수 있습니다. 이 설정 영역을 사용하면 태그를 관리할 수 있습니다. Priva는 추가 **관리, 삭제** **및 업데이트** 의 세 가지 기본 태그를 **제공합니다**. 이러한 태그 이름은 편집할 수 없지만 조직에 의미 있는 이러한 태그에 대한 설명을 제공할 수 있습니다.

또한 Priva는 조직의 사용에 대해 이름을 지정하고 정의할 수 있는 두 개의 사용자 지정 태그를 제공합니다. 이름을 편집할 때까지 사용자 지정 태그 **1** 및 사용자 지정 태그 **2** 로 나열됩니다.

태그 이름 및 설명을 편집하려면 아래 단계를 따르세요.

- Priva **설정** 페이지에서 데이터 검토 **태그를 선택합니다**.
- 편집할 목록에서 태그를 찾아 이름 옆에 있는 연필 편집 아이콘  을 선택합니다.
- 플라이아웃 창에서 사용 가능한 필드에서 편집합니다. 시스템 태그의 경우 설명만 편집할 수 있습니다. 사용자 지정 태그의 경우 이름과 설명을 편집할 수 있습니다.
- 완료되면 제출 **을 선택하여 변경** 내용을 저장합니다.

태그 설정은 모든 주체 권한 요청에 적용됩니다.

자세한 내용은 주체 권한 요청에 대한 데이터를 검토할 때 [태그 적용을 참조합니다](subject-rights-requests-data-review.md#apply-tags).