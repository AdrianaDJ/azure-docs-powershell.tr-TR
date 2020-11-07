---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermcomputeresourcesku
schema: 2.0.0
ms.openlocfilehash: e7ebc6a8e6b59679757f559ff2d09ebaa8c5475f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940194"
---
# <span data-ttu-id="0868e-101">Get-AzureRmComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="0868e-101">Get-AzureRmComputeResourceSku</span></span>

## <span data-ttu-id="0868e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0868e-102">SYNOPSIS</span></span>
<span data-ttu-id="0868e-103">Tüm hesaplama kaynak SKU 'Larını Listele</span><span class="sxs-lookup"><span data-stu-id="0868e-103">List all compute resource Skus</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0868e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0868e-104">SYNTAX</span></span>

```
Get-AzureRmComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0868e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0868e-105">DESCRIPTION</span></span>
<span data-ttu-id="0868e-106">Tüm hesaplama kaynak SKU 'Larını Listele</span><span class="sxs-lookup"><span data-stu-id="0868e-106">List all compute resource Skus</span></span>

## <span data-ttu-id="0868e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0868e-107">EXAMPLES</span></span>

### <span data-ttu-id="0868e-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0868e-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzureRmComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="0868e-109">Batı ABD bölgesindeki tüm hesaplama kaynak SKU 'larını Listele</span><span class="sxs-lookup"><span data-stu-id="0868e-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="0868e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0868e-110">PARAMETERS</span></span>

### <span data-ttu-id="0868e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0868e-111">-DefaultProfile</span></span>
<span data-ttu-id="0868e-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0868e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0868e-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0868e-113">CommonParameters</span></span>
<span data-ttu-id="0868e-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0868e-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0868e-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0868e-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0868e-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0868e-116">INPUTS</span></span>

### <span data-ttu-id="0868e-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0868e-117">None</span></span>

## <span data-ttu-id="0868e-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0868e-118">OUTPUTS</span></span>

### <span data-ttu-id="0868e-119">System. Object</span><span class="sxs-lookup"><span data-stu-id="0868e-119">System.Object</span></span>

## <span data-ttu-id="0868e-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0868e-120">NOTES</span></span>

## <span data-ttu-id="0868e-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0868e-121">RELATED LINKS</span></span>

