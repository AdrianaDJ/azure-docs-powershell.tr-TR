---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
ms.openlocfilehash: 9635031d6eaea5a7920a6862fb8cf20ce536c1db
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098310"
---
# <span data-ttu-id="7ada6-101">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="7ada6-101">Set-AzCdnOrigin</span></span>

## <span data-ttu-id="7ada6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ada6-102">SYNOPSIS</span></span>
<span data-ttu-id="7ada6-103">CDN kaynak sunucusunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7ada6-103">Updates a CDN origin server.</span></span>

## <span data-ttu-id="7ada6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7ada6-104">SYNTAX</span></span>

```
Set-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ada6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7ada6-105">DESCRIPTION</span></span>
<span data-ttu-id="7ada6-106">**Set-Azcdnorigın** cmdlet 'i, bir Azure Içerik teslim ağı (CDN) kaynak sunucusunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7ada6-106">The **Set-AzCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="7ada6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7ada6-107">EXAMPLES</span></span>

## <span data-ttu-id="7ada6-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7ada6-108">PARAMETERS</span></span>

### <span data-ttu-id="7ada6-109">-Cdnorigın</span><span class="sxs-lookup"><span data-stu-id="7ada6-109">-CdnOrigin</span></span>
<span data-ttu-id="7ada6-110">Bu cmdlet 'in güncelleştirdiği kaynak sunucuyu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7ada6-110">Specifies the origin server that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ada6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ada6-111">-DefaultProfile</span></span>
<span data-ttu-id="7ada6-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7ada6-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7ada6-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ada6-113">CommonParameters</span></span>
<span data-ttu-id="7ada6-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7ada6-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ada6-115">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7ada6-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ada6-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7ada6-116">INPUTS</span></span>

### <span data-ttu-id="7ada6-117">Microsoft. Azure. Commands. CDN. model. Origin. Psorigın</span><span class="sxs-lookup"><span data-stu-id="7ada6-117">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="7ada6-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7ada6-118">OUTPUTS</span></span>

### <span data-ttu-id="7ada6-119">Microsoft. Azure. Commands. CDN. model. Origin. Psorigın</span><span class="sxs-lookup"><span data-stu-id="7ada6-119">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="7ada6-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7ada6-120">NOTES</span></span>

## <span data-ttu-id="7ada6-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7ada6-121">RELATED LINKS</span></span>

[<span data-ttu-id="7ada6-122">Get-Azcdnorigın</span><span class="sxs-lookup"><span data-stu-id="7ada6-122">Get-AzCdnOrigin</span></span>](./Get-AzCdnOrigin.md)


