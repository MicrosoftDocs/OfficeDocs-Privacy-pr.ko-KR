---
title: 사용자 권한 설정 및 Microsoft Priva 역할 할당
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
- M365-priva-privacy-risk-management
- M365-priva-subject-rights-requests
search.appverid:
- MOE150
- MET150
description: Microsoft Priva 권한을 설정하고 사용자를 역할 그룹에 할당하는 방법을 알아봅니다.
ms.openlocfilehash: eca08327e2db909475dbf4c072b8f6843de3d57b
ms.sourcegitcommit: 3c27ecf7c86c8a3db38cae8819fc090eed192b4f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/25/2022
ms.locfileid: "65678225"
---
# <a name="set-user-permissions-and-assign-roles-in-microsoft-priva"></a>사용자 권한 설정 및 Microsoft Priva 역할 할당

조직 구성원에게 Microsoft Priva 사용할 수 있는 권한을 부여하려면 Microsoft Purview 규정 준수 포털 적절한 역할 그룹에 할당합니다.

> [!NOTE]
> 대부분의 Priva 역할은 현재 "개인 정보 관리"로 지정됩니다. 전체 목록은 아래를 참조하세요. Priva 관련된 역할은 Azure Active Directory 표시되지 않습니다.

## <a name="sign-in-and-set-permissions"></a>로그인 및 사용 권한 설정

1. [Microsoft Purview 규정 준수 포털](https://compliance.microsoft.com/) 이동하여 왼쪽 탐색 영역에서 **사용 권한을** 선택합니다.  
2. **Microsoft Purview 솔루션** 드롭다운 아래에서 **역할을** 선택합니다. 역할 그룹의 전체 목록이 표시됩니다.
3. 하나 이상의 사용자를 추가할 역할 그룹을 찾고(아래 역할 그룹 설명 참조) 그룹 이름 왼쪽에 있는 확인란을 선택합니다.
4. 해당 그룹의 플라이아웃 창에서 **멤버** 헤더 아래에서 **편집** 을 선택합니다.  
5. 플라이아웃 창의 왼쪽 탐색 영역에서 **구성원 선택을** 선택합니다. 다른 플라이아웃 창이 나타납니다.
6. **+ 추가** 를 선택하여 그룹에 추가할 사용자를 하나 이상 선택합니다.  
7. 추가할 이름 옆에 있는 확인란을 선택한 다음 아래쪽에 있는 **추가** 단추를 선택합니다.  
8. 사용자 할당이 완료되면 **완료**, **저장**, **닫기를** 차례로 선택합니다.

## <a name="learn-more-about-role-groups-and-roles"></a>역할 그룹 및 역할에 대해 자세히 알아보기

팀의 구조에 따라 특정 역할 그룹에 사용자를 할당하여 다양한 Priva 기능 집합을 관리할 수 있는 옵션이 있습니다. 수행해야 하는 작업과 적절한 파일 액세스 수준에 따라 멤버를 역할 그룹에 할당해야 합니다. 각 역할 그룹에는 하나 이상의 역할이 포함됩니다. 이러한 역할은 특정 Priva 작업 또는 해당 그룹의 멤버에 대해 활성화되거나 제한된 키 함수와 관련될 수 있습니다. 따라서 다른 사용자는 특정 Priva 기능에 대한 가시성 및 액세스 수준이 다를 수 있습니다.

필요한 경우 역할 그룹을 사용자 지정할 수 있습니다. 실수로 액세스가 손실되는 것을 방지하려면 사용자 지정하려는 기존 역할 그룹의 복사본을 만들고, 복사본에 식별 가능한 이름을 지정하고, 새 그룹에 대한 변경 내용을 만들고 확인하고, 적절하게 사용자를 할당하는 것이 좋습니다.

## <a name="privacy-management-role-group"></a>개인 정보 관리 역할 그룹

이 그룹에는 단일 그룹의 모든 Priva 권한 역할이 포함됩니다. 이 역할 그룹은 동일한 개인이 모든 업무를 수행할 수 있는 조직에 적합할 수 있습니다. 이 역할 그룹의 멤버 자격을 제공하면 해당 계정에 라이선스를 보유한 Priva 모든 기능에 대한 모든 액세스 권한이 부여됩니다.

이 그룹의 활성 멤버가 항상 하나 이상 있는지 확인하는 것이 좋습니다.

역할은 다음과 같습니다.

- 사례 관리  
- 데이터 분류 콘텐츠 뷰어  
- 데이터 분류 목록 뷰어  
- 개인 정보 관리 관리  
- 개인 정보 관리 분석  
- 개인 정보 관리 조사  
- 개인 정보 관리 영구 기여  
- 개인 정보 관리 임시 기여  
- 개인 정보 관리 뷰어  
- 주체 권한 요청 관리  
- View-Only 사례

## <a name="privacy-management-administrators-role-group"></a>개인 정보 관리 관리자 역할 그룹

이 역할 그룹의 구성원은 개인 정보 보호 위험 관리 정책, 주체 권한 요청, 권한 및 설정을 만들고, 읽고, 업데이트하고, 삭제하는 등 Priva 기능에 광범위하게 액세스할 수 있습니다.

역할은 다음과 같습니다.

- 사례 관리  
- 개인 정보 관리 관리  
- View-Only 사례

## <a name="privacy-management-analysts-role-group"></a>개인 정보 관리 분석가 역할 그룹

이 역할 그룹의 멤버는 사례 분석가 역할을 합니다. 정책 일치를 조사하고, 파일 메타데이터를 보고, 수정 작업을 수행할 수 있습니다. 이 그룹은 콘텐츠 탐색기를 통해 전체 파일에 액세스할 수 없습니다.

역할은 다음과 같습니다.

- 사례 관리  
- 데이터 분류 목록 뷰어  
- 개인 정보 관리 분석  
- View-Only 사례

### <a name="privacy-management-investigators-role-group"></a>개인 정보 관리 조사자 역할 그룹

이 그룹의 구성원은 데이터 조사자 역할을 합니다. 정책 일치를 조사하고, 연결된 파일 콘텐츠를 보고, 수정 작업을 수행할 수 있습니다. 이 그룹은 콘텐츠 탐색기를 통해 파일에 액세스할 수 있습니다.

역할은 다음과 같습니다.

- 사례 관리  
- 데이터 분류 콘텐츠 뷰어  
- 데이터 분류 목록 뷰어  
- 개인 정보 관리 조사  
- View-Only 사례

## <a name="privacy-management-viewer-role-group"></a>개인 정보 관리 뷰어 역할 그룹

이 그룹의 구성원은 개요, 데이터 프로필 및 주체 요청 보고서와 같은 Priva 분석 정보를 볼 수 있습니다.

역할은 다음과 같습니다.

- 개인 정보 관리 뷰어

## <a name="subject-rights-request-administrators-role-group"></a>주체 권한 요청 관리자 역할 그룹

이 그룹의 구성원은 주체 권한 요청을 관리하고 만들 수 있는 모든 권한을 갖습니다.

역할은 다음과 같습니다.

- 주체 권한 요청 관리

## <a name="privacy-management-contributors-role-group"></a>개인 정보 관리 기여자 역할 그룹

이 그룹의 구성원은 공동 작업자로 추가된 주체 권한 요청에 액세스할 수 있습니다.  

역할은 다음과 같습니다.

- 개인 정보 관리 임시 기여  
- 개인 정보 관리 영구 기여

## <a name="legal-disclaimer"></a>법적 고지 사항

[Microsoft Priva 법적 고지 사항](priva-disclaimer.md)