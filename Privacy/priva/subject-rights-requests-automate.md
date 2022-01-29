---
title: '주체 권한 요청에서 작업 자동화 '
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
search.appverid:
- MOE150
- MET150
description: Priva에서 주체 권한 요청에 Power Automate 필수 작업을 자동화하는 데 도움이 되는 Microsoft 365를 사용하는 방법을 설명합니다.
ms.openlocfilehash: 2e1fa97b9e2cc5889471fa163dec26a5a5e37d56
ms.sourcegitcommit: f145dff5e387a8e26db2f3a2c7de125978fbacc9
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/28/2022
ms.locfileid: "62249078"
---
# <a name="automate-tasks-in-subject-rights-requests"></a>주체 권한 요청에서 작업 자동화 

Microsoft Power Automate 응용 프로그램 및 서비스 전반에 걸쳐 작업을 자동화하는 워크플로 서비스입니다. Microsoft Priva Power Automate 권한 요청에 대해 기본 제공 흐름을 사용하도록 설정하면 ServiceNow에서 티켓을 만들거나 기한에 대한 일정 미리 알림을 추가하는 등 사례 및 사용자에 대한 중요한 작업을 자동화할 수 있습니다. 자세한 내용은 Power Automate [사이트를 참조하세요](/power-automate/getting-started).

주체 권한 요청 구독이 있는 고객은 Priva에 대한 권장 Power Automate 템플릿을 사용하기 위해 다른 Power Automate 라이선스가 필요하지 않습니다. 이러한 템플릿은 조직을 지원하고 핵심 주체 권한 요청 시나리오를 다루기 위해 사용자 지정될 수 있습니다. 이러한 템플릿에서 프리미엄 Power Automate 기능을 사용하려면 Microsoft 365 준수 커넥터를 사용하여 사용자 지정 템플릿을 만들거나 Microsoft 365 다른 준수 영역에 대해 Power Automate 템플릿을 사용하려면 추가 Power Automate 라이선스가 필요할 수 있습니다.

## <a name="create-a-new-power-automate-flow-from-a-template"></a>템플릿에서 새 Power Automate 흐름 만들기

1. 이 [Microsoft 365 규정 준수 센터](https://compliance.microsoft.com/) 탐색의 Priva 섹션으로 이동하고 **Priva Subject Rights Requests를 선택합니다**.
1. 목록에서 작업할 주체 권한 요청을 열고 자동화를 선택한 다음 관리 흐름 **Power Automate 선택합니다**. 그러면 흐름 플라이아웃 창이 열립니다.
1. 새 **옵션을 사용하여** 사용 가능한 옵션에서 사용할 서식 파일을 선택합니다. 여기에서 마법사의 프롬프트에 따라 설정을 완료합니다. 옵션은 템플릿 유형에 따라 달라집니다.

템플릿의 인스턴스를 저장한 후 흐름 인스턴스에 올바른 컨텍스트와 ID가 있도록 주체 권한 요청의 세부 정보 페이지에서 인스턴스를 실행해야 합니다. 요청을 열고 자동화 메뉴 **로 돌아가서** 템플릿을 선택한 다음 흐름 실행 **을 선택합니다**. 흐름 실행 활동 보기를 선택하여 과거 **활동을 볼 수 있습니다**.

### <a name="power-automate-templates-in-priva"></a>Power Automate 템플릿

- **ServiceNow** 에서 개인 정보 관리 사례에 대한 레코드 만들기: 이 템플릿은 ServiceNow 솔루션을 사용하여 주체 권한 요청 사례를 추적하려는 조직을 위한 것입니다. ServiceNow에 연결할 계정을 포함해 ServiceNow 인스턴스 세부 정보를 입력해야 합니다. 이 계정에는 ServiceNow에서 인시던트 만들기 및 인시던트 세부 정보를 입력할 수 있는 능력이 있어야 합니다. 인스턴스에 연결되면 주체 권한 요청 관리자는 ServiceNow에서 사례에 대한 레코드를 만들 수 있으며, 필요한 경우 서식 파일을 선택한 필드에 채울 대상을 사용자 지정할 수 있습니다. 커넥터에 대한 자세한 내용은 [ServiceNow Connector 참조 페이지를 참조하세요](/connectors/service-now/).
- **일정 미리** 알림 만들기: 이 템플릿은 주체 권한 요청에 대한 Outlook 일정에서 기한 미리 알림을 설정하기 위한 것입니다. 이 도구는 요청의 속성에서 특정 세부 정보(예: 요청 이름 및 기한)를 채우게 됩니다. 자세한 내용을 추가하고, 받는 사람을 지정하고, 기타 고급 설정을 조정할 수 있습니다.
- **주체 권한 요청에** 대해 태그로 파일 다운로드: 이 템플릿을 사용하면 특정 태그가 부여된 주체 권한 요청에 대한 파일을 검색할 수 있습니다. 흐름을 편집하여 사용자 지정 작업을 수행하거나 반환된 파일 목록을 보고 내부 프로세스 또는 도구에 활용할 수 있습니다.

## <a name="share-a-power-automate-flow"></a>공유 Power Automate 공유

흐름을 Power Automate 다른 소유자를 추가하고 흐름을 편집, 업데이트 및 삭제할 수 있습니다. 모든 소유자는 실행 기록에 액세스하여 다른 소유자를 추가하거나 제거할 수도 있습니다. 흐름을 공유하려면 작업할 주체 권한 요청을 열고 자동화를 선택한 다음 흐름 관리 Power Automate **선택합니다**. 이 창에서 기존 흐름을 선택한 다음 공유 옵션을 사용하여 사용자 또는 그룹을 추가할 수 있습니다.

또한 이 창에서는 서비스 흐름에 사용되는 서비스에 대한 포함된 연결을 관리하는 Power Automate 있습니다. 이러한 설정을 변경하면 흐름 실행 능력에 영향을 줄 수 있습니다.

## <a name="edit-or-delete-power-automate-flow"></a>흐름 편집 또는 Power Automate 삭제

흐름의 세부 Power Automate 조정하려면 주체 권한 요청을 열고 자동화를 선택한 다음 흐름 Power Automate **선택합니다**. 이 창에서 기존 흐름을 선택하여 세부 정보를 볼 수 있습니다. 모든 섹션에서 편집을 사용하여 속성을 변경한 다음 저장합니다.

흐름을 완전히 제거하려면 삭제 **옵션을** 사용합니다. 모든 소유자에 대한 흐름을 제거하고 모든 사용자에 대해 제거합니다. 이전 흐름 인스턴스는 데이터 손실을 방지하기 위해 계속 실행됩니다. 선택을 확인한 후, 선택을 끝까지 할 수 있습니다.

## <a name="legal-disclaimer"></a>법적 고지 조항

[Microsoft Priva 법적 고지 조항](priva-disclaimer.md)
