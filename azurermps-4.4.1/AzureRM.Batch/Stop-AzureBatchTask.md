---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 1EA57372-6FA5-45C9-94A1-50D53830FC10
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
ms.openlocfilehash: ac63bbdb95551ff5ff08661a92f0924d5853ade5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592248"
---
# <span data-ttu-id="6ab55-101">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="6ab55-101">Stop-AzureBatchTask</span></span>

## <span data-ttu-id="6ab55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ab55-102">SYNOPSIS</span></span>
<span data-ttu-id="6ab55-103">Toplu Iş görevini durdurur.</span><span class="sxs-lookup"><span data-stu-id="6ab55-103">Stops a Batch task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ab55-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6ab55-104">SYNTAX</span></span>

### <span data-ttu-id="6ab55-105">Kimliğe</span><span class="sxs-lookup"><span data-stu-id="6ab55-105">Id</span></span>
```
Stop-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ab55-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="6ab55-106">InputObject</span></span>
```
Stop-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ab55-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6ab55-107">DESCRIPTION</span></span>
<span data-ttu-id="6ab55-108">**Stop-AzureBatchTask** cmdlet 'ı bir Azure toplu görevini durdurur.</span><span class="sxs-lookup"><span data-stu-id="6ab55-108">The **Stop-AzureBatchTask** cmdlet stops an Azure Batch task.</span></span>

## <span data-ttu-id="6ab55-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6ab55-109">EXAMPLES</span></span>

### <span data-ttu-id="6ab55-110">Örnek 1: KIMLIĞE göre toplu görev silme</span><span class="sxs-lookup"><span data-stu-id="6ab55-110">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Stop-AzureBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="6ab55-111">Bu komut, kimliği Iş-000001 olan işin altında KIMLIK Task23 olan bir görevi durdurur.</span><span class="sxs-lookup"><span data-stu-id="6ab55-111">This command stops a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="6ab55-112">Komut sizden onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6ab55-112">The command prompts you for confirmation.</span></span>
<span data-ttu-id="6ab55-113">$Context değişkenine bağlam atamak için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6ab55-113">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="6ab55-114">Örnek 2: bir toplu Iş görevini ardışık düzen kullanarak durdurma</span><span class="sxs-lookup"><span data-stu-id="6ab55-114">Example 2: Stop a Batch task by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Stop-AzureBatchTask -BatchContext $Context
```

<span data-ttu-id="6ab55-115">Bu komut, Get-AzureBatchTask cmdlet 'ini kullanarak KIMLIĞI Iş-000001 olan Task26 KIMLIĞINE sahip toplu görevi alır.</span><span class="sxs-lookup"><span data-stu-id="6ab55-115">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the Get-AzureBatchTask cmdlet.</span></span>
<span data-ttu-id="6ab55-116">Komut, ardışık düzen işlecini kullanarak bu görevi geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="6ab55-116">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6ab55-117">Komut bu görevi durdurur.</span><span class="sxs-lookup"><span data-stu-id="6ab55-117">The command stops that task.</span></span>

## <span data-ttu-id="6ab55-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6ab55-118">PARAMETERS</span></span>

### <span data-ttu-id="6ab55-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6ab55-119">-BatchContext</span></span>
<span data-ttu-id="6ab55-120">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ab55-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6ab55-121">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6ab55-121">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="6ab55-122">-ID</span><span class="sxs-lookup"><span data-stu-id="6ab55-122">-Id</span></span>
<span data-ttu-id="6ab55-123">Bu cmdlet 'in durduğu görevin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ab55-123">Specifies the ID of the task that this cmdlet stops.</span></span>

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

### <span data-ttu-id="6ab55-124">-JobId</span><span class="sxs-lookup"><span data-stu-id="6ab55-124">-JobId</span></span>
<span data-ttu-id="6ab55-125">Görevi içeren işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ab55-125">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="6ab55-126">-Görev</span><span class="sxs-lookup"><span data-stu-id="6ab55-126">-Task</span></span>
<span data-ttu-id="6ab55-127">Bu cmdlet 'in durduğu görevi belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ab55-127">Specifies the task that this cmdlet stops.</span></span>
<span data-ttu-id="6ab55-128">Bir **Ince görev** nesnesi edinmek için Get-AzureBatchTask cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6ab55-128">To obtain a **PSCloudTask** object, use the Get-AzureBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="6ab55-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ab55-129">-DefaultProfile</span></span>
<span data-ttu-id="6ab55-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6ab55-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ab55-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ab55-131">CommonParameters</span></span>
<span data-ttu-id="6ab55-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6ab55-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ab55-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ab55-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ab55-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6ab55-134">INPUTS</span></span>

### <span data-ttu-id="6ab55-135">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6ab55-135">BatchAccountContext</span></span>
<span data-ttu-id="6ab55-136">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="6ab55-136">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="6ab55-137">Ince görev</span><span class="sxs-lookup"><span data-stu-id="6ab55-137">PSCloudTask</span></span>
<span data-ttu-id="6ab55-138">Parametre ' görev ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="6ab55-138">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="6ab55-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6ab55-139">OUTPUTS</span></span>

## <span data-ttu-id="6ab55-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6ab55-140">NOTES</span></span>

## <span data-ttu-id="6ab55-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6ab55-141">RELATED LINKS</span></span>

[<span data-ttu-id="6ab55-142">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="6ab55-142">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="6ab55-143">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="6ab55-143">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="6ab55-144">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="6ab55-144">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="6ab55-145">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="6ab55-145">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


