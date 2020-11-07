---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
ms.openlocfilehash: e1eb586ff23f5f56cd9fc117f5039d3ccc841367
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591432"
---
# <span data-ttu-id="7304c-101">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7304c-101">Disable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="7304c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7304c-102">SYNOPSIS</span></span>
<span data-ttu-id="7304c-103">Toplu iş çizelgesini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="7304c-103">Disables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7304c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7304c-104">SYNTAX</span></span>

```
Disable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7304c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7304c-105">DESCRIPTION</span></span>
<span data-ttu-id="7304c-106">**Disable-AzureBatchJobSchedule** cmdlet 'ı bir Azure toplu iş çizelgesini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="7304c-106">The **Disable-AzureBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="7304c-107">Bir zamanlamayı devre dışı bırakırsanız, işler bu zamanlamaya göre oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="7304c-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="7304c-108">Devre dışı bir zamanlamayı daha sonra etkinleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7304c-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="7304c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7304c-109">EXAMPLES</span></span>

### <span data-ttu-id="7304c-110">Örnek 1: iş çizelgesini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="7304c-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="7304c-111">Bu komut, KIMLIĞI JobSchedule17 olan iş zamanlamasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="7304c-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="7304c-112">$Context değişkenine bağlam atamak için **Get-AzureRmBatchAccountKeys** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7304c-112">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="7304c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7304c-113">PARAMETERS</span></span>

### <span data-ttu-id="7304c-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="7304c-114">-BatchContext</span></span>
<span data-ttu-id="7304c-115">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7304c-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7304c-116">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7304c-116">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="7304c-117">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="7304c-117">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="7304c-118">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7304c-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="7304c-119">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7304c-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="7304c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7304c-120">-DefaultProfile</span></span>
<span data-ttu-id="7304c-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7304c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7304c-122">-ID</span><span class="sxs-lookup"><span data-stu-id="7304c-122">-Id</span></span>
<span data-ttu-id="7304c-123">Bu cmdlet 'in devre dışı olduğu iş zamanlamasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="7304c-123">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

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

### <span data-ttu-id="7304c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7304c-124">CommonParameters</span></span>
<span data-ttu-id="7304c-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7304c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7304c-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7304c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7304c-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7304c-127">INPUTS</span></span>

### <span data-ttu-id="7304c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7304c-128">System.String</span></span>

### <span data-ttu-id="7304c-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7304c-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="7304c-130">Parametreler: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7304c-130">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="7304c-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7304c-131">OUTPUTS</span></span>

### <span data-ttu-id="7304c-132">System. void</span><span class="sxs-lookup"><span data-stu-id="7304c-132">System.Void</span></span>

## <span data-ttu-id="7304c-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7304c-133">NOTES</span></span>

## <span data-ttu-id="7304c-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7304c-134">RELATED LINKS</span></span>

[<span data-ttu-id="7304c-135">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7304c-135">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="7304c-136">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="7304c-136">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="7304c-137">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7304c-137">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="7304c-138">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7304c-138">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="7304c-139">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7304c-139">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="7304c-140">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7304c-140">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="7304c-141">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="7304c-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

