---
title: Priva 시작
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
description: 조직에 맞게 Microsoft Priva를 설정하고, 역할 및 사용 권한을 설정하고, 중요한 설정을 구성하는 방법에 대해 자세히 알아보습니다.
ms.openlocfilehash: 62e28361b57dd866b95ce566616473ed1a71e4ad
ms.sourcegitcommit: f145dff5e387a8e26db2f3a2c7de125978fbacc9
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/28/2022
ms.locfileid: "62249102"
---
# <a name="get-started-with-priva"></a>Priva 시작

개인 정보 위험을 식별하고 완화하는 데 도움을 받을 수 있도록 Microsoft Priva를 사용할 준비가 된 경우 다음 단계에 따라 선행 단계를 설정하고 개인 정보 정보 분석 탐색을 시작하세요.

## <a name="step-1-confirm-subscriptions-and-licensing"></a>1단계: 구독 및 라이선스 확인

Priva는 다음 라이선스를 [](https://compliance.microsoft.com/) Microsoft 365 규정 준수 센터 조직에서 구매할 수 있습니다.

- Microsoft 365 E3, E5, A3, A5
- Office 365 E1, E3, E5, A1, A3, A5

Priva는 Priva Privacy Risk Management 및 Priva Subject Rights Requests의 두 가지 솔루션에 대한 라이선스 옵션을 제공합니다. 이러한 구성은 개별적으로 또는 함께 구매할 수 있습니다. 주체 권한 요청에 대한 라이선스를 얻을 때 처리해야 하는 요청 수에 적합한 라이선스 계층을 선택할 수 있습니다. 원하는 경우 추가 요청을 구입할 수 있습니다.

자세한 라이선싱에 대한 지침은 [보안 및 준수에 대한 Microsoft 365 라이선스 지침](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance#privacy-management)을 참조하세요.

> [!Note]
> Priva는 미국 정부 Community(GCC) 보통, GCC 또는 DoD(국방부) 고객은 사용할 수 없습니다.

### <a name="get-free-trial-license"></a>무료 평가판 라이선스 다운로드

Priva를 시작할 때 무료 평가판 라이선스를 사용할 수 있습니다. 자격 및 가입 방법에 대한 자세한 내용은 [무료 Priva 평가판에 대해 자세히 알아보는 것을 참조합니다](priva-trial.md).

## <a name="step-2-enable-the-microsoft-365-audit-log"></a>2단계: 감사 Microsoft 365 사용

Microsoft 365 감사 로그는 조직 내의 모든 활동에 대한 요약입니다. 개인 정보 보호 위험 관리 정책은 정책 정보를 생성하는 데 이러한 활동을 사용할 수 있습니다.

조직에 이미 감사 로그가 켜져 있을 수 있습니다. 이러한 로그를 처음 사용하려면 감사 로그 검색 켜기 또는 끄 [](/microsoft-365/compliance/turn-audit-log-search-on-or-off) 기에서 감사를 켜는 단계별 지침을 참조하세요. 감사를 설정하면 감사 로그가 준비되고 있으며 준비가 완료된 후 몇 시간 내에 검색을 실행할 수 있다는 메시지가 표시됩니다. 이 작업은 한 번만 수행하면 됩니다. 감사 로그를 사용하는 Microsoft 365 자세한 내용은 감사 로그 검색[을 참조하세요](/microsoft-365/compliance/search-the-audit-log-in-security-and-compliance).

## <a name="step-3-set-user-permissions-and-assign-roles"></a>3단계: 사용자 권한 설정 및 역할 할당

Priva는 RBAC(역할 기반 액세스 제어) 사용 권한 모델을 사용 합니다. 역할이 할당된 사용자만 Priva에 액세스할 수 있으며 각 사용자가 허용하는 작업은 역할 유형에 따라 제한됩니다.

전역 관리자에게 Priva에 액세스하고 다른 사용자를 역할에 할당할 수 있는 권한이 있습니다. 사용자는 Priva에 대한 로그인 및 사용자 [Microsoft 365 규정 준수 센터 수 있습니다](https://compliance.microsoft.com/). 빠른 시작을 위해 개인 정보 관리 역할 그룹에는 Priva의 모든 기능에 액세스할 수 있는 권한이 있습니다. 이 그룹은 동일한 개인이 모든 업무를 수행할 수 있는 조직에 적합할 수 있습니다. 다른 개인 정보 보호 역할을 사용하면 보다 세부적인 제어를 수행하고 선택한 기능이나 기능에 사용자를 할당할 수 있습니다.

역할 그룹 및 액세스 권한을 부여하는 방법에 대한 자세한 내용은 사용자 권한 설정 및 [Priva에서 역할 할당을 참조합니다](priva-permissions.md).

## <a name="step-4-start-finding-and-visualizing-your-data"></a>4단계: 데이터 찾기 및 시각화 시작

Priva에 로그인하면 개요 **페이지가** 표시됩니다. 이 페이지에서는 문제를 빠르게 파악하고, 위험 지표를 식별하고, 문제를 해결하기 위한 조치를 취할 수 있도록 Microsoft 365 환경에서 개인 데이터가 진화하는 방법에 대한 동적 인사이트를 제공합니다. 개요는 등록 후 처음 24시간 내에 초기 정보를 채워야 합니다. Priva를 계속 사용할 때 개요 페이지가 새로 고쳐 현재 정보를 계속 제공합니다.

시간이 지날수록 데이터에 대한 추가 정보를 얻을 수 있도록  데이터 프로필 페이지는 더 많은 시각화 및 분석을 제공하고 지리적 위치 및 조직의 위치를 통해 조직의 데이터를 Microsoft 365 제공합니다.

이러한 페이지에 대한 자세한 내용은 Priva에서 개인 데이터 [찾기 및 시각화를 참조하세요](priva-data-profile.md).

## <a name="step-5-start-managing-risks-with-default-policies"></a>5단계: 기본 정책으로 위험 관리 시작

개인 정보 보호 위험 관리는 데이터를 평가하기 시작하고 데이터 최소화, 데이터 과다 노출 및 데이터 전송에 대한 주요 위험 시나리오를 살펴 봐야 합니다. 이러한 정책은 기본적으로 켜져 있습니다. 이러한 정책을 사용하여 위험의 위치를 평가한 다음 사용자의 사용자 전자 메일 알림을 설정하여 문제를 주의하고 이러한 위험에 대한 수정을 안내할 수 있습니다. 또한 제공된 정책 템플릿에서 자체 정책을 만들고 사용자 지정할 수 있습니다. 법률 고문과의 협의에서 식별될 수 있는 조직의 법적 및 규정 준수 요구에 맞게 정책을 조정할 수 있습니다. 자세한 내용은 [Create policies in Privacy Risk Management를 참조합니다](risk-management-policies.md).

## <a name="step-6-get-started-with-subject-rights-requests"></a>6단계: 주체 권한 요청 시작

Priva 주체 권한 요청은 주체 권한 요청 이행 프로세스를 자동화하여 기존 비즈니스 프로세스에 맞는 데이터 및 사용자 지정 가능한 워크플로에 쉽게 액세스할 수 있도록 합니다. 관련 데이터를 쉽게 찾고, 결과를 검토하고, 보고서를 만들 수 있습니다. 이렇게 하면 조직의 다른 전문가와 안전하게 공동 작업을 통해 주체 권한 요청을 완료할 수 있습니다. 기본 제공 서식 파일을 사용하여 비즈니스 워크플로를 관리하고 사용자 지정할 수도 있습니다. 이러한 기능 사용에 대한 자세한 내용은 [Priva Subject Rights Requests에 대한 자세한 정보를 참조합니다](subject-rights-requests.md).

## <a name="legal-disclaimer"></a>법적 고지 조항

[Microsoft Priva 법적 고지 조항](priva-disclaimer.md)
