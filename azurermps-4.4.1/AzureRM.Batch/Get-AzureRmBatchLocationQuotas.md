---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A39A415A-B403-48D3-AF80-CF7CFE382577
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchLocationQuotas.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchLocationQuotas.md
ms.openlocfilehash: 208ba1055523a1dc76de88d665a7b1dbd097144e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590763"
---
# <span data-ttu-id="20287-101">Get-AzureRmBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="20287-101">Get-AzureRmBatchLocationQuotas</span></span>

## <span data-ttu-id="20287-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20287-102">SYNOPSIS</span></span>
<span data-ttu-id="20287-103">Aboneliğiniz için toplu Iş hizmeti kotalarını verilen konumda alır.</span><span class="sxs-lookup"><span data-stu-id="20287-103">Gets the Batch service quotas for your subscription at the given location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20287-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="20287-104">SYNTAX</span></span>

```
Get-AzureRmBatchLocationQuotas [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="20287-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="20287-105">DESCRIPTION</span></span>
<span data-ttu-id="20287-106">Belirtilen aboneliğin toplu hizmet kotalarını belirtilen konumda alır.</span><span class="sxs-lookup"><span data-stu-id="20287-106">Gets the Batch service quotas for the specified subscription at the given location.</span></span>

## <span data-ttu-id="20287-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="20287-107">EXAMPLES</span></span>

### <span data-ttu-id="20287-108">Örnek 1: Batı ABD bölgesindeki aboneliğin toplu hizmet kotalarını alma</span><span class="sxs-lookup"><span data-stu-id="20287-108">Example 1: Get the Batch service quotas for the subscription in the West US region</span></span>
```
PS C:\>Get-AzureRmBatchLocationQuotas -Location "westus"
          AccountQuota Location
          ------------ --------
          1            westus
```

<span data-ttu-id="20287-109">Bu komut, Batı ABD bölgesindeki geçerli aboneliğin kotalarını alır.</span><span class="sxs-lookup"><span data-stu-id="20287-109">This command gets the quotas for the current subscription in the West US region.</span></span>
<span data-ttu-id="20287-110">Dönüş değeri, bu aboneliğin bu bölgede yalnızca bir toplu hesap oluşturabildiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="20287-110">The return value indicates that this subscription can create only one Batch account in that region.</span></span>

## <span data-ttu-id="20287-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="20287-111">PARAMETERS</span></span>

### <span data-ttu-id="20287-112">-Konum</span><span class="sxs-lookup"><span data-stu-id="20287-112">-Location</span></span>
<span data-ttu-id="20287-113">Bu cmdlet 'in kotaları denetlediği bölgeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="20287-113">Specifies the region for which this cmdlet checks the quotas.</span></span>
<span data-ttu-id="20287-114">Daha fazla bilgi için bkz https://azure.microsoft.com/regions) .</span><span class="sxs-lookup"><span data-stu-id="20287-114">For more information, see Azure Regions (https://azure.microsoft.com/regions).</span></span>

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

### <span data-ttu-id="20287-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20287-115">-DefaultProfile</span></span>
<span data-ttu-id="20287-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="20287-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20287-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20287-117">CommonParameters</span></span>
<span data-ttu-id="20287-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="20287-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20287-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20287-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20287-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="20287-120">INPUTS</span></span>

## <span data-ttu-id="20287-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="20287-121">OUTPUTS</span></span>

### <span data-ttu-id="20287-122">Microsoft.Azure.Commands.Batch. Modeller. PSBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="20287-122">Microsoft.Azure.Commands.Batch.Models.PSBatchLocationQuotas</span></span>

## <span data-ttu-id="20287-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="20287-123">NOTES</span></span>

## <span data-ttu-id="20287-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="20287-124">RELATED LINKS</span></span>

