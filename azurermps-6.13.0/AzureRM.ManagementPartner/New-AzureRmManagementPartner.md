---
external help file: Microsoft.Azure.Commands.ManagementPartner.dll-Help.xml
Module Name: AzureRM.ManagementPartner
online version: https://go.microsoft.com/fwlink/?LinkID=393044
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/New-AzureRmManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/New-AzureRmManagementPartner.md
ms.openlocfilehash: f49ff33dbe3b7fbfd41e91140671bf61d378f1ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593994"
---
# <span data-ttu-id="f92c8-101">New-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="f92c8-101">New-AzureRmManagementPartner</span></span>

## <span data-ttu-id="f92c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f92c8-102">SYNOPSIS</span></span>
<span data-ttu-id="f92c8-103">Bir Microsoft Iş ortağı ağının (MPN) KIMLIĞINI geçerli kimlik doğrulamalı Kullanıcı veya hizmet sorumlusuna ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="f92c8-103">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f92c8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f92c8-104">SYNTAX</span></span>

```
New-AzureRmManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f92c8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f92c8-105">DESCRIPTION</span></span>
<span data-ttu-id="f92c8-106">Bir Microsoft Iş ortağı ağının (MPN) KIMLIĞINI geçerli kimlik doğrulamalı Kullanıcı veya hizmet sorumlusuna ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="f92c8-106">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="f92c8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f92c8-107">EXAMPLES</span></span>

### <span data-ttu-id="f92c8-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f92c8-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="f92c8-109">Yönetim ortağı ekleme</span><span class="sxs-lookup"><span data-stu-id="f92c8-109">Add a management partner</span></span> 

## <span data-ttu-id="f92c8-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f92c8-110">PARAMETERS</span></span>

### <span data-ttu-id="f92c8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f92c8-111">-DefaultProfile</span></span>
<span data-ttu-id="f92c8-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f92c8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f92c8-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="f92c8-113">-PartnerId</span></span>
<span data-ttu-id="f92c8-114">Yönetim ortağı kimliği olan 6 basamaklı bir sayıdır</span><span class="sxs-lookup"><span data-stu-id="f92c8-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="f92c8-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="f92c8-115">-Confirm</span></span>
<span data-ttu-id="f92c8-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f92c8-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f92c8-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f92c8-117">-WhatIf</span></span>
<span data-ttu-id="f92c8-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f92c8-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f92c8-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f92c8-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f92c8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f92c8-120">CommonParameters</span></span>
<span data-ttu-id="f92c8-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f92c8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f92c8-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f92c8-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f92c8-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f92c8-123">INPUTS</span></span>

### <span data-ttu-id="f92c8-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f92c8-124">None</span></span>

## <span data-ttu-id="f92c8-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f92c8-125">OUTPUTS</span></span>

### <span data-ttu-id="f92c8-126">Microsoft. Azure. Commands. Managementpartners. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="f92c8-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="f92c8-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f92c8-127">NOTES</span></span>

## <span data-ttu-id="f92c8-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f92c8-128">RELATED LINKS</span></span>

[<span data-ttu-id="f92c8-129">Remove-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="f92c8-129">Remove-AzureRmManagementPartner</span></span>](./Remove-AzureRmManagementPartner.md)

[<span data-ttu-id="f92c8-130">Get-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="f92c8-130">Get-AzureRmManagementPartner</span></span>](./Get-AzureRmManagementPartner.md)

[<span data-ttu-id="f92c8-131">Güncelleştirme-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="f92c8-131">Update-AzureRmManagementPartner</span></span>](./Update-AzureRmManagementPartner.md)
