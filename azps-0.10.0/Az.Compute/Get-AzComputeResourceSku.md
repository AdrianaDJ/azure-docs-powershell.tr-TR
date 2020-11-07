---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: 751a551f5ed0a0a1968c74e5f94bcabad3b5ff32
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937057"
---
# <span data-ttu-id="824d1-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="824d1-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="824d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="824d1-102">SYNOPSIS</span></span>
<span data-ttu-id="824d1-103">Tüm hesaplama kaynak SKU 'Larını Listele</span><span class="sxs-lookup"><span data-stu-id="824d1-103">List all compute resource Skus</span></span>

## <span data-ttu-id="824d1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="824d1-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="824d1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="824d1-105">DESCRIPTION</span></span>
<span data-ttu-id="824d1-106">Tüm hesaplama kaynak SKU 'Larını Listele</span><span class="sxs-lookup"><span data-stu-id="824d1-106">List all compute resource Skus</span></span>

## <span data-ttu-id="824d1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="824d1-107">EXAMPLES</span></span>

### <span data-ttu-id="824d1-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="824d1-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="824d1-109">Batı ABD bölgesindeki tüm hesaplama kaynak SKU 'larını Listele</span><span class="sxs-lookup"><span data-stu-id="824d1-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="824d1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="824d1-110">PARAMETERS</span></span>

### <span data-ttu-id="824d1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="824d1-111">-DefaultProfile</span></span>
<span data-ttu-id="824d1-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="824d1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="824d1-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="824d1-113">CommonParameters</span></span>
<span data-ttu-id="824d1-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="824d1-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="824d1-115">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="824d1-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="824d1-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="824d1-116">INPUTS</span></span>

### <span data-ttu-id="824d1-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="824d1-117">None</span></span>

## <span data-ttu-id="824d1-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="824d1-118">OUTPUTS</span></span>

### <span data-ttu-id="824d1-119">System. Object</span><span class="sxs-lookup"><span data-stu-id="824d1-119">System.Object</span></span>

## <span data-ttu-id="824d1-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="824d1-120">NOTES</span></span>

## <span data-ttu-id="824d1-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="824d1-121">RELATED LINKS</span></span>

