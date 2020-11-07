---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C9E2D9EC-3B6A-492D-B183-9856185548CD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFileContent.md
ms.openlocfilehash: 92c485a743372eff7ddb8725172ac4d9bb030d22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764085"
---
# <span data-ttu-id="f5227-101">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="f5227-101">Get-AzureBatchNodeFileContent</span></span>

## <span data-ttu-id="f5227-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5227-102">SYNOPSIS</span></span>
<span data-ttu-id="f5227-103">Bir toplu Iş düğümü dosyası alır.</span><span class="sxs-lookup"><span data-stu-id="f5227-103">Gets a Batch node file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5227-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f5227-104">SYNTAX</span></span>

### <span data-ttu-id="f5227-105">Task_Id_Path</span><span class="sxs-lookup"><span data-stu-id="f5227-105">Task_Id_Path</span></span>
```
Get-AzureBatchNodeFileContent -JobId <String> -TaskId <String> [-Name] <String> -DestinationPath <String>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5227-106">Task_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="f5227-106">Task_Id_Stream</span></span>
```
Get-AzureBatchNodeFileContent -JobId <String> -TaskId <String> [-Name] <String> -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5227-107">ComputeNode_Id_Path</span><span class="sxs-lookup"><span data-stu-id="f5227-107">ComputeNode_Id_Path</span></span>
```
Get-AzureBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -DestinationPath <String> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5227-108">ComputeNode_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="f5227-108">ComputeNode_Id_Stream</span></span>
```
Get-AzureBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -DestinationStream <Stream> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5227-109">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="f5227-109">InputObject_Path</span></span>
```
Get-AzureBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationPath <String> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f5227-110">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="f5227-110">InputObject_Stream</span></span>
```
Get-AzureBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5227-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="f5227-111">DESCRIPTION</span></span>
<span data-ttu-id="f5227-112">**Get-AzureBatchNodeFileContent** cmdlet 'ı bir Azure toplu iş düğümü dosyası alır ve bunu bir dosya veya akışa kaydeder.</span><span class="sxs-lookup"><span data-stu-id="f5227-112">The **Get-AzureBatchNodeFileContent** cmdlet gets an Azure Batch node file and saves it as a file or to a stream.</span></span>

## <span data-ttu-id="f5227-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f5227-113">EXAMPLES</span></span>

