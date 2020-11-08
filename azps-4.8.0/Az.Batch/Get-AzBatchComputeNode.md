---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 93614655-A8F2-4A67-887D-43D41AB91F82
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchComputeNode.md
ms.openlocfilehash: a50329620944aa18458c3bb667e3a95ff45bc21f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109841"
---
# <span data-ttu-id="8e18d-101">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="8e18d-101">Get-AzBatchComputeNode</span></span>

## <span data-ttu-id="8e18d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e18d-102">SYNOPSIS</span></span>
<span data-ttu-id="8e18d-103">Havuzdan toplu işlem düğümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="8e18d-103">Gets Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="8e18d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8e18d-104">SYNTAX</span></span>

### <span data-ttu-id="8e18d-105">ODataFilter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8e18d-105">ODataFilter (Default)</span></span>
```
Get-AzBatchComputeNode [-PoolId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e18d-106">Kimliğe</span><span class="sxs-lookup"><span data-stu-id="8e18d-106">Id</span></span>
```
Get-AzBatchComputeNode [-PoolId] <String> [[-Id] <String>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e18d-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="8e18d-107">ParentObject</span></span>
```
Get-AzBatchComputeNode [[-Pool] <PSCloudPool>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e18d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8e18d-108">DESCRIPTION</span></span>
<span data-ttu-id="8e18d-109">**Get-AzBatchComputeNode** cmdlet 'i bir havuzdan Azure toplu işlem düğümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="8e18d-109">The **Get-AzBatchComputeNode** cmdlet gets Azure Batch compute nodes from a pool.</span></span>
<span data-ttu-id="8e18d-110">*PoolID* veya *Havuz* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="8e18d-110">Specify either the *PoolID* or *Pool* parameter.</span></span>
<span data-ttu-id="8e18d-111">Tek bir COMPUTE düğümü almak için *ID* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="8e18d-111">Specify the *Id* parameter to get a single compute node.</span></span>
<span data-ttu-id="8e18d-112">Açık bir veri Protokolü (OData) filtresiyle eşleşen hesaplama düğümlerini almak için *Filter* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="8e18d-112">Specify the *Filter* parameter to get the compute nodes that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="8e18d-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8e18d-113">EXAMPLES</span></span>

### <span data-ttu-id="8e18d-114">Örnek 1: KIMLIĞE göre işlem düğümü alma</span><span class="sxs-lookup"><span data-stu-id="8e18d-114">Example 1: Get a compute node by ID</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool06" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 1
StartTaskInformation  :
RecentTasks           : {}
StartTask             :
CertificateReferences :
Errors                :
```

<span data-ttu-id="8e18d-115">Bu komut, kimlik numarası Pool06 olan havuzdan TVM-2316545714_1-20150725t213220z olan COMPUTE düğümünü alır.</span><span class="sxs-lookup"><span data-stu-id="8e18d-115">This command gets the compute node that has the ID tvm-2316545714_1-20150725t213220z from the pool that has the ID Pool06.</span></span>
<span data-ttu-id="8e18d-116">$Context değişkenine bağlam atamak için Get-AzBatchAccountKey cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8e18d-116">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="8e18d-117">Örnek 2: havuzdan tüm boşta işlemi düğümlerini alma</span><span class="sxs-lookup"><span data-stu-id="8e18d-117">Example 2: Get all idle compute nodes from a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool06" -Filter "state eq 'idle'" -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : standard_d1_v2
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
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 0
StartTaskInformation  :
RecentTasks           :
StartTask             :
CertificateReferences :
Errors                :
```

<span data-ttu-id="8e18d-118">Bu komut, Pool06 KIMLIĞINE sahip havuzda bulunan tüm boşta COMPUTE düğümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="8e18d-118">This command gets all idle compute nodes that are contained in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="8e18d-119">Bu komut, *filtre* parametresini kullanarak Boşta durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e18d-119">The command specifies the idle state by using the *Filter* parameter.</span></span>

### <span data-ttu-id="8e18d-120">Örnek 3: belirtilen havuzda tüm işlem düğümlerini alma</span><span class="sxs-lookup"><span data-stu-id="8e18d-120">Example 3: Get all compute nodes in a specified pool</span></span>
```
PS C:\>Get-AzBatchPool -Id "Pool07" -BatchContext $Context | Get-AzBatchComputeNode -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : standard_d1_v2
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
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 0
StartTaskInformation  :
RecentTasks           :
StartTask             :
CertificateReferences :
Errors                :
```

<span data-ttu-id="8e18d-121">Bu komut, Get-AzBatchPool cmdlet 'ini kullanarak KIMLIK Pool07 havuzunu alır.</span><span class="sxs-lookup"><span data-stu-id="8e18d-121">This command gets the pool that has the ID Pool07 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="8e18d-122">Bu komut, ardışık düzen işlecini kullanarak bu havuzu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="8e18d-122">The command passes that pool to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8e18d-123">Bu cmdlet bu havuzdan tüm işlem düğümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="8e18d-123">That cmdlet gets all compute nodes from that pool.</span></span>

## <span data-ttu-id="8e18d-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8e18d-124">PARAMETERS</span></span>

### <span data-ttu-id="8e18d-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8e18d-125">-BatchContext</span></span>
<span data-ttu-id="8e18d-126">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e18d-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8e18d-127">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8e18d-127">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8e18d-128">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKey cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="8e18d-128">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8e18d-129">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8e18d-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8e18d-130">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="8e18d-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="8e18d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e18d-131">-DefaultProfile</span></span>
<span data-ttu-id="8e18d-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8e18d-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e18d-133">-Filtre</span><span class="sxs-lookup"><span data-stu-id="8e18d-133">-Filter</span></span>
<span data-ttu-id="8e18d-134">Bir OData filtre yan tümcesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e18d-134">Specifies an OData filter clause.</span></span>
<span data-ttu-id="8e18d-135">Bu cmdlet, bu parametrenin belirttiği filtreyle eşleşen işlem düğümlerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="8e18d-135">This cmdlet returns compute nodes that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="8e18d-136">Filtre belirtmezseniz, bu cmdlet havuzun tüm işlem düğümlerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="8e18d-136">If you do not specify a filter, this cmdlet returns all compute nodes for the pool.</span></span>

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

### <span data-ttu-id="8e18d-137">-ID</span><span class="sxs-lookup"><span data-stu-id="8e18d-137">-Id</span></span>
<span data-ttu-id="8e18d-138">Bu cmdlet 'in havuzdan aldığı COMPUTE düğümünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e18d-138">Specifies the ID of the compute node that this cmdlet gets from the pool.</span></span>
<span data-ttu-id="8e18d-139">Joker karakterler belirtemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="8e18d-139">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="8e18d-140">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="8e18d-140">-MaxCount</span></span>
<span data-ttu-id="8e18d-141">Döndürülecek en fazla işlem düğümü sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e18d-141">Specifies the maximum number of compute nodes to return.</span></span>
<span data-ttu-id="8e18d-142">Sıfır (0) veya daha kısa bir değer belirtirseniz cmdlet üst sınırı kullanmaz.</span><span class="sxs-lookup"><span data-stu-id="8e18d-142">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="8e18d-143">Varsayılan değer 1000 ' dır.</span><span class="sxs-lookup"><span data-stu-id="8e18d-143">The default value is 1000.</span></span>

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

### <span data-ttu-id="8e18d-144">-Havuz</span><span class="sxs-lookup"><span data-stu-id="8e18d-144">-Pool</span></span>
<span data-ttu-id="8e18d-145">Havuzu, COMPUTE düğümlerini içeren bir **Pscses havuzu** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e18d-145">Specifies the pool, as a **PSCloudPool** object, that contains the compute nodes.</span></span>
<span data-ttu-id="8e18d-146">**Pscses havuzu** nesnesi edinmek için Get-AzBatchPool cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8e18d-146">To obtain a **PSCloudPool** object, use the Get-AzBatchPool cmdlet.</span></span>

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

### <span data-ttu-id="8e18d-147">-PoolId</span><span class="sxs-lookup"><span data-stu-id="8e18d-147">-PoolId</span></span>
<span data-ttu-id="8e18d-148">Hesaplama düğümlerini içeren havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e18d-148">Specifies the ID of the pool that contains the compute nodes.</span></span>

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

### <span data-ttu-id="8e18d-149">-Select</span><span class="sxs-lookup"><span data-stu-id="8e18d-149">-Select</span></span>
<span data-ttu-id="8e18d-150">Bir OData select yan tümcesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e18d-150">Specifies an OData select clause.</span></span>
<span data-ttu-id="8e18d-151">Tüm nesne özellikleri yerine belirli özellikleri almak için bu parametre için bir değer belirtin.</span><span class="sxs-lookup"><span data-stu-id="8e18d-151">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="8e18d-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e18d-152">CommonParameters</span></span>
<span data-ttu-id="8e18d-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8e18d-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e18d-154">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8e18d-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e18d-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8e18d-155">INPUTS</span></span>

### <span data-ttu-id="8e18d-156">System. String</span><span class="sxs-lookup"><span data-stu-id="8e18d-156">System.String</span></span>

### <span data-ttu-id="8e18d-157">Microsoft.Azure.Commands.Batch. Modeller. Pscses havuzu</span><span class="sxs-lookup"><span data-stu-id="8e18d-157">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="8e18d-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8e18d-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="8e18d-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8e18d-159">OUTPUTS</span></span>

### <span data-ttu-id="8e18d-160">Microsoft.Azure.Commands.Batch. Modeller. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="8e18d-160">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

## <span data-ttu-id="8e18d-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8e18d-161">NOTES</span></span>

## <span data-ttu-id="8e18d-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8e18d-162">RELATED LINKS</span></span>

[<span data-ttu-id="8e18d-163">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="8e18d-163">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="8e18d-164">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="8e18d-164">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="8e18d-165">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="8e18d-165">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)

[<span data-ttu-id="8e18d-166">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="8e18d-166">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="8e18d-167">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="8e18d-167">Reset-AzBatchComputeNode</span></span>](./Reset-AzBatchComputeNode.md)

[<span data-ttu-id="8e18d-168">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="8e18d-168">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)

[<span data-ttu-id="8e18d-169">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="8e18d-169">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
