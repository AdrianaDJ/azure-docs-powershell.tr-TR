---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DBA02017-8372-4A91-A4F1-985777DEDAB9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchNodeFile.md
ms.openlocfilehash: a81d77ac1761c37dc3042394a4a70bda6848cc83
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762487"
---
# <span data-ttu-id="c87d9-101">Remove-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="c87d9-101">Remove-AzureBatchNodeFile</span></span>

## <span data-ttu-id="c87d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c87d9-102">SYNOPSIS</span></span>
<span data-ttu-id="c87d9-103">Görevin veya compute düğümünün düğüm dosyasını siler.</span><span class="sxs-lookup"><span data-stu-id="c87d9-103">Deletes a node file for a task or compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c87d9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c87d9-104">SYNTAX</span></span>

### <span data-ttu-id="c87d9-105">Görevini</span><span class="sxs-lookup"><span data-stu-id="c87d9-105">Task</span></span>
```
Remove-AzureBatchNodeFile -JobId <String> -TaskId <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c87d9-106">ComputeNode</span><span class="sxs-lookup"><span data-stu-id="c87d9-106">ComputeNode</span></span>
```
Remove-AzureBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c87d9-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="c87d9-107">InputObject</span></span>
```
Remove-AzureBatchNodeFile [[-InputObject] <PSNodeFile>] [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c87d9-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c87d9-108">DESCRIPTION</span></span>
<span data-ttu-id="c87d9-109">**Remove-AzureBatchNodeFile** cmdlet 'i, görev veya hesaplama düğümü Için bir Azure toplu iş düğümü dosyasını siler.</span><span class="sxs-lookup"><span data-stu-id="c87d9-109">The **Remove-AzureBatchNodeFile** cmdlet deletes an Azure Batch node file for a task or compute node.</span></span>

## <span data-ttu-id="c87d9-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c87d9-110">EXAMPLES</span></span>

### <span data-ttu-id="c87d9-111">Örnek 1: görevle bir dosyayı silme</span><span class="sxs-lookup"><span data-stu-id="c87d9-111">Example 1: Delete a file assocated with a task</span></span>
```
PS C:\>Remove-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="c87d9-112">Bu komut wd\testFile.txt adlı düğüm dosyasını siler.</span><span class="sxs-lookup"><span data-stu-id="c87d9-112">This command deletes the node file that is named wd\testFile.txt.</span></span>
<span data-ttu-id="c87d9-113">Bu dosya, iş Işi-000001 altında KIMLIĞI Task26 olan görevle ilişkilendirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="c87d9-113">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>

### <span data-ttu-id="c87d9-114">Örnek 2: işlem düğümünden dosya silme</span><span class="sxs-lookup"><span data-stu-id="c87d9-114">Example 2: Delete a file from a compute node</span></span>
```
PS C:\>Remove-AzureBatchNodeFile -PoolId "Pool07" -ComputeNodeId "tvm-2316545714_1-20150725t213220z" -Path "startup\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="c87d9-115">Bu komut, startup\testFile.txt adlı havuzda KIMLIĞI Pool07 olan havuzda belirtilen COMPUTE düğümünden silinir.</span><span class="sxs-lookup"><span data-stu-id="c87d9-115">This command deletes the node file that is named startup\testFile.txt from the specified compute node in the pool that has the ID Pool07.</span></span>

### <span data-ttu-id="c87d9-116">Örnek 3: ardışık düzeni kullanarak dosya kaldırma</span><span class="sxs-lookup"><span data-stu-id="c87d9-116">Example 3: Remove a file by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile2.txt" -BatchContext $Context | Remove-AzureBatchNodeFile -Force -BatchContext $Context
```

<span data-ttu-id="c87d9-117">Bu komut **Get-AzureBatchNodeFile** kullanarak düğüm dosyasını alır.</span><span class="sxs-lookup"><span data-stu-id="c87d9-117">This command gets the node file by using **Get-AzureBatchNodeFile**.</span></span>
<span data-ttu-id="c87d9-118">Bu dosya, iş Işi-000001 altında KIMLIĞI Task26 olan görevle ilişkilendirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="c87d9-118">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>
<span data-ttu-id="c87d9-119">Komut bu dosyayı geçerli cmdlet 'e ardışık düzeni kullanarak geçirir.</span><span class="sxs-lookup"><span data-stu-id="c87d9-119">The command passes that file to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="c87d9-120">Geçerli cmdlet, düğüm dosyasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c87d9-120">The current cmdlet removes the node file.</span></span>
<span data-ttu-id="c87d9-121">Komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c87d9-121">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="c87d9-122">Bu nedenle, komut sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="c87d9-122">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="c87d9-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c87d9-123">PARAMETERS</span></span>

