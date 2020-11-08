---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/get-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
ms.openlocfilehash: 1031c9c8828969d16097953aa7440e2c8c0a8c1b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109560"
---
# <span data-ttu-id="88f50-101">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="88f50-101">Get-AzManagementPartner</span></span>

## <span data-ttu-id="88f50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88f50-102">SYNOPSIS</span></span>
<span data-ttu-id="88f50-103">Geçerli kimliği doğrulanmış kullanıcı veya hizmet sorumlusunun Microsoft Iş ortağı ağı (MPN) KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="88f50-103">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="88f50-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="88f50-104">SYNTAX</span></span>

```
Get-AzManagementPartner [[-PartnerId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88f50-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="88f50-105">DESCRIPTION</span></span>
<span data-ttu-id="88f50-106">Geçerli kimliği doğrulanmış kullanıcı veya hizmet sorumlusunun Microsoft Iş ortağı ağı (MPN) KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="88f50-106">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="88f50-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="88f50-107">EXAMPLES</span></span>

### <span data-ttu-id="88f50-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="88f50-108">Example 1</span></span>
```powershell
PS C:\> Get-AzManagementPartner
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="88f50-109">Geçerli yönetim ortağı kimliği</span><span class="sxs-lookup"><span data-stu-id="88f50-109">Get the current management partner id</span></span>

### <span data-ttu-id="88f50-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="88f50-110">Example 2</span></span>
```powershell
PS C:\> Get-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="88f50-111">Geçerli yönetim ortağı kimliği, bir iş ortağı kimliği ile eşleşmezse, eşleşmezse başarısız olur</span><span class="sxs-lookup"><span data-stu-id="88f50-111">Get the current management partner id using a partner id, if they don't match, it will fail</span></span>

## <span data-ttu-id="88f50-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="88f50-112">PARAMETERS</span></span>

### <span data-ttu-id="88f50-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88f50-113">-DefaultProfile</span></span>
<span data-ttu-id="88f50-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="88f50-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88f50-115">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="88f50-115">-PartnerId</span></span>
<span data-ttu-id="88f50-116">Yönetim ortağı kimliği olan 6 basamaklı bir sayıdır</span><span class="sxs-lookup"><span data-stu-id="88f50-116">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="88f50-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88f50-117">CommonParameters</span></span>
<span data-ttu-id="88f50-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="88f50-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88f50-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88f50-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88f50-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="88f50-120">INPUTS</span></span>

### <span data-ttu-id="88f50-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="88f50-121">None</span></span>

## <span data-ttu-id="88f50-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="88f50-122">OUTPUTS</span></span>

### <span data-ttu-id="88f50-123">Microsoft. Azure. Commands. Managementpartners. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="88f50-123">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="88f50-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="88f50-124">NOTES</span></span>

## <span data-ttu-id="88f50-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="88f50-125">RELATED LINKS</span></span>

[<span data-ttu-id="88f50-126">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="88f50-126">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="88f50-127">Yeni-Azyönetim ortağı</span><span class="sxs-lookup"><span data-stu-id="88f50-127">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="88f50-128">Güncelleştirme-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="88f50-128">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)