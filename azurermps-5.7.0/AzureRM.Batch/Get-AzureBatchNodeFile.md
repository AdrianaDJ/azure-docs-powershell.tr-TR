---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 38ED2854-23D0-400E-A5C8-239346B2AF99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFile.md
ms.openlocfilehash: ac9a49b52dd2fecea12e3084e4d86077ddb06cb5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591729"
---
# <span data-ttu-id="cf7e1-101">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="cf7e1-101">Get-AzureBatchNodeFile</span></span>

## <span data-ttu-id="cf7e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf7e1-102">SYNOPSIS</span></span>
<span data-ttu-id="cf7e1-103">Toplu Iş düğümü dosyalarının özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="cf7e1-103">Gets the properties of Batch node files.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf7e1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cf7e1-104">SYNTAX</span></span>

### <span data-ttu-id="cf7e1-105">ComputeNode_Id (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cf7e1-105">ComputeNode_Id (Default)</span></span>
```
Get-AzureBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [[-Path] <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf7e1-106">Task_Id</span><span class="sxs-lookup"><span data-stu-id="cf7e1-106">Task_Id</span></span>
```
Get-AzureBatchNodeFile -JobId <String> -TaskId <String> [[-Path] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf7e1-107">Task_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="cf7e1-107">Task_ODataFilter</span></span>
```
Get-AzureBatchNodeFile -JobId <String> -TaskId <String> [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf7e1-108">ParentTask</span><span class="sxs-lookup"><span data-stu-id="cf7e1-108">ParentTask</span></span>
```
Get-AzureBatchNodeFile [[-Task] <PSCloudTask>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf7e1-109">ComputeNode_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="cf7e1-109">ComputeNode_ODataFilter</span></span>
```
Get-AzureBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Recursive] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cf7e1-110">ParentComputeNode</span><span class="sxs-lookup"><span data-stu-id="cf7e1-110">ParentComputeNode</span></span>
```
Get-AzureBatchNodeFile [[-ComputeNode] <PSComputeNode>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf7e1-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="cf7e1-111">DESCRIPTION</span></span>
<span data-ttu-id="cf7e1-112">**Get-AzureBatchNodeFile** cmdlet 'i, görevin veya compute düğümünün Azure toplu iş düğümü dosyalarının özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="cf7e1-112">The **Get-AzureBatchNodeFile** cmdlet gets the properties of the Azure Batch node files of a task or compute node.</span></span>
<span data-ttu-id="cf7e1-113">Sonuçlarınızı daraltmak için, açık bir veri Protokolü (OData) filtresi belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cf7e1-113">To narrow your results, you can specify an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="cf7e1-114">Bir görev belirtirseniz ancak filtre belirtmezseniz, bu cmdlet bu görevle ilgili tüm düğüm dosyalarının özelliklerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="cf7e1-114">If you specify a task, but not a filter, this cmdlet returns properties for all node files for that task.</span></span>
<span data-ttu-id="cf7e1-115">Bir işlem düğümü belirtirseniz ancak filtre belirtmezseniz, bu cmdlet bu işlem düğümündeki tüm düğüm dosyalarının özelliklerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="cf7e1-115">If you specify a compute node, but not a filter, this cmdlet returns properties for all node files for that compute node.</span></span>

## <span data-ttu-id="cf7e1-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cf7e1-116">EXAMPLES</span></span>

### <span data-ttu-id="cf7e1-117">Örnek 1: görevle ilişkili bir düğüm dosyasının özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="cf7e1-117">Example 1: Get the properties of a node file associated with a task</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "Stdout.txt" -BatchContext $Context
IsDirectory Name          Properties                                      Url

----------- ----          ----------                                      ---

False       StdOut.txt    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="cf7e1-118">Bu komut, Task26 kimliğine sahip olan görevle ilişkili StdOut.txt düğümü dosyasının özelliklerini alır-000001.</span><span class="sxs-lookup"><span data-stu-id="cf7e1-118">This command gets the properties of the StdOut.txt node file associated with the task that has the ID Task26 in the job that has the ID Job-000001.</span></span>
<span data-ttu-id="cf7e1-119">$Context değişkenine bağlam atamak için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="cf7e1-119">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="cf7e1-120">Örnek 2: filtre kullanarak görevle ilişkili düğüm dosyalarının özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="cf7e1-120">Example 2: Get the properties of node files associated with a task by using a filter</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job-00002" -TaskId "Task26" -Filter "startswith(name,'St')" -BatchContext $Context
IsDirectory Name        Properties                                      Url

----------- ----        ----------                                      ---

False       StdErr.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       StdOut.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="cf7e1-121">Bu komut adları St ile başlayan ve KIMLIĞI Iş-00002 olan iş altındaki KIMLIĞI Task26 olan görevle ilişkili olan düğüm dosyalarının özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="cf7e1-121">This command gets the properties of the node files whose names start with st and are associated with task that has the ID Task26 under job that has the ID Job-00002.</span></span>

### <span data-ttu-id="cf7e1-122">Örnek 3: görevle ilişkili düğüm dosyalarının özelliklerini yinelemeli olarak alma</span><span class="sxs-lookup"><span data-stu-id="cf7e1-122">Example 3: Recursively get the properties of node files associated with a task</span></span>
```
PS C:\>Get-AzureBatchTask "Job-00003" "Task31" -BatchContext $Context | Get-AzureBatchNodeFile -Recursive -BatchContext $Context
IsDirectory Name             Properties                                      Url

----------- ----             ----------                                      ---

False       ProcessEnv.cmd   Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       StdErr.txt       Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       StdOut.txt       Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
True        wd                                                               https://cmdletexample.westus.Batch.contoso... 
False       wd\newFile.txt   Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="cf7e1-123">Bu komut, Task31 iş Işinde KIMLIĞI olan görevle ilişkili tüm dosyaların özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="cf7e1-123">This command gets the properties of all files associated with the task that has the ID Task31 in job Job-00003.</span></span>
<span data-ttu-id="cf7e1-124">Bu komut *özyinelemeli* parametreyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf7e1-124">This command specifies the *Recursive* parameter.</span></span>
<span data-ttu-id="cf7e1-125">Bu nedenle, cmdlet özyinelemeli bir dosya araması gerçekleştirir ve wd\newFile.txt düğümü dosyasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="cf7e1-125">Therefore, the cmdlet performs a recursive file search is performed, and returns the wd\newFile.txt node file.</span></span>

### <span data-ttu-id="cf7e1-126">Örnek 4: işlem düğümünden tek bir dosya alma</span><span class="sxs-lookup"><span data-stu-id="cf7e1-126">Example 4: Get a single file from a compute node</span></span>
```
PS C:\>Get-AzureBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context
IsDirectory Name                    Properties                                      Url
----------- ----                    ----------                                      ---
False       startup\stdout.txt      Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="cf7e1-127">Bu komut, ComputeNode01 kimliğine sahip havuzda KIMLIK Pool22 olan COMPUTE düğümünden Startup\StdOut.txt adlı dosyayı alır.</span><span class="sxs-lookup"><span data-stu-id="cf7e1-127">This command gets the file that is named Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

### <span data-ttu-id="cf7e1-128">Örnek 5: işlem düğümünden bir klasörün altındaki tüm dosyaları alma</span><span class="sxs-lookup"><span data-stu-id="cf7e1-128">Example 5: Get all files under a folder from a compute node</span></span>
```
PS C:\>Get-AzureBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Filter "startswith(name,'startup')" -Recursive -BatchContext $Context
IsDirectory Name                      Properties                                      Url
----------- ----                      ----------                                      ---
True        startup                                                                   https://cmdletexample.westus.Batch.contoso... 
False       startup\ProcessEnv.cmd    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       startup\stderr.txt        Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       startup\stdout.txt        Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
True        startup\wd                                                                https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="cf7e1-129">Bu komut, ComputeNode01 kimliğine sahip havuzda KIMLIK Pool22 olan işlem düğümündeki başlangıç klasörünün altındaki tüm dosyaları alır.</span><span class="sxs-lookup"><span data-stu-id="cf7e1-129">This command gets all the files under the startup folder from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>
<span data-ttu-id="cf7e1-130">Bu cmdlet *özyinelemeli* parametreyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf7e1-130">This cmdlet specifies the *Recursive* parameter.</span></span>

### <span data-ttu-id="cf7e1-131">Örnek 6: işlem düğümünün kök klasöründen dosyaları alma</span><span class="sxs-lookup"><span data-stu-id="cf7e1-131">Example 6: Get files from the root folder of a compute node</span></span>
```
PS C:\>Get-AzureBatchComputeNode "Pool22" -Id "ComputeNode01" -BatchContext $Context | Get-AzureBatchNodeFile -BatchContext $Context
IsDirectory Name           Properties       Url
----------- ----           ----------       ---
True        shared                          https://cmdletexample.westus.Batch.contoso... 
True        startup                         https://cmdletexample.westus.Batch.contoso... 
True        workitems                       https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="cf7e1-132">Bu komut, ComputeNode01 kimliğine sahip havuzda KIMLIK Pool22 olan kök klasördeki tüm dosyaları alır.</span><span class="sxs-lookup"><span data-stu-id="cf7e1-132">This command gets all the files at the root folder of the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

## <span data-ttu-id="cf7e1-133">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cf7e1-133">PARAMETERS</span></span>

### <span data-ttu-id="cf7e1-134">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="cf7e1-134">-BatchContext</span></span>
<span data-ttu-id="cf7e1-135">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf7e1-135">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cf7e1-136">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="cf7e1-136">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="cf7e1-137">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="cf7e1-137">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="cf7e1-138">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="cf7e1-138">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="cf7e1-139">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="cf7e1-139">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf7e1-140">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="cf7e1-140">-ComputeNode</span></span>
<span data-ttu-id="cf7e1-141">Compute düğümünü, toplu Iş düğümü dosyalarını içeren bir **PSComputeNode** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf7e1-141">Specifies the compute node, as a **PSComputeNode** object, that contains the Batch node files.</span></span>
<span data-ttu-id="cf7e1-142">Compute node nesnesi edinmek için Get-AzureBatchComputeNode cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="cf7e1-142">To obtain a compute node object, use the Get-AzureBatchComputeNode cmdlet.</span></span>

```yaml
Type: PSComputeNode
Parameter Sets: ParentComputeNode
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf7e1-143">-Computenodeıd</span><span class="sxs-lookup"><span data-stu-id="cf7e1-143">-ComputeNodeId</span></span>
<span data-ttu-id="cf7e1-144">Toplu Iş düğümü dosyalarını içeren COMPUTE düğümünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf7e1-144">Specifies the ID of the compute node that contains the Batch node files.</span></span>

```yaml
Type: String
Parameter Sets: ComputeNode_Id, ComputeNode_ODataFilter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf7e1-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf7e1-145">-DefaultProfile</span></span>
<span data-ttu-id="cf7e1-146">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cf7e1-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf7e1-147">-Filtre</span><span class="sxs-lookup"><span data-stu-id="cf7e1-147">-Filter</span></span>
<span data-ttu-id="cf7e1-148">Bir OData filtre yan tümcesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf7e1-148">Specifies an OData filter clause.</span></span>
<span data-ttu-id="cf7e1-149">Bu cmdlet, bu parametrenin belirttiği filtreyle eşleşen düğüm dosyalarının özelliklerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="cf7e1-149">This cmdlet returns properties for node files that match the filter that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf7e1-150">-JobId</span><span class="sxs-lookup"><span data-stu-id="cf7e1-150">-JobId</span></span>
<span data-ttu-id="cf7e1-151">Hedef görevi içeren işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf7e1-151">Specifies the ID of the job that contains the target task.</span></span>

```yaml
Type: String
Parameter Sets: Task_Id, Task_ODataFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf7e1-152">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="cf7e1-152">-MaxCount</span></span>
<span data-ttu-id="cf7e1-153">Bu cmdlet 'in özellikleri döndürdüğü en fazla düğüm dosyası sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf7e1-153">Specifies the maximum number of node files for which this cmdlet returns properties.</span></span>
<span data-ttu-id="cf7e1-154">Sıfır (0) veya daha kısa bir değer belirtirseniz cmdlet üst sınırı kullanmaz.</span><span class="sxs-lookup"><span data-stu-id="cf7e1-154">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="cf7e1-155">Varsayılan değer 1000 ' dır.</span><span class="sxs-lookup"><span data-stu-id="cf7e1-155">The default value is 1000.</span></span>

```yaml
Type: Int32
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf7e1-156">-Yol</span><span class="sxs-lookup"><span data-stu-id="cf7e1-156">-Path</span></span>
<span data-ttu-id="cf7e1-157">Bu cmdlet 'in özellikleri aldığı düğüm dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf7e1-157">Specifies the path of the node file for which this cmdlet retrieves properties.</span></span>
<span data-ttu-id="cf7e1-158">Joker karakterler belirtemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="cf7e1-158">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: ComputeNode_Id, Task_Id
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf7e1-159">-PoolId</span><span class="sxs-lookup"><span data-stu-id="cf7e1-159">-PoolId</span></span>
<span data-ttu-id="cf7e1-160">Düğüm dosyalarının özelliklerini almak istediğiniz COMPUTE düğümünü içeren havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf7e1-160">Specifies the ID of the pool that contains the compute node from which to get properties of node files.</span></span>

```yaml
Type: String
Parameter Sets: ComputeNode_Id, ComputeNode_ODataFilter
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf7e1-161">-Yinelemeli</span><span class="sxs-lookup"><span data-stu-id="cf7e1-161">-Recursive</span></span>
<span data-ttu-id="cf7e1-162">Bu cmdlet 'in özyinelemeli dosya listesi döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="cf7e1-162">Indicates that this cmdlet returns a recursive list of files.</span></span>
<span data-ttu-id="cf7e1-163">Aksi halde, yalnızca kök klasördeki dosyaları döndürür.</span><span class="sxs-lookup"><span data-stu-id="cf7e1-163">Otherwise, it returns only the files in the root folder.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf7e1-164">-Görev</span><span class="sxs-lookup"><span data-stu-id="cf7e1-164">-Task</span></span>
<span data-ttu-id="cf7e1-165">Görevi, düğüm dosyalarının ilişkili olduğu bir **Ince görev** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf7e1-165">Specifies the task, as a **PSCloudTask** object, with which the node files are associated.</span></span>
<span data-ttu-id="cf7e1-166">Görev nesnesi almak için Get-AzureBatchTask cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="cf7e1-166">To obtain a task object, use the Get-AzureBatchTask cmdlet.</span></span>

```yaml
Type: PSCloudTask
Parameter Sets: ParentTask
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf7e1-167">-TaskID</span><span class="sxs-lookup"><span data-stu-id="cf7e1-167">-TaskId</span></span>
<span data-ttu-id="cf7e1-168">Bu cmdlet 'in düğüm dosyalarının özelliklerini aldığı görevin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf7e1-168">Specifies the ID of the task for which this cmdlet gets properties of node files.</span></span>

```yaml
Type: String
Parameter Sets: Task_Id, Task_ODataFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf7e1-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf7e1-169">CommonParameters</span></span>
<span data-ttu-id="cf7e1-170">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cf7e1-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf7e1-171">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf7e1-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf7e1-172">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cf7e1-172">INPUTS</span></span>

### <span data-ttu-id="cf7e1-173">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cf7e1-173">BatchAccountContext</span></span>
<span data-ttu-id="cf7e1-174">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="cf7e1-174">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="cf7e1-175">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="cf7e1-175">PSComputeNode</span></span>
<span data-ttu-id="cf7e1-176">' ComputeNode ' parametresi ardışık düzen için ' PSComputeNode ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="cf7e1-176">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

### <span data-ttu-id="cf7e1-177">Ince görev</span><span class="sxs-lookup"><span data-stu-id="cf7e1-177">PSCloudTask</span></span>
<span data-ttu-id="cf7e1-178">Parametre ' görev ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="cf7e1-178">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="cf7e1-179">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cf7e1-179">OUTPUTS</span></span>

### <span data-ttu-id="cf7e1-180">PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="cf7e1-180">PSNodeFile</span></span>

## <span data-ttu-id="cf7e1-181">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cf7e1-181">NOTES</span></span>

## <span data-ttu-id="cf7e1-182">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cf7e1-182">RELATED LINKS</span></span>

[<span data-ttu-id="cf7e1-183">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="cf7e1-183">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="cf7e1-184">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="cf7e1-184">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="cf7e1-185">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="cf7e1-185">Get-AzureBatchNodeFileContent</span></span>](./Get-AzureBatchNodeFileContent.md)

[<span data-ttu-id="cf7e1-186">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="cf7e1-186">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="cf7e1-187">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="cf7e1-187">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


