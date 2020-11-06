---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
ms.openlocfilehash: a878002c509fd2a895f61a97af1bef2afebc3691
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593736"
---
# <span data-ttu-id="72336-101">Set-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="72336-101">Set-AzureBatchJob</span></span>

## <span data-ttu-id="72336-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72336-102">SYNOPSIS</span></span>
<span data-ttu-id="72336-103">Toplu işlemi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="72336-103">Updates a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72336-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="72336-104">SYNTAX</span></span>

```
Set-AzureBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72336-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="72336-105">DESCRIPTION</span></span>
<span data-ttu-id="72336-106">**Set-AzureBatchJob** cmdlet 'ı bir Azure toplu işlemini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="72336-106">The **Set-AzureBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="72336-107">Bir **Ince iş** nesnesi almak için Get-AzureBatchJob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="72336-107">Use the Get-AzureBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="72336-108">Bu nesnenin özelliklerini değiştirin ve değişikliklerinizi toplu Iş hizmetine uygulamak için geçerli cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="72336-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="72336-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="72336-109">EXAMPLES</span></span>

### <span data-ttu-id="72336-110">Örnek 1: iş güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="72336-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzureBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzureBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="72336-111">İlk komut **Get-AzureBatchJob** kullanarak havuzu alır ve $Job değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="72336-111">The first command gets a pool by using **Get-AzureBatchJob** , and then stores it in the $Job variable.</span></span>

<span data-ttu-id="72336-112">İkinci komut $Job nesnesindeki öncelik belirtimini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="72336-112">The second command modifies the priority specification on the $Job object.</span></span>

<span data-ttu-id="72336-113">Son komutu, toplu Iş hizmetini $Job yerel nesneyle eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="72336-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="72336-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="72336-114">PARAMETERS</span></span>

### <span data-ttu-id="72336-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="72336-115">-BatchContext</span></span>
<span data-ttu-id="72336-116">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="72336-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="72336-117">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="72336-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="72336-118">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="72336-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="72336-119">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="72336-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="72336-120">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="72336-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="72336-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72336-121">-DefaultProfile</span></span>
<span data-ttu-id="72336-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="72336-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72336-123">-Job</span><span class="sxs-lookup"><span data-stu-id="72336-123">-Job</span></span>
<span data-ttu-id="72336-124">Bu cmdlet 'in toplu iş hizmetini güncelleştirdiği bir **Pscses işi** belirtir.</span><span class="sxs-lookup"><span data-stu-id="72336-124">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: PSCloudJob
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72336-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72336-125">CommonParameters</span></span>
<span data-ttu-id="72336-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="72336-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72336-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72336-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72336-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="72336-128">INPUTS</span></span>

### <span data-ttu-id="72336-129">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="72336-129">BatchAccountContext</span></span>
<span data-ttu-id="72336-130">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="72336-130">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="72336-131">Pschoparlör Işi</span><span class="sxs-lookup"><span data-stu-id="72336-131">PSCloudJob</span></span>
<span data-ttu-id="72336-132">Parametre ' Iş ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="72336-132">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="72336-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="72336-133">OUTPUTS</span></span>

## <span data-ttu-id="72336-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="72336-134">NOTES</span></span>

## <span data-ttu-id="72336-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="72336-135">RELATED LINKS</span></span>

[<span data-ttu-id="72336-136">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="72336-136">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="72336-137">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="72336-137">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="72336-138">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="72336-138">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="72336-139">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="72336-139">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="72336-140">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="72336-140">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="72336-141">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="72336-141">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="72336-142">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="72336-142">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="72336-143">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="72336-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


