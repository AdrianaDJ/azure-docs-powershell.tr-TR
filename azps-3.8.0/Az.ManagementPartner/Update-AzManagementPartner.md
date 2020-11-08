---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/update-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
ms.openlocfilehash: 326e16ff2f5bca8ca5ae987ebedf12cace87e11d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937452"
---
# <span data-ttu-id="69806-101">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="69806-101">Update-AzManagementPartner</span></span>

## <span data-ttu-id="69806-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69806-102">SYNOPSIS</span></span>
<span data-ttu-id="69806-103">Geçerli kimliği doğrulanmış kullanıcı veya hizmet sorumlusunun Microsoft Iş ortağı ağı (MPN) KIMLIĞINI güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="69806-103">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="69806-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="69806-104">SYNTAX</span></span>

```
Update-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69806-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="69806-105">DESCRIPTION</span></span>
<span data-ttu-id="69806-106">Geçerli kimliği doğrulanmış kullanıcı veya hizmet sorumlusunun Microsoft Iş ortağı ağı (MPN) KIMLIĞINI güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="69806-106">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="69806-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="69806-107">EXAMPLES</span></span>

### <span data-ttu-id="69806-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="69806-108">Example 1</span></span>
```powershell
PS C:\> Update-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="69806-109">Yönetim ortağını yeni bir iş 'e güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="69806-109">Update the management partner to a new one</span></span>

## <span data-ttu-id="69806-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="69806-110">PARAMETERS</span></span>

### <span data-ttu-id="69806-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69806-111">-DefaultProfile</span></span>
<span data-ttu-id="69806-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="69806-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69806-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="69806-113">-PartnerId</span></span>
<span data-ttu-id="69806-114">Yönetim ortağı kimliği olan 6 basamaklı bir sayıdır</span><span class="sxs-lookup"><span data-stu-id="69806-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="69806-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="69806-115">-Confirm</span></span>
<span data-ttu-id="69806-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="69806-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69806-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69806-117">-WhatIf</span></span>
<span data-ttu-id="69806-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="69806-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69806-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="69806-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69806-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69806-120">CommonParameters</span></span>
<span data-ttu-id="69806-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="69806-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69806-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69806-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69806-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="69806-123">INPUTS</span></span>

### <span data-ttu-id="69806-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="69806-124">None</span></span>

## <span data-ttu-id="69806-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="69806-125">OUTPUTS</span></span>

### <span data-ttu-id="69806-126">Microsoft. Azure. Commands. Managementpartners. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="69806-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="69806-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="69806-127">NOTES</span></span>

## <span data-ttu-id="69806-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="69806-128">RELATED LINKS</span></span>

[<span data-ttu-id="69806-129">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="69806-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="69806-130">Yeni-Azyönetim ortağı</span><span class="sxs-lookup"><span data-stu-id="69806-130">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="69806-131">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="69806-131">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)