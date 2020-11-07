---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: e3c33fb3d61479531303389defb0d7ebdbb3fb64
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917472"
---
# <span data-ttu-id="92b54-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="92b54-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="92b54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92b54-102">SYNOPSIS</span></span>
<span data-ttu-id="92b54-103">Tüm hesaplama kaynak SKU 'Larını Listele</span><span class="sxs-lookup"><span data-stu-id="92b54-103">List all compute resource Skus</span></span>

## <span data-ttu-id="92b54-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="92b54-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92b54-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="92b54-105">DESCRIPTION</span></span>
<span data-ttu-id="92b54-106">Tüm hesaplama kaynak SKU 'Larını Listele</span><span class="sxs-lookup"><span data-stu-id="92b54-106">List all compute resource Skus</span></span>

## <span data-ttu-id="92b54-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="92b54-107">EXAMPLES</span></span>

### <span data-ttu-id="92b54-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="92b54-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="92b54-109">Batı ABD bölgesindeki tüm hesaplama kaynak SKU 'larını Listele</span><span class="sxs-lookup"><span data-stu-id="92b54-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="92b54-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="92b54-110">PARAMETERS</span></span>

### <span data-ttu-id="92b54-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92b54-111">-DefaultProfile</span></span>
<span data-ttu-id="92b54-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="92b54-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92b54-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92b54-113">CommonParameters</span></span>
<span data-ttu-id="92b54-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="92b54-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92b54-115">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="92b54-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92b54-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="92b54-116">INPUTS</span></span>

### <span data-ttu-id="92b54-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="92b54-117">None</span></span>

## <span data-ttu-id="92b54-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="92b54-118">OUTPUTS</span></span>

### <span data-ttu-id="92b54-119">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="92b54-119">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="92b54-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="92b54-120">NOTES</span></span>

## <span data-ttu-id="92b54-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="92b54-121">RELATED LINKS</span></span>
