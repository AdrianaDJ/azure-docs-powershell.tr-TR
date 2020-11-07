---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPool.md
ms.openlocfilehash: d18a6bdc9a2064e21507c909005692d5d21c63f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591804"
---
# <span data-ttu-id="af4df-101">Set-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="af4df-101">Set-AzureBatchPool</span></span>

## <span data-ttu-id="af4df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af4df-102">SYNOPSIS</span></span>
<span data-ttu-id="af4df-103">Havuzun özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="af4df-103">Updates the properties of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af4df-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="af4df-104">SYNTAX</span></span>

```
Set-AzureBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af4df-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="af4df-105">DESCRIPTION</span></span>
<span data-ttu-id="af4df-106">**Set-AzureBatchPool** cmdlet 'ı, Azure toplu iş hizmetindeki bir havuzun özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="af4df-106">The **Set-AzureBatchPool** cmdlet updates the properties of a pool in the Azure Batch service.</span></span>
<span data-ttu-id="af4df-107">Bir **Pscses havuzu** nesnesi almak için Get-AzureBatchPool cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="af4df-107">Use the Get-AzureBatchPool cmdlet to get a **PSCloudPool** object.</span></span>
<span data-ttu-id="af4df-108">Bu nesnenin özelliklerini değiştirin ve değişikliklerinizi toplu Iş hizmetine uygulamak için geçerli cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="af4df-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="af4df-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="af4df-109">EXAMPLES</span></span>

### <span data-ttu-id="af4df-110">Örnek 1: havuz güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="af4df-110">Example 1: Update a pool</span></span>
```
PS C:\>$Pool = Get-AzureBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzureBatchPool -Pool $Pool -BatchContext $Context
```

<span data-ttu-id="af4df-111">İlk komut **Get-AzureBatchPool** kullanarak havuzu alır ve $Pool değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="af4df-111">The first command gets a pool by using **Get-AzureBatchPool** , and then stores it in the $Pool variable.</span></span>

<span data-ttu-id="af4df-112">Sonraki üç komut $Pool nesnedeki başlangıç görevi belirtimini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="af4df-112">The next three commands modify the start task specification on the $Pool object.</span></span>

<span data-ttu-id="af4df-113">Son komutu, toplu Iş hizmetini $Pool yerel nesneyle eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="af4df-113">The final command updates the Batch service to match the local object in $Pool.</span></span>

## <span data-ttu-id="af4df-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="af4df-114">PARAMETERS</span></span>

### <span data-ttu-id="af4df-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="af4df-115">-BatchContext</span></span>
<span data-ttu-id="af4df-116">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="af4df-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="af4df-117">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="af4df-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="af4df-118">-Havuz</span><span class="sxs-lookup"><span data-stu-id="af4df-118">-Pool</span></span>
<span data-ttu-id="af4df-119">Bu cmdlet 'in toplu Iş hizmetini güncelleştirdiği **Pschoparlör havuzunu** belirtir.</span><span class="sxs-lookup"><span data-stu-id="af4df-119">Specifies the **PSCloudPool** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="af4df-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af4df-120">-DefaultProfile</span></span>
<span data-ttu-id="af4df-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="af4df-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af4df-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af4df-122">CommonParameters</span></span>
<span data-ttu-id="af4df-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="af4df-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af4df-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af4df-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af4df-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="af4df-125">INPUTS</span></span>

### <span data-ttu-id="af4df-126">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="af4df-126">BatchAccountContext</span></span>
<span data-ttu-id="af4df-127">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="af4df-127">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="af4df-128">Pscses havuzu</span><span class="sxs-lookup"><span data-stu-id="af4df-128">PSCloudPool</span></span>
<span data-ttu-id="af4df-129">Parametre ' havuz ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="af4df-129">Parameter 'Pool' accepts value of type 'PSCloudPool' from the pipeline</span></span>

## <span data-ttu-id="af4df-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="af4df-130">OUTPUTS</span></span>

## <span data-ttu-id="af4df-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="af4df-131">NOTES</span></span>

## <span data-ttu-id="af4df-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="af4df-132">RELATED LINKS</span></span>

[<span data-ttu-id="af4df-133">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="af4df-133">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="af4df-134">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="af4df-134">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="af4df-135">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="af4df-135">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="af4df-136">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="af4df-136">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="af4df-137">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="af4df-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

