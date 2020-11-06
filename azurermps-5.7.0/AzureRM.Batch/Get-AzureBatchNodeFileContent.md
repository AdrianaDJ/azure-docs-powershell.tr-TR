---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C9E2D9EC-3B6A-492D-B183-9856185548CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchnodefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFileContent.md
ms.openlocfilehash: 7795182ff1594c098a2afd778c137c48dc74c955
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591728"
---
# <span data-ttu-id="b3750-101">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="b3750-101">Get-AzureBatchNodeFileContent</span></span>

## <span data-ttu-id="b3750-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3750-102">SYNOPSIS</span></span>
<span data-ttu-id="b3750-103">Bir toplu Iş düğümü dosyası alır.</span><span class="sxs-lookup"><span data-stu-id="b3750-103">Gets a Batch node file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3750-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b3750-104">SYNTAX</span></span>

### <span data-ttu-id="b3750-105">Task_Id_Path</span><span class="sxs-lookup"><span data-stu-id="b3750-105">Task_Id_Path</span></span>
```
Get-AzureBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationPath <String>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3750-106">Task_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="b3750-106">Task_Id_Stream</span></span>
```
Get-AzureBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3750-107">ComputeNode_Id_Path</span><span class="sxs-lookup"><span data-stu-id="b3750-107">ComputeNode_Id_Path</span></span>
```
Get-AzureBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationPath <String> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3750-108">ComputeNode_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="b3750-108">ComputeNode_Id_Stream</span></span>
```
Get-AzureBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationStream <Stream> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3750-109">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="b3750-109">InputObject_Path</span></span>
```
Get-AzureBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationPath <String> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b3750-110">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="b3750-110">InputObject_Stream</span></span>
```
Get-AzureBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3750-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="b3750-111">DESCRIPTION</span></span>
<span data-ttu-id="b3750-112">**Get-AzureBatchNodeFileContent** cmdlet 'ı bir Azure toplu iş düğümü dosyası alır ve bunu bir dosya veya akışa kaydeder.</span><span class="sxs-lookup"><span data-stu-id="b3750-112">The **Get-AzureBatchNodeFileContent** cmdlet gets an Azure Batch node file and saves it as a file or to a stream.</span></span>

## <span data-ttu-id="b3750-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b3750-113">EXAMPLES</span></span>

