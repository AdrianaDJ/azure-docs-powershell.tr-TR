---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
ms.openlocfilehash: 8db1f11cfd434beb52eb32e4b175b2dab67ecbdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763175"
---
# <span data-ttu-id="991bc-101">Stop-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="991bc-101">Stop-AzureBatchPoolResize</span></span>

## <span data-ttu-id="991bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="991bc-102">SYNOPSIS</span></span>
<span data-ttu-id="991bc-103">Havuz yeniden boyutlandırma işlemini durdurur.</span><span class="sxs-lookup"><span data-stu-id="991bc-103">Stops a pool resize operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="991bc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="991bc-104">SYNTAX</span></span>

```
Stop-AzureBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="991bc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="991bc-105">DESCRIPTION</span></span>
<span data-ttu-id="991bc-106">**Stop-AzureBatchPoolResize** cmdlet 'i, havuzda bir Azure toplu yeniden boyutlandırma işlemini durdurur.</span><span class="sxs-lookup"><span data-stu-id="991bc-106">The **Stop-AzureBatchPoolResize** cmdlet stops an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="991bc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="991bc-107">EXAMPLES</span></span>

### <span data-ttu-id="991bc-108">Örnek 1: havuzu yeniden boyutlandırmayı durdurma</span><span class="sxs-lookup"><span data-stu-id="991bc-108">Example 1: Stop resizing a pool</span></span>
```
PS C:\>Stop-AzureBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

<span data-ttu-id="991bc-109">Bu komut, ContosoPool06 KIMLIĞINE sahip havuzda yeniden boyutlandırma işlemini durdurur.</span><span class="sxs-lookup"><span data-stu-id="991bc-109">This command stops a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="991bc-110">$Context değişkenine bağlam atamak için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="991bc-110">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="991bc-111">Örnek 2: ardışık düzeni kullanarak havuzu yeniden boyutlandırmayı durdurma</span><span class="sxs-lookup"><span data-stu-id="991bc-111">Example 2: Stop resizing a pool by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzureBatchPoolResize -BatchContext $Context
```

<span data-ttu-id="991bc-112">Bu komut, ardışık düzen işlecini kullanarak havuzu yeniden boyutlandırmayı durdurur.</span><span class="sxs-lookup"><span data-stu-id="991bc-112">This command stops resizing a pool by using the pipeline operator.</span></span>
<span data-ttu-id="991bc-113">Komut, Get-AzureBatchPool cmdlet 'ini kullanarak KIMLIĞI ContosoPool06 olan havuzu alır.</span><span class="sxs-lookup"><span data-stu-id="991bc-113">The command gets the pool that has the ID ContosoPool06 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="991bc-114">Komut bu havuz nesnesini geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="991bc-114">The command passes that pool object to the current cmdlet.</span></span>
<span data-ttu-id="991bc-115">Komut bu havuzda yeniden boyutlandırma işlemini durdurur.</span><span class="sxs-lookup"><span data-stu-id="991bc-115">The command stops the resize operation on that pool.</span></span>

## <span data-ttu-id="991bc-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="991bc-116">PARAMETERS</span></span>

### <span data-ttu-id="991bc-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="991bc-117">-BatchContext</span></span>
<span data-ttu-id="991bc-118">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="991bc-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="991bc-119">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="991bc-119">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="991bc-120">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="991bc-120">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="991bc-121">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="991bc-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="991bc-122">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="991bc-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="991bc-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="991bc-123">-DefaultProfile</span></span>
<span data-ttu-id="991bc-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="991bc-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="991bc-125">-ID</span><span class="sxs-lookup"><span data-stu-id="991bc-125">-Id</span></span>
<span data-ttu-id="991bc-126">Bu cmdlet 'in yeniden boyutlandırma işlemini durdurduğu havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="991bc-126">Specifies the ID of the pool for which this cmdlet stops a resizing operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="991bc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="991bc-127">CommonParameters</span></span>
<span data-ttu-id="991bc-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="991bc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="991bc-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="991bc-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="991bc-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="991bc-130">INPUTS</span></span>

### <span data-ttu-id="991bc-131">System. String</span><span class="sxs-lookup"><span data-stu-id="991bc-131">System.String</span></span>

### <span data-ttu-id="991bc-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="991bc-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="991bc-133">Parametreler: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="991bc-133">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="991bc-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="991bc-134">OUTPUTS</span></span>

### <span data-ttu-id="991bc-135">System. void</span><span class="sxs-lookup"><span data-stu-id="991bc-135">System.Void</span></span>

## <span data-ttu-id="991bc-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="991bc-136">NOTES</span></span>

## <span data-ttu-id="991bc-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="991bc-137">RELATED LINKS</span></span>

[<span data-ttu-id="991bc-138">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="991bc-138">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="991bc-139">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="991bc-139">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="991bc-140">Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="991bc-140">Start-AzureBatchPoolResize</span></span>](./Start-AzureBatchPoolResize.md)

[<span data-ttu-id="991bc-141">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="991bc-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


