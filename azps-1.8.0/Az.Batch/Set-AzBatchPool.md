---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
ms.openlocfilehash: 7ab0d9f64b14f6fbdd572f69ecb081114d78891d
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93938602"
---
# <span data-ttu-id="876b9-101">Set-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="876b9-101">Set-AzBatchPool</span></span>

## <span data-ttu-id="876b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="876b9-102">SYNOPSIS</span></span>
<span data-ttu-id="876b9-103">Havuzun özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="876b9-103">Updates the properties of a pool.</span></span>

## <span data-ttu-id="876b9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="876b9-104">SYNTAX</span></span>

```
Set-AzBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="876b9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="876b9-105">DESCRIPTION</span></span>
<span data-ttu-id="876b9-106">**Set-AzBatchPool** cmdlet 'ı, Azure toplu iş hizmetindeki bir havuzun özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="876b9-106">The **Set-AzBatchPool** cmdlet updates the properties of a pool in the Azure Batch service.</span></span>
<span data-ttu-id="876b9-107">Bir **Pscses havuzu** nesnesi almak için Get-AzBatchPool cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="876b9-107">Use the Get-AzBatchPool cmdlet to get a **PSCloudPool** object.</span></span>
<span data-ttu-id="876b9-108">Bu nesnenin özelliklerini değiştirin ve değişikliklerinizi toplu Iş hizmetine uygulamak için geçerli cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="876b9-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="876b9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="876b9-109">EXAMPLES</span></span>

### <span data-ttu-id="876b9-110">Örnek 1: havuz güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="876b9-110">Example 1: Update a pool</span></span>
```
PS C:\>$Pool = Get-AzBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzBatchPool -Pool $Pool -BatchContext $Context
```

<span data-ttu-id="876b9-111">İlk komut **Get-AzBatchPool** kullanarak bir havuz alır ve $Pool değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="876b9-111">The first command gets a pool by using **Get-AzBatchPool** , and then stores it in the $Pool variable.</span></span>
<span data-ttu-id="876b9-112">Sonraki üç komut $Pool nesnedeki başlangıç görevi belirtimini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="876b9-112">The next three commands modify the start task specification on the $Pool object.</span></span>
<span data-ttu-id="876b9-113">Son komutu, toplu Iş hizmetini $Pool yerel nesneyle eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="876b9-113">The final command updates the Batch service to match the local object in $Pool.</span></span>

## <span data-ttu-id="876b9-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="876b9-114">PARAMETERS</span></span>

### <span data-ttu-id="876b9-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="876b9-115">-BatchContext</span></span>
<span data-ttu-id="876b9-116">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="876b9-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="876b9-117">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="876b9-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="876b9-118">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="876b9-118">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="876b9-119">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="876b9-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="876b9-120">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="876b9-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="876b9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="876b9-121">-DefaultProfile</span></span>
<span data-ttu-id="876b9-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="876b9-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="876b9-123">-Havuz</span><span class="sxs-lookup"><span data-stu-id="876b9-123">-Pool</span></span>
<span data-ttu-id="876b9-124">Bu cmdlet 'in toplu Iş hizmetini güncelleştirdiği **Pschoparlör havuzunu** belirtir.</span><span class="sxs-lookup"><span data-stu-id="876b9-124">Specifies the **PSCloudPool** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudPool
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="876b9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="876b9-125">CommonParameters</span></span>
<span data-ttu-id="876b9-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="876b9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="876b9-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="876b9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="876b9-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="876b9-128">INPUTS</span></span>

### <span data-ttu-id="876b9-129">Microsoft.Azure.Commands.Batch. Modeller. Pscses havuzu</span><span class="sxs-lookup"><span data-stu-id="876b9-129">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="876b9-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="876b9-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="876b9-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="876b9-131">OUTPUTS</span></span>

### <span data-ttu-id="876b9-132">System. void</span><span class="sxs-lookup"><span data-stu-id="876b9-132">System.Void</span></span>

## <span data-ttu-id="876b9-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="876b9-133">NOTES</span></span>

## <span data-ttu-id="876b9-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="876b9-134">RELATED LINKS</span></span>

[<span data-ttu-id="876b9-135">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="876b9-135">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="876b9-136">Get-Aztopluaccountkeys</span><span class="sxs-lookup"><span data-stu-id="876b9-136">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="876b9-137">Yeni-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="876b9-137">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="876b9-138">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="876b9-138">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="876b9-139">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="876b9-139">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


