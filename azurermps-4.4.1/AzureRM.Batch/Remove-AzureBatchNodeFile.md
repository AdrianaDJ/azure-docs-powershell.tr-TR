---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DBA02017-8372-4A91-A4F1-985777DEDAB9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchNodeFile.md
ms.openlocfilehash: 5b8797cf2f6068098d1ca407f0f97283dd171af5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591145"
---
# <span data-ttu-id="d4261-101">Remove-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="d4261-101">Remove-AzureBatchNodeFile</span></span>

## <span data-ttu-id="d4261-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4261-102">SYNOPSIS</span></span>
<span data-ttu-id="d4261-103">Görevin veya compute düğümünün düğüm dosyasını siler.</span><span class="sxs-lookup"><span data-stu-id="d4261-103">Deletes a node file for a task or compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4261-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d4261-104">SYNTAX</span></span>

### <span data-ttu-id="d4261-105">Görevini</span><span class="sxs-lookup"><span data-stu-id="d4261-105">Task</span></span>
```
Remove-AzureBatchNodeFile -JobId <String> -TaskId <String> -Name <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4261-106">ComputeNode</span><span class="sxs-lookup"><span data-stu-id="d4261-106">ComputeNode</span></span>
```
Remove-AzureBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> -Name <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4261-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="d4261-107">InputObject</span></span>
```
Remove-AzureBatchNodeFile [[-InputObject] <PSNodeFile>] [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d4261-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d4261-108">DESCRIPTION</span></span>
<span data-ttu-id="d4261-109">**Remove-AzureBatchNodeFile** cmdlet 'i, görev veya hesaplama düğümü Için bir Azure toplu iş düğümü dosyasını siler.</span><span class="sxs-lookup"><span data-stu-id="d4261-109">The **Remove-AzureBatchNodeFile** cmdlet deletes an Azure Batch node file for a task or compute node.</span></span>

## <span data-ttu-id="d4261-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d4261-110">EXAMPLES</span></span>

### <span data-ttu-id="d4261-111">Örnek 1: görevle bir dosyayı silme</span><span class="sxs-lookup"><span data-stu-id="d4261-111">Example 1: Delete a file assocated with a task</span></span>
```
PS C:\>Remove-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Name "wd\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="d4261-112">Bu komut wd\testFile.txt adlı düğüm dosyasını siler.</span><span class="sxs-lookup"><span data-stu-id="d4261-112">This command deletes the node file that is named wd\testFile.txt.</span></span>
<span data-ttu-id="d4261-113">Bu dosya, iş Işi-000001 altında KIMLIĞI Task26 olan görevle ilişkilendirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="d4261-113">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>

### <span data-ttu-id="d4261-114">Örnek 2: işlem düğümünden dosya silme</span><span class="sxs-lookup"><span data-stu-id="d4261-114">Example 2: Delete a file from a compute node</span></span>
```
PS C:\>Remove-AzureBatchNodeFile -PoolId "Pool07" -ComputeNodeId "tvm-2316545714_1-20150725t213220z" -Name "startup\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="d4261-115">Bu komut, startup\testFile.txt adlı havuzda KIMLIĞI Pool07 olan havuzda belirtilen COMPUTE düğümünden silinir.</span><span class="sxs-lookup"><span data-stu-id="d4261-115">This command deletes the node file that is named startup\testFile.txt from the specified compute node in the pool that has the ID Pool07.</span></span>

### <span data-ttu-id="d4261-116">Örnek 3: ardışık düzeni kullanarak dosya kaldırma</span><span class="sxs-lookup"><span data-stu-id="d4261-116">Example 3: Remove a file by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Name "wd\testFile2.txt" -BatchContext $Context | Remove-AzureBatchNodeFile -Force -BatchContext $Context
```

<span data-ttu-id="d4261-117">Bu komut **Get-AzureBatchNodeFile** kullanarak düğüm dosyasını alır.</span><span class="sxs-lookup"><span data-stu-id="d4261-117">This command gets the node file by using **Get-AzureBatchNodeFile**.</span></span>
<span data-ttu-id="d4261-118">Bu dosya, iş Işi-000001 altında KIMLIĞI Task26 olan görevle ilişkilendirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="d4261-118">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>
<span data-ttu-id="d4261-119">Komut bu dosyayı geçerli cmdlet 'e ardışık düzeni kullanarak geçirir.</span><span class="sxs-lookup"><span data-stu-id="d4261-119">The command passes that file to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="d4261-120">Geçerli cmdlet, düğüm dosyasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d4261-120">The current cmdlet removes the node file.</span></span>
<span data-ttu-id="d4261-121">Komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4261-121">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="d4261-122">Bu nedenle, komut sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="d4261-122">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="d4261-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d4261-123">PARAMETERS</span></span>

