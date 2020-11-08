---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: 970cbb3e03a4934f648df2f6f8c06275a30740de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108154"
---
# <span data-ttu-id="077c2-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="077c2-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="077c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="077c2-102">SYNOPSIS</span></span>
<span data-ttu-id="077c2-103">Tüm hesaplama kaynak SKU 'Larını Listele</span><span class="sxs-lookup"><span data-stu-id="077c2-103">List all compute resource Skus</span></span>

## <span data-ttu-id="077c2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="077c2-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="077c2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="077c2-105">DESCRIPTION</span></span>
<span data-ttu-id="077c2-106">Tüm hesaplama kaynak SKU 'Larını Listele</span><span class="sxs-lookup"><span data-stu-id="077c2-106">List all compute resource Skus</span></span>

## <span data-ttu-id="077c2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="077c2-107">EXAMPLES</span></span>

### <span data-ttu-id="077c2-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="077c2-108">Example 1</span></span>
```
PS C:\> Get-AzComputeResourceSku "westus";
```

<span data-ttu-id="077c2-109">Batı ABD bölgesindeki tüm hesaplama kaynak SKU 'larını Listele</span><span class="sxs-lookup"><span data-stu-id="077c2-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="077c2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="077c2-110">PARAMETERS</span></span>

### <span data-ttu-id="077c2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="077c2-111">-DefaultProfile</span></span>
<span data-ttu-id="077c2-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="077c2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="077c2-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="077c2-113">-Location</span></span>
<span data-ttu-id="077c2-114">Listedeki kullanılabilir SKU 'ların konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="077c2-114">Specifies a location of the available skus to list.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="077c2-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="077c2-115">CommonParameters</span></span>
<span data-ttu-id="077c2-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="077c2-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="077c2-117">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="077c2-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="077c2-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="077c2-118">INPUTS</span></span>

### <span data-ttu-id="077c2-119">System. String</span><span class="sxs-lookup"><span data-stu-id="077c2-119">System.String</span></span>

## <span data-ttu-id="077c2-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="077c2-120">OUTPUTS</span></span>

### <span data-ttu-id="077c2-121">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="077c2-121">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="077c2-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="077c2-122">NOTES</span></span>

## <span data-ttu-id="077c2-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="077c2-123">RELATED LINKS</span></span>
