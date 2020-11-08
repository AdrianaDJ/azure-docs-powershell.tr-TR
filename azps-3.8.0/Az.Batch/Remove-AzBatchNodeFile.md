---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DBA02017-8372-4A91-A4F1-985777DEDAB9
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchNodeFile.md
ms.openlocfilehash: 7e9aeebebfc5720ab006d43071eadeabe6bcf655
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097907"
---
# <span data-ttu-id="e51cd-101">Remove-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="e51cd-101">Remove-AzBatchNodeFile</span></span>

## <span data-ttu-id="e51cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e51cd-102">SYNOPSIS</span></span>
<span data-ttu-id="e51cd-103">Görevin veya compute düğümünün düğüm dosyasını siler.</span><span class="sxs-lookup"><span data-stu-id="e51cd-103">Deletes a node file for a task or compute node.</span></span>

## <span data-ttu-id="e51cd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e51cd-104">SYNTAX</span></span>

### <span data-ttu-id="e51cd-105">Görevini</span><span class="sxs-lookup"><span data-stu-id="e51cd-105">Task</span></span>
```
Remove-AzBatchNodeFile -JobId <String> -TaskId <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e51cd-106">ComputeNode</span><span class="sxs-lookup"><span data-stu-id="e51cd-106">ComputeNode</span></span>
```
Remove-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e51cd-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="e51cd-107">InputObject</span></span>
```
Remove-AzBatchNodeFile [[-InputObject] <PSNodeFile>] [-Force] [-Recursive] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e51cd-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e51cd-108">DESCRIPTION</span></span>
<span data-ttu-id="e51cd-109">**Remove-AzBatchNodeFile** cmdlet 'i, görev veya hesaplama düğümü Için bir Azure toplu iş düğümü dosyasını siler.</span><span class="sxs-lookup"><span data-stu-id="e51cd-109">The **Remove-AzBatchNodeFile** cmdlet deletes an Azure Batch node file for a task or compute node.</span></span>

## <span data-ttu-id="e51cd-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e51cd-110">EXAMPLES</span></span>

### <span data-ttu-id="e51cd-111">Örnek 1: görevle ilişkilendirilmiş dosyayı silme</span><span class="sxs-lookup"><span data-stu-id="e51cd-111">Example 1: Delete a file associated with a task</span></span>
```
PS C:\>Remove-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="e51cd-112">Bu komut wd\testFile.txt adlı düğüm dosyasını siler.</span><span class="sxs-lookup"><span data-stu-id="e51cd-112">This command deletes the node file that is named wd\testFile.txt.</span></span>
<span data-ttu-id="e51cd-113">Bu dosya, iş Işi-000001 altında KIMLIĞI Task26 olan görevle ilişkilendirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="e51cd-113">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>

### <span data-ttu-id="e51cd-114">Örnek 2: işlem düğümünden dosya silme</span><span class="sxs-lookup"><span data-stu-id="e51cd-114">Example 2: Delete a file from a compute node</span></span>
```
PS C:\>Remove-AzBatchNodeFile -PoolId "Pool07" -ComputeNodeId "tvm-2316545714_1-20150725t213220z" -Path "startup\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="e51cd-115">Bu komut, startup\testFile.txt adlı havuzda KIMLIĞI Pool07 olan havuzda belirtilen COMPUTE düğümünden silinir.</span><span class="sxs-lookup"><span data-stu-id="e51cd-115">This command deletes the node file that is named startup\testFile.txt from the specified compute node in the pool that has the ID Pool07.</span></span>

### <span data-ttu-id="e51cd-116">Örnek 3: ardışık düzeni kullanarak dosya kaldırma</span><span class="sxs-lookup"><span data-stu-id="e51cd-116">Example 3: Remove a file by using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile2.txt" -BatchContext $Context | Remove-AzBatchNodeFile -Force -BatchContext $Context
```

<span data-ttu-id="e51cd-117">Bu komut **Get-AzBatchNodeFile** kullanarak düğüm dosyasını alır.</span><span class="sxs-lookup"><span data-stu-id="e51cd-117">This command gets the node file by using **Get-AzBatchNodeFile**.</span></span>
<span data-ttu-id="e51cd-118">Bu dosya, iş Işi-000001 altında KIMLIĞI Task26 olan görevle ilişkilendirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="e51cd-118">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>
<span data-ttu-id="e51cd-119">Komut bu dosyayı geçerli cmdlet 'e ardışık düzeni kullanarak geçirir.</span><span class="sxs-lookup"><span data-stu-id="e51cd-119">The command passes that file to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="e51cd-120">Geçerli cmdlet, düğüm dosyasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e51cd-120">The current cmdlet removes the node file.</span></span>
<span data-ttu-id="e51cd-121">Komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e51cd-121">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="e51cd-122">Bu nedenle, komut sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="e51cd-122">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="e51cd-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e51cd-123">PARAMETERS</span></span>