### <span data-ttu-id="b3750-114">Örnek 1: görevle ilişkilendirilmiş bir toplu Iş düğümü dosyası alma ve dosyayı kaydetme</span><span class="sxs-lookup"><span data-stu-id="b3750-114">Example 1: Get a Batch node file associated with a task and save the file</span></span>
```
PS C:\>Get-AzureBatchNodeFileContent -JobId "Job01" -TaskId "Task01" -Path "StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="b3750-115">Bu komut, StdOut.txt adlı düğüm dosyasını alır ve yerel bilgisayardaki E:\PowerShell\StdOut.txt dosya yoluna kaydeder.</span><span class="sxs-lookup"><span data-stu-id="b3750-115">This command gets the node file that is named StdOut.txt, and saves it to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="b3750-116">StdOut.txt düğümü, KIMLIĞI Job01 olan iş için KIMLIĞI Task01 olan görevle ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="b3750-116">The StdOut.txt node file is associated with task that has the ID Task01 for the job that has the ID Job01.</span></span>
<span data-ttu-id="b3750-117">$Context değişkenine bağlam atamak için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b3750-117">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="b3750-118">Örnek 2: bir toplu Iş düğümü dosyası alın ve ardışık düzeni kullanarak belirtilen dosya yoluna kaydedin</span><span class="sxs-lookup"><span data-stu-id="b3750-118">Example 2: Get a Batch node file and save it to a specified file path using the pipeline</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job02" -TaskId "Task02" -Path "StdErr.txt" -BatchContext $Context | Get-AzureBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="b3750-119">Bu komut, StdErr.txt adındaki düğüm dosyasını Get-AzureBatchNodeFile cmdlet 'i kullanarak alır.</span><span class="sxs-lookup"><span data-stu-id="b3750-119">This command gets the node file that is named StdErr.txt by using the Get-AzureBatchNodeFile cmdlet.</span></span>
<span data-ttu-id="b3750-120">Komut, ardışık düzen işlecini kullanarak bu dosyayı geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="b3750-120">The command passes that file to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b3750-121">Geçerli cmdlet, dosyayı yerel bilgisayardaki E:\PowerShell\StdOut.txt dosya yoluna kaydeder.</span><span class="sxs-lookup"><span data-stu-id="b3750-121">The current cmdlet saves that file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="b3750-122">StdOut.txt düğümü, KIMLIĞI Job02 olan iş için KIMLIĞI Task02 olan görevle ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="b3750-122">The StdOut.txt node file is associated with the task that has the ID Task02 for the job that has the ID Job02.</span></span>

### <span data-ttu-id="b3750-123">Örnek 3: görevle ilişkilendirilmiş bir toplu Iş düğümü dosyası alma ve bunu bir akışa yönlendirme</span><span class="sxs-lookup"><span data-stu-id="b3750-123">Example 3: Get a Batch node file associated with a task and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchNodeFileContent -JobId "Job03" -TaskId "Task11" -Path "StdOut.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="b3750-124">İlk komut New-Object cmdlet 'ini kullanarak bir akış oluşturur ve $Stream değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b3750-124">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>

<span data-ttu-id="b3750-125">İkinci komut, KIMLIĞI Job03 olan iş için KIMLIĞI Task11 olan görevden StdOut.txt adlı düğüm dosyasını alır.</span><span class="sxs-lookup"><span data-stu-id="b3750-125">The second command gets the node file that is named StdOut.txt from the task that has the ID Task11 for the job that has the ID Job03.</span></span>
<span data-ttu-id="b3750-126">Komut dosya içeriğini $Stream akışa yönlendirir.</span><span class="sxs-lookup"><span data-stu-id="b3750-126">The command directs file contents to the stream in $Stream.</span></span>

### <span data-ttu-id="b3750-127">Örnek 4: işlem düğümünden bir düğüm dosyası alma ve kaydetme</span><span class="sxs-lookup"><span data-stu-id="b3750-127">Example 4: Get a node file from a compute node and save it</span></span>
```
PS C:\>Get-AzureBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="b3750-128">Bu komut, ComputeNode01 kimliğine sahip havuzda KIMLIK Pool01 olan işlem düğümünden düğüm dosyası Startup\StdOut.txt alır.</span><span class="sxs-lookup"><span data-stu-id="b3750-128">This command gets the node file Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="b3750-129">Komut dosyayı yerel bilgisayardaki E:\PowerShell\StdOut.txt dosya yoluna kaydeder.</span><span class="sxs-lookup"><span data-stu-id="b3750-129">The command saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="b3750-130">Örnek 5: işlem düğümünden bir düğüm dosyası alın ve bunu ardışık düzen kullanarak kaydedin</span><span class="sxs-lookup"><span data-stu-id="b3750-130">Example 5: Get a node file from a compute node and save it by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchNodeFile -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context | Get-AzureBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="b3750-131">Bu komut, ComputeNode01 KIMLIĞINE sahip işlem düğümünden Get-AzureBatchNodeFile kullanarak düğüm dosyası Startup\StdOut.txt alır.</span><span class="sxs-lookup"><span data-stu-id="b3750-131">This command gets the node file Startup\StdOut.txt by using Get-AzureBatchNodeFile from the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="b3750-132">Compute düğümü, KIMLIK Pool01 havuzunda.</span><span class="sxs-lookup"><span data-stu-id="b3750-132">The compute node is in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="b3750-133">Komut bu düğüm dosyasını geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="b3750-133">The command passes that node file to the current cmdlet.</span></span>
<span data-ttu-id="b3750-134">Bu cmdlet dosyayı yerel bilgisayardaki E:\PowerShell\StdOut.txt dosya yoluna kaydeder.</span><span class="sxs-lookup"><span data-stu-id="b3750-134">That cmdlet saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="b3750-135">Örnek 6: işlem düğümünden bir düğüm dosyası alın ve bunu bir akışa yönlendirin</span><span class="sxs-lookup"><span data-stu-id="b3750-135">Example 6: Get a node file from a compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "startup\stdout.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="b3750-136">İlk komut New-Object cmdlet 'ini kullanarak bir akış oluşturur ve $Stream değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b3750-136">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>

<span data-ttu-id="b3750-137">İkinci komut, KIMLIĞI Pool01 olan havuzda KIMLIĞI ComputeNode01 olan COMPUTE düğümünden StdOut.txt adlı düğüm dosyasını alır.</span><span class="sxs-lookup"><span data-stu-id="b3750-137">The second command gets the node file that is named StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="b3750-138">Komut dosya içeriğini $Stream akışa yönlendirir.</span><span class="sxs-lookup"><span data-stu-id="b3750-138">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="b3750-139">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b3750-139">PARAMETERS</span></span>

### <span data-ttu-id="b3750-140">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b3750-140">-BatchContext</span></span>
<span data-ttu-id="b3750-141">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3750-141">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b3750-142">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b3750-142">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b3750-143">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="b3750-143">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b3750-144">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b3750-144">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b3750-145">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b3750-145">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b3750-146">-ByteRangeEnd</span><span class="sxs-lookup"><span data-stu-id="b3750-146">-ByteRangeEnd</span></span>
<span data-ttu-id="b3750-147">İndirilecek bayt aralığının sonu.</span><span class="sxs-lookup"><span data-stu-id="b3750-147">The end of the byte range to be downloaded.</span></span>
```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3750-148">-ByteRangeStart</span><span class="sxs-lookup"><span data-stu-id="b3750-148">-ByteRangeStart</span></span>
<span data-ttu-id="b3750-149">İndirilecek bayt aralığının başlangıcı.</span><span class="sxs-lookup"><span data-stu-id="b3750-149">The start of the byte range to be downloaded.</span></span>
```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3750-150">-Computenodeıd</span><span class="sxs-lookup"><span data-stu-id="b3750-150">-ComputeNodeId</span></span>
<span data-ttu-id="b3750-151">Bu cmdlet 'in döndürdüğü düğüm dosyasını içeren COMPUTE düğümünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3750-151">Specifies the ID of the compute node that contains the node file that this cmdlet returns.</span></span>

