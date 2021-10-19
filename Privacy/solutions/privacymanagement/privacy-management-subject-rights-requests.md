---
title: 개인 정보 관리의 주체 권한 요청에 대해 자세히 알아보기
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
description: 개인 정보 관리의 주체 권한 요청 영역은 개인 데이터를 찾고 콘텐츠를 검토하고 보고서를 만드는 데 도움이 됩니다.
ms.openlocfilehash: 7809f3a9dbf40b1cc0c745f710a3831ce6cf77ca
ms.sourcegitcommit: 85e085eb17af8b4efd1f45207445e1b3c3679600
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/19/2021
ms.locfileid: "60478430"
---
# <a name="learn-about-subject-rights-requests"></a>주체 권한 요청에 대한 자세한 정보

전 세계의 특정 개인 정보 보호 규정에 따라 개인(또는 데이터 주체)은 회사가 수집한 개인 데이터를 검토하거나 관리하기 위한 요청을 할 수 있습니다. 이러한 요청을 DSRs(데이터 주체 요청), DSARS(데이터 주체 액세스 요청) 또는 소비자 권한 요청이라고도 합니다. 많은 양의 정보를 저장하는 기업의 경우 관련 데이터를 찾는 것이 큰 과제가 될 수 있습니다.

개인 정보 보호 관리는 주체 권한 요청을 통해 이러한 문의를 처리하는 데 도움이 될 수 있습니다. 또한 주제 데이터를 검색하고, 결과를 검토하고, 적절한 파일을 수집하고, 보고서를 생성하는 데 도움이 될 수 있는 워크플로, 자동화 및 공동 작업 기능을 제공합니다.

## <a name="how-privacy-management-supports-subject-rights-request-fulfillment"></a>개인 정보 관리에서 주체 권한 요청 이행을 지원하는 방법

주체 권한 요청 주기는 조직에 대한 개인의 요청으로 시작됩니다. 일단 수신된 후 개인 정보 관리 기능을 사용하여 해당 데이터를 수집하고, 공동 작업하고, 검토하고, 보고서를 만들 수 있습니다. 그런 다음 데이터 주체에게 찾은 결과를 알리고 개인 정보 관리 외부에서 필요한 기타 작업을 수행하여 데이터 지우기 등의 요청을 수행할 수 있습니다. 워크플로를 관리하고 자동화하는 데 도움을 주기 위해 개인 정보 관리의 통합된 통합된 Power Automate 수 있습니다.

![주체 권한 요청에 대한 워크플로입니다.](../../media/privacy-management-srr-cycle.png)

### <a name="create-requests-and-collect-data"></a>요청 만들기 및 데이터 수집

개인 정보 관리는 조직이 조직에서 저장하는 콘텐츠에서 데이터 주체와 관련된 데이터를 찾기 위한 강력한 검색 옵션을 Microsoft 365. 또한 이러한 요청에 대해 수집한 데이터 내에서 검토할 항목의 우선 순위를 지정하는 데 도움이 됩니다. 개인 정보 보호 관리는 잠재적으로 기밀로 Microsoft Information Protection 수 있는 콘텐츠를 나타내며, 이러한 레이블로 항목에 플래그를 지정하는 민감도 레이블을 인식하고 있습니다. 또한 개인 정보 보호 관리는 여러 사용자 데이터가 포함될 수 있는 항목을 검색하고 플래그를 지정합니다. 여기서 데이터 주체에게 콘텐츠를 제공하기 전에 콘텐츠를 다시 적용해야 할 수 있습니다.

자세한 내용은 주체 권한 요청 [만들기를 참조합니다.](privacy-management-subject-rights-requests-create.md)

### <a name="data-matching"></a>데이터 일치

데이터 일치를 사용하면 개인 정보 관리를 통해 정확한 제공된 데이터 값에 따라 데이터 주체를 식별할 수 있습니다. 이 유형의 정보를 업로드하면 콘텐츠를 검색하는 정확도를 높일 수 있으며 주체 권한 요청을 만들 때 필드를 수동으로 제공해야 하는 필요성이 간소화됩니다. 또한 주체 권한 요청 내의 컨텍스트와 가장 많은 데이터 주체 콘텐츠가 있는 항목을 소개하는 개요 타일에 대한 컨텍스트를 제공합니다. 자세한 내용은 데이터 일치 [관리를 참조합니다.](privacy-management-subject-rights-requests-data-matching.md)

### <a name="review-data-and-collaborate-on-requests"></a>데이터 검토 및 요청 공동 작업

데이터가 수집된 후 결과를 평가하고, 보고서 및 내보내기에서 포함할 가장 관련성이 높은 항목을 선택하고, 필요한 모든 항목을 시정할 수 있습니다. 이 작업을 개인 정보 관리 파이프라인 내에서 팀 구성원 간에 공동으로 수행할 수 있습니다.
자세한 내용은 주체 권한 요청 검토 및 [공동 작업을 참조합니다.](privacy-management-subject-rights-requests-review.md)

### <a name="fulfill-requests"></a>요청 이행

개인 정보 관리는 보고서를 만들고 데이터 주체에게 다시 보낼 파일을 수집하는 도구를 제공합니다. 자세한 내용은 주체 권한 요청 내보내기 및 요청 이행 관리를 [참조합니다.](privacy-management-subject-rights-requests-fulfill.md)

### <a name="automate-tasks"></a>작업 자동화

기본 제공 템플릿을 사용하여 개인 정보 관리 내에서 워크플로 프로세스를 만들고 자동화할 Power Automate 있습니다. 이러한 템플릿은 ServiceNow에서 티켓을 작성하거나 일정 초대 설정과 같은 작업을 지원합니다. 자세한 내용은 주체 권한 요청 [작업 자동화를 참조합니다.](privacy-management-subject-rights-requests-automate-tasks.md)

## <a name="legal-disclaimer"></a>법적 고지 조항

[개인 정보 관리 법적 고지 조항](privacy-management-disclaimer.md)
