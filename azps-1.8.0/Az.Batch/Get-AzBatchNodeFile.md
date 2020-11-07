---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 38ED2854-23D0-400E-A5C8-239346B2AF99
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFile.md
ms.openlocfilehash: 3337cfa2423d6bc3a26c96ea734ce517f2707a04
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93761879"
---
# <span data-ttu-id="f0c8d-101">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="f0c8d-101">Get-AzBatchNodeFile</span></span>

## <span data-ttu-id="f0c8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0c8d-102">SYNOPSIS</span></span>
<span data-ttu-id="f0c8d-103">Toplu Iş düğümü dosyalarının özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="f0c8d-103">Gets the properties of Batch node files.</span></span>

## <span data-ttu-id="f0c8d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f0c8d-104">SYNTAX</span></span>

### <span data-ttu-id="f0c8d-105">ComputeNode_Id (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f0c8d-105">ComputeNode_Id (Default)</span></span>
```
Get-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [[-Path] <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0c8d-106">Task_Id</span><span class="sxs-lookup"><span data-stu-id="f0c8d-106">Task_Id</span></span>
```
Get-AzBatchNodeFile -JobId <String> -TaskId <String> [[-Path] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0c8d-107">Task_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="f0c8d-107">Task_ODataFilter</span></span>
```
Get-AzBatchNodeFile -JobId <String> -TaskId <String> [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0c8d-108">ParentTask</span><span class="sxs-lookup"><span data-stu-id="f0c8d-108">ParentTask</span></span>
```
Get-AzBatchNodeFile [[-Task] <PSCloudTask>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0c8d-109">ComputeNode_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="f0c8d-109">ComputeNode_ODataFilter</span></span>
```
Get-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Recursive] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f0c8d-110">ParentComputeNode</span><span class="sxs-lookup"><span data-stu-id="f0c8d-110">ParentComputeNode</span></span>
```
Get-AzBatchNodeFile [[-ComputeNode] <PSComputeNode>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0c8d-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="f0c8d-111">DESCRIPTION</span></span>
<span data-ttu-id="f0c8d-112">**Get-AzBatchNodeFile** cmdlet 'i, görevin veya compute düğümünün Azure toplu iş düğümü dosyalarının özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="f0c8d-112">The **Get-AzBatchNodeFile** cmdlet gets the properties of the Azure Batch node files of a task or compute node.</span></span>
<span data-ttu-id="f0c8d-113">Sonuçlarınızı daraltmak için, açık bir veri Protokolü (OData) filtresi belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f0c8d-113">To narrow your results, you can specify an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="f0c8d-114">Bir görev belirtirseniz ancak filtre belirtmezseniz, bu cmdlet bu görevle ilgili tüm düğüm dosyalarının özelliklerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="f0c8d-114">If you specify a task, but not a filter, this cmdlet returns properties for all node files for that task.</span></span>
<span data-ttu-id="f0c8d-115">Bir işlem düğümü belirtirseniz ancak filtre belirtmezseniz, bu cmdlet bu işlem düğümündeki tüm düğüm dosyalarının özelliklerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="f0c8d-115">If you specify a compute node, but not a filter, this cmdlet returns properties for all node files for that compute node.</span></span>

## <span data-ttu-id="f0c8d-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f0c8d-116">EXAMPLES</span></span>

### <span data-ttu-id="f0c8d-117">Örnek 1: görevle ilişkili bir düğüm dosyasının özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="f0c8d-117">Example 1: Get the properties of a node file associated with a task</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "Stdout.txt" -BatchContext $Context
IsDirectory Name          Properties                                      Url

----------- ----          ----------                                      ---

False       StdOut.txt    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="f0c8d-118">Bu komut, Task26 kimliğine sahip olan görevle ilişkili StdOut.txt düğümü dosyasının özelliklerini alır-000001.</span><span class="sxs-lookup"><span data-stu-id="f0c8d-118">This command gets the properties of the StdOut.txt node file associated with the task that has the ID Task26 in the job that has the ID Job-000001.</span></span>
<span data-ttu-id="f0c8d-119">$Context değişkenine bağlam atamak için Get-AzBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f0c8d-119">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="f0c8d-120">Örnek 2: filtre kullanarak görevle ilişkili düğüm dosyalarının özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="f0c8d-120">Example 2: Get the properties of node files associated with a task by using a filter</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-00002" -TaskId "Task26" -Filter "startswith(name,'St')" -BatchContext $Context
IsDirectory Name        Properties                                      Url

----------- ----        ----------                                      ---

False       StdErr.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       StdOut.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="f0c8d-121">Bu komut adları St ile başlayan ve KIMLIĞI Iş-00002 olan iş altındaki KIMLIĞI Task26 olan görevle ilişkili olan düğüm dosyalarının özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="f0c8d-121">This command gets the properties of the node files whose names start with st and are associated with task that has the ID Task26 under job that has the ID Job-00002.</span></span>

### <span data-ttu-id="f0c8d-122">Örnek 3: görevle ilişkili düğüm dosyalarının özelliklerini yinelemeli olarak alma</span><span class="sxs-lookup"><span data-stu-id="f0c8d-122">Example 3: Recursively get the properties of node files associated with a task</span></span>
```
PS C:\>Get-AzBatchTask "Job-00003" "Task31" -BatchContext $Context | Get-AzBatchNodeFile -Recursive -BatchContext $Context
IsDirectory Name             Properties                                      Url

----------- ----             ----------                                      ---

False       ProcessEnv.cmd   Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       StdErr.txt       Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       StdOut.txt       Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
True        wd                                                               https://cmdletexample.westus.Batch.contoso... 
False       wd\newFile.txt   Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="f0c8d-123">Bu komut, Task31 iş Işinde KIMLIĞI olan görevle ilişkili tüm dosyaların özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="f0c8d-123">This command gets the properties of all files associated with the task that has the ID Task31 in job Job-00003.</span></span>
<span data-ttu-id="f0c8d-124">Bu komut *özyinelemeli* parametreyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0c8d-124">This command specifies the *Recursive* parameter.</span></span>
<span data-ttu-id="f0c8d-125">Bu nedenle, cmdlet özyinelemeli bir dosya araması gerçekleştirir ve wd\newFile.txt düğümü dosyasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="f0c8d-125">Therefore, the cmdlet performs a recursive file search is performed, and returns the wd\newFile.txt node file.</span></span>

### <span data-ttu-id="f0c8d-126">Örnek 4: işlem düğümünden tek bir dosya alma</span><span class="sxs-lookup"><span data-stu-id="f0c8d-126">Example 4: Get a single file from a compute node</span></span>
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context
IsDirectory Name                    Properties                                      Url
----------- ----                    ----------                                      ---
False       startup\stdout.txt      Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="f0c8d-127">Bu komut, ComputeNode01 kimliğine sahip havuzda KIMLIK Pool22 olan COMPUTE düğümünden Startup\StdOut.txt adlı dosyayı alır.</span><span class="sxs-lookup"><span data-stu-id="f0c8d-127">This command gets the file that is named Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

### <span data-ttu-id="f0c8d-128">Örnek 5: işlem düğümünden bir klasörün altındaki tüm dosyaları alma</span><span class="sxs-lookup"><span data-stu-id="f0c8d-128">Example 5: Get all files under a folder from a compute node</span></span>
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Filter "startswith(name,'startup')" -Recursive -BatchContext $Context
IsDirectory Name                      Properties                                      Url
----------- ----                      ----------                                      ---
True        startup                                                                   https://cmdletexample.westus.Batch.contoso... 
False       startup\ProcessEnv.cmd    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       startup\stderr.txt        Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       startup\stdout.txt        Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
True        startup\wd                                                                https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="f0c8d-129">Bu komut, ComputeNode01 kimliğine sahip havuzda KIMLIK Pool22 olan işlem düğümündeki başlangıç klasörünün altındaki tüm dosyaları alır.</span><span class="sxs-lookup"><span data-stu-id="f0c8d-129">This command gets all the files under the startup folder from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>
<span data-ttu-id="f0c8d-130">Bu cmdlet *özyinelemeli* parametreyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0c8d-130">This cmdlet specifies the *Recursive* parameter.</span></span>

### <span data-ttu-id="f0c8d-131">Örnek 6: işlem düğümünün kök klasöründen dosyaları alma</span><span class="sxs-lookup"><span data-stu-id="f0c8d-131">Example 6: Get files from the root folder of a compute node</span></span>
```
PS C:\>Get-AzBatchComputeNode "Pool22" -Id "ComputeNode01" -BatchContext $Context | Get-AzBatchNodeFile -BatchContext $Context
IsDirectory Name           Properties       Url
----------- ----           ----------       ---
True        shared                          https://cmdletexample.westus.Batch.contoso... 
True        startup                         https://cmdletexample.westus.Batch.contoso... 
True        workitems                       https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="f0c8d-132">Bu komut, ComputeNode01 kimliğine sahip havuzda KIMLIK Pool22 olan kök klasördeki tüm dosyaları alır.</span><span class="sxs-lookup"><span data-stu-id="f0c8d-132">This command gets all the files at the root folder of the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

## <span data-ttu-id="f0c8d-133">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f0c8d-133">PARAMETERS</span></span>

### <span data-ttu-id="f0c8d-134">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f0c8d-134">-BatchContext</span></span>
<span data-ttu-id="f0c8d-135">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0c8d-135">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f0c8d-136">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f0c8d-136">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f0c8d-137">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="f0c8d-137">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f0c8d-138">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f0c8d-138">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f0c8d-139">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f0c8d-139">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f0c8d-140">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="f0c8d-140">-ComputeNode</span></span>
<span data-ttu-id="f0c8d-141">Compute düğümünü, toplu Iş düğümü dosyalarını içeren bir **PSComputeNode** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0c8d-141">Specifies the compute node, as a **PSComputeNode** object, that contains the Batch node files.</span></span>
<span data-ttu-id="f0c8d-142">Compute node nesnesi edinmek için Get-AzBatchComputeNode cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f0c8d-142">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: ParentComputeNode
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0c8d-143">-Computenodeıd</span><span class="sxs-lookup"><span data-stu-id="f0c8d-143">-ComputeNodeId</span></span>
<span data-ttu-id="f0c8d-144">Toplu Iş düğümü dosyalarını içeren COMPUTE düğümünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0c8d-144">Specifies the ID of the compute node that contains the Batch node files.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id, ComputeNode_ODataFilter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0c8d-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0c8d-145">-DefaultProfile</span></span>
<span data-ttu-id="f0c8d-146">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f0c8d-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0c8d-147">-Filtre</span><span class="sxs-lookup"><span data-stu-id="f0c8d-147">-Filter</span></span>
<span data-ttu-id="f0c8d-148">Bir OData filtre yan tümcesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0c8d-148">Specifies an OData filter clause.</span></span>
<span data-ttu-id="f0c8d-149">Bu cmdlet, bu parametrenin belirttiği filtreyle eşleşen düğüm dosyalarının özelliklerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="f0c8d-149">This cmdlet returns properties for node files that match the filter that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c8d-150">-JobId</span><span class="sxs-lookup"><span data-stu-id="f0c8d-150">-JobId</span></span>
<span data-ttu-id="f0c8d-151">Hedef görevi içeren işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0c8d-151">Specifies the ID of the job that contains the target task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id, Task_ODataFilter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0c8d-152">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="f0c8d-152">-MaxCount</span></span>
<span data-ttu-id="f0c8d-153">Bu cmdlet 'in özellikleri döndürdüğü en fazla düğüm dosyası sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0c8d-153">Specifies the maximum number of node files for which this cmdlet returns properties.</span></span>
<span data-ttu-id="f0c8d-154">Sıfır (0) veya daha kısa bir değer belirtirseniz cmdlet üst sınırı kullanmaz.</span><span class="sxs-lookup"><span data-stu-id="f0c8d-154">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="f0c8d-155">Varsayılan değer 1000 ' dır.</span><span class="sxs-lookup"><span data-stu-id="f0c8d-155">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c8d-156">-Yol</span><span class="sxs-lookup"><span data-stu-id="f0c8d-156">-Path</span></span>
<span data-ttu-id="f0c8d-157">Bu cmdlet 'in özellikleri aldığı düğüm dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0c8d-157">Specifies the path of the node file for which this cmdlet retrieves properties.</span></span>
<span data-ttu-id="f0c8d-158">Joker karakterler belirtemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="f0c8d-158">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id, Task_Id
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c8d-159">-PoolId</span><span class="sxs-lookup"><span data-stu-id="f0c8d-159">-PoolId</span></span>
<span data-ttu-id="f0c8d-160">Düğüm dosyalarının özelliklerini almak istediğiniz COMPUTE düğümünü içeren havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0c8d-160">Specifies the ID of the pool that contains the compute node from which to get properties of node files.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id, ComputeNode_ODataFilter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0c8d-161">-Yinelemeli</span><span class="sxs-lookup"><span data-stu-id="f0c8d-161">-Recursive</span></span>
<span data-ttu-id="f0c8d-162">Bu cmdlet 'in özyinelemeli dosya listesi döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="f0c8d-162">Indicates that this cmdlet returns a recursive list of files.</span></span>
<span data-ttu-id="f0c8d-163">Aksi halde, yalnızca kök klasördeki dosyaları döndürür.</span><span class="sxs-lookup"><span data-stu-id="f0c8d-163">Otherwise, it returns only the files in the root folder.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c8d-164">-Görev</span><span class="sxs-lookup"><span data-stu-id="f0c8d-164">-Task</span></span>
<span data-ttu-id="f0c8d-165">Görevi, düğüm dosyalarının ilişkili olduğu bir **Ince görev** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0c8d-165">Specifies the task, as a **PSCloudTask** object, with which the node files are associated.</span></span>
<span data-ttu-id="f0c8d-166">Görev nesnesi almak için Get-AzBatchTask cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f0c8d-166">To obtain a task object, use the Get-AzBatchTask cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: ParentTask
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0c8d-167">-TaskID</span><span class="sxs-lookup"><span data-stu-id="f0c8d-167">-TaskId</span></span>
<span data-ttu-id="f0c8d-168">Bu cmdlet 'in düğüm dosyalarının özelliklerini aldığı görevin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0c8d-168">Specifies the ID of the task for which this cmdlet gets properties of node files.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id, Task_ODataFilter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0c8d-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0c8d-169">CommonParameters</span></span>
<span data-ttu-id="f0c8d-170">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f0c8d-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0c8d-171">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0c8d-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0c8d-172">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f0c8d-172">INPUTS</span></span>

### <span data-ttu-id="f0c8d-173">System. String</span><span class="sxs-lookup"><span data-stu-id="f0c8d-173">System.String</span></span>

### <span data-ttu-id="f0c8d-174">Microsoft.Azure.Commands.Batch. Modeller. Ince görev</span><span class="sxs-lookup"><span data-stu-id="f0c8d-174">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="f0c8d-175">Microsoft.Azure.Commands.Batch. Modeller. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="f0c8d-175">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="f0c8d-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f0c8d-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f0c8d-177">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f0c8d-177">OUTPUTS</span></span>

### <span data-ttu-id="f0c8d-178">Microsoft.Azure.Commands.Batch. Modeller. PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="f0c8d-178">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

## <span data-ttu-id="f0c8d-179">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f0c8d-179">NOTES</span></span>

## <span data-ttu-id="f0c8d-180">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f0c8d-180">RELATED LINKS</span></span>

[<span data-ttu-id="f0c8d-181">Get-Aztopluaccountkeys</span><span class="sxs-lookup"><span data-stu-id="f0c8d-181">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="f0c8d-182">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="f0c8d-182">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="f0c8d-183">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="f0c8d-183">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)

[<span data-ttu-id="f0c8d-184">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="f0c8d-184">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="f0c8d-185">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="f0c8d-185">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


