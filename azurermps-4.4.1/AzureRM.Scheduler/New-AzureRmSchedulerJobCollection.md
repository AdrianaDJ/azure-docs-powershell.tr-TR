---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: D82270AD-50C2-4980-ABE2-58049C187875
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: d3577b906134a940a9339441f305d98c32b8fe74
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593012"
---
# <span data-ttu-id="7897a-101">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="7897a-101">New-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="7897a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7897a-102">SYNOPSIS</span></span>
<span data-ttu-id="7897a-103">İş koleksiyonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7897a-103">Creates a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7897a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7897a-104">SYNTAX</span></span>

```
New-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> -Location <String>
 [-Plan <String>] [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7897a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7897a-105">DESCRIPTION</span></span>
<span data-ttu-id="7897a-106">**New-AzureRmSchedulerJobCollection** cmdlet 'ı, Azure Zamanlayıcısı 'nda bir iş koleksiyonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7897a-106">The **New-AzureRmSchedulerJobCollection** cmdlet creates a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="7897a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7897a-107">EXAMPLES</span></span>

## <span data-ttu-id="7897a-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7897a-108">PARAMETERS</span></span>

### <span data-ttu-id="7897a-109">Frekans</span><span class="sxs-lookup"><span data-stu-id="7897a-109">-Frequency</span></span>
<span data-ttu-id="7897a-110">İş koleksiyonundaki herhangi bir projede belirtebileceğiniz en yüksek frekansı belirtir.</span><span class="sxs-lookup"><span data-stu-id="7897a-110">Specifies the maximum frequency that you can specify on any job in the job collection.</span></span>
<span data-ttu-id="7897a-111">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7897a-111">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7897a-112">Dakikanın</span><span class="sxs-lookup"><span data-stu-id="7897a-112">Minute</span></span> 
- <span data-ttu-id="7897a-113">Saati</span><span class="sxs-lookup"><span data-stu-id="7897a-113">Hour</span></span> 
- <span data-ttu-id="7897a-114">Günündeki</span><span class="sxs-lookup"><span data-stu-id="7897a-114">Day</span></span> 
- <span data-ttu-id="7897a-115">Haftada</span><span class="sxs-lookup"><span data-stu-id="7897a-115">Week</span></span> 
- <span data-ttu-id="7897a-116">Ay</span><span class="sxs-lookup"><span data-stu-id="7897a-116">Month</span></span>

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

### <span data-ttu-id="7897a-117">-Aralık</span><span class="sxs-lookup"><span data-stu-id="7897a-117">-Interval</span></span>
<span data-ttu-id="7897a-118">Yinelenme aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7897a-118">Specifies an interval of recurrence.</span></span>

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

### <span data-ttu-id="7897a-119">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="7897a-119">-JobCollectionName</span></span>
<span data-ttu-id="7897a-120">İş koleksiyonu için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="7897a-120">Specifies a name for the job collection.</span></span>

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

### <span data-ttu-id="7897a-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="7897a-121">-Location</span></span>
<span data-ttu-id="7897a-122">Bu cmdlet 'in iş koleksiyonunu oluşturduğu Azure bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7897a-122">Specifies the Azure region in which this cmdlet creates the job collection.</span></span>

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

### <span data-ttu-id="7897a-123">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="7897a-123">-MaxJobCount</span></span>
<span data-ttu-id="7897a-124">İş koleksiyonunda oluşturabileceğiniz en fazla iş sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7897a-124">Specifies the maximum number of jobs that you can create in the job collection.</span></span>
<span data-ttu-id="7897a-125">Maksimum değer, *plan* parametresinin belirttiği plana bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="7897a-125">The maximum depends on the plan that the *Plan* parameter specifies.</span></span>

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

### <span data-ttu-id="7897a-126">-Plan</span><span class="sxs-lookup"><span data-stu-id="7897a-126">-Plan</span></span>
<span data-ttu-id="7897a-127">İş koleksiyonu planını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7897a-127">Specifies the job collection plan.</span></span>
<span data-ttu-id="7897a-128">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7897a-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7897a-129">Bırakılamıyor</span><span class="sxs-lookup"><span data-stu-id="7897a-129">Free</span></span> 
- <span data-ttu-id="7897a-130">Ardından</span><span class="sxs-lookup"><span data-stu-id="7897a-130">Standard</span></span> 
- <span data-ttu-id="7897a-131">P10Premium</span><span class="sxs-lookup"><span data-stu-id="7897a-131">P10Premium</span></span> 
- <span data-ttu-id="7897a-132">P20Premium</span><span class="sxs-lookup"><span data-stu-id="7897a-132">P20Premium</span></span>

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

### <span data-ttu-id="7897a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7897a-133">-ResourceGroupName</span></span>
<span data-ttu-id="7897a-134">İş koleksiyonu için kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7897a-134">Specifies the resource group for the job collection.</span></span>

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

### <span data-ttu-id="7897a-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="7897a-135">-Confirm</span></span>
<span data-ttu-id="7897a-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7897a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7897a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7897a-137">-WhatIf</span></span>
<span data-ttu-id="7897a-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7897a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7897a-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7897a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7897a-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7897a-140">-DefaultProfile</span></span>
<span data-ttu-id="7897a-141">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7897a-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7897a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7897a-142">CommonParameters</span></span>
<span data-ttu-id="7897a-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7897a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7897a-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7897a-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7897a-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7897a-145">INPUTS</span></span>

## <span data-ttu-id="7897a-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7897a-146">OUTPUTS</span></span>

### <span data-ttu-id="7897a-147">Microsoft. Azure. Commands. Scheduler. modeller. PSJobCollectionDefinition</span><span class="sxs-lookup"><span data-stu-id="7897a-147">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="7897a-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7897a-148">NOTES</span></span>

## <span data-ttu-id="7897a-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7897a-149">RELATED LINKS</span></span>

[<span data-ttu-id="7897a-150">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="7897a-150">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="7897a-151">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="7897a-151">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="7897a-152">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="7897a-152">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="7897a-153">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="7897a-153">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="7897a-154">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="7897a-154">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


