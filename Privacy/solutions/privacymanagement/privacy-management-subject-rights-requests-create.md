---
title: 개인 정보 관리에서 주체 권한 요청 만들기
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
description: 개인 정보 관리에서 새 주체 권한 요청을 만드는 방법을 학습합니다.
ms.openlocfilehash: 316d515be454b6aceed95f68c6f3da6fa0e7567c
ms.sourcegitcommit: 85e085eb17af8b4efd1f45207445e1b3c3679600
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/19/2021
ms.locfileid: "60478367"
---
# <a name="create-a-subject-rights-request"></a>주체 권한 요청 만들기

주체 권한 관리 관리자는 개인 정보 관리의 주체 권한 요청 페이지를 통해 새 주체 권한 요청을 열 수 있습니다. 마법사는 데이터 주체에 대한 개인 데이터를 찾아 요청 이행 프로세스를 시작하는 프로세스를 안내합니다.

또한 개인 정보 관리를 통해 정확한 제공된 데이터 값에 따라 데이터 주체가 식별될 수 있도록 추가 자료를 업로드할 수도 있습니다. 자세한 내용은 데이터 일치 [관리를 참조합니다.](privacy-management-subject-rights-requests-data-matching.md)

## <a name="use-the-subject-rights-request-creation-wizard"></a>주체 권한 요청 만들기 마법사 사용

