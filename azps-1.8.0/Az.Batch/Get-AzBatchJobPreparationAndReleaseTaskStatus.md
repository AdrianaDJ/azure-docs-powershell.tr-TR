---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobpreparationandreleasetaskstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: accba78cd05d6fcc18eb7f48c7cfb2839c0e9417
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93761890"
---
# <span data-ttu-id="066d5-101">Get-AzBatchJobPreparationAndReleaseTaskStatus</span><span class="sxs-lookup"><span data-stu-id="066d5-101">Get-AzBatchJobPreparationAndReleaseTaskStatus</span></span>

## <span data-ttu-id="066d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="066d5-102">SYNOPSIS</span></span>
<span data-ttu-id="066d5-103">Toplu iş hazırlığını alır ve görev durumunu bırakın.</span><span class="sxs-lookup"><span data-stu-id="066d5-103">Gets Batch job preparation and release task status.</span></span>

## <span data-ttu-id="066d5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="066d5-104">SYNTAX</span></span>

### <span data-ttu-id="066d5-105">Kimlik (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="066d5-105">Id (Default)</span></span>
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-Id] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="066d5-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="066d5-106">InputObject</span></span>
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-InputObject] <PSCloudJob> [-Filter <String>]
 [-MaxCount <Int32>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="066d5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="066d5-107">DESCRIPTION</span></span>
<span data-ttu-id="066d5-108">**Get-AzBatchJobPreparationAndReleaseTaskStatus** cmdlet 'ı bir toplu Iş Için Azure toplu iş hazırlığı ve serbest bırakma görev durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="066d5-108">The **Get-AzBatchJobPreparationAndReleaseTaskStatus** cmdlet gets the Azure Batch job preparation and release task status for a Batch job.</span></span>
<span data-ttu-id="066d5-109">Bu cmdlet 'e *kimlik* parametresini veya bir **Pscses işi** örneği sağlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="066d5-109">You must supply the *Id* parameter or a **PSCloudJob** instance to this cmdlet.</span></span>

## <span data-ttu-id="066d5-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="066d5-110">EXAMPLES</span></span>

### <span data-ttu-id="066d5-111">Örnek 1: işin iş hazırlığı ve sürüm durumunu alma</span><span class="sxs-lookup"><span data-stu-id="066d5-111">Example 1: Get the job preparation and release status of a job</span></span>
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

<span data-ttu-id="066d5-112">Bu komut, iş için iş hazırlama ve görev durumunu "test" olarak alır.</span><span class="sxs-lookup"><span data-stu-id="066d5-112">This command gets the job preparation and release task status for job "Test".</span></span>
<span data-ttu-id="066d5-113">$Context değişkenine bağlam atamak için Get-AzBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="066d5-113">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="066d5-114">Örnek 2: filtre içeren bir işin iş hazırlama ve sürüm durumunu alma ve belirtilen</span><span class="sxs-lookup"><span data-stu-id="066d5-114">Example 2: Get the job preparation and release status of a job with Filter and Select specified</span></span>
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

ComputeNodeId                          :
ComputeNodeUrl                         :
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 :
```

<span data-ttu-id="066d5-115">Bu komut, "TVM-2316545714_1-20170613t201733z" düğümündeki "test" işi için iş hazırlığı ve sürüm durumunu alır ve JobPreparationTaskExecutionInformation bilgilerini yalnızca geri döndürmek için select yan tümcesini kullanır</span><span class="sxs-lookup"><span data-stu-id="066d5-115">This command gets the job preparation and release task status for job "Test" on node "tvm-2316545714_1-20170613t201733z" and uses the Select clause to specify to only return the JobPreparationTaskExecutionInformation information</span></span>

## <span data-ttu-id="066d5-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="066d5-116">PARAMETERS</span></span>

### <span data-ttu-id="066d5-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="066d5-117">-BatchContext</span></span>
<span data-ttu-id="066d5-118">Toplu Iş hizmetiyle etkileşim kurarken kullanılacak BatchAccountContext örneği.</span><span class="sxs-lookup"><span data-stu-id="066d5-118">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="066d5-119">Access tuşlarının doldurulduğuna bir BatchAccountContext nesnesi almak için Get-AzBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="066d5-119">Use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>

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

### <span data-ttu-id="066d5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="066d5-120">-DefaultProfile</span></span>
<span data-ttu-id="066d5-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="066d5-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="066d5-122">-Genişletme</span><span class="sxs-lookup"><span data-stu-id="066d5-122">-Expand</span></span>
<span data-ttu-id="066d5-123">Açık Veri Protokolü (OData) genişletme yan tümcesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="066d5-123">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="066d5-124">Aldığınız ana varlığın ilişkili varlıklarını almak için bu parametre için bir değer belirtin.</span><span class="sxs-lookup"><span data-stu-id="066d5-124">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="066d5-125">-Filtre</span><span class="sxs-lookup"><span data-stu-id="066d5-125">-Filter</span></span>
<span data-ttu-id="066d5-126">Bir OData filtre yan tümcesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="066d5-126">Specifies an OData filter clause.</span></span>
<span data-ttu-id="066d5-127">Filtre belirtmezseniz, bu cmdlet iş için tüm iş hazırlığı ve sürüm görev durumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="066d5-127">If you do not specify a filter, this cmdlet returns all job preparation and release task status' for the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="066d5-128">-ID</span><span class="sxs-lookup"><span data-stu-id="066d5-128">-Id</span></span>
<span data-ttu-id="066d5-129">Hazırlığı ve bırakma görevleri alınacak olan işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="066d5-129">Specifies the ID of the job whose preparation and release tasks should be retrieved.</span></span>
<span data-ttu-id="066d5-130">Joker karakterler belirtemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="066d5-130">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="066d5-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="066d5-131">-InputObject</span></span>
<span data-ttu-id="066d5-132">Hazırlık ve bırakma görev durumunu almak için işi temsil eden bir **Pschoparlör iş** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="066d5-132">Specifies a **PSCloudJob** object that represents the job to get the preparation and release task status from.</span></span>
<span data-ttu-id="066d5-133">Bir **Ince iş** nesnesi edinmek için Get-AzBatchJob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="066d5-133">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="066d5-134">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="066d5-134">-MaxCount</span></span>
<span data-ttu-id="066d5-135">Döndürülecek en yüksek iş hazırlığı ve sürüm görev durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="066d5-135">Specifies the maximum number of jobs preparation and release task status' to return.</span></span>
<span data-ttu-id="066d5-136">Sıfır (0) veya daha kısa bir değer belirtirseniz cmdlet üst sınırı kullanmaz.</span><span class="sxs-lookup"><span data-stu-id="066d5-136">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="066d5-137">Varsayılan değer 1000 ' dır.</span><span class="sxs-lookup"><span data-stu-id="066d5-137">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="066d5-138">-Select</span><span class="sxs-lookup"><span data-stu-id="066d5-138">-Select</span></span>
<span data-ttu-id="066d5-139">Bir OData select yan tümcesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="066d5-139">Specifies an OData select clause.</span></span>
<span data-ttu-id="066d5-140">Tüm nesne özellikleri yerine belirli özellikleri almak için bu parametre için bir değer belirtin.</span><span class="sxs-lookup"><span data-stu-id="066d5-140">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="066d5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="066d5-141">CommonParameters</span></span>
<span data-ttu-id="066d5-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="066d5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="066d5-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="066d5-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="066d5-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="066d5-144">INPUTS</span></span>

### <span data-ttu-id="066d5-145">Microsoft.Azure.Commands.Batch. Modeller. Pscses Işi</span><span class="sxs-lookup"><span data-stu-id="066d5-145">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="066d5-146">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="066d5-146">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="066d5-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="066d5-147">OUTPUTS</span></span>

### <span data-ttu-id="066d5-148">Microsoft.Azure.Commands.Batch. Modeller. PSJobPreparationAndReleaseTaskExecutionInformation</span><span class="sxs-lookup"><span data-stu-id="066d5-148">Microsoft.Azure.Commands.Batch.Models.PSJobPreparationAndReleaseTaskExecutionInformation</span></span>

## <span data-ttu-id="066d5-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="066d5-149">NOTES</span></span>

## <span data-ttu-id="066d5-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="066d5-150">RELATED LINKS</span></span>

[<span data-ttu-id="066d5-151">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="066d5-151">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="066d5-152">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="066d5-152">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)
