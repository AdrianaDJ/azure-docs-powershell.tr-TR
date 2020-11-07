---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
ms.openlocfilehash: 74af4f7c4bc4f211f22be111bff4ecf0a8b9831a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917555"
---
# <span data-ttu-id="b8c4d-101">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="b8c4d-101">Set-AzCdnOrigin</span></span>

## <span data-ttu-id="b8c4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8c4d-102">SYNOPSIS</span></span>
<span data-ttu-id="b8c4d-103">CDN kaynak sunucusunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b8c4d-103">Updates a CDN origin server.</span></span>

## <span data-ttu-id="b8c4d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b8c4d-104">SYNTAX</span></span>

```
Set-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8c4d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b8c4d-105">DESCRIPTION</span></span>
<span data-ttu-id="b8c4d-106">**Set-Azcdnorigın** cmdlet 'i, bir Azure Içerik teslim ağı (CDN) kaynak sunucusunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b8c4d-106">The **Set-AzCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="b8c4d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b8c4d-107">EXAMPLES</span></span>

## <span data-ttu-id="b8c4d-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b8c4d-108">PARAMETERS</span></span>

### <span data-ttu-id="b8c4d-109">-Cdnorigın</span><span class="sxs-lookup"><span data-stu-id="b8c4d-109">-CdnOrigin</span></span>
<span data-ttu-id="b8c4d-110">Bu cmdlet 'in güncelleştirdiği kaynak sunucuyu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b8c4d-110">Specifies the origin server that this cmdlet updates.</span></span>

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

### <span data-ttu-id="b8c4d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8c4d-111">-DefaultProfile</span></span>
<span data-ttu-id="b8c4d-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b8c4d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8c4d-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8c4d-113">CommonParameters</span></span>
<span data-ttu-id="b8c4d-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b8c4d-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8c4d-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8c4d-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8c4d-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b8c4d-116">INPUTS</span></span>

### <span data-ttu-id="b8c4d-117">Microsoft. Azure. Commands. CDN. model. Origin. Psorigın</span><span class="sxs-lookup"><span data-stu-id="b8c4d-117">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="b8c4d-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b8c4d-118">OUTPUTS</span></span>

### <span data-ttu-id="b8c4d-119">Microsoft. Azure. Commands. CDN. model. Origin. Psorigın</span><span class="sxs-lookup"><span data-stu-id="b8c4d-119">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="b8c4d-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b8c4d-120">NOTES</span></span>

## <span data-ttu-id="b8c4d-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b8c4d-121">RELATED LINKS</span></span>

[<span data-ttu-id="b8c4d-122">Get-Azcdnorigın</span><span class="sxs-lookup"><span data-stu-id="b8c4d-122">Get-AzCdnOrigin</span></span>](./Get-AzCdnOrigin.md)


