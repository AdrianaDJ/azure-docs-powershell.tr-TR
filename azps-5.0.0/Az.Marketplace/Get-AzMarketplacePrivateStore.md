---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/get-azmarketplaceprivatestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStore.md
ms.openlocfilehash: fcd59eb37a518cc4f6cd0b5d1c580706d2f6e8bd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278639"
---
# <span data-ttu-id="39067-101">Get-AzMarketplacePrivateStore</span><span class="sxs-lookup"><span data-stu-id="39067-101">Get-AzMarketplacePrivateStore</span></span>

## <span data-ttu-id="39067-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39067-102">SYNOPSIS</span></span>
<span data-ttu-id="39067-103">Özel mağaza listesi al</span><span class="sxs-lookup"><span data-stu-id="39067-103">Get private store list</span></span>

## <span data-ttu-id="39067-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="39067-104">SYNTAX</span></span>

```
Get-AzMarketplacePrivateStore [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39067-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="39067-105">DESCRIPTION</span></span>
<span data-ttu-id="39067-106">Kiracı kapsamı altında oluşturulmuş özel mağaza listesini alma</span><span class="sxs-lookup"><span data-stu-id="39067-106">Get private store list that were created under tenant scope</span></span>

## <span data-ttu-id="39067-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="39067-107">EXAMPLES</span></span>

### <span data-ttu-id="39067-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="39067-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStore


Availability   : enabled
PrivateStoreId : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
ETag           : "47006253-0000-0100-0000-5ecb6df90000"
Id             : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d
Name           : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
Type           : Microsoft.Marketplace/privateStores
```

<span data-ttu-id="39067-109">Kiracı kapsamı altında oluşturulmuş özel mağaza listesi</span><span class="sxs-lookup"><span data-stu-id="39067-109">private store list that were created under tenant scope</span></span>

## <span data-ttu-id="39067-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="39067-110">PARAMETERS</span></span>

### <span data-ttu-id="39067-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39067-111">-DefaultProfile</span></span>
<span data-ttu-id="39067-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="39067-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39067-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39067-113">CommonParameters</span></span>
<span data-ttu-id="39067-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="39067-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39067-115">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="39067-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39067-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="39067-116">INPUTS</span></span>

### <span data-ttu-id="39067-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="39067-117">None</span></span>

## <span data-ttu-id="39067-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="39067-118">OUTPUTS</span></span>

### <span data-ttu-id="39067-119">Microsoft. Azure. Commands. Market. modeller. PrivateStore. PSPrivateStore</span><span class="sxs-lookup"><span data-stu-id="39067-119">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStore</span></span>

## <span data-ttu-id="39067-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="39067-120">NOTES</span></span>

## <span data-ttu-id="39067-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="39067-121">RELATED LINKS</span></span>