```yaml
Type: String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3750-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3750-152">-DefaultProfile</span></span>
<span data-ttu-id="b3750-153">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b3750-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3750-154">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="b3750-154">-DestinationPath</span></span>
<span data-ttu-id="b3750-155">Bu cmdlet 'in düğüm dosyasını kaydettiği dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3750-155">Specifies the file path where this cmdlet saves the node file.</span></span>

```yaml
Type: String
Parameter Sets: Task_Id_Path, ComputeNode_Id_Path, InputObject_Path
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3750-156">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="b3750-156">-DestinationStream</span></span>
<span data-ttu-id="b3750-157">Bu cmdlet 'in düğüm dosyası içeriğini yazdığı akışı belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3750-157">Specifies the stream into which this cmdlet writes the node file contents.</span></span>
<span data-ttu-id="b3750-158">Bu cmdlet bu akışı kapatmaz veya geri sarmaz.</span><span class="sxs-lookup"><span data-stu-id="b3750-158">This cmdlet does not close or rewind this stream.</span></span>

```yaml
Type: Stream
Parameter Sets: Task_Id_Stream, ComputeNode_Id_Stream, InputObject_Stream
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3750-159">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3750-159">-InputObject</span></span>
<span data-ttu-id="b3750-160">Bu cmdlet 'in aldığı dosyayı, **Psnodefile** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3750-160">Specifies the file that this cmdlet gets, as a **PSNodeFile** object.</span></span>
<span data-ttu-id="b3750-161">Düğüm dosyası nesnesi edinmek için Get-AzureBatchNodeFile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b3750-161">To obtain a node file object, use the Get-AzureBatchNodeFile cmdlet.</span></span>

```yaml
Type: PSNodeFile
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3750-162">-JobId</span><span class="sxs-lookup"><span data-stu-id="b3750-162">-JobId</span></span>
<span data-ttu-id="b3750-163">Hedef görevi içeren işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3750-163">Specifies the ID of the job that contains the target task.</span></span>

```yaml
Type: String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3750-164">-Yol</span><span class="sxs-lookup"><span data-stu-id="b3750-164">-Path</span></span>
<span data-ttu-id="b3750-165">İndirilecek olan düğüm dosyasının yolu.</span><span class="sxs-lookup"><span data-stu-id="b3750-165">The path of the node file to download.</span></span>

```yaml
Type: String
Parameter Sets: Task_Id_Path, Task_Id_Stream, ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3750-166">-PoolId</span><span class="sxs-lookup"><span data-stu-id="b3750-166">-PoolId</span></span>
<span data-ttu-id="b3750-167">Bu cmdlet 'in aldığı düğüm dosyasını içeren COMPUTE düğümünü içeren havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3750-167">Specifies the ID of the pool that contains the compute node that contains the node file that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3750-168">-TaskID</span><span class="sxs-lookup"><span data-stu-id="b3750-168">-TaskId</span></span>
<span data-ttu-id="b3750-169">Görevin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3750-169">Specifies the ID of the task.</span></span>

```yaml
Type: String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3750-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3750-170">CommonParameters</span></span>
<span data-ttu-id="b3750-171">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b3750-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3750-172">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3750-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3750-173">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b3750-173">INPUTS</span></span>

### <span data-ttu-id="b3750-174">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b3750-174">BatchAccountContext</span></span>
<span data-ttu-id="b3750-175">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="b3750-175">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="b3750-176">PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="b3750-176">PSNodeFile</span></span>
<span data-ttu-id="b3750-177">' InputObject ' parametresi ardışık düzenin ' PSNodeFile ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="b3750-177">Parameter 'InputObject' accepts value of type 'PSNodeFile' from the pipeline</span></span>

## <span data-ttu-id="b3750-178">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b3750-178">OUTPUTS</span></span>

## <span data-ttu-id="b3750-179">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b3750-179">NOTES</span></span>

## <span data-ttu-id="b3750-180">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b3750-180">RELATED LINKS</span></span>

[<span data-ttu-id="b3750-181">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b3750-181">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="b3750-182">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="b3750-182">Get-AzureBatchNodeFile</span></span>](./Get-AzureBatchNodeFile.md)

[<span data-ttu-id="b3750-183">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="b3750-183">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


