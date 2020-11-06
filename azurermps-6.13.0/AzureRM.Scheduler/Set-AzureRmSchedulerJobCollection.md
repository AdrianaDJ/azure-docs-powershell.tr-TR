---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F9CF1EEB-6EFF-4C24-AC79-1328034D22A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: 535455f73795d85acf05da191694f35dbeee9ba5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589354"
---
# <span data-ttu-id="bcac9-101">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="bcac9-101">Set-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="bcac9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcac9-102">SYNOPSIS</span></span>
<span data-ttu-id="bcac9-103">İş koleksiyonunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="bcac9-103">Modifies a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bcac9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bcac9-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-Location <String>]
 [-Plan <String>] [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcac9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bcac9-105">DESCRIPTION</span></span>
<span data-ttu-id="bcac9-106">**Set-AzureRmSchedulerJobCollection** cmdlet 'ı, Azure Zamanlayıcısı 'ndaki bir iş koleksiyonunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="bcac9-106">The **Set-AzureRmSchedulerJobCollection** cmdlet modifies a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="bcac9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bcac9-107">EXAMPLES</span></span>

## <span data-ttu-id="bcac9-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bcac9-108">PARAMETERS</span></span>

### <span data-ttu-id="bcac9-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcac9-109">-DefaultProfile</span></span>
<span data-ttu-id="bcac9-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bcac9-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcac9-111">Frekans</span><span class="sxs-lookup"><span data-stu-id="bcac9-111">-Frequency</span></span>
<span data-ttu-id="bcac9-112">İş koleksiyonundaki herhangi bir projede belirtebileceğiniz en yüksek frekansı belirtir.</span><span class="sxs-lookup"><span data-stu-id="bcac9-112">Specifies the maximum frequency that you can specify on any job in the job collection.</span></span>
<span data-ttu-id="bcac9-113">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="bcac9-113">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bcac9-114">Dakikanın</span><span class="sxs-lookup"><span data-stu-id="bcac9-114">Minute</span></span> 
- <span data-ttu-id="bcac9-115">Saati</span><span class="sxs-lookup"><span data-stu-id="bcac9-115">Hour</span></span> 
- <span data-ttu-id="bcac9-116">Günündeki</span><span class="sxs-lookup"><span data-stu-id="bcac9-116">Day</span></span> 
- <span data-ttu-id="bcac9-117">Haftada</span><span class="sxs-lookup"><span data-stu-id="bcac9-117">Week</span></span> 
- <span data-ttu-id="bcac9-118">Ay</span><span class="sxs-lookup"><span data-stu-id="bcac9-118">Month</span></span>

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

### <span data-ttu-id="bcac9-119">-Aralık</span><span class="sxs-lookup"><span data-stu-id="bcac9-119">-Interval</span></span>
<span data-ttu-id="bcac9-120">Yinelenme aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bcac9-120">Specifies an interval of recurrence.</span></span>

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

### <span data-ttu-id="bcac9-121">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="bcac9-121">-JobCollectionName</span></span>
<span data-ttu-id="bcac9-122">İş koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bcac9-122">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="bcac9-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="bcac9-123">-Location</span></span>
<span data-ttu-id="bcac9-124">İş koleksiyonunun var olduğu Azure bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bcac9-124">Specifies the Azure region in which the job collection exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcac9-125">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="bcac9-125">-MaxJobCount</span></span>
<span data-ttu-id="bcac9-126">İş koleksiyonunda oluşturabileceğiniz en fazla iş sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bcac9-126">Specifies the maximum number of jobs that you can create in the job collection.</span></span>
<span data-ttu-id="bcac9-127">Maksimum değer, *plan* parametresinin belirttiği plana bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="bcac9-127">The maximum depends on the plan that the *Plan* parameter specifies.</span></span>

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

### <span data-ttu-id="bcac9-128">-Plan</span><span class="sxs-lookup"><span data-stu-id="bcac9-128">-Plan</span></span>
<span data-ttu-id="bcac9-129">İş koleksiyonu planını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bcac9-129">Specifies the job collection plan.</span></span>
<span data-ttu-id="bcac9-130">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="bcac9-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bcac9-131">Bırakılamıyor</span><span class="sxs-lookup"><span data-stu-id="bcac9-131">Free</span></span> 
- <span data-ttu-id="bcac9-132">Ardından</span><span class="sxs-lookup"><span data-stu-id="bcac9-132">Standard</span></span> 
- <span data-ttu-id="bcac9-133">P10Premium</span><span class="sxs-lookup"><span data-stu-id="bcac9-133">P10Premium</span></span> 
- <span data-ttu-id="bcac9-134">P20Premium</span><span class="sxs-lookup"><span data-stu-id="bcac9-134">P20Premium</span></span>

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

### <span data-ttu-id="bcac9-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcac9-135">-ResourceGroupName</span></span>
<span data-ttu-id="bcac9-136">İş koleksiyonunun kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="bcac9-136">Specifies the resource group of the job collection.</span></span>

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

### <span data-ttu-id="bcac9-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="bcac9-137">-Confirm</span></span>
<span data-ttu-id="bcac9-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bcac9-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcac9-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcac9-139">-WhatIf</span></span>
<span data-ttu-id="bcac9-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bcac9-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcac9-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bcac9-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcac9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcac9-142">CommonParameters</span></span>
<span data-ttu-id="bcac9-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bcac9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcac9-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcac9-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcac9-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bcac9-145">INPUTS</span></span>

### <span data-ttu-id="bcac9-146">System. String</span><span class="sxs-lookup"><span data-stu-id="bcac9-146">System.String</span></span>

## <span data-ttu-id="bcac9-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bcac9-147">OUTPUTS</span></span>

### <span data-ttu-id="bcac9-148">Microsoft. Azure. Commands. Scheduler. modeller. PSJobCollectionDefinition</span><span class="sxs-lookup"><span data-stu-id="bcac9-148">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="bcac9-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bcac9-149">NOTES</span></span>

## <span data-ttu-id="bcac9-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bcac9-150">RELATED LINKS</span></span>

[<span data-ttu-id="bcac9-151">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="bcac9-151">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="bcac9-152">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="bcac9-152">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="bcac9-153">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="bcac9-153">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="bcac9-154">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="bcac9-154">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="bcac9-155">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="bcac9-155">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)


