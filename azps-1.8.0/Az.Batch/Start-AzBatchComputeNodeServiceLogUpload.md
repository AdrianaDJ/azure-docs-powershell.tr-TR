---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/Start-AzBatchComputeNodeServiceLogUpload
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchComputeNodeServiceLogUpload.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchComputeNodeServiceLogUpload.md
ms.openlocfilehash: 8bfc771ccfa8faf2c7a5eea973d214ac8a639797
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917627"
---
# <span data-ttu-id="2a932-101">Start-AzBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="2a932-101">Start-AzBatchComputeNodeServiceLogUpload</span></span>

## <span data-ttu-id="2a932-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a932-102">SYNOPSIS</span></span>
<span data-ttu-id="2a932-103">Compute node hizmeti günlük dosyalarını bir Azure depolama kapsayıcısına yükleyin.</span><span class="sxs-lookup"><span data-stu-id="2a932-103">Upload compute node service log files to an Azure Storage container.</span></span>

## <span data-ttu-id="2a932-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2a932-104">SYNTAX</span></span>

### <span data-ttu-id="2a932-105">AzureBatchComputeNodeServiceLogUpload (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2a932-105">AzureBatchComputeNodeServiceLogUpload (Default)</span></span>
```
Start-AzBatchComputeNodeServiceLogUpload [-ContainerUrl] <String> [-StartTime] <DateTime> [-EndTime <DateTime>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2a932-106">Kimliğe</span><span class="sxs-lookup"><span data-stu-id="2a932-106">Id</span></span>
```
Start-AzBatchComputeNodeServiceLogUpload [-PoolId] <String> [-ComputeNodeId] <String> [-ContainerUrl] <String>
 [-StartTime] <DateTime> [-EndTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a932-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="2a932-107">ParentObject</span></span>
```
Start-AzBatchComputeNodeServiceLogUpload [-ComputeNode] <PSComputeNode> [-ContainerUrl] <String>
 [-StartTime] <DateTime> [-EndTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a932-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2a932-108">DESCRIPTION</span></span>
<span data-ttu-id="2a932-109">Bu cmdlet, bir hatayla karşılaşırsanız ve Azure desteğine geçmek istiyorsanız, işlem düğümlerinden Azure toplu Iş hizmeti günlük dosyalarını toplar.</span><span class="sxs-lookup"><span data-stu-id="2a932-109">This cmdlet gathers Azure Batch service log files from compute nodes if you are experiencing an error and wish to escalate to Azure support.</span></span> <span data-ttu-id="2a932-110">Toplu Iş hizmetindeki hata ayıklama sorunlarına yardımcı olması için Azure toplu Iş hizmeti günlük dosyalarının Azure desteğiyle paylaşılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="2a932-110">The Azure Batch service log files should be shared with Azure support to aid in debugging issues with the Batch service.</span></span> 

## <span data-ttu-id="2a932-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2a932-111">EXAMPLES</span></span>

### <span data-ttu-id="2a932-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2a932-112">Example 1</span></span>

```powershell
PS C:\> $storageContext = New-AzStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzBatchAccountKeys -AccountName "contosobatch"
PS C:\> Start-AzBatchComputeNodeServiceLogUpload -BatchContext $batchContext -PoolId "contosopool" -ComputeNodeId "tvm-1612030122_1-20180405t234700z" -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    4 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="2a932-113">1 Ocak 2018 tarihinde veya bu tarihten sonra yazılan, Ocak gece yarısından itibaren, işlem düğümünün bulunduğu havuzun havuz kimliği (</span><span class="sxs-lookup"><span data-stu-id="2a932-113">Upload compute node service logs written on or after January 1, 2018 midnight, which were obtained from the compute node, given pool id of the pool in which the compute node resides, and compute node id.</span></span>

### <span data-ttu-id="2a932-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="2a932-114">Example 2</span></span>

```powershell
PS C:\> $storageContext = New-AzStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzBatchAccountKeys -AccountName "contosobatch"
PS C:\> Start-AzBatchComputeNodeServiceLogUpload -BatchContext $batchContext -PoolId "contosopool" -ComputeNodeId "tvm-1612030122_1-20180405t234700z" -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z" -EndTime "2018-01-10 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    2 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="2a932-115">Compute düğümünden alınan, 2018 Ocak, gece yarısı ve 10 Ocak 2018, gece yarısından itibaren yazılan COMPUTE node hizmeti günlüklerinin, işlem düğümünün bulunduğu havuzun havuz kimliği</span><span class="sxs-lookup"><span data-stu-id="2a932-115">Upload compute node service logs written on or after January 1, 2018 midnight and before January 10, 2018 midnight, which were obtained from the compute node, given pool id of the pool in which the compute node resides, and compute node id.</span></span>

### <span data-ttu-id="2a932-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="2a932-116">Example 3</span></span>

```powershell
PS C:\> $storageContext = New-AzStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzBatchAccountKeys -AccountName "contosobatch"
PS C:\> Get-AzBatchComputeNode -BatchContext $batchContext -Id "tvm-1612030122_1-20180405t234700z" -PoolId "contosopool" | Start-AzBatchComputeNodeServiceLogUpload -BatchContext $batchContext -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z" -EndTime "2018-01-10 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    2 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="2a932-117">Compute node nesnesinden edinilen 1 Ocak 2018, gece, 2018 10 Ocak, gece, gece (</span><span class="sxs-lookup"><span data-stu-id="2a932-117">Upload compute node service logs written on or after January 1, 2018 midnight and before January 10, 2018 midnight, which were obtained from the compute node object.</span></span>

## <span data-ttu-id="2a932-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2a932-118">PARAMETERS</span></span>

### <span data-ttu-id="2a932-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="2a932-119">-BatchContext</span></span>
<span data-ttu-id="2a932-120">Toplu Iş hizmetiyle etkileşim kurarken kullanılacak BatchAccountContext örneği.</span><span class="sxs-lookup"><span data-stu-id="2a932-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="2a932-121">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2a932-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="2a932-122">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="2a932-122">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="2a932-123">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2a932-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="2a932-124">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2a932-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="2a932-125">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="2a932-125">-ComputeNode</span></span>
<span data-ttu-id="2a932-126">Hizmet günlüklerinin alındığı **PSComputeNode** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a932-126">Specifies the **PSComputeNode** object from which service logs are retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: ParentObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a932-127">-Computenodeıd</span><span class="sxs-lookup"><span data-stu-id="2a932-127">-ComputeNodeId</span></span>
<span data-ttu-id="2a932-128">İşlem düğümünün kimliği.</span><span class="sxs-lookup"><span data-stu-id="2a932-128">The id of the compute node.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a932-129">-ContainerUrl</span><span class="sxs-lookup"><span data-stu-id="2a932-129">-ContainerUrl</span></span>
<span data-ttu-id="2a932-130">Azure depolama için kapsayıcı URL 'si.</span><span class="sxs-lookup"><span data-stu-id="2a932-130">The container url to Azure Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a932-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a932-131">-DefaultProfile</span></span>
<span data-ttu-id="2a932-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2a932-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a932-133">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="2a932-133">-EndTime</span></span>
<span data-ttu-id="2a932-134">Hizmet günlüğünün karşıya yüklenecek bitiş saati (isteğe bağlı).</span><span class="sxs-lookup"><span data-stu-id="2a932-134">The end time of service log to be uploaded (optional).</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a932-135">-PoolId</span><span class="sxs-lookup"><span data-stu-id="2a932-135">-PoolId</span></span>
<span data-ttu-id="2a932-136">Compute düğümünü içeren havuzun kimliği.</span><span class="sxs-lookup"><span data-stu-id="2a932-136">The id of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="2a932-137">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="2a932-137">-StartTime</span></span>
<span data-ttu-id="2a932-138">Hizmet günlüğünün karşıya yüklenmesi için başlangıç saati.</span><span class="sxs-lookup"><span data-stu-id="2a932-138">The start time of service log to be uploaded.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a932-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="2a932-139">-Confirm</span></span>
<span data-ttu-id="2a932-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2a932-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a932-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a932-141">-WhatIf</span></span>
<span data-ttu-id="2a932-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2a932-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2a932-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2a932-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a932-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a932-144">CommonParameters</span></span>
<span data-ttu-id="2a932-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2a932-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a932-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a932-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a932-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2a932-147">INPUTS</span></span>

### <span data-ttu-id="2a932-148">Microsoft.Azure.Commands.Batch. Modeller. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="2a932-148">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="2a932-149">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2a932-149">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="2a932-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2a932-150">OUTPUTS</span></span>

### <span data-ttu-id="2a932-151">Microsoft.Azure.Commands.Batch. Modeller. PSStartComputeNodeServiceLogUploadResult</span><span class="sxs-lookup"><span data-stu-id="2a932-151">Microsoft.Azure.Commands.Batch.Models.PSStartComputeNodeServiceLogUploadResult</span></span>

## <span data-ttu-id="2a932-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2a932-152">NOTES</span></span>

## <span data-ttu-id="2a932-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2a932-153">RELATED LINKS</span></span>