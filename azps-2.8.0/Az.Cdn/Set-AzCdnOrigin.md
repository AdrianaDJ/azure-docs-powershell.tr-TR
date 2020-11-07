---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
ms.openlocfilehash: 71f5732f7473a90af0509d2e3932ca5151ef870a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753048"
---
# <span data-ttu-id="b67f7-101">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="b67f7-101">Set-AzCdnOrigin</span></span>

## <span data-ttu-id="b67f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b67f7-102">SYNOPSIS</span></span>
<span data-ttu-id="b67f7-103">CDN kaynak sunucusunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b67f7-103">Updates a CDN origin server.</span></span>

## <span data-ttu-id="b67f7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b67f7-104">SYNTAX</span></span>

```
Set-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b67f7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b67f7-105">DESCRIPTION</span></span>
<span data-ttu-id="b67f7-106">**Set-Azcdnorigın** cmdlet 'i, bir Azure Içerik teslim ağı (CDN) kaynak sunucusunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b67f7-106">The **Set-AzCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="b67f7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b67f7-107">EXAMPLES</span></span>

## <span data-ttu-id="b67f7-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b67f7-108">PARAMETERS</span></span>

### <span data-ttu-id="b67f7-109">-Cdnorigın</span><span class="sxs-lookup"><span data-stu-id="b67f7-109">-CdnOrigin</span></span>
<span data-ttu-id="b67f7-110">Bu cmdlet 'in güncelleştirdiği kaynak sunucuyu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b67f7-110">Specifies the origin server that this cmdlet updates.</span></span>

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

### <span data-ttu-id="b67f7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b67f7-111">-DefaultProfile</span></span>
<span data-ttu-id="b67f7-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b67f7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b67f7-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b67f7-113">CommonParameters</span></span>
<span data-ttu-id="b67f7-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b67f7-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b67f7-115">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b67f7-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b67f7-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b67f7-116">INPUTS</span></span>

### <span data-ttu-id="b67f7-117">Microsoft. Azure. Commands. CDN. model. Origin. Psorigın</span><span class="sxs-lookup"><span data-stu-id="b67f7-117">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="b67f7-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b67f7-118">OUTPUTS</span></span>

### <span data-ttu-id="b67f7-119">Microsoft. Azure. Commands. CDN. model. Origin. Psorigın</span><span class="sxs-lookup"><span data-stu-id="b67f7-119">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="b67f7-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b67f7-120">NOTES</span></span>

## <span data-ttu-id="b67f7-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b67f7-121">RELATED LINKS</span></span>

[<span data-ttu-id="b67f7-122">Get-Azcdnorigın</span><span class="sxs-lookup"><span data-stu-id="b67f7-122">Get-AzCdnOrigin</span></span>](./Get-AzCdnOrigin.md)


