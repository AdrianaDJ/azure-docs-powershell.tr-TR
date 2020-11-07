---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
ms.openlocfilehash: 73d80d3547ea895e5cbd35b2d514d9a757164bed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594833"
---
# <span data-ttu-id="9025b-101">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9025b-101">Disable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="9025b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9025b-102">SYNOPSIS</span></span>
<span data-ttu-id="9025b-103">Toplu iş çizelgesini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="9025b-103">Disables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9025b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9025b-104">SYNTAX</span></span>

```
Disable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9025b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9025b-105">DESCRIPTION</span></span>
<span data-ttu-id="9025b-106">**Disable-AzureBatchJobSchedule** cmdlet 'ı bir Azure toplu iş çizelgesini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="9025b-106">The **Disable-AzureBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="9025b-107">Bir zamanlamayı devre dışı bırakırsanız, işler bu zamanlamaya göre oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="9025b-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="9025b-108">Devre dışı bir zamanlamayı daha sonra etkinleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9025b-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="9025b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9025b-109">EXAMPLES</span></span>

### <span data-ttu-id="9025b-110">Örnek 1: iş çizelgesini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="9025b-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="9025b-111">Bu komut, KIMLIĞI JobSchedule17 olan iş zamanlamasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="9025b-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="9025b-112">$Context değişkenine bağlam atamak için **Get-AzureRmBatchAccountKeys** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9025b-112">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="9025b-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9025b-113">PARAMETERS</span></span>

### <span data-ttu-id="9025b-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="9025b-114">-BatchContext</span></span>
<span data-ttu-id="9025b-115">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9025b-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9025b-116">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9025b-116">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="9025b-117">-ID</span><span class="sxs-lookup"><span data-stu-id="9025b-117">-Id</span></span>
<span data-ttu-id="9025b-118">Bu cmdlet 'in devre dışı olduğu iş zamanlamasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="9025b-118">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

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

### <span data-ttu-id="9025b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9025b-119">-DefaultProfile</span></span>
<span data-ttu-id="9025b-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9025b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9025b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9025b-121">CommonParameters</span></span>
<span data-ttu-id="9025b-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9025b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9025b-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9025b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9025b-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9025b-124">INPUTS</span></span>

### <span data-ttu-id="9025b-125">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9025b-125">BatchAccountContext</span></span>
<span data-ttu-id="9025b-126">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="9025b-126">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="9025b-127">Dizisi</span><span class="sxs-lookup"><span data-stu-id="9025b-127">String</span></span>
<span data-ttu-id="9025b-128">' ID ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="9025b-128">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="9025b-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9025b-129">OUTPUTS</span></span>

## <span data-ttu-id="9025b-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9025b-130">NOTES</span></span>

## <span data-ttu-id="9025b-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9025b-131">RELATED LINKS</span></span>

[<span data-ttu-id="9025b-132">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9025b-132">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="9025b-133">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="9025b-133">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="9025b-134">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9025b-134">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="9025b-135">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9025b-135">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="9025b-136">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9025b-136">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="9025b-137">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9025b-137">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="9025b-138">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="9025b-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