### <span data-ttu-id="c87d9-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c87d9-124">-BatchContext</span></span>
<span data-ttu-id="c87d9-125">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c87d9-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c87d9-126">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c87d9-126">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c87d9-127">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="c87d9-127">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c87d9-128">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c87d9-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c87d9-129">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c87d9-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c87d9-130">-Computenodeıd</span><span class="sxs-lookup"><span data-stu-id="c87d9-130">-ComputeNodeId</span></span>
<span data-ttu-id="c87d9-131">Bu cmdlet 'in sildiği toplu Iş düğümü dosyasını içeren COMPUTE düğümünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c87d9-131">Specifies the ID of the compute node that contains the Batch node file that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="c87d9-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c87d9-132">-DefaultProfile</span></span>
<span data-ttu-id="c87d9-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c87d9-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c87d9-134">-Force</span><span class="sxs-lookup"><span data-stu-id="c87d9-134">-Force</span></span>
<span data-ttu-id="c87d9-135">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="c87d9-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c87d9-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c87d9-136">-InputObject</span></span>
<span data-ttu-id="c87d9-137">Bu cmdlet 'in sildiği düğüm dosyasını temsil eden **Psnodefile** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c87d9-137">Specifies **PSNodeFile** object that represent the node file that this cmdlet deletes.</span></span>
<span data-ttu-id="c87d9-138">**Psnodefile** almak için Get-AzureBatchNodeFile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c87d9-138">To obtain a **PSNodeFile** , use the Get-AzureBatchNodeFile cmdlet.</span></span>

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

### <span data-ttu-id="c87d9-139">-JobId</span><span class="sxs-lookup"><span data-stu-id="c87d9-139">-JobId</span></span>
<span data-ttu-id="c87d9-140">Görevi içeren işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c87d9-140">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="c87d9-141">-Yol</span><span class="sxs-lookup"><span data-stu-id="c87d9-141">-Path</span></span>
<span data-ttu-id="c87d9-142">Silinecek olan düğüm dosyasının dosya yolu.</span><span class="sxs-lookup"><span data-stu-id="c87d9-142">The file path of the node file to delete.</span></span>

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

### <span data-ttu-id="c87d9-143">-PoolId</span><span class="sxs-lookup"><span data-stu-id="c87d9-143">-PoolId</span></span>
<span data-ttu-id="c87d9-144">Bu cmdlet 'in dosyayı kaldıran COMPUTE düğümlerini içeren havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c87d9-144">Specifies the ID of the pool that contains the compute nodes for which this cmdlet removes a file.</span></span>

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

### <span data-ttu-id="c87d9-145">-Yinelemeli</span><span class="sxs-lookup"><span data-stu-id="c87d9-145">-Recursive</span></span>
<span data-ttu-id="c87d9-146">Bu cmdlet 'in klasörü ve belirtilen yolun altındaki tüm alt klasörleri ve dosyaları sildiği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="c87d9-146">Indicates that this cmdlet deletes the folder and all subfolders and files under the specified path.</span></span>
<span data-ttu-id="c87d9-147">Bu cmdlet yalnızca yol bir klasör olduğunda ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="c87d9-147">This cmdlet is relevant only if the path is a folder.</span></span>

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

### <span data-ttu-id="c87d9-148">-TaskID</span><span class="sxs-lookup"><span data-stu-id="c87d9-148">-TaskId</span></span>
<span data-ttu-id="c87d9-149">Görevin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c87d9-149">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="c87d9-150">-Onay</span><span class="sxs-lookup"><span data-stu-id="c87d9-150">-Confirm</span></span>
<span data-ttu-id="c87d9-151">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c87d9-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c87d9-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c87d9-152">-WhatIf</span></span>
<span data-ttu-id="c87d9-153">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c87d9-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c87d9-154">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c87d9-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c87d9-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c87d9-155">CommonParameters</span></span>
<span data-ttu-id="c87d9-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c87d9-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c87d9-157">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c87d9-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c87d9-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c87d9-158">INPUTS</span></span>

### <span data-ttu-id="c87d9-159">System. String</span><span class="sxs-lookup"><span data-stu-id="c87d9-159">System.String</span></span>

### <span data-ttu-id="c87d9-160">Microsoft.Azure.Commands.Batch. Modeller. PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="c87d9-160">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>
<span data-ttu-id="c87d9-161">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c87d9-161">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="c87d9-162">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c87d9-162">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="c87d9-163">Parametreler: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c87d9-163">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="c87d9-164">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c87d9-164">OUTPUTS</span></span>

### <span data-ttu-id="c87d9-165">System. void</span><span class="sxs-lookup"><span data-stu-id="c87d9-165">System.Void</span></span>

## <span data-ttu-id="c87d9-166">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c87d9-166">NOTES</span></span>

## <span data-ttu-id="c87d9-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c87d9-167">RELATED LINKS</span></span>

[<span data-ttu-id="c87d9-168">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c87d9-168">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="c87d9-169">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="c87d9-169">Get-AzureBatchNodeFile</span></span>](./Get-AzureBatchNodeFile.md)

[<span data-ttu-id="c87d9-170">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="c87d9-170">Get-AzureBatchNodeFileContent</span></span>](./Get-AzureBatchNodeFileContent.md)

