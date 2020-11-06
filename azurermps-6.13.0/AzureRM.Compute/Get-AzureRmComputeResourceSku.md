---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
ms.openlocfilehash: cf10674f3140e618b82b40e6c8288126cb941c3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588573"
---
# <span data-ttu-id="18bd0-101">Get-AzureRmComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="18bd0-101">Get-AzureRmComputeResourceSku</span></span>

## <span data-ttu-id="18bd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18bd0-102">SYNOPSIS</span></span>
<span data-ttu-id="18bd0-103">Tüm hesaplama kaynak SKU 'Larını Listele</span><span class="sxs-lookup"><span data-stu-id="18bd0-103">List all compute resource Skus</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18bd0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="18bd0-104">SYNTAX</span></span>

```
Get-AzureRmComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18bd0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="18bd0-105">DESCRIPTION</span></span>
<span data-ttu-id="18bd0-106">Tüm hesaplama kaynak SKU 'Larını Listele</span><span class="sxs-lookup"><span data-stu-id="18bd0-106">List all compute resource Skus</span></span>

## <span data-ttu-id="18bd0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="18bd0-107">EXAMPLES</span></span>

### <span data-ttu-id="18bd0-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="18bd0-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzureRmComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="18bd0-109">Batı ABD bölgesindeki tüm hesaplama kaynak SKU 'larını Listele</span><span class="sxs-lookup"><span data-stu-id="18bd0-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="18bd0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="18bd0-110">PARAMETERS</span></span>

### <span data-ttu-id="18bd0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18bd0-111">-DefaultProfile</span></span>
<span data-ttu-id="18bd0-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="18bd0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18bd0-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18bd0-113">CommonParameters</span></span>
<span data-ttu-id="18bd0-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="18bd0-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18bd0-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18bd0-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18bd0-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="18bd0-116">INPUTS</span></span>

### <span data-ttu-id="18bd0-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="18bd0-117">None</span></span>

## <span data-ttu-id="18bd0-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="18bd0-118">OUTPUTS</span></span>

### <span data-ttu-id="18bd0-119">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="18bd0-119">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="18bd0-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="18bd0-120">NOTES</span></span>

## <span data-ttu-id="18bd0-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="18bd0-121">RELATED LINKS</span></span>
