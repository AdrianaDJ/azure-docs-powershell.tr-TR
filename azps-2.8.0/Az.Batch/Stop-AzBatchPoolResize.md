---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
ms.openlocfilehash: 9e970251671297a6fa4a0019bb663c9e34cbe4d7
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93938634"
---
# <span data-ttu-id="b9588-101">Stop-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="b9588-101">Stop-AzBatchPoolResize</span></span>

## <span data-ttu-id="b9588-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9588-102">SYNOPSIS</span></span>
<span data-ttu-id="b9588-103">Havuz yeniden boyutlandırma işlemini durdurur.</span><span class="sxs-lookup"><span data-stu-id="b9588-103">Stops a pool resize operation.</span></span>

## <span data-ttu-id="b9588-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b9588-104">SYNTAX</span></span>

```
Stop-AzBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9588-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b9588-105">DESCRIPTION</span></span>
<span data-ttu-id="b9588-106">**Stop-AzBatchPoolResize** cmdlet 'i, havuzda bir Azure toplu yeniden boyutlandırma işlemini durdurur.</span><span class="sxs-lookup"><span data-stu-id="b9588-106">The **Stop-AzBatchPoolResize** cmdlet stops an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="b9588-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b9588-107">EXAMPLES</span></span>

### <span data-ttu-id="b9588-108">Örnek 1: havuzu yeniden boyutlandırmayı durdurma</span><span class="sxs-lookup"><span data-stu-id="b9588-108">Example 1: Stop resizing a pool</span></span>
```
PS C:\>Stop-AzBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

<span data-ttu-id="b9588-109">Bu komut, ContosoPool06 KIMLIĞINE sahip havuzda yeniden boyutlandırma işlemini durdurur.</span><span class="sxs-lookup"><span data-stu-id="b9588-109">This command stops a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="b9588-110">$Context değişkenine bağlam atamak için Get-AzBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b9588-110">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="b9588-111">Örnek 2: ardışık düzeni kullanarak havuzu yeniden boyutlandırmayı durdurma</span><span class="sxs-lookup"><span data-stu-id="b9588-111">Example 2: Stop resizing a pool by using the pipeline</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzBatchPoolResize -BatchContext $Context
```

<span data-ttu-id="b9588-112">Bu komut, ardışık düzen işlecini kullanarak havuzu yeniden boyutlandırmayı durdurur.</span><span class="sxs-lookup"><span data-stu-id="b9588-112">This command stops resizing a pool by using the pipeline operator.</span></span>
<span data-ttu-id="b9588-113">Komut, Get-AzBatchPool cmdlet 'ini kullanarak KIMLIĞI ContosoPool06 olan havuzu alır.</span><span class="sxs-lookup"><span data-stu-id="b9588-113">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="b9588-114">Komut bu havuz nesnesini geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="b9588-114">The command passes that pool object to the current cmdlet.</span></span>
<span data-ttu-id="b9588-115">Komut bu havuzda yeniden boyutlandırma işlemini durdurur.</span><span class="sxs-lookup"><span data-stu-id="b9588-115">The command stops the resize operation on that pool.</span></span>

## <span data-ttu-id="b9588-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b9588-116">PARAMETERS</span></span>

### <span data-ttu-id="b9588-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b9588-117">-BatchContext</span></span>
<span data-ttu-id="b9588-118">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b9588-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b9588-119">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b9588-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b9588-120">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="b9588-120">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b9588-121">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b9588-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b9588-122">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b9588-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b9588-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9588-123">-DefaultProfile</span></span>
<span data-ttu-id="b9588-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b9588-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9588-125">-ID</span><span class="sxs-lookup"><span data-stu-id="b9588-125">-Id</span></span>
<span data-ttu-id="b9588-126">Bu cmdlet 'in yeniden boyutlandırma işlemini durdurduğu havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b9588-126">Specifies the ID of the pool for which this cmdlet stops a resizing operation.</span></span>

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

### <span data-ttu-id="b9588-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9588-127">CommonParameters</span></span>
<span data-ttu-id="b9588-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b9588-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9588-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9588-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9588-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b9588-130">INPUTS</span></span>

### <span data-ttu-id="b9588-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b9588-131">System.String</span></span>

### <span data-ttu-id="b9588-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b9588-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b9588-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b9588-133">OUTPUTS</span></span>

### <span data-ttu-id="b9588-134">System. void</span><span class="sxs-lookup"><span data-stu-id="b9588-134">System.Void</span></span>

## <span data-ttu-id="b9588-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b9588-135">NOTES</span></span>

## <span data-ttu-id="b9588-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b9588-136">RELATED LINKS</span></span>

[<span data-ttu-id="b9588-137">Get-Aztopluaccountkeys</span><span class="sxs-lookup"><span data-stu-id="b9588-137">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="b9588-138">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="b9588-138">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="b9588-139">Start-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="b9588-139">Start-AzBatchPoolResize</span></span>](./Start-AzBatchPoolResize.md)

[<span data-ttu-id="b9588-140">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="b9588-140">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


