---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A39A415A-B403-48D3-AF80-CF7CFE382577
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchlocationquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
ms.openlocfilehash: 5c20529e174e37bd4d9d5d3f60b56c448206d09e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109837"
---
# <span data-ttu-id="8ea65-101">Get-AzBatchLocationQuota</span><span class="sxs-lookup"><span data-stu-id="8ea65-101">Get-AzBatchLocationQuota</span></span>

## <span data-ttu-id="8ea65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ea65-102">SYNOPSIS</span></span>
<span data-ttu-id="8ea65-103">Aboneliğiniz için toplu Iş hizmeti kotalarını verilen konumda alır.</span><span class="sxs-lookup"><span data-stu-id="8ea65-103">Gets the Batch service quotas for your subscription at the given location.</span></span>

## <span data-ttu-id="8ea65-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8ea65-104">SYNTAX</span></span>

```
Get-AzBatchLocationQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ea65-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8ea65-105">DESCRIPTION</span></span>
<span data-ttu-id="8ea65-106">Belirtilen aboneliğin toplu hizmet kotalarını belirtilen konumda alır.</span><span class="sxs-lookup"><span data-stu-id="8ea65-106">Gets the Batch service quotas for the specified subscription at the given location.</span></span>

## <span data-ttu-id="8ea65-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8ea65-107">EXAMPLES</span></span>

### <span data-ttu-id="8ea65-108">Örnek 1: Batı ABD bölgesindeki aboneliğin toplu hizmet kotalarını alma</span><span class="sxs-lookup"><span data-stu-id="8ea65-108">Example 1: Get the Batch service quotas for the subscription in the West US region</span></span>
```
PS C:\>Get-AzBatchLocationQuota -Location "westus"
          AccountQuota Location
          ------------ --------
          1            westus
```

<span data-ttu-id="8ea65-109">Bu komut, Batı ABD bölgesindeki geçerli aboneliğin kotalarını alır.</span><span class="sxs-lookup"><span data-stu-id="8ea65-109">This command gets the quotas for the current subscription in the West US region.</span></span>
<span data-ttu-id="8ea65-110">Dönüş değeri, bu aboneliğin bu bölgede yalnızca bir toplu hesap oluşturabildiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ea65-110">The return value indicates that this subscription can create only one Batch account in that region.</span></span>

## <span data-ttu-id="8ea65-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8ea65-111">PARAMETERS</span></span>

### <span data-ttu-id="8ea65-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ea65-112">-DefaultProfile</span></span>
<span data-ttu-id="8ea65-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8ea65-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ea65-114">-Konum</span><span class="sxs-lookup"><span data-stu-id="8ea65-114">-Location</span></span>
<span data-ttu-id="8ea65-115">Bu cmdlet 'in kotaları denetlediği bölgeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ea65-115">Specifies the region for which this cmdlet checks the quotas.</span></span>
<span data-ttu-id="8ea65-116">Daha fazla bilgi için bkz https://azure.microsoft.com/regions) .</span><span class="sxs-lookup"><span data-stu-id="8ea65-116">For more information, see Azure Regions (https://azure.microsoft.com/regions).</span></span>

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

### <span data-ttu-id="8ea65-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ea65-117">CommonParameters</span></span>
<span data-ttu-id="8ea65-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8ea65-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ea65-119">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8ea65-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ea65-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8ea65-120">INPUTS</span></span>

### <span data-ttu-id="8ea65-121">System. String</span><span class="sxs-lookup"><span data-stu-id="8ea65-121">System.String</span></span>

## <span data-ttu-id="8ea65-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8ea65-122">OUTPUTS</span></span>

### <span data-ttu-id="8ea65-123">Microsoft.Azure.Commands.Batch. Modeller. PSBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="8ea65-123">Microsoft.Azure.Commands.Batch.Models.PSBatchLocationQuotas</span></span>

## <span data-ttu-id="8ea65-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8ea65-124">NOTES</span></span>

## <span data-ttu-id="8ea65-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8ea65-125">RELATED LINKS</span></span>
