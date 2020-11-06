---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
ms.openlocfilehash: be73b757bf20a2f688d7f7293ac4022e7bc8f4aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591423"
---
# <span data-ttu-id="a0504-101">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a0504-101">Enable-AzureBatchJob</span></span>

## <span data-ttu-id="a0504-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0504-102">SYNOPSIS</span></span>
<span data-ttu-id="a0504-103">Toplu işi etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="a0504-103">Enables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0504-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a0504-104">SYNTAX</span></span>

```
Enable-AzureBatchJob [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0504-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a0504-105">DESCRIPTION</span></span>
<span data-ttu-id="a0504-106">**Enable-AzureBatchJob** cmdlet 'ı bir Azure toplu işine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="a0504-106">The **Enable-AzureBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="a0504-107">İşi etkinleştirdikten sonra yeni görevler çalıştırılabilir.</span><span class="sxs-lookup"><span data-stu-id="a0504-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="a0504-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a0504-108">EXAMPLES</span></span>

### <span data-ttu-id="a0504-109">Örnek 1: bir toplu işi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="a0504-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzureBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="a0504-110">Bu komut, Iş-000001 KIMLIĞINE sahip işi etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="a0504-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="a0504-111">$Context değişkenine bağlam atamak için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a0504-111">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="a0504-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a0504-112">PARAMETERS</span></span>

### <span data-ttu-id="a0504-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a0504-113">-BatchContext</span></span>
<span data-ttu-id="a0504-114">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0504-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a0504-115">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a0504-115">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a0504-116">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="a0504-116">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a0504-117">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a0504-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a0504-118">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a0504-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a0504-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0504-119">-DefaultProfile</span></span>
<span data-ttu-id="a0504-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a0504-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0504-121">-ID</span><span class="sxs-lookup"><span data-stu-id="a0504-121">-Id</span></span>
<span data-ttu-id="a0504-122">Bu cmdlet 'in etkinleştirmesine iş KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0504-122">Specifies the ID of the job that this cmdlet enables.</span></span>

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

### <span data-ttu-id="a0504-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0504-123">CommonParameters</span></span>
<span data-ttu-id="a0504-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a0504-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0504-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0504-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0504-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a0504-126">INPUTS</span></span>

### <span data-ttu-id="a0504-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a0504-127">System.String</span></span>

### <span data-ttu-id="a0504-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a0504-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="a0504-129">Parametreler: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a0504-129">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="a0504-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a0504-130">OUTPUTS</span></span>

### <span data-ttu-id="a0504-131">System. void</span><span class="sxs-lookup"><span data-stu-id="a0504-131">System.Void</span></span>

## <span data-ttu-id="a0504-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a0504-132">NOTES</span></span>

## <span data-ttu-id="a0504-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a0504-133">RELATED LINKS</span></span>

[<span data-ttu-id="a0504-134">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a0504-134">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="a0504-135">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a0504-135">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="a0504-136">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a0504-136">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="a0504-137">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a0504-137">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="a0504-138">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a0504-138">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="a0504-139">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="a0504-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