1. 에서 [Microsoft 365 규정 준수 센터](https://compliance.microsoft.com/)개인 정보 관리 섹션으로 이동하고 주체 **권한 요청 을 선택합니다.**
1. 새 요청을 시작하려면 요청 **만들기 를 선택합니다.**
1. 요청을 한 데이터 주체를 식별하고 회사와의 관계를 지정합니다.
1. 데이터 주체와 관련된 항목에 대한 기본 검색을 실행합니다. 데이터를 검색하기 전에 검색을 구체화하거나 예상 결과를 구체화하려는 경우 이 단계에서 이러한 선택을 할 수 있습니다. 모든 항목을 비워 두고 다음 단계로 이동할 수 있습니다. 옵션에 대한 자세한 내용은 [검색](#define-search-settings) 설정 정의 및 검색 구체화 [를 참조하세요.](#refine-your-search)
1. 데이터 주체가 데이터로 원하는 작업을 기반으로 요청 유형을 선택하십시오. 요청이 특정 데이터 개인 정보 보호 규정과 관련된 경우 제공된 목록에서 해당 요청을 선택하여 컨텍스트를 더 추가할 수도 있습니다. 기한(필수)을 설정하면 요청에 접근하거나 기한이 지난 요청을 쉽게 정렬하고 시기에 따라 해결할 수 있습니다. 요청 유형은 다음과 같습니다.
   - **액세스:** 조직에서 데이터 주체의 개인 정보를 요약하여 Microsoft 365.
   - **내보내기:** 검토하는 동안 수집 및 주석을 달고 수집된 데이터 주체의 개인 정보의 요약 및 내보내기 기능을 제공합니다.
   - **추가 작업용 태그가** 지정된 목록: 검토 중에 사용자가 태그를 지정하는 파일의 요약을 생성합니다. 개인 정보 관리 외부에서 추가 작업이 필요할 수 있습니다. 예를 들어 요청에 따라 데이터 주체의 개인 정보를 쉽게 지우는 데 도움이 될 수 있습니다. 주체 권한 요청에 대한 사용자 지정 데이터 검토 태그는 전역 관리 센터에서 관리할 **설정.**
1. 이 요청의 이름을 확인하고 참조를 위한 선택적 설명을 추가합니다.
1. 이전 단계에서 입력한 내용의 요약을 검토합니다. 요청 만들기 를 선택하기 전에 모든 필드를 **편집할 수 있습니다.**

### <a name="define-search-settings"></a>검색 설정 정의

주체 권한 요청을 만드는 동안 다음 검색 옵션 중 하나 또는 모두를 선택하면 제목에 대한 데이터를 찾을 수 있습니다.

- **데이터 주체가 작성한** 콘텐츠 포함: 여기에는 데이터 주체가 제작한 콘텐츠가 포함하며 더 높은 볼륨의 데이터를 반환할 수 있습니다.
- **검색 구체화:** 이렇게 하면 데이터 주체 식별에 도움이 되는 추가 속성을 지정할 수 있습니다. 여기서 검색 범위를 특정 서비스 또는 리소스로 Microsoft 365 다른 조건을 선택하여 요청 범위를 조정할 수 있습니다. 이 옵션을 선택한 후 사용자 지정 검색 매개 변수를 입력하라는 메시지가 표시될 것입니다.
- **먼저 예상** 데이터 확인: 이를 통해 데이터가 자동으로 검색되기 전에 예상되는 데이터의 수를 알 수 있습니다.

### <a name="refine-your-search"></a>검색 구체화

검색 설정을 정의하는 동안 검색을 구체화하기로 선택한 경우 고급 검색 매개 변수를 입력해야 합니다. 식별자를 **추가하고,** **조건을** 설정하고, 검색할 Microsoft 365 수 있습니다. 

- **식별자 추가:** 이름, 전자 메일 주소 및/또는 기타 옵션과 같은 데이터 주체에 대한 보다 식별 정보를 제공합니다. 각 필드에서 여러 값을 세미코론으로 구분합니다.
- **조건:** 드롭다운에서 유형을 선택하여 검색 조건을 추가합니다. 이러한 유형은 시간, 크기, 보존 레이블, 보낸 사람 및 받는 사람 등 데이터의 가능한 속성에 해당합니다. 원하는 형식을 선택하여 추가한 다음 원하는 속성을 설정할 수 있습니다. 텍스트 필드 항목의 경우 세미 콜론으로 구분된 여러 키워드를 추가할 수 있습니다. 원하는 수만큼 콘텐츠 형식을 추가할 수 있습니다.
- **위치:** 검색 범위를 특정 사이트, SharePoint 채널 Teams 위치로 비즈니스용 OneDrive 수 있습니다. 각 위치에 대해 모든 인스턴스(예: 모든 Exchange 또는 특정 인스턴스(예: 한 사용자의 사서함)를 선택할 수 있습니다. 각 위치 옵션에 대해 **선택...** 링크를 선택하여 특정 인스턴스에 대한 정보를 입력합니다. 적절한 검색어를 식별하는 데 도움이 필요한 경우 다음을 참조합니다.
  - 새 SharePoint 관리 센터에서 사이트 관리: 사이트를 정렬 [및 필터링하는 방법과](/sharepoint/manage-sites-in-new-admin-center)사이트 검색 방법에 대한 SharePoint 제공합니다. 검색 필드의 URL을 SharePoint 데 사용할 수 있습니다.
  - [Get-Team](/powershell/module/teams/get-team): 특정 속성/정보로 Microsoft Teams 팀을 찾는 방법에 대한 정보를 제공합니다. 채팅 및 채널을 식별하는 데 Teams 사용할 수 있습니다.
  - [url OneDrive](/onedrive/list-onedrive-urls#about-onedrive-urls)정보: 사용자의 URL에 대한 적절한 형식 및 속성에 대한 OneDrive 제공합니다. 검색에서 사이트 OneDrive 식별하는 데 도움이 됩니다.

올바른 데이터 주체가 식별되도록 선택을 신중하게 검토하는 것이 좋습니다. 예를 들어 이름으로 사서함을 검색하고 이름이 비슷한 여러 개인을 찾는 경우 요청에 사서함을 추가하기 전에 올바른 사서함을 확인합니다.

## <a name="next-steps"></a>다음 단계

요청을 만들면 주체 권한 요청 페이지에 해당 요청이 나열됩니다. 검토를 진행하는 방법에 대한 자세한 내용은 [Review data and collaborate on requests을 참조합니다.](privacy-management-subject-rights-requests-review.md)

## <a name="legal-disclaimer"></a>법적 고지 조항

[개인 정보 관리 법적 고지 조항](privacy-management-disclaimer.md)
