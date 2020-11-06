---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/set-azurermcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnOrigin.md
ms.openlocfilehash: 395ee4b20ae2c26d05ad66489b3c643d0f4245a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591380"
---
# <span data-ttu-id="f22ad-101">Set-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="f22ad-101">Set-AzureRmCdnOrigin</span></span>

## <span data-ttu-id="f22ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f22ad-102">SYNOPSIS</span></span>
<span data-ttu-id="f22ad-103">CDN kaynak sunucusunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f22ad-103">Updates a CDN origin server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f22ad-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f22ad-104">SYNTAX</span></span>

```
Set-AzureRmCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f22ad-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f22ad-105">DESCRIPTION</span></span>
<span data-ttu-id="f22ad-106">**Set-Azurermcvseçnorigın** cmdlet 'i, bir Azure Içerik teslim ağı (CDN) kaynak sunucusunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f22ad-106">The **Set-AzureRmCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="f22ad-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f22ad-107">EXAMPLES</span></span>

## <span data-ttu-id="f22ad-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f22ad-108">PARAMETERS</span></span>

### <span data-ttu-id="f22ad-109">-Cdnorigın</span><span class="sxs-lookup"><span data-stu-id="f22ad-109">-CdnOrigin</span></span>
<span data-ttu-id="f22ad-110">Bu cmdlet 'in güncelleştirdiği kaynak sunucuyu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f22ad-110">Specifies the origin server that this cmdlet updates.</span></span>

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

### <span data-ttu-id="f22ad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f22ad-111">-DefaultProfile</span></span>
<span data-ttu-id="f22ad-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f22ad-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f22ad-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f22ad-113">CommonParameters</span></span>
<span data-ttu-id="f22ad-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f22ad-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f22ad-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f22ad-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f22ad-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f22ad-116">INPUTS</span></span>

### <span data-ttu-id="f22ad-117">Microsoft. Azure. Commands. CDN. model. Origin. Psorigın</span><span class="sxs-lookup"><span data-stu-id="f22ad-117">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>
<span data-ttu-id="f22ad-118">Parametreler: Cdnorigın (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f22ad-118">Parameters: CdnOrigin (ByValue)</span></span>

## <span data-ttu-id="f22ad-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f22ad-119">OUTPUTS</span></span>

### <span data-ttu-id="f22ad-120">Microsoft. Azure. Commands. CDN. model. Origin. Psorigın</span><span class="sxs-lookup"><span data-stu-id="f22ad-120">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="f22ad-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f22ad-121">NOTES</span></span>

## <span data-ttu-id="f22ad-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f22ad-122">RELATED LINKS</span></span>

[<span data-ttu-id="f22ad-123">Get-Azurermcvseçnorigın</span><span class="sxs-lookup"><span data-stu-id="f22ad-123">Get-AzureRmCdnOrigin</span></span>](./Get-AzureRmCdnOrigin.md)


