---
external help file: Microsoft.Azure.Commands.ManagementPartner.dll-Help.xml
Module Name: AzureRM.ManagementPartner
online version: https://go.microsoft.com/fwlink/?LinkID=393054
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Update-AzureRmManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Update-AzureRmManagementPartner.md
ms.openlocfilehash: 9d1694cdde3edd94112fc5b1960fd870b842d6e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763044"
---
# <span data-ttu-id="31347-101">Update-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="31347-101">Update-AzureRmManagementPartner</span></span>

## <span data-ttu-id="31347-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31347-102">SYNOPSIS</span></span>
<span data-ttu-id="31347-103">Geçerli kimliği doğrulanmış kullanıcı veya hizmet sorumlusunun Microsoft Iş ortağı ağı (MPN) KIMLIĞINI güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="31347-103">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31347-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="31347-104">SYNTAX</span></span>

```
Update-AzureRmManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31347-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="31347-105">DESCRIPTION</span></span>
<span data-ttu-id="31347-106">Geçerli kimliği doğrulanmış kullanıcı veya hizmet sorumlusunun Microsoft Iş ortağı ağı (MPN) KIMLIĞINI güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="31347-106">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="31347-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="31347-107">EXAMPLES</span></span>

### <span data-ttu-id="31347-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="31347-108">Example 1</span></span>
```powershell
PS C:\> Update-AzureRmManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="31347-109">Yönetim ortağını yeni bir iş 'e güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="31347-109">Update the management partner to a new one</span></span>

## <span data-ttu-id="31347-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="31347-110">PARAMETERS</span></span>

### <span data-ttu-id="31347-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31347-111">-DefaultProfile</span></span>
<span data-ttu-id="31347-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="31347-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31347-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="31347-113">-PartnerId</span></span>
<span data-ttu-id="31347-114">Yönetim ortağı kimliği olan 6 basamaklı bir sayıdır</span><span class="sxs-lookup"><span data-stu-id="31347-114">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31347-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="31347-115">-Confirm</span></span>
<span data-ttu-id="31347-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="31347-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31347-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31347-117">-WhatIf</span></span>
<span data-ttu-id="31347-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="31347-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31347-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="31347-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31347-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31347-120">CommonParameters</span></span>
<span data-ttu-id="31347-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="31347-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31347-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31347-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31347-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="31347-123">INPUTS</span></span>

### <span data-ttu-id="31347-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="31347-124">None</span></span>

## <span data-ttu-id="31347-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="31347-125">OUTPUTS</span></span>

### <span data-ttu-id="31347-126">Microsoft. Azure. Commands. resources. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="31347-126">Microsoft.Azure.Commands.Resources.PSManagementPartner</span></span>

## <span data-ttu-id="31347-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="31347-127">NOTES</span></span>

## <span data-ttu-id="31347-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="31347-128">RELATED LINKS</span></span>

[<span data-ttu-id="31347-129">Remove-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="31347-129">Remove-AzureRmManagementPartner</span></span>](./Remove-AzureRmManagementPartner.md)

[<span data-ttu-id="31347-130">Yeni-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="31347-130">New-AzureRmManagementPartner</span></span>](./New-AzureRmManagementPartner.md)

[<span data-ttu-id="31347-131">Get-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="31347-131">Get-AzureRmManagementPartner</span></span>](./Get-AzureRmManagementPartner.md)
