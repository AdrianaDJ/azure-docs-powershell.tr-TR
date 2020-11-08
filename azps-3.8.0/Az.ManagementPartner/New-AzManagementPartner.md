---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/new-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/New-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/New-AzManagementPartner.md
ms.openlocfilehash: 9e6c56fa48b71e2571b7702e170bdc3e9e41f3aa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937456"
---
# <span data-ttu-id="72268-101">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="72268-101">New-AzManagementPartner</span></span>

## <span data-ttu-id="72268-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72268-102">SYNOPSIS</span></span>
<span data-ttu-id="72268-103">Bir Microsoft Iş ortağı ağının (MPN) KIMLIĞINI geçerli kimlik doğrulamalı Kullanıcı veya hizmet sorumlusuna ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="72268-103">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="72268-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="72268-104">SYNTAX</span></span>

```
New-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="72268-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="72268-105">DESCRIPTION</span></span>
<span data-ttu-id="72268-106">Bir Microsoft Iş ortağı ağının (MPN) KIMLIĞINI geçerli kimlik doğrulamalı Kullanıcı veya hizmet sorumlusuna ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="72268-106">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="72268-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="72268-107">EXAMPLES</span></span>

### <span data-ttu-id="72268-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="72268-108">Example 1</span></span>
```powershell
PS C:\> New-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="72268-109">Yönetim ortağı ekleme</span><span class="sxs-lookup"><span data-stu-id="72268-109">Add a management partner</span></span>

## <span data-ttu-id="72268-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="72268-110">PARAMETERS</span></span>

### <span data-ttu-id="72268-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72268-111">-DefaultProfile</span></span>
<span data-ttu-id="72268-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="72268-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72268-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="72268-113">-PartnerId</span></span>
<span data-ttu-id="72268-114">Yönetim ortağı kimliği olan 6 basamaklı bir sayıdır</span><span class="sxs-lookup"><span data-stu-id="72268-114">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72268-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="72268-115">-Confirm</span></span>
<span data-ttu-id="72268-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="72268-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72268-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72268-117">-WhatIf</span></span>
<span data-ttu-id="72268-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="72268-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72268-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="72268-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72268-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72268-120">CommonParameters</span></span>
<span data-ttu-id="72268-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="72268-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72268-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72268-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72268-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="72268-123">INPUTS</span></span>

### <span data-ttu-id="72268-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="72268-124">None</span></span>

## <span data-ttu-id="72268-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="72268-125">OUTPUTS</span></span>

### <span data-ttu-id="72268-126">Microsoft. Azure. Commands. Managementpartners. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="72268-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="72268-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="72268-127">NOTES</span></span>

## <span data-ttu-id="72268-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="72268-128">RELATED LINKS</span></span>

[<span data-ttu-id="72268-129">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="72268-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="72268-130">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="72268-130">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="72268-131">Güncelleştirme-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="72268-131">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)