### <span data-ttu-id="e51cd-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e51cd-124">-BatchContext</span></span>
<span data-ttu-id="e51cd-125">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e51cd-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e51cd-126">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e51cd-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e51cd-127">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKey cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="e51cd-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e51cd-128">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e51cd-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e51cd-129">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e51cd-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e51cd-130">-Computenodeıd</span><span class="sxs-lookup"><span data-stu-id="e51cd-130">-ComputeNodeId</span></span>
<span data-ttu-id="e51cd-131">Bu cmdlet 'in sildiği toplu Iş düğümü dosyasını içeren COMPUTE düğümünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e51cd-131">Specifies the ID of the compute node that contains the Batch node file that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e51cd-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e51cd-132">-DefaultProfile</span></span>
<span data-ttu-id="e51cd-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e51cd-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e51cd-134">-Force</span><span class="sxs-lookup"><span data-stu-id="e51cd-134">-Force</span></span>
<span data-ttu-id="e51cd-135">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="e51cd-135">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e51cd-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e51cd-136">-InputObject</span></span>
<span data-ttu-id="e51cd-137">Bu cmdlet 'in sildiği düğüm dosyasını temsil eden **Psnodefile** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e51cd-137">Specifies **PSNodeFile** object that represent the node file that this cmdlet deletes.</span></span>
<span data-ttu-id="e51cd-138">**Psnodefile** almak için Get-AzBatchNodeFile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e51cd-138">To obtain a **PSNodeFile** , use the Get-AzBatchNodeFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNodeFile
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e51cd-139">-JobId</span><span class="sxs-lookup"><span data-stu-id="e51cd-139">-JobId</span></span>
<span data-ttu-id="e51cd-140">Görevi içeren işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e51cd-140">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e51cd-141">-Yol</span><span class="sxs-lookup"><span data-stu-id="e51cd-141">-Path</span></span>
<span data-ttu-id="e51cd-142">Silinecek olan düğüm dosyasının dosya yolu.</span><span class="sxs-lookup"><span data-stu-id="e51cd-142">The file path of the node file to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: Task, ComputeNode
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e51cd-143">-PoolId</span><span class="sxs-lookup"><span data-stu-id="e51cd-143">-PoolId</span></span>
<span data-ttu-id="e51cd-144">Bu cmdlet 'in dosyayı kaldıran COMPUTE düğümlerini içeren havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e51cd-144">Specifies the ID of the pool that contains the compute nodes for which this cmdlet removes a file.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e51cd-145">-Yinelemeli</span><span class="sxs-lookup"><span data-stu-id="e51cd-145">-Recursive</span></span>
<span data-ttu-id="e51cd-146">Bu cmdlet 'in klasörü ve belirtilen yolun altındaki tüm alt klasörleri ve dosyaları sildiği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="e51cd-146">Indicates that this cmdlet deletes the folder and all subfolders and files under the specified path.</span></span>
<span data-ttu-id="e51cd-147">Bu cmdlet yalnızca yol bir klasör olduğunda ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="e51cd-147">This cmdlet is relevant only if the path is a folder.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e51cd-148">-TaskID</span><span class="sxs-lookup"><span data-stu-id="e51cd-148">-TaskId</span></span>
<span data-ttu-id="e51cd-149">Görevin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e51cd-149">Specifies the ID of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e51cd-150">-Onay</span><span class="sxs-lookup"><span data-stu-id="e51cd-150">-Confirm</span></span>
<span data-ttu-id="e51cd-151">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e51cd-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e51cd-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e51cd-152">-WhatIf</span></span>
<span data-ttu-id="e51cd-153">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e51cd-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e51cd-154">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e51cd-154">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e51cd-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e51cd-155">CommonParameters</span></span>
<span data-ttu-id="e51cd-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e51cd-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e51cd-157">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e51cd-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e51cd-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e51cd-158">INPUTS</span></span>

### <span data-ttu-id="e51cd-159">System. String</span><span class="sxs-lookup"><span data-stu-id="e51cd-159">System.String</span></span>

### <span data-ttu-id="e51cd-160">Microsoft.Azure.Commands.Batch. Modeller. PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="e51cd-160">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

### <span data-ttu-id="e51cd-161">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e51cd-161">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e51cd-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e51cd-162">OUTPUTS</span></span>

### <span data-ttu-id="e51cd-163">System. void</span><span class="sxs-lookup"><span data-stu-id="e51cd-163">System.Void</span></span>

## <span data-ttu-id="e51cd-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e51cd-164">NOTES</span></span>

## <span data-ttu-id="e51cd-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e51cd-165">RELATED LINKS</span></span>

[<span data-ttu-id="e51cd-166">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="e51cd-166">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="e51cd-167">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="e51cd-167">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="e51cd-168">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="e51cd-168">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)


