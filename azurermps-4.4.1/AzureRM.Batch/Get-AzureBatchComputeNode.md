---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 93614655-A8F2-4A67-887D-43D41AB91F82
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchComputeNode.md
ms.openlocfilehash: f503352352c31369e594325c060cf0ab68490095
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594824"
---
# <span data-ttu-id="d8a6d-101">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="d8a6d-101">Get-AzureBatchComputeNode</span></span>

## <span data-ttu-id="d8a6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8a6d-102">SYNOPSIS</span></span>
<span data-ttu-id="d8a6d-103">Havuzdan toplu işlem düğümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="d8a6d-103">Gets Batch compute nodes from a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8a6d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d8a6d-104">SYNTAX</span></span>

### <span data-ttu-id="d8a6d-105">ODataFilter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d8a6d-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchComputeNode [-PoolId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8a6d-106">Kimliğe</span><span class="sxs-lookup"><span data-stu-id="d8a6d-106">Id</span></span>
```
Get-AzureBatchComputeNode [-PoolId] <String> [[-Id] <String>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8a6d-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="d8a6d-107">ParentObject</span></span>
```
Get-AzureBatchComputeNode [[-Pool] <PSCloudPool>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8a6d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d8a6d-108">DESCRIPTION</span></span>
<span data-ttu-id="d8a6d-109">**Get-AzureBatchComputeNode** cmdlet 'i bir havuzdan Azure toplu işlem düğümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="d8a6d-109">The **Get-AzureBatchComputeNode** cmdlet gets Azure Batch compute nodes from a pool.</span></span>
<span data-ttu-id="d8a6d-110">*PoolID* veya *Havuz* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="d8a6d-110">Specify either the *PoolID* or *Pool* parameter.</span></span>
<span data-ttu-id="d8a6d-111">Tek bir COMPUTE düğümü almak için *ID* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="d8a6d-111">Specify the *Id* parameter to get a single compute node.</span></span>
<span data-ttu-id="d8a6d-112">Açık bir veri Protokolü (OData) filtresiyle eşleşen hesaplama düğümlerini almak için *Filter* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="d8a6d-112">Specify the *Filter* parameter to get the compute nodes that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="d8a6d-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d8a6d-113">EXAMPLES</span></span>

### <span data-ttu-id="d8a6d-114">Örnek 1: KIMLIĞE göre işlem düğümü alma</span><span class="sxs-lookup"><span data-stu-id="d8a6d-114">Example 1: Get a compute node by ID</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool06" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : small
TotalTasksRun         : 1
StartTaskInformation  : 
RecentTasks           : {}
StartTask             : 
CertificateReferences : 
Errors                :
```

<span data-ttu-id="d8a6d-115">Bu komut, kimlik numarası Pool06 olan havuzdan TVM-2316545714_1-20150725t213220z olan COMPUTE düğümünü alır.</span><span class="sxs-lookup"><span data-stu-id="d8a6d-115">This command gets the compute node that has the ID tvm-2316545714_1-20150725t213220z from the pool that has the ID Pool06.</span></span>
<span data-ttu-id="d8a6d-116">$Context değişkenine bağlam atamak için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d8a6d-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="d8a6d-117">Örnek 2: havuzdan tüm boşta işlemi düğümlerini alma</span><span class="sxs-lookup"><span data-stu-id="d8a6d-117">Example 2: Get all idle compute nodes from a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool06" -Filter "state eq 'idle'" -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : small
TotalTasksRun         : 1
StartTaskInformation  : 
RecentTasks           : {}
StartTask             : 
CertificateReferences : 
Errors                : 

Id                    : tvm-2316545714_2-20150726t172920z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_2-20150726t172920z
State                 : Idle
StateTransitionTime   : 7/26/2015 5:33:58 PM
LastBootTime          : 7/26/2015 5:33:58 PM
AllocationTime        : 7/26/2015 5:29:20 PM
IPAddress             : 10.14.121.38
AffinityId            : TVM:tvm-2316545714_2-20150726t172920z
VirtualMachineSize    : small
TotalTasksRun         : 0
StartTaskInformation  : 
RecentTasks           : 
StartTask             : 
CertificateReferences : 
Errors                :
```

<span data-ttu-id="d8a6d-118">Bu komut, Pool06 KIMLIĞINE sahip havuzda bulunan tüm boşta COMPUTE düğümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="d8a6d-118">This command gets all idle compute nodes that are contained in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="d8a6d-119">Bu komut, *filtre* parametresini kullanarak Boşta durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8a6d-119">The command specifies the idle state by using the *Filter* parameter.</span></span>

### <span data-ttu-id="d8a6d-120">Örnek 3: belirtilen havuzda tüm işlem düğümlerini alma</span><span class="sxs-lookup"><span data-stu-id="d8a6d-120">Example 3: Get all compute nodes in a specified pool</span></span>
```
PS C:\>Get-AzureBatchPool -Id "Pool07" -BatchContext $Context | Get-AzureBatchComputeNode -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : small
TotalTasksRun         : 1
StartTaskInformation  : 
RecentTasks           : {}
StartTask             : 
CertificateReferences : 
Errors                : 


Id                    : tvm-2316545714_2-20150726t172920z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_2-20150726t172920z
State                 : Idle
StateTransitionTime   : 7/26/2015 5:33:58 PM
LastBootTime          : 7/26/2015 5:33:58 PM
AllocationTime        : 7/26/2015 5:29:20 PM

IPAddress             : 10.14.121.38
AffinityId            : TVM:tvm-2316545714_2-20150726t172920z
VirtualMachineSize    : small
TotalTasksRun         : 0
StartTaskInformation  : 
RecentTasks           : 
StartTask             : 
CertificateReferences : 
Errors                :
```

<span data-ttu-id="d8a6d-121">Bu komut, Get-AzureBatchPool cmdlet 'ini kullanarak KIMLIK Pool07 havuzunu alır.</span><span class="sxs-lookup"><span data-stu-id="d8a6d-121">This command gets the pool that has the ID Pool07 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="d8a6d-122">Bu komut, ardışık düzen işlecini kullanarak bu havuzu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="d8a6d-122">The command passes that pool to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d8a6d-123">Bu cmdlet bu havuzdan tüm işlem düğümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="d8a6d-123">That cmdlet gets all compute nodes from that pool.</span></span>

## <span data-ttu-id="d8a6d-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d8a6d-124">PARAMETERS</span></span>

### <span data-ttu-id="d8a6d-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d8a6d-125">-BatchContext</span></span>
<span data-ttu-id="d8a6d-126">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8a6d-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d8a6d-127">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d8a6d-127">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="d8a6d-128">-Filtre</span><span class="sxs-lookup"><span data-stu-id="d8a6d-128">-Filter</span></span>
<span data-ttu-id="d8a6d-129">Bir OData filtre yan tümcesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8a6d-129">Specifies an OData filter clause.</span></span>
<span data-ttu-id="d8a6d-130">Bu cmdlet, bu parametrenin belirttiği filtreyle eşleşen işlem düğümlerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="d8a6d-130">This cmdlet returns compute nodes that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="d8a6d-131">Filtre belirtmezseniz, bu cmdlet havuzun tüm işlem düğümlerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="d8a6d-131">If you do not specify a filter, this cmdlet returns all compute nodes for the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, ParentObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8a6d-132">-ID</span><span class="sxs-lookup"><span data-stu-id="d8a6d-132">-Id</span></span>
<span data-ttu-id="d8a6d-133">Bu cmdlet 'in havuzdan aldığı COMPUTE düğümünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8a6d-133">Specifies the ID of the compute node that this cmdlet gets from the pool.</span></span>
<span data-ttu-id="d8a6d-134">Joker karakterler belirtemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="d8a6d-134">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8a6d-135">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="d8a6d-135">-MaxCount</span></span>
<span data-ttu-id="d8a6d-136">Döndürülecek en fazla işlem düğümü sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8a6d-136">Specifies the maximum number of compute nodes to return.</span></span>
<span data-ttu-id="d8a6d-137">Sıfır (0) veya daha kısa bir değer belirtirseniz cmdlet üst sınırı kullanmaz.</span><span class="sxs-lookup"><span data-stu-id="d8a6d-137">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="d8a6d-138">Varsayılan değer 1000 ' dır.</span><span class="sxs-lookup"><span data-stu-id="d8a6d-138">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter, ParentObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8a6d-139">-Havuz</span><span class="sxs-lookup"><span data-stu-id="d8a6d-139">-Pool</span></span>
<span data-ttu-id="d8a6d-140">Havuzu, COMPUTE düğümlerini içeren bir **Pscses havuzu** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8a6d-140">Specifies the pool, as a **PSCloudPool** object, that contains the compute nodes.</span></span>
<span data-ttu-id="d8a6d-141">**Pscses havuzu** nesnesi edinmek için Get-AzureBatchPool cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d8a6d-141">To obtain a **PSCloudPool** object, use the Get-AzureBatchPool cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudPool
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8a6d-142">-PoolId</span><span class="sxs-lookup"><span data-stu-id="d8a6d-142">-PoolId</span></span>
<span data-ttu-id="d8a6d-143">Hesaplama düğümlerini içeren havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8a6d-143">Specifies the ID of the pool that contains the compute nodes.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8a6d-144">-Select</span><span class="sxs-lookup"><span data-stu-id="d8a6d-144">-Select</span></span>
<span data-ttu-id="d8a6d-145">Bir OData select yan tümcesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8a6d-145">Specifies an OData select clause.</span></span>
<span data-ttu-id="d8a6d-146">Tüm nesne özellikleri yerine belirli özellikleri almak için bu parametre için bir değer belirtin.</span><span class="sxs-lookup"><span data-stu-id="d8a6d-146">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="d8a6d-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8a6d-147">-DefaultProfile</span></span>
<span data-ttu-id="d8a6d-148">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d8a6d-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8a6d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8a6d-149">CommonParameters</span></span>
<span data-ttu-id="d8a6d-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d8a6d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8a6d-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8a6d-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8a6d-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d8a6d-152">INPUTS</span></span>

### <span data-ttu-id="d8a6d-153">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d8a6d-153">BatchAccountContext</span></span>
<span data-ttu-id="d8a6d-154">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="d8a6d-154">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="d8a6d-155">Pscses havuzu</span><span class="sxs-lookup"><span data-stu-id="d8a6d-155">PSCloudPool</span></span>
<span data-ttu-id="d8a6d-156">Parametre ' havuz ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="d8a6d-156">Parameter 'Pool' accepts value of type 'PSCloudPool' from the pipeline</span></span>

## <span data-ttu-id="d8a6d-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d8a6d-157">OUTPUTS</span></span>

### <span data-ttu-id="d8a6d-158">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="d8a6d-158">PSComputeNode</span></span>

## <span data-ttu-id="d8a6d-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d8a6d-159">NOTES</span></span>

## <span data-ttu-id="d8a6d-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d8a6d-160">RELATED LINKS</span></span>

[<span data-ttu-id="d8a6d-161">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="d8a6d-161">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="d8a6d-162">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="d8a6d-162">Get-AzureBatchNodeFile</span></span>](./Get-AzureBatchNodeFile.md)

[<span data-ttu-id="d8a6d-163">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="d8a6d-163">Get-AzureBatchNodeFileContent</span></span>](./Get-AzureBatchNodeFileContent.md)

[<span data-ttu-id="d8a6d-164">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="d8a6d-164">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="d8a6d-165">Reset-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="d8a6d-165">Reset-AzureBatchComputeNode</span></span>](./Reset-AzureBatchComputeNode.md)

[<span data-ttu-id="d8a6d-166">Restart-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="d8a6d-166">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)

[<span data-ttu-id="d8a6d-167">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="d8a6d-167">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


