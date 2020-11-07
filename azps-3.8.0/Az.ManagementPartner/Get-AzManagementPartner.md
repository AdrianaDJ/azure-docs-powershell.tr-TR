---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/get-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
ms.openlocfilehash: 1031c9c8828969d16097953aa7440e2c8c0a8c1b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937459"
---
# <span data-ttu-id="37e95-101">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="37e95-101">Get-AzManagementPartner</span></span>

## <span data-ttu-id="37e95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37e95-102">SYNOPSIS</span></span>
<span data-ttu-id="37e95-103">Geçerli kimliği doğrulanmış kullanıcı veya hizmet sorumlusunun Microsoft Iş ortağı ağı (MPN) KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="37e95-103">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="37e95-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="37e95-104">SYNTAX</span></span>

```
Get-AzManagementPartner [[-PartnerId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37e95-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="37e95-105">DESCRIPTION</span></span>
<span data-ttu-id="37e95-106">Geçerli kimliği doğrulanmış kullanıcı veya hizmet sorumlusunun Microsoft Iş ortağı ağı (MPN) KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="37e95-106">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="37e95-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="37e95-107">EXAMPLES</span></span>

### <span data-ttu-id="37e95-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="37e95-108">Example 1</span></span>
```powershell
PS C:\> Get-AzManagementPartner
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="37e95-109">Geçerli yönetim ortağı kimliği</span><span class="sxs-lookup"><span data-stu-id="37e95-109">Get the current management partner id</span></span>

### <span data-ttu-id="37e95-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="37e95-110">Example 2</span></span>
```powershell
PS C:\> Get-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="37e95-111">Geçerli yönetim ortağı kimliği, bir iş ortağı kimliği ile eşleşmezse, eşleşmezse başarısız olur</span><span class="sxs-lookup"><span data-stu-id="37e95-111">Get the current management partner id using a partner id, if they don't match, it will fail</span></span>

## <span data-ttu-id="37e95-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="37e95-112">PARAMETERS</span></span>

### <span data-ttu-id="37e95-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37e95-113">-DefaultProfile</span></span>
<span data-ttu-id="37e95-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="37e95-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37e95-115">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="37e95-115">-PartnerId</span></span>
<span data-ttu-id="37e95-116">Yönetim ortağı kimliği olan 6 basamaklı bir sayıdır</span><span class="sxs-lookup"><span data-stu-id="37e95-116">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37e95-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37e95-117">CommonParameters</span></span>
<span data-ttu-id="37e95-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="37e95-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37e95-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37e95-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37e95-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="37e95-120">INPUTS</span></span>

### <span data-ttu-id="37e95-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="37e95-121">None</span></span>

## <span data-ttu-id="37e95-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="37e95-122">OUTPUTS</span></span>

### <span data-ttu-id="37e95-123">Microsoft. Azure. Commands. Managementpartners. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="37e95-123">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="37e95-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="37e95-124">NOTES</span></span>

## <span data-ttu-id="37e95-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="37e95-125">RELATED LINKS</span></span>

[<span data-ttu-id="37e95-126">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="37e95-126">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="37e95-127">Yeni-Azyönetim ortağı</span><span class="sxs-lookup"><span data-stu-id="37e95-127">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="37e95-128">Güncelleştirme-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="37e95-128">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)