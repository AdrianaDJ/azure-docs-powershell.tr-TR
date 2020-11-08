---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpoolnodecount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolNodeCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolNodeCount.md
ms.openlocfilehash: b3b1adfe9549a7b04a1e7c6d57542cef8a40cfd7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098487"
---
# <span data-ttu-id="869d9-101">Get-AzBatchPoolNodeCount</span><span class="sxs-lookup"><span data-stu-id="869d9-101">Get-AzBatchPoolNodeCount</span></span>

## <span data-ttu-id="869d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="869d9-102">SYNOPSIS</span></span>
<span data-ttu-id="869d9-103">Havuz kimliğine göre gruplandırılmış olarak düğüm başına toplu Iş düğümü sayısını alır.</span><span class="sxs-lookup"><span data-stu-id="869d9-103">Gets Batch node counts per node state grouped by pool id.</span></span>

## <span data-ttu-id="869d9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="869d9-104">SYNTAX</span></span>

### <span data-ttu-id="869d9-105">AzureBatchPoolNodeCounts (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="869d9-105">AzureBatchPoolNodeCounts (Default)</span></span>
```
Get-AzBatchPoolNodeCount -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="869d9-106">PoolId</span><span class="sxs-lookup"><span data-stu-id="869d9-106">PoolId</span></span>
```
Get-AzBatchPoolNodeCount [-PoolId <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="869d9-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="869d9-107">ParentObject</span></span>
```
Get-AzBatchPoolNodeCount [-Pool <PSCloudPool>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="869d9-108">ODataFilter</span><span class="sxs-lookup"><span data-stu-id="869d9-108">ODataFilter</span></span>
```
Get-AzBatchPoolNodeCount [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="869d9-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="869d9-109">DESCRIPTION</span></span>
<span data-ttu-id="869d9-110">Get-AzBatchPoolNodeCount cmdlet, müşterilerin havuza göre gruplandırılan düğüm başına düşen düğüm sayısını almasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="869d9-110">The Get-AzBatchPoolNodeCount cmdlet allows customers to get back node counts per node state grouped by pool.</span></span> <span data-ttu-id="869d9-111">Olası düğüm durumları oluşturuluyor, boşta, leavingPool, OFFLINE, yeniden başlatılıyor, reımaging, çalışıyor, başlatılıyor, startTaskFailed, bilinmiyor, kullanılamaz ve waitingForStartTask.</span><span class="sxs-lookup"><span data-stu-id="869d9-111">Possible node states are creating, idle, leavingPool, offline, preempted, rebooting, reimaging, running, starting, startTaskFailed, unknown, unusable and waitingForStartTask.</span></span> <span data-ttu-id="869d9-112">Cmdlet PoolId veya havuz parametresini yalnızca havuz kimliği belirtilen havuz filtrelemek için alır.</span><span class="sxs-lookup"><span data-stu-id="869d9-112">The cmdlet takes PoolId or Pool parameter to filter only pool with pool id specified.</span></span> 

## <span data-ttu-id="869d9-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="869d9-113">EXAMPLES</span></span>

### <span data-ttu-id="869d9-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="869d9-114">Example 1</span></span>
```
PS C:\> $batchContext = Get-AzBatchAccountKey -AccountName "contosobatch"
PS C:\> Get-AzBatchPoolNodeCount -BatchContext $batchContext

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0
contosopool2                   Idle: 1, Rebooting: 1, Total: 2                              Total: 0
```

<span data-ttu-id="869d9-115">Geçerli toplu hesap bağlamı altındaki havuzlar için düğüm sayısını listeler.</span><span class="sxs-lookup"><span data-stu-id="869d9-115">List node counts per node state for pools under current batch account context.</span></span>

### <span data-ttu-id="869d9-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="869d9-116">Example 2</span></span>

```powershell
PS C:\> Get-AzBatchPoolNodeCount -BatchContext $batchContext -PoolId "contosopool1"

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0

PS C:\> $poolnodecounts = Get-AzBatchPoolNodeCount -BatchContext $batchContext -PoolId "contosopool1"
PS C:\> $poolnodecounts.Dedicated

Creating            : 1
Idle                : 1
LeavingPool         : 0
Offline             : 0
Preempted           : 0
Rebooting           : 1
Reimaging           : 0
Running             : 5
Starting            : 0
StartTaskFailed     : 0
Total               : 8
Unknown             : 0
Unusable            : 0
WaitingForStartTask : 0

PS C:\> Get-AzBatchPool -Id "contosopool1" -BatchContext $batchContext | Get-AzBatchPoolNodeCount -BatchContext $batchContext

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0
```

<span data-ttu-id="869d9-117">Havuz için belirli bir havuz kimliği</span><span class="sxs-lookup"><span data-stu-id="869d9-117">Show node counts per node state for a pool given pool id.</span></span>

## <span data-ttu-id="869d9-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="869d9-118">PARAMETERS</span></span>

### <span data-ttu-id="869d9-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="869d9-119">-BatchContext</span></span>
<span data-ttu-id="869d9-120">Toplu Iş hizmetiyle etkileşim kurarken kullanılacak BatchAccountContext örneği.</span><span class="sxs-lookup"><span data-stu-id="869d9-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="869d9-121">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="869d9-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="869d9-122">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKey cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="869d9-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="869d9-123">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="869d9-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="869d9-124">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="869d9-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="869d9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="869d9-125">-DefaultProfile</span></span>
<span data-ttu-id="869d9-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="869d9-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="869d9-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="869d9-127">-MaxCount</span></span>
<span data-ttu-id="869d9-128">Döndürülecek en fazla havuz sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="869d9-128">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="869d9-129">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="869d9-129">The default value is 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="869d9-130">-Havuz</span><span class="sxs-lookup"><span data-stu-id="869d9-130">-Pool</span></span>
<span data-ttu-id="869d9-131">Düğüm sayılarının alınacağı **Pschoparlör havuzunu** belirtir.</span><span class="sxs-lookup"><span data-stu-id="869d9-131">Specifies the **PSCloudPool** for which to get node counts.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudPool
Parameter Sets: ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="869d9-132">-PoolId</span><span class="sxs-lookup"><span data-stu-id="869d9-132">-PoolId</span></span>
<span data-ttu-id="869d9-133">Düğüm sayılarının alınacağı havuzun kimliği.</span><span class="sxs-lookup"><span data-stu-id="869d9-133">The id of the pool for which to get node counts.</span></span>

```yaml
Type: System.String
Parameter Sets: PoolId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="869d9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="869d9-134">CommonParameters</span></span>
<span data-ttu-id="869d9-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="869d9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="869d9-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="869d9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="869d9-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="869d9-137">INPUTS</span></span>

### <span data-ttu-id="869d9-138">System. String</span><span class="sxs-lookup"><span data-stu-id="869d9-138">System.String</span></span>

### <span data-ttu-id="869d9-139">Microsoft.Azure.Commands.Batch. Modeller. Pscses havuzu</span><span class="sxs-lookup"><span data-stu-id="869d9-139">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="869d9-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="869d9-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="869d9-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="869d9-141">OUTPUTS</span></span>

### <span data-ttu-id="869d9-142">Microsoft.Azure.Commands.Batch. Modeller. PSPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="869d9-142">Microsoft.Azure.Commands.Batch.Models.PSPoolNodeCounts</span></span>

## <span data-ttu-id="869d9-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="869d9-143">NOTES</span></span>

## <span data-ttu-id="869d9-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="869d9-144">RELATED LINKS</span></span>

[<span data-ttu-id="869d9-145">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="869d9-145">Get-AzBatchAccountKey</span></span>]()

[<span data-ttu-id="869d9-146">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="869d9-146">Get-AzBatchJob</span></span>]()

[<span data-ttu-id="869d9-147">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="869d9-147">Azure Batch Cmdlets</span></span>]()

