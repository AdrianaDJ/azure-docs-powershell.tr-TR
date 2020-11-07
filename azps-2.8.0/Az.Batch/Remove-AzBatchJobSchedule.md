---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJobSchedule.md
ms.openlocfilehash: 398671292e67520977a683c3da9178b33dc69329
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753166"
---
# <span data-ttu-id="eb7f4-101">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="eb7f4-101">Remove-AzBatchJobSchedule</span></span>

## <span data-ttu-id="eb7f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb7f4-102">SYNOPSIS</span></span>
<span data-ttu-id="eb7f4-103">Toplu iş çizelgesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="eb7f4-103">Removes a Batch job schedule.</span></span>

## <span data-ttu-id="eb7f4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eb7f4-104">SYNTAX</span></span>

```
Remove-AzBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb7f4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="eb7f4-105">DESCRIPTION</span></span>
<span data-ttu-id="eb7f4-106">**Remove-Azbatchjobzamanlama** cmdlet 'ı bir Azure toplu iş çizelgesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="eb7f4-106">The **Remove-AzBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="eb7f4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eb7f4-107">EXAMPLES</span></span>

### <span data-ttu-id="eb7f4-108">Örnek 1: toplu iş çizelgesini silme</span><span class="sxs-lookup"><span data-stu-id="eb7f4-108">Example 1: Delete a Batch job schedule</span></span>
```
PS C:\>Remove-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
```

<span data-ttu-id="eb7f4-109">Bu komut Myjobzamanlama KIMLIĞI olan iş zamanlamasını siler.</span><span class="sxs-lookup"><span data-stu-id="eb7f4-109">This command deletes the job schedule that has the ID MyJobSchedule.</span></span>
<span data-ttu-id="eb7f4-110">Komut, işi silmeden önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="eb7f4-110">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="eb7f4-111">$Context değişkenine bağlam atamak için Get-AzBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="eb7f4-111">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="eb7f4-112">Örnek 2: ardışık düzeni kullanarak onaysız bir toplu iş silme</span><span class="sxs-lookup"><span data-stu-id="eb7f4-112">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context | Remove-AzBatchJobSchedule -Force -BatchContext $Context
```

<span data-ttu-id="eb7f4-113">Bu komut, Get-AzBatchJobSchedule cmdlet 'ini kullanarak KIMLIĞI Myjobplan olan iş zamanlamasını alır.</span><span class="sxs-lookup"><span data-stu-id="eb7f4-113">This command gets the job schedule that has the ID MyJobSchedule by using the Get-AzBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="eb7f4-114">Komut, iş çizelgesini ardışık düzen işlecini kullanarak geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="eb7f4-114">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="eb7f4-115">Komut bu iş çizelgesini siler.</span><span class="sxs-lookup"><span data-stu-id="eb7f4-115">The command deletes that job schedule.</span></span>
<span data-ttu-id="eb7f4-116">Komut *Force* parametresini içerdiğinden sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="eb7f4-116">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="eb7f4-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eb7f4-117">PARAMETERS</span></span>

### <span data-ttu-id="eb7f4-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="eb7f4-118">-BatchContext</span></span>
<span data-ttu-id="eb7f4-119">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="eb7f4-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="eb7f4-120">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="eb7f4-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="eb7f4-121">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="eb7f4-121">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="eb7f4-122">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="eb7f4-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="eb7f4-123">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="eb7f4-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="eb7f4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb7f4-124">-DefaultProfile</span></span>
<span data-ttu-id="eb7f4-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="eb7f4-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb7f4-126">-Force</span><span class="sxs-lookup"><span data-stu-id="eb7f4-126">-Force</span></span>
<span data-ttu-id="eb7f4-127">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="eb7f4-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="eb7f4-128">-ID</span><span class="sxs-lookup"><span data-stu-id="eb7f4-128">-Id</span></span>
<span data-ttu-id="eb7f4-129">Kaldırılacak iş zamanlamasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="eb7f4-129">Specifies the ID of the job schedule to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb7f4-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="eb7f4-130">-Confirm</span></span>
<span data-ttu-id="eb7f4-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="eb7f4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb7f4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb7f4-132">-WhatIf</span></span>
<span data-ttu-id="eb7f4-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="eb7f4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb7f4-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="eb7f4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb7f4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb7f4-135">CommonParameters</span></span>
<span data-ttu-id="eb7f4-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eb7f4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb7f4-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb7f4-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb7f4-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eb7f4-138">INPUTS</span></span>

### <span data-ttu-id="eb7f4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="eb7f4-139">System.String</span></span>

### <span data-ttu-id="eb7f4-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="eb7f4-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="eb7f4-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eb7f4-141">OUTPUTS</span></span>

### <span data-ttu-id="eb7f4-142">System. void</span><span class="sxs-lookup"><span data-stu-id="eb7f4-142">System.Void</span></span>

## <span data-ttu-id="eb7f4-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eb7f4-143">NOTES</span></span>

## <span data-ttu-id="eb7f4-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eb7f4-144">RELATED LINKS</span></span>

[<span data-ttu-id="eb7f4-145">Disable-Azbatchjobzamanlama</span><span class="sxs-lookup"><span data-stu-id="eb7f4-145">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="eb7f4-146">Enable-Azbatchjobzamanlama</span><span class="sxs-lookup"><span data-stu-id="eb7f4-146">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="eb7f4-147">Get-Azbatchjobplan</span><span class="sxs-lookup"><span data-stu-id="eb7f4-147">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="eb7f4-148">Yeni-Azbatchjobplanlama</span><span class="sxs-lookup"><span data-stu-id="eb7f4-148">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="eb7f4-149">Set-Azbatchjobplan</span><span class="sxs-lookup"><span data-stu-id="eb7f4-149">Set-AzBatchJobSchedule</span></span>](./Set-AzBatchJobSchedule.md)

[<span data-ttu-id="eb7f4-150">Stop-Azbatchjobzamanlama</span><span class="sxs-lookup"><span data-stu-id="eb7f4-150">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


