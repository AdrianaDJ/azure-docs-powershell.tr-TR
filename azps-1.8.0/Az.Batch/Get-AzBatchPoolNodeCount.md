---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpoolnodecount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolNodeCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolNodeCount.md
ms.openlocfilehash: 0390e6f156e305c3ba5f34d78dcf33520098bee3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761468"
---
# <span data-ttu-id="6bfd1-101">Get-AzBatchPoolNodeCount</span><span class="sxs-lookup"><span data-stu-id="6bfd1-101">Get-AzBatchPoolNodeCount</span></span>

## <span data-ttu-id="6bfd1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bfd1-102">SYNOPSIS</span></span>
<span data-ttu-id="6bfd1-103">Havuz kimliğine göre gruplandırılmış olarak düğüm başına toplu Iş düğümü sayısını alır.</span><span class="sxs-lookup"><span data-stu-id="6bfd1-103">Gets Batch node counts per node state grouped by pool id.</span></span>

## <span data-ttu-id="6bfd1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6bfd1-104">SYNTAX</span></span>

### <span data-ttu-id="6bfd1-105">AzureBatchPoolNodeCounts (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6bfd1-105">AzureBatchPoolNodeCounts (Default)</span></span>
```
Get-AzBatchPoolNodeCount -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6bfd1-106">PoolId</span><span class="sxs-lookup"><span data-stu-id="6bfd1-106">PoolId</span></span>
```
Get-AzBatchPoolNodeCount [-PoolId <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6bfd1-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="6bfd1-107">ParentObject</span></span>
```
Get-AzBatchPoolNodeCount [-Pool <PSCloudPool>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6bfd1-108">ODataFilter</span><span class="sxs-lookup"><span data-stu-id="6bfd1-108">ODataFilter</span></span>
```
Get-AzBatchPoolNodeCount [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6bfd1-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="6bfd1-109">DESCRIPTION</span></span>
<span data-ttu-id="6bfd1-110">Get-AzBatchPoolNodeCount cmdlet, müşterilerin havuza göre gruplandırılan düğüm başına düşen düğüm sayısını almasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="6bfd1-110">The Get-AzBatchPoolNodeCount cmdlet allows customers to get back node counts per node state grouped by pool.</span></span> <span data-ttu-id="6bfd1-111">Olası düğüm durumları oluşturuluyor, boşta, leavingPool, OFFLINE, yeniden başlatılıyor, reımaging, çalışıyor, başlatılıyor, startTaskFailed, bilinmiyor, kullanılamaz ve waitingForStartTask.</span><span class="sxs-lookup"><span data-stu-id="6bfd1-111">Possible node states are creating, idle, leavingPool, offline, preempted, rebooting, reimaging, running, starting, startTaskFailed, unknown, unusable and waitingForStartTask.</span></span> <span data-ttu-id="6bfd1-112">Cmdlet PoolId veya havuz parametresini yalnızca havuz kimliği belirtilen havuz filtrelemek için alır.</span><span class="sxs-lookup"><span data-stu-id="6bfd1-112">The cmdlet takes PoolId or Pool parameter to filter only pool with pool id specified.</span></span> 

## <span data-ttu-id="6bfd1-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6bfd1-113">EXAMPLES</span></span>

### <span data-ttu-id="6bfd1-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6bfd1-114">Example 1</span></span>

```powershell
PS C:\> $batchContext = Get-AzBatchAccountKeys -AccountName "contosobatch"
PS C:\> Get-AzBatchPoolNodeCount -BatchContext $batchContext

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0
contosopool2                   Idle: 1, Rebooting: 1, Total: 2                              Total: 0
```

<span data-ttu-id="6bfd1-115">Geçerli toplu hesap bağlamı altındaki havuzlar için düğüm sayısını listeler.</span><span class="sxs-lookup"><span data-stu-id="6bfd1-115">List node counts per node state for pools under current batch account context.</span></span>

### <span data-ttu-id="6bfd1-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="6bfd1-116">Example 2</span></span>

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

<span data-ttu-id="6bfd1-117">Havuz için belirli bir havuz kimliği</span><span class="sxs-lookup"><span data-stu-id="6bfd1-117">Show node counts per node state for a pool given pool id.</span></span>

## <span data-ttu-id="6bfd1-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6bfd1-118">PARAMETERS</span></span>

### <span data-ttu-id="6bfd1-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6bfd1-119">-BatchContext</span></span>
<span data-ttu-id="6bfd1-120">Toplu Iş hizmetiyle etkileşim kurarken kullanılacak BatchAccountContext örneği.</span><span class="sxs-lookup"><span data-stu-id="6bfd1-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="6bfd1-121">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6bfd1-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="6bfd1-122">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="6bfd1-122">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="6bfd1-123">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6bfd1-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="6bfd1-124">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="6bfd1-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6bfd1-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bfd1-125">-DefaultProfile</span></span>
<span data-ttu-id="6bfd1-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6bfd1-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6bfd1-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="6bfd1-127">-MaxCount</span></span>
<span data-ttu-id="6bfd1-128">Döndürülecek en fazla havuz sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6bfd1-128">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="6bfd1-129">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="6bfd1-129">The default value is 10.</span></span>

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

### <span data-ttu-id="6bfd1-130">-Havuz</span><span class="sxs-lookup"><span data-stu-id="6bfd1-130">-Pool</span></span>
<span data-ttu-id="6bfd1-131">Düğüm sayılarının alınacağı **Pschoparlör havuzunu** belirtir.</span><span class="sxs-lookup"><span data-stu-id="6bfd1-131">Specifies the **PSCloudPool** for which to get node counts.</span></span>

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

### <span data-ttu-id="6bfd1-132">-PoolId</span><span class="sxs-lookup"><span data-stu-id="6bfd1-132">-PoolId</span></span>
<span data-ttu-id="6bfd1-133">Düğüm sayılarının alınacağı havuzun kimliği.</span><span class="sxs-lookup"><span data-stu-id="6bfd1-133">The id of the pool for which to get node counts.</span></span>

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

### <span data-ttu-id="6bfd1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bfd1-134">CommonParameters</span></span>
<span data-ttu-id="6bfd1-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6bfd1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bfd1-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bfd1-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bfd1-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6bfd1-137">INPUTS</span></span>

### <span data-ttu-id="6bfd1-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6bfd1-138">System.String</span></span>

### <span data-ttu-id="6bfd1-139">Microsoft.Azure.Commands.Batch. Modeller. Pscses havuzu</span><span class="sxs-lookup"><span data-stu-id="6bfd1-139">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="6bfd1-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6bfd1-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="6bfd1-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6bfd1-141">OUTPUTS</span></span>

### <span data-ttu-id="6bfd1-142">Microsoft.Azure.Commands.Batch. Modeller. PSPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="6bfd1-142">Microsoft.Azure.Commands.Batch.Models.PSPoolNodeCounts</span></span>

## <span data-ttu-id="6bfd1-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6bfd1-143">NOTES</span></span>

## <span data-ttu-id="6bfd1-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6bfd1-144">RELATED LINKS</span></span>

[<span data-ttu-id="6bfd1-145">Get-Aztopluaccountkeys</span><span class="sxs-lookup"><span data-stu-id="6bfd1-145">Get-AzBatchAccountKeys</span></span>]()

[<span data-ttu-id="6bfd1-146">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="6bfd1-146">Get-AzBatchJob</span></span>]()

[<span data-ttu-id="6bfd1-147">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="6bfd1-147">Azure Batch Cmdlets</span></span>]()

