---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: D82270AD-50C2-4980-ABE2-58049C187875
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: 479b91f222852ebfc356d320cf880eb2ae99db6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588362"
---
# <span data-ttu-id="e6e51-101">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="e6e51-101">New-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="e6e51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6e51-102">SYNOPSIS</span></span>
<span data-ttu-id="e6e51-103">İş koleksiyonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e6e51-103">Creates a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6e51-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e6e51-104">SYNTAX</span></span>

```
New-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> -Location <String>
 [-Plan <String>] [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6e51-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e6e51-105">DESCRIPTION</span></span>
<span data-ttu-id="e6e51-106">**New-AzureRmSchedulerJobCollection** cmdlet 'ı, Azure Zamanlayıcısı 'nda bir iş koleksiyonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e6e51-106">The **New-AzureRmSchedulerJobCollection** cmdlet creates a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="e6e51-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e6e51-107">EXAMPLES</span></span>

## <span data-ttu-id="e6e51-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e6e51-108">PARAMETERS</span></span>

### <span data-ttu-id="e6e51-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6e51-109">-DefaultProfile</span></span>
<span data-ttu-id="e6e51-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e6e51-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6e51-111">Frekans</span><span class="sxs-lookup"><span data-stu-id="e6e51-111">-Frequency</span></span>
<span data-ttu-id="e6e51-112">İş koleksiyonundaki herhangi bir projede belirtebileceğiniz en yüksek frekansı belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6e51-112">Specifies the maximum frequency that you can specify on any job in the job collection.</span></span>
<span data-ttu-id="e6e51-113">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e6e51-113">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e6e51-114">Dakikanın</span><span class="sxs-lookup"><span data-stu-id="e6e51-114">Minute</span></span> 
- <span data-ttu-id="e6e51-115">Saati</span><span class="sxs-lookup"><span data-stu-id="e6e51-115">Hour</span></span> 
- <span data-ttu-id="e6e51-116">Günündeki</span><span class="sxs-lookup"><span data-stu-id="e6e51-116">Day</span></span> 
- <span data-ttu-id="e6e51-117">Haftada</span><span class="sxs-lookup"><span data-stu-id="e6e51-117">Week</span></span> 
- <span data-ttu-id="e6e51-118">Ay</span><span class="sxs-lookup"><span data-stu-id="e6e51-118">Month</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Minute, Hour, Day, Week, Month

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e51-119">-Aralık</span><span class="sxs-lookup"><span data-stu-id="e6e51-119">-Interval</span></span>
<span data-ttu-id="e6e51-120">Yinelenme aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6e51-120">Specifies an interval of recurrence.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e51-121">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="e6e51-121">-JobCollectionName</span></span>
<span data-ttu-id="e6e51-122">İş koleksiyonu için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6e51-122">Specifies a name for the job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6e51-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="e6e51-123">-Location</span></span>
<span data-ttu-id="e6e51-124">Bu cmdlet 'in iş koleksiyonunu oluşturduğu Azure bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6e51-124">Specifies the Azure region in which this cmdlet creates the job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6e51-125">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="e6e51-125">-MaxJobCount</span></span>
<span data-ttu-id="e6e51-126">İş koleksiyonunda oluşturabileceğiniz en fazla iş sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6e51-126">Specifies the maximum number of jobs that you can create in the job collection.</span></span>
<span data-ttu-id="e6e51-127">Maksimum değer, *plan* parametresinin belirttiği plana bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e6e51-127">The maximum depends on the plan that the *Plan* parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e51-128">-Plan</span><span class="sxs-lookup"><span data-stu-id="e6e51-128">-Plan</span></span>
<span data-ttu-id="e6e51-129">İş koleksiyonu planını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6e51-129">Specifies the job collection plan.</span></span>
<span data-ttu-id="e6e51-130">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e6e51-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e6e51-131">Bırakılamıyor</span><span class="sxs-lookup"><span data-stu-id="e6e51-131">Free</span></span> 
- <span data-ttu-id="e6e51-132">Ardından</span><span class="sxs-lookup"><span data-stu-id="e6e51-132">Standard</span></span> 
- <span data-ttu-id="e6e51-133">P10Premium</span><span class="sxs-lookup"><span data-stu-id="e6e51-133">P10Premium</span></span> 
- <span data-ttu-id="e6e51-134">P20Premium</span><span class="sxs-lookup"><span data-stu-id="e6e51-134">P20Premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Standard, P10Premium, P20Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6e51-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6e51-135">-ResourceGroupName</span></span>
<span data-ttu-id="e6e51-136">İş koleksiyonu için kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6e51-136">Specifies the resource group for the job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6e51-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="e6e51-137">-Confirm</span></span>
<span data-ttu-id="e6e51-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e6e51-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6e51-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6e51-139">-WhatIf</span></span>
<span data-ttu-id="e6e51-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e6e51-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6e51-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e6e51-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6e51-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6e51-142">CommonParameters</span></span>
<span data-ttu-id="e6e51-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e6e51-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6e51-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6e51-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6e51-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e6e51-145">INPUTS</span></span>

### <span data-ttu-id="e6e51-146">System. String</span><span class="sxs-lookup"><span data-stu-id="e6e51-146">System.String</span></span>

## <span data-ttu-id="e6e51-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e6e51-147">OUTPUTS</span></span>

### <span data-ttu-id="e6e51-148">Microsoft. Azure. Commands. Scheduler. modeller. PSJobCollectionDefinition</span><span class="sxs-lookup"><span data-stu-id="e6e51-148">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="e6e51-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e6e51-149">NOTES</span></span>

## <span data-ttu-id="e6e51-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e6e51-150">RELATED LINKS</span></span>

[<span data-ttu-id="e6e51-151">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="e6e51-151">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="e6e51-152">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="e6e51-152">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="e6e51-153">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="e6e51-153">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="e6e51-154">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="e6e51-154">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="e6e51-155">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="e6e51-155">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


