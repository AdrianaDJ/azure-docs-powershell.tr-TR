---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 1EA57372-6FA5-45C9-94A1-50D53830FC10
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchTask.md
ms.openlocfilehash: 7d1b3b05f3432a5fc512c7dff03eb51c4223701d
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "94107230"
---
# <span data-ttu-id="d61f4-101">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="d61f4-101">Stop-AzBatchTask</span></span>

## <span data-ttu-id="d61f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d61f4-102">SYNOPSIS</span></span>
<span data-ttu-id="d61f4-103">Toplu Iş görevini durdurur.</span><span class="sxs-lookup"><span data-stu-id="d61f4-103">Stops a Batch task.</span></span>

## <span data-ttu-id="d61f4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d61f4-104">SYNTAX</span></span>

### <span data-ttu-id="d61f4-105">Kimliğe</span><span class="sxs-lookup"><span data-stu-id="d61f4-105">Id</span></span>
```
Stop-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d61f4-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d61f4-106">InputObject</span></span>
```
Stop-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d61f4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d61f4-107">DESCRIPTION</span></span>
<span data-ttu-id="d61f4-108">**Stop-AzBatchTask** cmdlet 'ı bir Azure toplu görevini durdurur.</span><span class="sxs-lookup"><span data-stu-id="d61f4-108">The **Stop-AzBatchTask** cmdlet stops an Azure Batch task.</span></span>

## <span data-ttu-id="d61f4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d61f4-109">EXAMPLES</span></span>

### <span data-ttu-id="d61f4-110">Örnek 1: KIMLIĞE göre toplu görev silme</span><span class="sxs-lookup"><span data-stu-id="d61f4-110">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Stop-AzBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="d61f4-111">Bu komut, kimliği Iş-000001 olan işin altında KIMLIK Task23 olan bir görevi durdurur.</span><span class="sxs-lookup"><span data-stu-id="d61f4-111">This command stops a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="d61f4-112">Komut sizden onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d61f4-112">The command prompts you for confirmation.</span></span>
<span data-ttu-id="d61f4-113">$Context değişkenine bağlam atamak için Get-AzBatchAccountKey cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d61f4-113">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="d61f4-114">Örnek 2: bir toplu Iş görevini ardışık düzen kullanarak durdurma</span><span class="sxs-lookup"><span data-stu-id="d61f4-114">Example 2: Stop a Batch task by using the pipeline</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Stop-AzBatchTask -BatchContext $Context
```

<span data-ttu-id="d61f4-115">Bu komut, Get-AzBatchTask cmdlet 'ini kullanarak KIMLIĞI Iş-000001 olan Task26 KIMLIĞINE sahip toplu görevi alır.</span><span class="sxs-lookup"><span data-stu-id="d61f4-115">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the Get-AzBatchTask cmdlet.</span></span>
<span data-ttu-id="d61f4-116">Komut, ardışık düzen işlecini kullanarak bu görevi geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="d61f4-116">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d61f4-117">Komut bu görevi durdurur.</span><span class="sxs-lookup"><span data-stu-id="d61f4-117">The command stops that task.</span></span>

## <span data-ttu-id="d61f4-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d61f4-118">PARAMETERS</span></span>

### <span data-ttu-id="d61f4-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d61f4-119">-BatchContext</span></span>
<span data-ttu-id="d61f4-120">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d61f4-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d61f4-121">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d61f4-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d61f4-122">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKey cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="d61f4-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d61f4-123">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d61f4-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d61f4-124">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d61f4-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d61f4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d61f4-125">-DefaultProfile</span></span>
<span data-ttu-id="d61f4-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d61f4-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d61f4-127">-ID</span><span class="sxs-lookup"><span data-stu-id="d61f4-127">-Id</span></span>
<span data-ttu-id="d61f4-128">Bu cmdlet 'in durduğu görevin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d61f4-128">Specifies the ID of the task that this cmdlet stops.</span></span>

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

### <span data-ttu-id="d61f4-129">-JobId</span><span class="sxs-lookup"><span data-stu-id="d61f4-129">-JobId</span></span>
<span data-ttu-id="d61f4-130">Görevi içeren işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d61f4-130">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="d61f4-131">-Görev</span><span class="sxs-lookup"><span data-stu-id="d61f4-131">-Task</span></span>
<span data-ttu-id="d61f4-132">Bu cmdlet 'in durduğu görevi belirtir.</span><span class="sxs-lookup"><span data-stu-id="d61f4-132">Specifies the task that this cmdlet stops.</span></span>
<span data-ttu-id="d61f4-133">Bir **Ince görev** nesnesi edinmek için Get-AzBatchTask cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d61f4-133">To obtain a **PSCloudTask** object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="d61f4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d61f4-134">CommonParameters</span></span>
<span data-ttu-id="d61f4-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d61f4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d61f4-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d61f4-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d61f4-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d61f4-137">INPUTS</span></span>

### <span data-ttu-id="d61f4-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d61f4-138">System.String</span></span>

### <span data-ttu-id="d61f4-139">Microsoft.Azure.Commands.Batch. Modeller. Ince görev</span><span class="sxs-lookup"><span data-stu-id="d61f4-139">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="d61f4-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d61f4-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d61f4-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d61f4-141">OUTPUTS</span></span>

### <span data-ttu-id="d61f4-142">System. void</span><span class="sxs-lookup"><span data-stu-id="d61f4-142">System.Void</span></span>

## <span data-ttu-id="d61f4-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d61f4-143">NOTES</span></span>

## <span data-ttu-id="d61f4-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d61f4-144">RELATED LINKS</span></span>

[<span data-ttu-id="d61f4-145">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="d61f4-145">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="d61f4-146">Yeni-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="d61f4-146">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="d61f4-147">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="d61f4-147">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="d61f4-148">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="d61f4-148">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


