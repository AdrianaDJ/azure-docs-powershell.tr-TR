---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C9E2D9EC-3B6A-492D-B183-9856185548CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchnodefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
ms.openlocfilehash: b04461caa9b3f10438706a5a2a2017eef3e71cb3
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93938680"
---
# <span data-ttu-id="2a3ad-101">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="2a3ad-101">Get-AzBatchNodeFileContent</span></span>

## <span data-ttu-id="2a3ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a3ad-102">SYNOPSIS</span></span>
<span data-ttu-id="2a3ad-103">Bir toplu Iş düğümü dosyası alır.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-103">Gets a Batch node file.</span></span>

## <span data-ttu-id="2a3ad-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2a3ad-104">SYNTAX</span></span>

### <span data-ttu-id="2a3ad-105">Task_Id_Path</span><span class="sxs-lookup"><span data-stu-id="2a3ad-105">Task_Id_Path</span></span>
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationPath <String>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a3ad-106">Task_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="2a3ad-106">Task_Id_Stream</span></span>
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a3ad-107">ComputeNode_Id_Path</span><span class="sxs-lookup"><span data-stu-id="2a3ad-107">ComputeNode_Id_Path</span></span>
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationPath <String> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a3ad-108">ComputeNode_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="2a3ad-108">ComputeNode_Id_Stream</span></span>
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationStream <Stream> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a3ad-109">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="2a3ad-109">InputObject_Path</span></span>
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationPath <String> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2a3ad-110">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="2a3ad-110">InputObject_Stream</span></span>
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationStream <Stream> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2a3ad-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="2a3ad-111">DESCRIPTION</span></span>
<span data-ttu-id="2a3ad-112">**Get-AzBatchNodeFileContent** cmdlet 'ı bir Azure toplu iş düğümü dosyası alır ve bunu bir dosya veya akışa kaydeder.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-112">The **Get-AzBatchNodeFileContent** cmdlet gets an Azure Batch node file and saves it as a file or to a stream.</span></span>

## <span data-ttu-id="2a3ad-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2a3ad-113">EXAMPLES</span></span>

