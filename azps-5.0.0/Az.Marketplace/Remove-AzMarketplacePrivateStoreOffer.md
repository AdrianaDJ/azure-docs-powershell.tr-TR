---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/remove-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: 93c7a1e580d85201465c460740e3d6e327db22aa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278636"
---
# <span data-ttu-id="bb623-101">Remove-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="bb623-101">Remove-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="bb623-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb623-102">SYNOPSIS</span></span>
<span data-ttu-id="bb623-103">Özel mağazadan bir teklifi kaldırma.</span><span class="sxs-lookup"><span data-stu-id="bb623-103">Remove an offer from private store.</span></span>

## <span data-ttu-id="bb623-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bb623-104">SYNTAX</span></span>

```
Remove-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb623-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bb623-105">DESCRIPTION</span></span>
<span data-ttu-id="bb623-106">Kiracı kapsamında oluşturulmuş özel mağazadan bir teklifi kaldırın.</span><span class="sxs-lookup"><span data-stu-id="bb623-106">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="bb623-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bb623-107">EXAMPLES</span></span>

### <span data-ttu-id="bb623-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bb623-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid
```

<span data-ttu-id="bb623-109">Kiracı kapsamında oluşturulmuş özel mağazadan bir teklifi kaldırın.</span><span class="sxs-lookup"><span data-stu-id="bb623-109">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="bb623-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bb623-110">PARAMETERS</span></span>

### <span data-ttu-id="bb623-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb623-111">-DefaultProfile</span></span>
<span data-ttu-id="bb623-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bb623-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb623-113">-OfferId</span><span class="sxs-lookup"><span data-stu-id="bb623-113">-OfferId</span></span>
<span data-ttu-id="bb623-114">Gerekli Azure Market privateStore teklifi</span><span class="sxs-lookup"><span data-stu-id="bb623-114">Required Azure Marketplace privateStore offer</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb623-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="bb623-115">-PassThru</span></span>
<span data-ttu-id="bb623-116">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="bb623-116">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="bb623-117">-Privatestoreıd</span><span class="sxs-lookup"><span data-stu-id="bb623-117">-PrivateStoreId</span></span>
<span data-ttu-id="bb623-118">Gerekli Azure Market privateStore</span><span class="sxs-lookup"><span data-stu-id="bb623-118">Required Azure Marketplace privateStore</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb623-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="bb623-119">-Confirm</span></span>
<span data-ttu-id="bb623-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bb623-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb623-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb623-121">-WhatIf</span></span>
<span data-ttu-id="bb623-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bb623-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb623-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bb623-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb623-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb623-124">CommonParameters</span></span>
<span data-ttu-id="bb623-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bb623-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb623-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bb623-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb623-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bb623-127">INPUTS</span></span>

### <span data-ttu-id="bb623-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="bb623-128">None</span></span>

## <span data-ttu-id="bb623-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bb623-129">OUTPUTS</span></span>

### <span data-ttu-id="bb623-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bb623-130">System.Boolean</span></span>

## <span data-ttu-id="bb623-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bb623-131">NOTES</span></span>

## <span data-ttu-id="bb623-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bb623-132">RELATED LINKS</span></span>
