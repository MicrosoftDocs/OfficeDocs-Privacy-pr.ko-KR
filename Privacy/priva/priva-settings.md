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
description: Microsoft Priva 대한 전역 설정 옵션에 대해 알아봅니다.
ms.openlocfilehash: a6f2fe55600d6cc3018c9d15f05a6d9e459a1486
ms.sourcegitcommit: 3c83e8133a5a71f4e1d76a0b2981ab3ec9cd6602
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/13/2022
ms.locfileid: "66046602"
---
# <a name="configure-priva-settings"></a>Priva 설정 구성

화면의 오른쪽 위 모서리에 있는 기어 아이콘을 선택하여 Microsoft Priva 설정을 관리할 수 있습니다. 여기서 옵션을 사용하면 높은 수준의 기본 설정을 설정하고 키 속성을 사용자 지정할 수 있습니다. 이 페이지에서는 주요 설정 범주에 대한 개요를 제공합니다.

## <a name="anonymization"></a>익명

개인 정보 보호 위험 관리 기능 내에서 익명화된 버전의 사용자 이름을 특정 역할의 사용자에게 표시할 수 있습니다. 익명화 기능은 중요한 데이터를 검토하는 동안 사용자의 ID를 마스킹하는 데 도움이 되도록 식별 가능한 표시 이름을 일반 레이블로 바꿉니다. 이 옵션은 주체 권한 요청 솔루션에 적용되지 않습니다.

## <a name="user-notification-emails"></a>사용자 알림 이메일  

개인 정보 보호 위험 관리의 정책을 사용하면 사용자 환경에서 잠재적인 개인 정보 위험을 평가하기 위한 매개 변수를 설정할 수 있습니다. 정책 일치가 감지되면 개인 정보 보호 위험 관리에서 취할 수정 작업에 대한 권장 사항 및 개인 정보 보호 교육 링크가 포함된 이메일을 사용자에게 보낼 수 있습니다. **설정** 개인 정보 보호 위험 관리의 전자 메일 알림 기능을 전체적으로 사용하거나 사용하지 않도록 설정할 수 있습니다. 설정 알림 기능이 해제되면 모든 전자 메일이 비활성화됩니다. 정책에 대한 자세한 내용은 [개인 정보 보호 위험 관리에서 정책 만들기를](risk-management-policies.md) 참조하세요.

## <a name="teams-collaboration"></a>Teams 공동 작업  

Microsoft Teams 기능을 Priva 주체 권한 요청 통합하여 이해 관계자와의 협업을 강화합니다. **주체 권한 요청에 대한 Microsoft Teams 기능을 켜도록** 확인란을 선택하면 각 요청에 대해 연결된 Teams 채널이 자동으로 만들어집니다. 요청의 **협력자** 탭에서 Teams 채널에 사용자를 추가할 수 있습니다.

이 기능을 켜면 모든 요청에 Teams 기능이 적용됩니다. 확인란을 선택 취소하면 모든 요청에 대해 이러한 기능이 해제됩니다. [데이터 검토 프로세스 중에 협업에](subject-rights-requests-data-review.md#collaboration-for-data-review) 대해 자세히 알아봅니다.

## <a name="data-matching"></a>데이터 일치  

이 섹션을 사용하여 데이터 주체의 특성을 설명하는 데이터 스키마를 업로드하면 Microsoft 365 환경 내에서 개인 데이터를 검색할 때 올바른 데이터 주체를 식별하는 데 도움이 됩니다. 스키마 및 규칙 패키지는 XML 형식으로 만들어지고 업로드됩니다. **개인 데이터 업로드** 에서 제공된 스키마와 일치하는 개인 데이터를 제출할 수도 있습니다. 사용자 고유의 파일을 만들고 업로드하거나 Azure에서 개인 데이터를 업로드하도록 선택할 수 있습니다. [주체 권한 요청에 대한 데이터 일치](subject-rights-requests-data-match.md)에 대해 자세히 알아봅니다.

## <a name="data-retention-periods"></a>데이터 보존 기간

이 설정은 Priva 주체 권한 요청 관련이 있습니다. 이를 통해 요청이 닫힌 후 생성된 수집된 데이터 및 보고서를 보존할 기간에 대한 기본 설정을 제어할 수 있습니다. 30일 또는 90일로 설정할 수 있으며 사용자가 만든 모든 주체 권한 요청에 적용됩니다. 데이터 보존 기간이 조직의 정책 및 법적 의무를 준수하는지 확인하는 것이 좋습니다. [주체 권한 요청에 대한 데이터 보존에](subject-rights-requests-reports.md#retention-periods-for-reports-and-data) 대해 자세히 알아봅니다.

## <a name="data-review-tags"></a>데이터 검토 태그

데이터 검토 태그를 사용하여 주체 권한 요청에서 검색되는 콘텐츠 항목을 표시할 수 있습니다. 이 설정 영역을 사용하면 태그를 관리할 수 있습니다. Priva **후속** 작업, **삭제** 및 **업데이트** 라는 세 가지 기본 태그를 제공합니다. 이러한 태그 이름은 편집할 수 없지만 조직에 의미 있는 태그에 대한 설명을 제공할 수 있습니다.

Priva 조직의 용도로 이름을 지정하고 정의할 수 있는 두 개의 사용자 지정 태그도 제공합니다. 이름을 편집할 때까지 **사용자 지정 태그 1** 및 **사용자 지정 태그 2** 로 나열됩니다.

아래 단계에 따라 태그 이름 및 설명을 편집합니다.

- Priva **설정** 페이지에서 **데이터 검토 태그를** 선택합니다.
- 편집하려는 목록에서 태그를 찾아 이름 옆에 있는 연필 **편집** 아이콘을 선택합니다.
- 플라이아웃 창에서 사용 가능한 필드에서 편집합니다. 시스템 태그의 경우 설명만 편집할 수 있습니다. 사용자 지정 태그의 경우 이름과 설명을 편집할 수 있습니다.
- 완료되면 **제출** 을 선택하여 변경 내용을 저장합니다.

태그 설정은 모든 주체 권한 요청에 적용됩니다.

[주체 권한 요청에 대한 데이터를 검토할 때 태그를 적용하는 방법에 대해](subject-rights-requests-data-review.md#apply-tags) 자세히 알아봅니다.