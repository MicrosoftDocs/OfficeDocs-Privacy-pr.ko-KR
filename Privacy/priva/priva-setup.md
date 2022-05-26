---
title: Priva 시작하기
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
- MET150fcf
description: 조직에 대한 Microsoft Priva 설정하고, 역할 및 권한을 설정하고, 중요한 설정을 구성하는 방법을 알아봅니다.
ms.openlocfilehash: 945cbfd2625be50cb89eeaa8fe09e0effaea79d5
ms.sourcegitcommit: 3c27ecf7c86c8a3db38cae8819fc090eed192b4f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/25/2022
ms.locfileid: "65678215"
---
# <a name="get-started-with-priva"></a>Priva 시작하기

조직에서 개인 정보 보호 위험을 식별하고 완화하는 데 도움이 되는 Microsoft Priva 사용할 준비가 되면 다음 단계에 따라 설정을 도와주세요.

## <a name="confirm-subscriptions-and-licensing"></a>구독 및 라이선스 확인

Priva [Microsoft Purview 규정 준수 포털](https://compliance.microsoft.com/) 내에서 사용할 수 있으며 다음 라이선스를 가진 조직에서 구입할 수 있습니다.

- Microsoft 365 E3, E5, A3, A5
- Office 365 E1, E3, E5, A1, A3, A5

Priva Priva 개인 정보 위험 관리 및 Priva 주체 권한 요청 두 가지 솔루션에 대한 라이선스 옵션을 제공합니다. 개별적으로 또는 함께 구매할 수 있습니다. 주체 권한 요청에 대한 라이선스를 가져올 때 처리해야 하는 요청 수에 적합한 라이선스 계층을 선택할 수 있습니다. 언제든지 추가 요청을 구매할 수 있습니다.

자세한 라이선싱에 대한 지침은 [보안 및 준수에 대한 Microsoft 365 라이선스 지침](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance#microsoft-priva)을 참조하세요.

> [!Note]
> 미국 정부 Community(GCC) 온건, GCC High 또는 국방부(DoD) 고객은 Priva 사용할 수 없습니다.

### <a name="start-a-free-trial"></a>무료 평가판 시작

평가판 구독을 사용하여 두 Priva 솔루션의 모든 기능과 기능을 살펴봅니다. [Priva 평가판](priva-trial.md)에 등록하는 방법을 알아봅니다.

## <a name="enable-the-microsoft-365-audit-log"></a>Microsoft 365 감사 로그 사용

Microsoft 365 감사 로그는 조직 내의 모든 활동에 대한 요약입니다. 개인 정보 보호 위험 관리 정책은 정책 인사이트를 생성하기 위해 이러한 활동을 사용할 수 있습니다.

조직에 이미 감사 로그가 설정되어 있을 수 있습니다. 처음으로 사용을 시작해야 하는 경우 감사를 켜는 단계별 지침 [은 감사 로그 검색 설정 또는 해제](/microsoft-365/compliance/turn-audit-log-search-on-or-off) 를 참조하세요. 감사를 설정하면 감사 로그가 준비되고 있으며 준비가 완료된 후 몇 시간 내에 검색을 실행할 수 있다는 메시지가 표시됩니다. 이 작업은 한 번만 수행하면 됩니다. Microsoft 365 감사 로그 사용에 대한 자세한 내용은 [감사 로그 검색을 참조하세요](/microsoft-365/compliance/search-the-audit-log-in-security-and-compliance).

## <a name="set-user-permissions-and-assign-roles"></a>사용자 권한 설정 및 역할 할당

Priva RBAC(역할 기반 액세스 제어) 권한 모델을 사용합니다. 역할이 할당된 사용자만 Priva 액세스할 수 있으며 각 사용자가 허용하는 작업은 역할 유형에 따라 제한됩니다.

전역 관리자는 Priva 액세스하고 다른 사용자를 역할에 할당할 수 있는 권한이 있습니다. Priva 대한 [Microsoft Purview 규정 준수 포털](https://compliance.microsoft.com/) 로그인하고 사용자 권한을 설정할 수 있습니다. 빠른 시작을 위해 개인 정보 관리 역할 그룹에는 Priva 모든 기능에 액세스할 수 있는 권한이 있습니다. 이 그룹은 동일한 개인이 모든 업무를 수행할 수 있는 조직에 적합할 수 있습니다. 다른 개인 정보 보호 역할을 사용하면 보다 세분화된 제어를 수행하고 선택한 기능 또는 함수에 사용자를 할당할 수 있습니다.

역할 그룹 및 액세스 권한을 부여하는 방법에 대한 자세한 내용은 [Priva 사용자 권한 설정 및 역할 할당을](priva-permissions.md) 참조하세요.

## <a name="start-finding-and-visualizing-your-data"></a>데이터 찾기 및 시각화 시작

Priva 로그인하면 **개요** 페이지가 표시됩니다. 이 페이지에서는 문제를 신속하게 파악하고, 위험 지표를 식별하고, 문제를 해결하기 위한 조치를 취할 수 있도록 Microsoft 365 환경에서 개인 데이터가 어떻게 진화하고 있는지에 대한 동적 인사이트를 제공합니다. 개요는 등록 후 처음 24시간 이내에 초기 인사이트를 채워야 합니다. Priva 계속 사용하면 개요 페이지가 새로 고쳐지고 현재 정보를 계속 제공합니다.

시간에 따른 데이터에 대한 추가 인사이트를 위해 **데이터 프로필** 페이지에서 더 많은 시각화 및 분석을 제공하고 지리적 위치 및 Microsoft 365 위치별로 조직의 데이터를 전체적으로 볼 수 있습니다.

이러한 페이지에 대한 자세한 내용은 [Priva 개인 데이터 찾기 및 시각화를](priva-data-profile.md) 참조하세요.

## <a name="start-managing-risks-with-default-policies"></a>기본 정책을 사용하여 위험 관리 시작

개인 정보 보호 위험 관리는 데이터를 평가하기 시작하고 데이터 최소화, 데이터 과다 노출 및 데이터 전송을 위한 주요 위험 시나리오를 살펴봅니다. 이러한 정책은 기본적으로 켜져 있습니다. 이러한 정책을 사용하여 위험 위치를 평가한 다음 사용자가 주의에 문제를 제기하고 이러한 위험의 수정을 안내할 수 있도록 사용자 전자 메일 알림을 켤 수 있습니다. 또한 제공된 정책 템플릿에서 고유한 정책을 만들고 사용자 지정할 수 있습니다. 법률 고문과 협의하여 식별될 수 있는 조직의 법률 및 규정 준수 요구 사항을 충족하도록 정책을 조정할 수 있습니다. 자세한 내용은 [개인 정보 보호 위험 관리에서 정책 만들기를](risk-management-policies.md) 참조하세요.

## <a name="get-started-with-subject-rights-requests"></a>주체 권한 요청이 있는 시작

Priva 주체 권한 요청 주체 권한 요청 처리 프로세스를 자동화하여 기존 비즈니스 프로세스에 적합한 데이터 및 사용자 지정 가능한 워크플로에 쉽게 액세스할 수 있도록 합니다. 관련 데이터를 쉽게 찾고, 결과를 검토하고, 보고서를 생성할 수 있습니다. 그 과정에서 조직의 다른 전문가와 안전하게 협업하여 주체 권한 요청을 완료할 수 있습니다. 기본 제공 템플릿을 사용하여 비즈니스 워크플로를 관리하고 사용자 지정할 수도 있습니다. 이러한 기능을 사용하는 방법에 대한 자세한 내용은 [Priva 주체 권한 요청 대해 알아보세요](subject-rights-requests.md).

## <a name="priva-availability"></a>가용성 Priva

Microsoft Priva 전 세계 고객이 사용할 수 있습니다. 조직에서 데이터 상주 요구 사항을 충족하기 위해 아래에 나열된 로컬 데이터 센터 중 하나에서 테넌트 프로비전하는 경우 Microsoft Purview 규정 준수 포털 왼쪽 탐색에서 Priva 솔루션을 사용할 수 없습니다.

- 노르웨이
- 폴란드
- 카타르
- 싱가포르
- 남아프리카 공화국
- 대한민국
- 스페인
- 스웨덴
- 스위스
- 아랍에미리트

## <a name="legal-disclaimer"></a>법적 고지 사항

[Microsoft Priva 법적 고지 사항](priva-disclaimer.md)
