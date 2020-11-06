---
external help file: Microsoft.Azure.Commands.ManagementPartner.dll-Help.xml
Module Name: AzureRM.ManagementPartner
online version: https://go.microsoft.com/fwlink/?LinkID=393045
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Remove-AzureRmManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Remove-AzureRmManagementPartner.md
ms.openlocfilehash: 3bb1b54abf947d5fc2a05538cc31ce53fb794ab7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593995"
---
# <span data-ttu-id="91537-101">Remove-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="91537-101">Remove-AzureRmManagementPartner</span></span>

## <span data-ttu-id="91537-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91537-102">SYNOPSIS</span></span>
<span data-ttu-id="91537-103">Geçerli kimliği doğrulanmış kullanıcı veya hizmet sorumlusunun Microsoft Iş ortağı ağı (MPN) KIMLIĞINI silin.</span><span class="sxs-lookup"><span data-stu-id="91537-103">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91537-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="91537-104">SYNTAX</span></span>

```
Remove-AzureRmManagementPartner [-PartnerId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91537-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="91537-105">DESCRIPTION</span></span>
<span data-ttu-id="91537-106">Geçerli kimliği doğrulanmış kullanıcı veya hizmet sorumlusunun Microsoft Iş ortağı ağı (MPN) KIMLIĞINI silin.</span><span class="sxs-lookup"><span data-stu-id="91537-106">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="91537-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="91537-107">EXAMPLES</span></span>

### <span data-ttu-id="91537-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="91537-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzureRmManagementPartner -PartnerId 123457 -PassThru
true
```

<span data-ttu-id="91537-109">Yönetim ortağını kaldır</span><span class="sxs-lookup"><span data-stu-id="91537-109">Remove management partner</span></span> 

## <span data-ttu-id="91537-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="91537-110">PARAMETERS</span></span>

### <span data-ttu-id="91537-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91537-111">-DefaultProfile</span></span>
<span data-ttu-id="91537-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="91537-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91537-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="91537-113">-PartnerId</span></span>
<span data-ttu-id="91537-114">Yönetim ortağı kimliği olan 6 basamaklı bir sayıdır</span><span class="sxs-lookup"><span data-stu-id="91537-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="91537-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="91537-115">-PassThru</span></span>
<span data-ttu-id="91537-116">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="91537-116">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91537-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="91537-117">-Confirm</span></span>
<span data-ttu-id="91537-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="91537-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91537-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91537-119">-WhatIf</span></span>
<span data-ttu-id="91537-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="91537-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91537-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="91537-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91537-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91537-122">CommonParameters</span></span>
<span data-ttu-id="91537-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="91537-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91537-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91537-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91537-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="91537-125">INPUTS</span></span>

### <span data-ttu-id="91537-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="91537-126">None</span></span>

## <span data-ttu-id="91537-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="91537-127">OUTPUTS</span></span>

### <span data-ttu-id="91537-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="91537-128">System.Boolean</span></span>

## <span data-ttu-id="91537-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="91537-129">NOTES</span></span>

## <span data-ttu-id="91537-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="91537-130">RELATED LINKS</span></span>

[<span data-ttu-id="91537-131">Yeni-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="91537-131">New-AzureRmManagementPartner</span></span>](./New-AzureRmManagementPartner.md)

[<span data-ttu-id="91537-132">Get-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="91537-132">Get-AzureRmManagementPartner</span></span>](./Get-AzureRmManagementPartner.md)

[<span data-ttu-id="91537-133">Güncelleştirme-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="91537-133">Update-AzureRmManagementPartner</span></span>](./Update-AzureRmManagementPartner.md)
