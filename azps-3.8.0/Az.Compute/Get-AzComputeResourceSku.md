---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: ab57e922a7ef63d14a36bbd91ed268822e2c61e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103691"
---
# <span data-ttu-id="abdf4-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="abdf4-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="abdf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abdf4-102">SYNOPSIS</span></span>
<span data-ttu-id="abdf4-103">Tüm hesaplama kaynak SKU 'Larını Listele</span><span class="sxs-lookup"><span data-stu-id="abdf4-103">List all compute resource Skus</span></span>

## <span data-ttu-id="abdf4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="abdf4-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="abdf4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="abdf4-105">DESCRIPTION</span></span>
<span data-ttu-id="abdf4-106">Tüm hesaplama kaynak SKU 'Larını Listele</span><span class="sxs-lookup"><span data-stu-id="abdf4-106">List all compute resource Skus</span></span>

## <span data-ttu-id="abdf4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="abdf4-107">EXAMPLES</span></span>

### <span data-ttu-id="abdf4-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="abdf4-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="abdf4-109">Batı ABD bölgesindeki tüm hesaplama kaynak SKU 'larını Listele</span><span class="sxs-lookup"><span data-stu-id="abdf4-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="abdf4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="abdf4-110">PARAMETERS</span></span>

### <span data-ttu-id="abdf4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abdf4-111">-DefaultProfile</span></span>
<span data-ttu-id="abdf4-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="abdf4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abdf4-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abdf4-113">CommonParameters</span></span>
<span data-ttu-id="abdf4-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="abdf4-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abdf4-115">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="abdf4-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abdf4-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="abdf4-116">INPUTS</span></span>

### <span data-ttu-id="abdf4-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="abdf4-117">None</span></span>

## <span data-ttu-id="abdf4-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="abdf4-118">OUTPUTS</span></span>

### <span data-ttu-id="abdf4-119">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="abdf4-119">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="abdf4-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="abdf4-120">NOTES</span></span>

## <span data-ttu-id="abdf4-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="abdf4-121">RELATED LINKS</span></span>
