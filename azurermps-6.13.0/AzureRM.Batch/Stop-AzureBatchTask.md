---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 1EA57372-6FA5-45C9-94A1-50D53830FC10
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
ms.openlocfilehash: 18a96a72cc965f5e93a035ba6ed7b91ba5419edf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592333"
---
# <span data-ttu-id="17504-101">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="17504-101">Stop-AzureBatchTask</span></span>

## <span data-ttu-id="17504-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17504-102">SYNOPSIS</span></span>
<span data-ttu-id="17504-103">Toplu Iş görevini durdurur.</span><span class="sxs-lookup"><span data-stu-id="17504-103">Stops a Batch task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17504-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="17504-104">SYNTAX</span></span>

### <span data-ttu-id="17504-105">Kimliğe</span><span class="sxs-lookup"><span data-stu-id="17504-105">Id</span></span>
```
Stop-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17504-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="17504-106">InputObject</span></span>
```
Stop-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17504-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="17504-107">DESCRIPTION</span></span>
<span data-ttu-id="17504-108">**Stop-AzureBatchTask** cmdlet 'ı bir Azure toplu görevini durdurur.</span><span class="sxs-lookup"><span data-stu-id="17504-108">The **Stop-AzureBatchTask** cmdlet stops an Azure Batch task.</span></span>

## <span data-ttu-id="17504-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="17504-109">EXAMPLES</span></span>

### <span data-ttu-id="17504-110">Örnek 1: KIMLIĞE göre toplu görev silme</span><span class="sxs-lookup"><span data-stu-id="17504-110">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Stop-AzureBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="17504-111">Bu komut, kimliği Iş-000001 olan işin altında KIMLIK Task23 olan bir görevi durdurur.</span><span class="sxs-lookup"><span data-stu-id="17504-111">This command stops a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="17504-112">Komut sizden onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="17504-112">The command prompts you for confirmation.</span></span>
<span data-ttu-id="17504-113">$Context değişkenine bağlam atamak için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="17504-113">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="17504-114">Örnek 2: bir toplu Iş görevini ardışık düzen kullanarak durdurma</span><span class="sxs-lookup"><span data-stu-id="17504-114">Example 2: Stop a Batch task by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Stop-AzureBatchTask -BatchContext $Context
```

<span data-ttu-id="17504-115">Bu komut, Get-AzureBatchTask cmdlet 'ini kullanarak KIMLIĞI Iş-000001 olan Task26 KIMLIĞINE sahip toplu görevi alır.</span><span class="sxs-lookup"><span data-stu-id="17504-115">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the Get-AzureBatchTask cmdlet.</span></span>
<span data-ttu-id="17504-116">Komut, ardışık düzen işlecini kullanarak bu görevi geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="17504-116">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="17504-117">Komut bu görevi durdurur.</span><span class="sxs-lookup"><span data-stu-id="17504-117">The command stops that task.</span></span>

## <span data-ttu-id="17504-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="17504-118">PARAMETERS</span></span>

### <span data-ttu-id="17504-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="17504-119">-BatchContext</span></span>
<span data-ttu-id="17504-120">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="17504-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="17504-121">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="17504-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="17504-122">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="17504-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="17504-123">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="17504-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="17504-124">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="17504-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="17504-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17504-125">-DefaultProfile</span></span>
<span data-ttu-id="17504-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="17504-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17504-127">-ID</span><span class="sxs-lookup"><span data-stu-id="17504-127">-Id</span></span>
<span data-ttu-id="17504-128">Bu cmdlet 'in durduğu görevin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="17504-128">Specifies the ID of the task that this cmdlet stops.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17504-129">-JobId</span><span class="sxs-lookup"><span data-stu-id="17504-129">-JobId</span></span>
<span data-ttu-id="17504-130">Görevi içeren işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="17504-130">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17504-131">-Görev</span><span class="sxs-lookup"><span data-stu-id="17504-131">-Task</span></span>
<span data-ttu-id="17504-132">Bu cmdlet 'in durduğu görevi belirtir.</span><span class="sxs-lookup"><span data-stu-id="17504-132">Specifies the task that this cmdlet stops.</span></span>
<span data-ttu-id="17504-133">Bir **Ince görev** nesnesi edinmek için Get-AzureBatchTask cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="17504-133">To obtain a **PSCloudTask** object, use the Get-AzureBatchTask cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17504-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17504-134">CommonParameters</span></span>
<span data-ttu-id="17504-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="17504-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17504-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17504-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17504-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="17504-137">INPUTS</span></span>

### <span data-ttu-id="17504-138">System. String</span><span class="sxs-lookup"><span data-stu-id="17504-138">System.String</span></span>

### <span data-ttu-id="17504-139">Microsoft.Azure.Commands.Batch. Modeller. Ince görev</span><span class="sxs-lookup"><span data-stu-id="17504-139">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>
<span data-ttu-id="17504-140">Parametreler: görev (ByValue)</span><span class="sxs-lookup"><span data-stu-id="17504-140">Parameters: Task (ByValue)</span></span>

### <span data-ttu-id="17504-141">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="17504-141">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="17504-142">Parametreler: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="17504-142">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="17504-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="17504-143">OUTPUTS</span></span>

### <span data-ttu-id="17504-144">System. void</span><span class="sxs-lookup"><span data-stu-id="17504-144">System.Void</span></span>

## <span data-ttu-id="17504-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="17504-145">NOTES</span></span>

## <span data-ttu-id="17504-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="17504-146">RELATED LINKS</span></span>

[<span data-ttu-id="17504-147">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="17504-147">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="17504-148">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="17504-148">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="17504-149">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="17504-149">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="17504-150">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="17504-150">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