### <span data-ttu-id="f5227-114">Örnek 1: görevle ilişkilendirilmiş bir toplu Iş düğümü dosyası alma ve dosyayı kaydetme</span><span class="sxs-lookup"><span data-stu-id="f5227-114">Example 1: Get a Batch node file associated with a task and save the file</span></span>
```
PS C:\>Get-AzureBatchNodeFileContent -JobId "Job01" -TaskId "Task01" -Name "StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="f5227-115">Bu komut, StdOut.txt adlı düğüm dosyasını alır ve yerel bilgisayardaki E:\PowerShell\StdOut.txt dosya yoluna kaydeder.</span><span class="sxs-lookup"><span data-stu-id="f5227-115">This command gets the node file that is named StdOut.txt, and saves it to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="f5227-116">StdOut.txt düğümü, KIMLIĞI Job01 olan iş için KIMLIĞI Task01 olan görevle ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="f5227-116">The StdOut.txt node file is associated with task that has the ID Task01 for the job that has the ID Job01.</span></span>
<span data-ttu-id="f5227-117">$Context değişkenine bağlam atamak için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f5227-117">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="f5227-118">Örnek 2: bir toplu Iş düğümü dosyası alın ve ardışık düzeni kullanarak belirtilen dosya yoluna kaydedin</span><span class="sxs-lookup"><span data-stu-id="f5227-118">Example 2: Get a Batch node file and save it to a specified file path using the pipeline</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job02" -TaskId "Task02" -Name "StdErr.txt" -BatchContext $Context | Get-AzureBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="f5227-119">Bu komut, StdErr.txt adındaki düğüm dosyasını Get-AzureBatchNodeFile cmdlet 'i kullanarak alır.</span><span class="sxs-lookup"><span data-stu-id="f5227-119">This command gets the node file that is named StdErr.txt by using the Get-AzureBatchNodeFile cmdlet.</span></span>
<span data-ttu-id="f5227-120">Komut, ardışık düzen işlecini kullanarak bu dosyayı geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="f5227-120">The command passes that file to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f5227-121">Geçerli cmdlet, dosyayı yerel bilgisayardaki E:\PowerShell\StdOut.txt dosya yoluna kaydeder.</span><span class="sxs-lookup"><span data-stu-id="f5227-121">The current cmdlet saves that file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="f5227-122">StdOut.txt düğümü, KIMLIĞI Job02 olan iş için KIMLIĞI Task02 olan görevle ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="f5227-122">The StdOut.txt node file is associated with the task that has the ID Task02 for the job that has the ID Job02.</span></span>

### <span data-ttu-id="f5227-123">Örnek 3: görevle ilişkilendirilmiş bir toplu Iş düğümü dosyası alma ve bunu bir akışa yönlendirme</span><span class="sxs-lookup"><span data-stu-id="f5227-123">Example 3: Get a Batch node file associated with a task and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchNodeFileContent -JobId "Job03" -TaskId "Task11" -Name "StdOut.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="f5227-124">İlk komut New-Object cmdlet 'ini kullanarak bir akış oluşturur ve $Stream değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f5227-124">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>

<span data-ttu-id="f5227-125">İkinci komut, KIMLIĞI Job03 olan iş için KIMLIĞI Task11 olan görevden StdOut.txt adlı düğüm dosyasını alır.</span><span class="sxs-lookup"><span data-stu-id="f5227-125">The second command gets the node file that is named StdOut.txt from the task that has the ID Task11 for the job that has the ID Job03.</span></span>
<span data-ttu-id="f5227-126">Komut dosya içeriğini $Stream akışa yönlendirir.</span><span class="sxs-lookup"><span data-stu-id="f5227-126">The command directs file contents to the stream in $Stream.</span></span>

### <span data-ttu-id="f5227-127">Örnek 4: işlem düğümünden bir düğüm dosyası alma ve kaydetme</span><span class="sxs-lookup"><span data-stu-id="f5227-127">Example 4: Get a node file from a compute node and save it</span></span>
```
PS C:\>Get-AzureBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "Startup\StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="f5227-128">Bu komut, ComputeNode01 kimliğine sahip havuzda KIMLIK Pool01 olan işlem düğümünden düğüm dosyası Startup\StdOut.txt alır.</span><span class="sxs-lookup"><span data-stu-id="f5227-128">This command gets the node file Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="f5227-129">Komut dosyayı yerel bilgisayardaki E:\PowerShell\StdOut.txt dosya yoluna kaydeder.</span><span class="sxs-lookup"><span data-stu-id="f5227-129">The command saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="f5227-130">Örnek 5: işlem düğümünden bir düğüm dosyası alın ve bunu ardışık düzen kullanarak kaydedin</span><span class="sxs-lookup"><span data-stu-id="f5227-130">Example 5: Get a node file from a compute node and save it by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchNodeFile -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "Startup\StdOut.txt" -BatchContext $Context | Get-AzureBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="f5227-131">Bu komut, ComputeNode01 KIMLIĞINE sahip işlem düğümünden Get-AzureBatchNodeFile kullanarak düğüm dosyası Startup\StdOut.txt alır.</span><span class="sxs-lookup"><span data-stu-id="f5227-131">This command gets the node file Startup\StdOut.txt by using Get-AzureBatchNodeFile from the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="f5227-132">Compute düğümü, KIMLIK Pool01 havuzunda.</span><span class="sxs-lookup"><span data-stu-id="f5227-132">The compute node is in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="f5227-133">Komut bu düğüm dosyasını geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="f5227-133">The command passes that node file to the current cmdlet.</span></span>
<span data-ttu-id="f5227-134">Bu cmdlet dosyayı yerel bilgisayardaki E:\PowerShell\StdOut.txt dosya yoluna kaydeder.</span><span class="sxs-lookup"><span data-stu-id="f5227-134">That cmdlet saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="f5227-135">Örnek 6: işlem düğümünden bir düğüm dosyası alın ve bunu bir akışa yönlendirin</span><span class="sxs-lookup"><span data-stu-id="f5227-135">Example 6: Get a node file from a compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "startup\stdout.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="f5227-136">İlk komut New-Object cmdlet 'ini kullanarak bir akış oluşturur ve $Stream değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f5227-136">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>

<span data-ttu-id="f5227-137">İkinci komut, KIMLIĞI Pool01 olan havuzda KIMLIĞI ComputeNode01 olan COMPUTE düğümünden StdOut.txt adlı düğüm dosyasını alır.</span><span class="sxs-lookup"><span data-stu-id="f5227-137">The second command gets the node file that is named StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="f5227-138">Komut dosya içeriğini $Stream akışa yönlendirir.</span><span class="sxs-lookup"><span data-stu-id="f5227-138">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="f5227-139">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f5227-139">PARAMETERS</span></span>

### <span data-ttu-id="f5227-140">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f5227-140">-BatchContext</span></span>
<span data-ttu-id="f5227-141">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5227-141">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f5227-142">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f5227-142">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="f5227-143">-ByteRangeEnd</span><span class="sxs-lookup"><span data-stu-id="f5227-143">-ByteRangeEnd</span></span>
<span data-ttu-id="f5227-144">İndirilecek bayt aralığının sonu.</span><span class="sxs-lookup"><span data-stu-id="f5227-144">The end of the byte range to be downloaded.</span></span>
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

