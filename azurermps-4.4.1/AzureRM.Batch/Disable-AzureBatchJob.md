---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C831F934-7513-4882-A155-816E56CD9807
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJob.md
ms.openlocfilehash: 2e19e6b1733ccc3dfe0a802756e2c0a517232803
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764906"
---
# <span data-ttu-id="fee83-101">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="fee83-101">Disable-AzureBatchJob</span></span>

## <span data-ttu-id="fee83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fee83-102">SYNOPSIS</span></span>
<span data-ttu-id="fee83-103">Toplu işi devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="fee83-103">Disables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fee83-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fee83-104">SYNTAX</span></span>

```
Disable-AzureBatchJob [-Id] <String> [-DisableJobOption] <DisableJobOption> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fee83-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fee83-105">DESCRIPTION</span></span>
<span data-ttu-id="fee83-106">**Disable-AzureBatchJob** cmdlet 'ı bir Azure toplu işlemini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="fee83-106">The **Disable-AzureBatchJob** cmdlet disables an Azure Batch job.</span></span>
<span data-ttu-id="fee83-107">İşi etkinleştirdikten sonra yeni görevler çalıştırılabilir.</span><span class="sxs-lookup"><span data-stu-id="fee83-107">After you enable a job, new tasks can run.</span></span>
<span data-ttu-id="fee83-108">Devre dışı bırakılan işler yeni görevleri çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="fee83-108">Disabled jobs do not run new tasks.</span></span>
<span data-ttu-id="fee83-109">Devre dışı bir işi daha sonra etkinleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fee83-109">You can enable a disabled job later.</span></span>

## <span data-ttu-id="fee83-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fee83-110">EXAMPLES</span></span>

### <span data-ttu-id="fee83-111">Örnek 1: toplu işi devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="fee83-111">Example 1: Disable a Batch job</span></span>
```
PS C:\>Disable-AzureBatchJob -Id "Job-000001" -DisableJobOption "Terminate" -BatchContext $Context
```

<span data-ttu-id="fee83-112">Bu komut, Iş KIMLIĞI-000001 olan işi devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="fee83-112">This command disables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="fee83-113">Komut, iş için etkin görevleri sonlandırır.</span><span class="sxs-lookup"><span data-stu-id="fee83-113">The command terminates active tasks for the job.</span></span>
<span data-ttu-id="fee83-114">$Context değişkenine bağlam atamak için **Get-AzureRmBatchAccountKeys** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="fee83-114">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="fee83-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fee83-115">PARAMETERS</span></span>

### <span data-ttu-id="fee83-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="fee83-116">-BatchContext</span></span>
<span data-ttu-id="fee83-117">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fee83-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="fee83-118">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="fee83-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="fee83-119">-DisableJobOption</span><span class="sxs-lookup"><span data-stu-id="fee83-119">-DisableJobOption</span></span>
<span data-ttu-id="fee83-120">Bu cmdlet 'in devre dışı olduğu iş ile ilişkili etkin görevlerle ne yapılması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fee83-120">Specifies what to do with active tasks associated with the job that this cmdlet disables.</span></span>
<span data-ttu-id="fee83-121">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="fee83-121">Valid values are:</span></span> 

- <span data-ttu-id="fee83-122">Requeue</span><span class="sxs-lookup"><span data-stu-id="fee83-122">Requeue</span></span> 
- <span data-ttu-id="fee83-123">Ermesini</span><span class="sxs-lookup"><span data-stu-id="fee83-123">Terminate</span></span> 
- <span data-ttu-id="fee83-124">Yönergesi</span><span class="sxs-lookup"><span data-stu-id="fee83-124">Wait</span></span>

```yaml
Type: Microsoft.Azure.Batch.Common.DisableJobOption
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, Wait

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fee83-125">-ID</span><span class="sxs-lookup"><span data-stu-id="fee83-125">-Id</span></span>
<span data-ttu-id="fee83-126">Bu cmdlet 'in devre dışı bırakacağını belirten KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="fee83-126">Specifies the ID of the job that this cmdlet disables.</span></span>

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

### <span data-ttu-id="fee83-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fee83-127">-DefaultProfile</span></span>
<span data-ttu-id="fee83-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fee83-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fee83-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fee83-129">CommonParameters</span></span>
<span data-ttu-id="fee83-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fee83-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fee83-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fee83-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fee83-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fee83-132">INPUTS</span></span>

### <span data-ttu-id="fee83-133">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="fee83-133">BatchAccountContext</span></span>
<span data-ttu-id="fee83-134">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="fee83-134">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="fee83-135">Dizisi</span><span class="sxs-lookup"><span data-stu-id="fee83-135">String</span></span>
<span data-ttu-id="fee83-136">' ID ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="fee83-136">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="fee83-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fee83-137">OUTPUTS</span></span>

## <span data-ttu-id="fee83-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fee83-138">NOTES</span></span>

## <span data-ttu-id="fee83-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fee83-139">RELATED LINKS</span></span>

[<span data-ttu-id="fee83-140">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="fee83-140">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="fee83-141">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="fee83-141">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="fee83-142">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="fee83-142">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="fee83-143">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="fee83-143">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="fee83-144">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="fee83-144">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="fee83-145">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="fee83-145">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="fee83-146">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="fee83-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


