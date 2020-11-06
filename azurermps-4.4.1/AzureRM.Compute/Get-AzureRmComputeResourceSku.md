---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
ms.openlocfilehash: fd4a06375a4dfab7f8b8cd4b08a2112310e99b73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594311"
---
# <span data-ttu-id="66027-101">Get-AzureRmComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="66027-101">Get-AzureRmComputeResourceSku</span></span>

## <span data-ttu-id="66027-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66027-102">SYNOPSIS</span></span>
<span data-ttu-id="66027-103">Tüm hesaplama kaynak SKU 'Larını Listele</span><span class="sxs-lookup"><span data-stu-id="66027-103">List all compute resource Skus</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66027-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="66027-104">SYNTAX</span></span>

```
Get-AzureRmComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66027-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="66027-105">DESCRIPTION</span></span>
<span data-ttu-id="66027-106">Tüm hesaplama kaynak SKU 'Larını Listele</span><span class="sxs-lookup"><span data-stu-id="66027-106">List all compute resource Skus</span></span>

## <span data-ttu-id="66027-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="66027-107">EXAMPLES</span></span>

### <span data-ttu-id="66027-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="66027-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzureRmComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="66027-109">Batı ABD bölgesindeki tüm hesaplama kaynak SKU 'larını Listele</span><span class="sxs-lookup"><span data-stu-id="66027-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="66027-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="66027-110">PARAMETERS</span></span>

### <span data-ttu-id="66027-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66027-111">-DefaultProfile</span></span>
<span data-ttu-id="66027-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="66027-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66027-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66027-113">CommonParameters</span></span>
<span data-ttu-id="66027-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="66027-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66027-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66027-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66027-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="66027-116">INPUTS</span></span>

### <span data-ttu-id="66027-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="66027-117">None</span></span>

## <span data-ttu-id="66027-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="66027-118">OUTPUTS</span></span>

### <span data-ttu-id="66027-119">System. Object</span><span class="sxs-lookup"><span data-stu-id="66027-119">System.Object</span></span>

## <span data-ttu-id="66027-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="66027-120">NOTES</span></span>

## <span data-ttu-id="66027-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="66027-121">RELATED LINKS</span></span>