### <span data-ttu-id="f5227-145">-ByteRangeStart</span><span class="sxs-lookup"><span data-stu-id="f5227-145">-ByteRangeStart</span></span>
<span data-ttu-id="f5227-146">İndirilecek bayt aralığının başlangıcı.</span><span class="sxs-lookup"><span data-stu-id="f5227-146">The start of the byte range to be downloaded.</span></span>
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

### <span data-ttu-id="f5227-147">-Computenodeıd</span><span class="sxs-lookup"><span data-stu-id="f5227-147">-ComputeNodeId</span></span>
<span data-ttu-id="f5227-148">Bu cmdlet 'in döndürdüğü düğüm dosyasını içeren COMPUTE düğümünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5227-148">Specifies the ID of the compute node that contains the node file that this cmdlet returns.</span></span>

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

### <span data-ttu-id="f5227-149">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="f5227-149">-DestinationPath</span></span>
<span data-ttu-id="f5227-150">Bu cmdlet 'in düğüm dosyasını kaydettiği dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5227-150">Specifies the file path where this cmdlet saves the node file.</span></span>

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

### <span data-ttu-id="f5227-151">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="f5227-151">-DestinationStream</span></span>
<span data-ttu-id="f5227-152">Bu cmdlet 'in düğüm dosyası içeriğini yazdığı akışı belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5227-152">Specifies the stream into which this cmdlet writes the node file contents.</span></span>
<span data-ttu-id="f5227-153">Bu cmdlet bu akışı kapatmaz veya geri sarmaz.</span><span class="sxs-lookup"><span data-stu-id="f5227-153">This cmdlet does not close or rewind this stream.</span></span>

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

### <span data-ttu-id="f5227-154">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5227-154">-InputObject</span></span>
<span data-ttu-id="f5227-155">Bu cmdlet 'in aldığı dosyayı, **Psnodefile** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5227-155">Specifies the file that this cmdlet gets, as a **PSNodeFile** object.</span></span>
<span data-ttu-id="f5227-156">Düğüm dosyası nesnesi edinmek için Get-AzureBatchNodeFile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f5227-156">To obtain a node file object, use the Get-AzureBatchNodeFile cmdlet.</span></span>

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

### <span data-ttu-id="f5227-157">-JobId</span><span class="sxs-lookup"><span data-stu-id="f5227-157">-JobId</span></span>
<span data-ttu-id="f5227-158">Hedef görevi içeren işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5227-158">Specifies the ID of the job that contains the target task.</span></span>

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

### <span data-ttu-id="f5227-159">-Ad</span><span class="sxs-lookup"><span data-stu-id="f5227-159">-Name</span></span>
<span data-ttu-id="f5227-160">Bu cmdlet 'in aldığı düğüm dosyasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5227-160">Specifies the name of the node file that this cmdlet retrieves.</span></span>
<span data-ttu-id="f5227-161">Joker karakterler belirtemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="f5227-161">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream, ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5227-162">-PoolId</span><span class="sxs-lookup"><span data-stu-id="f5227-162">-PoolId</span></span>
<span data-ttu-id="f5227-163">Bu cmdlet 'in aldığı düğüm dosyasını içeren COMPUTE düğümünü içeren havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5227-163">Specifies the ID of the pool that contains the compute node that contains the node file that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f5227-164">-TaskID</span><span class="sxs-lookup"><span data-stu-id="f5227-164">-TaskId</span></span>
<span data-ttu-id="f5227-165">Görevin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5227-165">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="f5227-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5227-166">-DefaultProfile</span></span>
<span data-ttu-id="f5227-167">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f5227-167">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5227-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5227-168">CommonParameters</span></span>
<span data-ttu-id="f5227-169">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f5227-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5227-170">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5227-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5227-171">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f5227-171">INPUTS</span></span>

### <span data-ttu-id="f5227-172">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f5227-172">BatchAccountContext</span></span>
<span data-ttu-id="f5227-173">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="f5227-173">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="f5227-174">PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="f5227-174">PSNodeFile</span></span>
<span data-ttu-id="f5227-175">' InputObject ' parametresi ardışık düzenin ' PSNodeFile ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="f5227-175">Parameter 'InputObject' accepts value of type 'PSNodeFile' from the pipeline</span></span>

## <span data-ttu-id="f5227-176">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f5227-176">OUTPUTS</span></span>

## <span data-ttu-id="f5227-177">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f5227-177">NOTES</span></span>

## <span data-ttu-id="f5227-178">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f5227-178">RELATED LINKS</span></span>

[<span data-ttu-id="f5227-179">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="f5227-179">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="f5227-180">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="f5227-180">Get-AzureBatchNodeFile</span></span>](./Get-AzureBatchNodeFile.md)

[<span data-ttu-id="f5227-181">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="f5227-181">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


