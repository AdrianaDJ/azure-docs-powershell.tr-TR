---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
ms.openlocfilehash: eb15991e0bf7aefd60b53dbb02785a1b2004cb22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594820"
---
# <span data-ttu-id="b9fb9-101">Set-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b9fb9-101">Set-AzureBatchJob</span></span>

## <span data-ttu-id="b9fb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9fb9-102">SYNOPSIS</span></span>
<span data-ttu-id="b9fb9-103">Toplu işlemi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b9fb9-103">Updates a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9fb9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b9fb9-104">SYNTAX</span></span>

```
Set-AzureBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9fb9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b9fb9-105">DESCRIPTION</span></span>
<span data-ttu-id="b9fb9-106">**Set-AzureBatchJob** cmdlet 'ı bir Azure toplu işlemini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b9fb9-106">The **Set-AzureBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="b9fb9-107">Bir **Ince iş** nesnesi almak için Get-AzureBatchJob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b9fb9-107">Use the Get-AzureBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="b9fb9-108">Bu nesnenin özelliklerini değiştirin ve değişikliklerinizi toplu Iş hizmetine uygulamak için geçerli cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="b9fb9-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="b9fb9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b9fb9-109">EXAMPLES</span></span>

### <span data-ttu-id="b9fb9-110">Örnek 1: iş güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="b9fb9-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzureBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzureBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="b9fb9-111">İlk komut **Get-AzureBatchJob** kullanarak havuzu alır ve $Job değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b9fb9-111">The first command gets a pool by using **Get-AzureBatchJob** , and then stores it in the $Job variable.</span></span>

<span data-ttu-id="b9fb9-112">İkinci komut $Job nesnesindeki öncelik belirtimini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b9fb9-112">The second command modifies the priority specification on the $Job object.</span></span>

<span data-ttu-id="b9fb9-113">Son komutu, toplu Iş hizmetini $Job yerel nesneyle eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b9fb9-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="b9fb9-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b9fb9-114">PARAMETERS</span></span>

### <span data-ttu-id="b9fb9-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b9fb9-115">-BatchContext</span></span>
<span data-ttu-id="b9fb9-116">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b9fb9-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b9fb9-117">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b9fb9-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="b9fb9-118">-Job</span><span class="sxs-lookup"><span data-stu-id="b9fb9-118">-Job</span></span>
<span data-ttu-id="b9fb9-119">Bu cmdlet 'in toplu iş hizmetini güncelleştirdiği bir **Pscses işi** belirtir.</span><span class="sxs-lookup"><span data-stu-id="b9fb9-119">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9fb9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9fb9-120">-DefaultProfile</span></span>
<span data-ttu-id="b9fb9-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b9fb9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9fb9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9fb9-122">CommonParameters</span></span>
<span data-ttu-id="b9fb9-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b9fb9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9fb9-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9fb9-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9fb9-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b9fb9-125">INPUTS</span></span>

### <span data-ttu-id="b9fb9-126">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b9fb9-126">BatchAccountContext</span></span>
<span data-ttu-id="b9fb9-127">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="b9fb9-127">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="b9fb9-128">Pschoparlör Işi</span><span class="sxs-lookup"><span data-stu-id="b9fb9-128">PSCloudJob</span></span>
<span data-ttu-id="b9fb9-129">Parametre ' Iş ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="b9fb9-129">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="b9fb9-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b9fb9-130">OUTPUTS</span></span>

## <span data-ttu-id="b9fb9-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b9fb9-131">NOTES</span></span>

## <span data-ttu-id="b9fb9-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b9fb9-132">RELATED LINKS</span></span>

[<span data-ttu-id="b9fb9-133">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b9fb9-133">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="b9fb9-134">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b9fb9-134">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="b9fb9-135">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b9fb9-135">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="b9fb9-136">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b9fb9-136">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="b9fb9-137">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b9fb9-137">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="b9fb9-138">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b9fb9-138">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="b9fb9-139">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b9fb9-139">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="b9fb9-140">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="b9fb9-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


