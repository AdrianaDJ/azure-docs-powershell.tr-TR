---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPool.md
ms.openlocfilehash: 9f9b2a406d5fc728e9297fc4093a60b3f6ec4bf8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592944"
---
# <span data-ttu-id="580b5-101">Set-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="580b5-101">Set-AzureBatchPool</span></span>

## <span data-ttu-id="580b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="580b5-102">SYNOPSIS</span></span>
<span data-ttu-id="580b5-103">Havuzun özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="580b5-103">Updates the properties of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="580b5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="580b5-104">SYNTAX</span></span>

```
Set-AzureBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="580b5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="580b5-105">DESCRIPTION</span></span>
<span data-ttu-id="580b5-106">**Set-AzureBatchPool** cmdlet 'ı, Azure toplu iş hizmetindeki bir havuzun özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="580b5-106">The **Set-AzureBatchPool** cmdlet updates the properties of a pool in the Azure Batch service.</span></span>
<span data-ttu-id="580b5-107">Bir **Pscses havuzu** nesnesi almak için Get-AzureBatchPool cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="580b5-107">Use the Get-AzureBatchPool cmdlet to get a **PSCloudPool** object.</span></span>
<span data-ttu-id="580b5-108">Bu nesnenin özelliklerini değiştirin ve değişikliklerinizi toplu Iş hizmetine uygulamak için geçerli cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="580b5-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="580b5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="580b5-109">EXAMPLES</span></span>

### <span data-ttu-id="580b5-110">Örnek 1: havuz güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="580b5-110">Example 1: Update a pool</span></span>
```
PS C:\>$Pool = Get-AzureBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzureBatchPool -Pool $Pool -BatchContext $Context
```

<span data-ttu-id="580b5-111">İlk komut **Get-AzureBatchPool** kullanarak havuzu alır ve $Pool değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="580b5-111">The first command gets a pool by using **Get-AzureBatchPool** , and then stores it in the $Pool variable.</span></span>

<span data-ttu-id="580b5-112">Sonraki üç komut $Pool nesnedeki başlangıç görevi belirtimini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="580b5-112">The next three commands modify the start task specification on the $Pool object.</span></span>

<span data-ttu-id="580b5-113">Son komutu, toplu Iş hizmetini $Pool yerel nesneyle eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="580b5-113">The final command updates the Batch service to match the local object in $Pool.</span></span>

## <span data-ttu-id="580b5-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="580b5-114">PARAMETERS</span></span>

### <span data-ttu-id="580b5-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="580b5-115">-BatchContext</span></span>
<span data-ttu-id="580b5-116">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="580b5-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="580b5-117">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="580b5-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="580b5-118">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="580b5-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="580b5-119">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="580b5-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="580b5-120">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="580b5-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="580b5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="580b5-121">-DefaultProfile</span></span>
<span data-ttu-id="580b5-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="580b5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="580b5-123">-Havuz</span><span class="sxs-lookup"><span data-stu-id="580b5-123">-Pool</span></span>
<span data-ttu-id="580b5-124">Bu cmdlet 'in toplu Iş hizmetini güncelleştirdiği **Pschoparlör havuzunu** belirtir.</span><span class="sxs-lookup"><span data-stu-id="580b5-124">Specifies the **PSCloudPool** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: PSCloudPool
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="580b5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="580b5-125">CommonParameters</span></span>
<span data-ttu-id="580b5-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="580b5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="580b5-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="580b5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="580b5-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="580b5-128">INPUTS</span></span>

### <span data-ttu-id="580b5-129">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="580b5-129">BatchAccountContext</span></span>
<span data-ttu-id="580b5-130">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="580b5-130">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="580b5-131">Pscses havuzu</span><span class="sxs-lookup"><span data-stu-id="580b5-131">PSCloudPool</span></span>
<span data-ttu-id="580b5-132">Parametre ' havuz ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="580b5-132">Parameter 'Pool' accepts value of type 'PSCloudPool' from the pipeline</span></span>

## <span data-ttu-id="580b5-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="580b5-133">OUTPUTS</span></span>

## <span data-ttu-id="580b5-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="580b5-134">NOTES</span></span>

## <span data-ttu-id="580b5-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="580b5-135">RELATED LINKS</span></span>

[<span data-ttu-id="580b5-136">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="580b5-136">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="580b5-137">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="580b5-137">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="580b5-138">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="580b5-138">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="580b5-139">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="580b5-139">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="580b5-140">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="580b5-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


