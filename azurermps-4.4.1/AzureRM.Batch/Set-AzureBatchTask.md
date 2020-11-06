---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
ms.openlocfilehash: b572a7aefc3076671e78895f5fea531929858873
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593828"
---
# <span data-ttu-id="8d704-101">Set-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="8d704-101">Set-AzureBatchTask</span></span>

## <span data-ttu-id="8d704-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d704-102">SYNOPSIS</span></span>
<span data-ttu-id="8d704-103">Görevin özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8d704-103">Updates the properties of a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d704-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8d704-104">SYNTAX</span></span>

```
Set-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d704-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8d704-105">DESCRIPTION</span></span>
<span data-ttu-id="8d704-106">**Set-AzureBatchTask** cmdlet 'ı, Azure Batch hizmetindeki bir görevin özelliklerini günceller.</span><span class="sxs-lookup"><span data-stu-id="8d704-106">The **Set-AzureBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="8d704-107">Bir **Ince görev** nesnesi almak için Get-AzureBatchTask cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8d704-107">Use the Get-AzureBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="8d704-108">Bu nesnenin özelliklerini değiştirin ve değişikliklerinizi toplu Iş hizmetine uygulamak için geçerli cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="8d704-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="8d704-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8d704-109">EXAMPLES</span></span>

### <span data-ttu-id="8d704-110">Örnek 1: görevi güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="8d704-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzureBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzureBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="8d704-111">İlk komut **Get-AzureBatchTask** kullanarak bir görevi alır ve $Task değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="8d704-111">The first command gets a task by using **Get-AzureBatchTask** , and then stores it in the $Task variable.</span></span>

<span data-ttu-id="8d704-112">Sonraki iki komut $Task görevin kısıtlamalarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8d704-112">The next two commands modify the constraints of the task in $Task.</span></span>

<span data-ttu-id="8d704-113">Son komutu, toplu Iş hizmetini $Task yerel nesneyle eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8d704-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="8d704-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8d704-114">PARAMETERS</span></span>

### <span data-ttu-id="8d704-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8d704-115">-BatchContext</span></span>
<span data-ttu-id="8d704-116">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d704-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8d704-117">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8d704-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="8d704-118">-Görev</span><span class="sxs-lookup"><span data-stu-id="8d704-118">-Task</span></span>
<span data-ttu-id="8d704-119">Bu cmdlet 'in toplu Iş hizmetini güncelleştirdiği **Pscses görevini** belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d704-119">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d704-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d704-120">-DefaultProfile</span></span>
<span data-ttu-id="8d704-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8d704-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d704-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d704-122">CommonParameters</span></span>
<span data-ttu-id="8d704-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8d704-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d704-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d704-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d704-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8d704-125">INPUTS</span></span>

### <span data-ttu-id="8d704-126">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8d704-126">BatchAccountContext</span></span>
<span data-ttu-id="8d704-127">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="8d704-127">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="8d704-128">Ince görev</span><span class="sxs-lookup"><span data-stu-id="8d704-128">PSCloudTask</span></span>
<span data-ttu-id="8d704-129">Parametre ' görev ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="8d704-129">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="8d704-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8d704-130">OUTPUTS</span></span>

## <span data-ttu-id="8d704-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8d704-131">NOTES</span></span>

## <span data-ttu-id="8d704-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8d704-132">RELATED LINKS</span></span>

[<span data-ttu-id="8d704-133">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="8d704-133">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="8d704-134">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="8d704-134">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="8d704-135">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="8d704-135">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="8d704-136">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="8d704-136">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="8d704-137">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="8d704-137">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="8d704-138">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="8d704-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