### <span data-ttu-id="d4261-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d4261-124">-BatchContext</span></span>
<span data-ttu-id="d4261-125">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4261-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d4261-126">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d4261-126">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="d4261-127">-Computenodeıd</span><span class="sxs-lookup"><span data-stu-id="d4261-127">-ComputeNodeId</span></span>
<span data-ttu-id="d4261-128">Bu cmdlet 'in sildiği toplu Iş düğümü dosyasını içeren COMPUTE düğümünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4261-128">Specifies the ID of the compute node that contains the Batch node file that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="d4261-129">-Force</span><span class="sxs-lookup"><span data-stu-id="d4261-129">-Force</span></span>
<span data-ttu-id="d4261-130">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="d4261-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d4261-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4261-131">-InputObject</span></span>
<span data-ttu-id="d4261-132">Bu cmdlet 'in sildiği düğüm dosyasını temsil eden **Psnodefile** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4261-132">Specifies **PSNodeFile** object that represent the node file that this cmdlet deletes.</span></span>
<span data-ttu-id="d4261-133">**Psnodefile** almak için Get-AzureBatchNodeFile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d4261-133">To obtain a **PSNodeFile** , use the Get-AzureBatchNodeFile cmdlet.</span></span>

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

### <span data-ttu-id="d4261-134">-JobId</span><span class="sxs-lookup"><span data-stu-id="d4261-134">-JobId</span></span>
<span data-ttu-id="d4261-135">Görevi içeren işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4261-135">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="d4261-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="d4261-136">-Name</span></span>
<span data-ttu-id="d4261-137">Bu cmdlet 'in sildiği düğüm dosyasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4261-137">Specifies the name of the node file that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: Task, ComputeNode
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4261-138">-PoolId</span><span class="sxs-lookup"><span data-stu-id="d4261-138">-PoolId</span></span>
<span data-ttu-id="d4261-139">Bu cmdlet 'in dosyayı kaldıran COMPUTE düğümlerini içeren havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4261-139">Specifies the ID of the pool that contains the compute nodes for which this cmdlet removes a file.</span></span>

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

### <span data-ttu-id="d4261-140">-Yinelemeli</span><span class="sxs-lookup"><span data-stu-id="d4261-140">-Recursive</span></span>
<span data-ttu-id="d4261-141">Bu cmdlet 'in klasörü ve belirtilen yolun altındaki tüm alt klasörleri ve dosyaları sildiği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="d4261-141">Indicates that this cmdlet deletes the folder and all subfolders and files under the specified path.</span></span>
<span data-ttu-id="d4261-142">Bu cmdlet yalnızca yol bir klasör olduğunda ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="d4261-142">This cmdlet is relevant only if the path is a folder.</span></span>

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

### <span data-ttu-id="d4261-143">-TaskID</span><span class="sxs-lookup"><span data-stu-id="d4261-143">-TaskId</span></span>
<span data-ttu-id="d4261-144">Görevin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4261-144">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="d4261-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="d4261-145">-Confirm</span></span>
<span data-ttu-id="d4261-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d4261-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4261-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4261-147">-WhatIf</span></span>
<span data-ttu-id="d4261-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d4261-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4261-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d4261-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4261-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4261-150">-DefaultProfile</span></span>
<span data-ttu-id="d4261-151">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d4261-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4261-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4261-152">CommonParameters</span></span>
<span data-ttu-id="d4261-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d4261-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4261-154">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4261-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4261-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d4261-155">INPUTS</span></span>

### <span data-ttu-id="d4261-156">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d4261-156">BatchAccountContext</span></span>
<span data-ttu-id="d4261-157">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="d4261-157">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="d4261-158">PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="d4261-158">PSNodeFile</span></span>
<span data-ttu-id="d4261-159">' InputObject ' parametresi ardışık düzenin ' PSNodeFile ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="d4261-159">Parameter 'InputObject' accepts value of type 'PSNodeFile' from the pipeline</span></span>

## <span data-ttu-id="d4261-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d4261-160">OUTPUTS</span></span>

## <span data-ttu-id="d4261-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d4261-161">NOTES</span></span>

## <span data-ttu-id="d4261-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d4261-162">RELATED LINKS</span></span>

[<span data-ttu-id="d4261-163">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="d4261-163">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="d4261-164">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="d4261-164">Get-AzureBatchNodeFile</span></span>](./Get-AzureBatchNodeFile.md)

[<span data-ttu-id="d4261-165">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="d4261-165">Get-AzureBatchNodeFileContent</span></span>](./Get-AzureBatchNodeFileContent.md)