### <span data-ttu-id="2a3ad-114">Örnek 1: görevle ilişkilendirilmiş bir toplu Iş düğümü dosyası alma ve dosyayı kaydetme</span><span class="sxs-lookup"><span data-stu-id="2a3ad-114">Example 1: Get a Batch node file associated with a task and save the file</span></span>
```
PS C:\>Get-AzBatchNodeFileContent -JobId "Job01" -TaskId "Task01" -Path "StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="2a3ad-115">Bu komut, StdOut.txt adlı düğüm dosyasını alır ve yerel bilgisayardaki E:\PowerShell\StdOut.txt dosya yoluna kaydeder.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-115">This command gets the node file that is named StdOut.txt, and saves it to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="2a3ad-116">StdOut.txt düğümü, KIMLIĞI Job01 olan iş için KIMLIĞI Task01 olan görevle ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-116">The StdOut.txt node file is associated with task that has the ID Task01 for the job that has the ID Job01.</span></span>
<span data-ttu-id="2a3ad-117">$Context değişkenine bağlam atamak için Get-AzBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-117">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="2a3ad-118">Örnek 2: bir toplu Iş düğümü dosyası alın ve ardışık düzeni kullanarak belirtilen dosya yoluna kaydedin</span><span class="sxs-lookup"><span data-stu-id="2a3ad-118">Example 2: Get a Batch node file and save it to a specified file path using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job02" -TaskId "Task02" -Path "StdErr.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="2a3ad-119">Bu komut, StdErr.txt adındaki düğüm dosyasını Get-AzBatchNodeFile cmdlet 'i kullanarak alır.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-119">This command gets the node file that is named StdErr.txt by using the Get-AzBatchNodeFile cmdlet.</span></span>
<span data-ttu-id="2a3ad-120">Komut, ardışık düzen işlecini kullanarak bu dosyayı geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-120">The command passes that file to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2a3ad-121">Geçerli cmdlet, dosyayı yerel bilgisayardaki E:\PowerShell\StdOut.txt dosya yoluna kaydeder.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-121">The current cmdlet saves that file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="2a3ad-122">StdOut.txt düğümü, KIMLIĞI Job02 olan iş için KIMLIĞI Task02 olan görevle ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-122">The StdOut.txt node file is associated with the task that has the ID Task02 for the job that has the ID Job02.</span></span>

### <span data-ttu-id="2a3ad-123">Örnek 3: görevle ilişkilendirilmiş bir toplu Iş düğümü dosyası alma ve bunu bir akışa yönlendirme</span><span class="sxs-lookup"><span data-stu-id="2a3ad-123">Example 3: Get a Batch node file associated with a task and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -JobId "Job03" -TaskId "Task11" -Path "StdOut.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="2a3ad-124">İlk komut New-Object cmdlet 'ini kullanarak bir akış oluşturur ve $Stream değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-124">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="2a3ad-125">İkinci komut, KIMLIĞI Job03 olan iş için KIMLIĞI Task11 olan görevden StdOut.txt adlı düğüm dosyasını alır.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-125">The second command gets the node file that is named StdOut.txt from the task that has the ID Task11 for the job that has the ID Job03.</span></span>
<span data-ttu-id="2a3ad-126">Komut dosya içeriğini $Stream akışa yönlendirir.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-126">The command directs file contents to the stream in $Stream.</span></span>

### <span data-ttu-id="2a3ad-127">Örnek 4: işlem düğümünden bir düğüm dosyası alma ve kaydetme</span><span class="sxs-lookup"><span data-stu-id="2a3ad-127">Example 4: Get a node file from a compute node and save it</span></span>
```
PS C:\>Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="2a3ad-128">Bu komut, ComputeNode01 kimliğine sahip havuzda KIMLIK Pool01 olan işlem düğümünden düğüm dosyası Startup\StdOut.txt alır.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-128">This command gets the node file Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="2a3ad-129">Komut dosyayı yerel bilgisayardaki E:\PowerShell\StdOut.txt dosya yoluna kaydeder.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-129">The command saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="2a3ad-130">Örnek 5: işlem düğümünden bir düğüm dosyası alın ve bunu ardışık düzen kullanarak kaydedin</span><span class="sxs-lookup"><span data-stu-id="2a3ad-130">Example 5: Get a node file from a compute node and save it by using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="2a3ad-131">Bu komut, ComputeNode01 KIMLIĞINE sahip işlem düğümünden Get-AzBatchNodeFile kullanarak düğüm dosyası Startup\StdOut.txt alır.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-131">This command gets the node file Startup\StdOut.txt by using Get-AzBatchNodeFile from the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="2a3ad-132">Compute düğümü, KIMLIK Pool01 havuzunda.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-132">The compute node is in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="2a3ad-133">Komut bu düğüm dosyasını geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-133">The command passes that node file to the current cmdlet.</span></span>
<span data-ttu-id="2a3ad-134">Bu cmdlet dosyayı yerel bilgisayardaki E:\PowerShell\StdOut.txt dosya yoluna kaydeder.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-134">That cmdlet saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="2a3ad-135">Örnek 6: işlem düğümünden bir düğüm dosyası alın ve bunu bir akışa yönlendirin</span><span class="sxs-lookup"><span data-stu-id="2a3ad-135">Example 6: Get a node file from a compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "startup\stdout.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="2a3ad-136">İlk komut New-Object cmdlet 'ini kullanarak bir akış oluşturur ve $Stream değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-136">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="2a3ad-137">İkinci komut, KIMLIĞI Pool01 olan havuzda KIMLIĞI ComputeNode01 olan COMPUTE düğümünden StdOut.txt adlı düğüm dosyasını alır.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-137">The second command gets the node file that is named StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="2a3ad-138">Komut dosya içeriğini $Stream akışa yönlendirir.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-138">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="2a3ad-139">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2a3ad-139">PARAMETERS</span></span>

