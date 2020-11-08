---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
ms.openlocfilehash: dc5267f93845c6e373b5a6b623df710bd19671ba
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "94107232"
---
# <span data-ttu-id="ac625-101">Stop-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="ac625-101">Stop-AzBatchPoolResize</span></span>

## <span data-ttu-id="ac625-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac625-102">SYNOPSIS</span></span>
<span data-ttu-id="ac625-103">Havuz yeniden boyutlandırma işlemini durdurur.</span><span class="sxs-lookup"><span data-stu-id="ac625-103">Stops a pool resize operation.</span></span>

## <span data-ttu-id="ac625-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ac625-104">SYNTAX</span></span>

```
Stop-AzBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac625-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ac625-105">DESCRIPTION</span></span>
<span data-ttu-id="ac625-106">**Stop-AzBatchPoolResize** cmdlet 'i, havuzda bir Azure toplu yeniden boyutlandırma işlemini durdurur.</span><span class="sxs-lookup"><span data-stu-id="ac625-106">The **Stop-AzBatchPoolResize** cmdlet stops an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="ac625-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ac625-107">EXAMPLES</span></span>

### <span data-ttu-id="ac625-108">Örnek 1: havuzu yeniden boyutlandırmayı durdurma</span><span class="sxs-lookup"><span data-stu-id="ac625-108">Example 1: Stop resizing a pool</span></span>
```
PS C:\>Stop-AzBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

<span data-ttu-id="ac625-109">Bu komut, ContosoPool06 KIMLIĞINE sahip havuzda yeniden boyutlandırma işlemini durdurur.</span><span class="sxs-lookup"><span data-stu-id="ac625-109">This command stops a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="ac625-110">$Context değişkenine bağlam atamak için Get-AzBatchAccountKey cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ac625-110">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="ac625-111">Örnek 2: ardışık düzeni kullanarak havuzu yeniden boyutlandırmayı durdurma</span><span class="sxs-lookup"><span data-stu-id="ac625-111">Example 2: Stop resizing a pool by using the pipeline</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzBatchPoolResize -BatchContext $Context
```

<span data-ttu-id="ac625-112">Bu komut, ardışık düzen işlecini kullanarak havuzu yeniden boyutlandırmayı durdurur.</span><span class="sxs-lookup"><span data-stu-id="ac625-112">This command stops resizing a pool by using the pipeline operator.</span></span>
<span data-ttu-id="ac625-113">Komut, Get-AzBatchPool cmdlet 'ini kullanarak KIMLIĞI ContosoPool06 olan havuzu alır.</span><span class="sxs-lookup"><span data-stu-id="ac625-113">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="ac625-114">Komut bu havuz nesnesini geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="ac625-114">The command passes that pool object to the current cmdlet.</span></span>
<span data-ttu-id="ac625-115">Komut bu havuzda yeniden boyutlandırma işlemini durdurur.</span><span class="sxs-lookup"><span data-stu-id="ac625-115">The command stops the resize operation on that pool.</span></span>

## <span data-ttu-id="ac625-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ac625-116">PARAMETERS</span></span>

### <span data-ttu-id="ac625-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ac625-117">-BatchContext</span></span>
<span data-ttu-id="ac625-118">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac625-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ac625-119">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ac625-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ac625-120">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKey cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="ac625-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ac625-121">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ac625-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ac625-122">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ac625-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ac625-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac625-123">-DefaultProfile</span></span>
<span data-ttu-id="ac625-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ac625-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac625-125">-ID</span><span class="sxs-lookup"><span data-stu-id="ac625-125">-Id</span></span>
<span data-ttu-id="ac625-126">Bu cmdlet 'in yeniden boyutlandırma işlemini durdurduğu havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac625-126">Specifies the ID of the pool for which this cmdlet stops a resizing operation.</span></span>

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

### <span data-ttu-id="ac625-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac625-127">CommonParameters</span></span>
<span data-ttu-id="ac625-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ac625-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac625-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ac625-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac625-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ac625-130">INPUTS</span></span>

### <span data-ttu-id="ac625-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ac625-131">System.String</span></span>

### <span data-ttu-id="ac625-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ac625-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ac625-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ac625-133">OUTPUTS</span></span>

### <span data-ttu-id="ac625-134">System. void</span><span class="sxs-lookup"><span data-stu-id="ac625-134">System.Void</span></span>

## <span data-ttu-id="ac625-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ac625-135">NOTES</span></span>

## <span data-ttu-id="ac625-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ac625-136">RELATED LINKS</span></span>

[<span data-ttu-id="ac625-137">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="ac625-137">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="ac625-138">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="ac625-138">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="ac625-139">Start-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="ac625-139">Start-AzBatchPoolResize</span></span>](./Start-AzBatchPoolResize.md)

[<span data-ttu-id="ac625-140">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="ac625-140">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


