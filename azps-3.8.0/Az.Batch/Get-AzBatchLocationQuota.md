---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A39A415A-B403-48D3-AF80-CF7CFE382577
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchlocationquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
ms.openlocfilehash: 5c20529e174e37bd4d9d5d3f60b56c448206d09e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104132"
---
# <span data-ttu-id="824aa-101">Get-AzBatchLocationQuota</span><span class="sxs-lookup"><span data-stu-id="824aa-101">Get-AzBatchLocationQuota</span></span>

## <span data-ttu-id="824aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="824aa-102">SYNOPSIS</span></span>
<span data-ttu-id="824aa-103">Aboneliğiniz için toplu Iş hizmeti kotalarını verilen konumda alır.</span><span class="sxs-lookup"><span data-stu-id="824aa-103">Gets the Batch service quotas for your subscription at the given location.</span></span>

## <span data-ttu-id="824aa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="824aa-104">SYNTAX</span></span>

```
Get-AzBatchLocationQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="824aa-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="824aa-105">DESCRIPTION</span></span>
<span data-ttu-id="824aa-106">Belirtilen aboneliğin toplu hizmet kotalarını belirtilen konumda alır.</span><span class="sxs-lookup"><span data-stu-id="824aa-106">Gets the Batch service quotas for the specified subscription at the given location.</span></span>

## <span data-ttu-id="824aa-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="824aa-107">EXAMPLES</span></span>

### <span data-ttu-id="824aa-108">Örnek 1: Batı ABD bölgesindeki aboneliğin toplu hizmet kotalarını alma</span><span class="sxs-lookup"><span data-stu-id="824aa-108">Example 1: Get the Batch service quotas for the subscription in the West US region</span></span>
```
PS C:\>Get-AzBatchLocationQuota -Location "westus"
          AccountQuota Location
          ------------ --------
          1            westus
```

<span data-ttu-id="824aa-109">Bu komut, Batı ABD bölgesindeki geçerli aboneliğin kotalarını alır.</span><span class="sxs-lookup"><span data-stu-id="824aa-109">This command gets the quotas for the current subscription in the West US region.</span></span>
<span data-ttu-id="824aa-110">Dönüş değeri, bu aboneliğin bu bölgede yalnızca bir toplu hesap oluşturabildiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="824aa-110">The return value indicates that this subscription can create only one Batch account in that region.</span></span>

## <span data-ttu-id="824aa-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="824aa-111">PARAMETERS</span></span>

### <span data-ttu-id="824aa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="824aa-112">-DefaultProfile</span></span>
<span data-ttu-id="824aa-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="824aa-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="824aa-114">-Konum</span><span class="sxs-lookup"><span data-stu-id="824aa-114">-Location</span></span>
<span data-ttu-id="824aa-115">Bu cmdlet 'in kotaları denetlediği bölgeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="824aa-115">Specifies the region for which this cmdlet checks the quotas.</span></span>
<span data-ttu-id="824aa-116">Daha fazla bilgi için bkz https://azure.microsoft.com/regions) .</span><span class="sxs-lookup"><span data-stu-id="824aa-116">For more information, see Azure Regions (https://azure.microsoft.com/regions).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="824aa-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="824aa-117">CommonParameters</span></span>
<span data-ttu-id="824aa-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="824aa-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="824aa-119">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="824aa-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="824aa-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="824aa-120">INPUTS</span></span>

### <span data-ttu-id="824aa-121">System. String</span><span class="sxs-lookup"><span data-stu-id="824aa-121">System.String</span></span>

## <span data-ttu-id="824aa-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="824aa-122">OUTPUTS</span></span>

### <span data-ttu-id="824aa-123">Microsoft.Azure.Commands.Batch. Modeller. PSBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="824aa-123">Microsoft.Azure.Commands.Batch.Models.PSBatchLocationQuotas</span></span>

## <span data-ttu-id="824aa-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="824aa-124">NOTES</span></span>

## <span data-ttu-id="824aa-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="824aa-125">RELATED LINKS</span></span>