### <span data-ttu-id="2a3ad-140">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="2a3ad-140">-BatchContext</span></span>
<span data-ttu-id="2a3ad-141">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-141">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2a3ad-142">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-142">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="2a3ad-143">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-143">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="2a3ad-144">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-144">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="2a3ad-145">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-145">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="2a3ad-146">-ByteRangeEnd</span><span class="sxs-lookup"><span data-stu-id="2a3ad-146">-ByteRangeEnd</span></span>
<span data-ttu-id="2a3ad-147">İndirilecek bayt aralığının sonu.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-147">The end of the byte range to be downloaded.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a3ad-148">-ByteRangeStart</span><span class="sxs-lookup"><span data-stu-id="2a3ad-148">-ByteRangeStart</span></span>
<span data-ttu-id="2a3ad-149">İndirilecek bayt aralığının başlangıcı.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-149">The start of the byte range to be downloaded.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a3ad-150">-Computenodeıd</span><span class="sxs-lookup"><span data-stu-id="2a3ad-150">-ComputeNodeId</span></span>
<span data-ttu-id="2a3ad-151">Bu cmdlet 'in döndürdüğü düğüm dosyasını içeren COMPUTE düğümünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-151">Specifies the ID of the compute node that contains the node file that this cmdlet returns.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a3ad-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a3ad-152">-DefaultProfile</span></span>
<span data-ttu-id="2a3ad-153">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a3ad-154">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="2a3ad-154">-DestinationPath</span></span>
<span data-ttu-id="2a3ad-155">Bu cmdlet 'in düğüm dosyasını kaydettiği dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-155">Specifies the file path where this cmdlet saves the node file.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, ComputeNode_Id_Path, InputObject_Path
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a3ad-156">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="2a3ad-156">-DestinationStream</span></span>
<span data-ttu-id="2a3ad-157">Bu cmdlet 'in düğüm dosyası içeriğini yazdığı akışı belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-157">Specifies the stream into which this cmdlet writes the node file contents.</span></span>
<span data-ttu-id="2a3ad-158">Bu cmdlet bu akışı kapatmaz veya geri sarmaz.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-158">This cmdlet does not close or rewind this stream.</span></span>

```yaml
Type: System.IO.Stream
Parameter Sets: Task_Id_Stream, ComputeNode_Id_Stream, InputObject_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a3ad-159">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a3ad-159">-InputObject</span></span>
<span data-ttu-id="2a3ad-160">Bu cmdlet 'in aldığı dosyayı, **Psnodefile** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-160">Specifies the file that this cmdlet gets, as a **PSNodeFile** object.</span></span>
<span data-ttu-id="2a3ad-161">Düğüm dosyası nesnesi edinmek için Get-AzBatchNodeFile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-161">To obtain a node file object, use the Get-AzBatchNodeFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNodeFile
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a3ad-162">-JobId</span><span class="sxs-lookup"><span data-stu-id="2a3ad-162">-JobId</span></span>
<span data-ttu-id="2a3ad-163">Hedef görevi içeren işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-163">Specifies the ID of the job that contains the target task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a3ad-164">-Yol</span><span class="sxs-lookup"><span data-stu-id="2a3ad-164">-Path</span></span>
<span data-ttu-id="2a3ad-165">İndirilecek olan düğüm dosyasının yolu.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-165">The path of the node file to download.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream, ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a3ad-166">-PoolId</span><span class="sxs-lookup"><span data-stu-id="2a3ad-166">-PoolId</span></span>
<span data-ttu-id="2a3ad-167">Bu cmdlet 'in aldığı düğüm dosyasını içeren COMPUTE düğümünü içeren havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-167">Specifies the ID of the pool that contains the compute node that contains the node file that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a3ad-168">-TaskID</span><span class="sxs-lookup"><span data-stu-id="2a3ad-168">-TaskId</span></span>
<span data-ttu-id="2a3ad-169">Görevin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-169">Specifies the ID of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a3ad-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a3ad-170">CommonParameters</span></span>
<span data-ttu-id="2a3ad-171">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2a3ad-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a3ad-172">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a3ad-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a3ad-173">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2a3ad-173">INPUTS</span></span>

### <span data-ttu-id="2a3ad-174">System. String</span><span class="sxs-lookup"><span data-stu-id="2a3ad-174">System.String</span></span>

### <span data-ttu-id="2a3ad-175">Microsoft.Azure.Commands.Batch. Modeller. PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="2a3ad-175">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

### <span data-ttu-id="2a3ad-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2a3ad-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="2a3ad-177">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2a3ad-177">OUTPUTS</span></span>

### <span data-ttu-id="2a3ad-178">System. void</span><span class="sxs-lookup"><span data-stu-id="2a3ad-178">System.Void</span></span>

## <span data-ttu-id="2a3ad-179">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2a3ad-179">NOTES</span></span>

## <span data-ttu-id="2a3ad-180">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2a3ad-180">RELATED LINKS</span></span>

[<span data-ttu-id="2a3ad-181">Get-Aztopluaccountkeys</span><span class="sxs-lookup"><span data-stu-id="2a3ad-181">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="2a3ad-182">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="2a3ad-182">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="2a3ad-183">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="2a3ad-183">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)

