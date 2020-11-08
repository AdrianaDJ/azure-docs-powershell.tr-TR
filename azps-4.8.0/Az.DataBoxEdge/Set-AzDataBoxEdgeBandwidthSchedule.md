---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: 503f274b07b13bc19b4994f8b440ffc853f69bc5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274588"
---
# <span data-ttu-id="a241e-101">Set-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="a241e-101">Set-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="a241e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a241e-102">SYNOPSIS</span></span>
<span data-ttu-id="a241e-103">Bant genişliği zamanlamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a241e-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="a241e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a241e-104">SYNTAX</span></span>

### <span data-ttu-id="a241e-105">UpdateByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a241e-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a241e-106">Updatebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="a241e-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a241e-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="a241e-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a241e-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="a241e-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a241e-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a241e-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a241e-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="a241e-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a241e-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="a241e-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a241e-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="a241e-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a241e-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="a241e-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a241e-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="a241e-114">DESCRIPTION</span></span>
<span data-ttu-id="a241e-115">**Set-AzDataBoxEdgeBandwidthSchedule** cmdlet 'ı bir veri kutusu uç aygıtı Için bir bant genişliği zamanlamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a241e-115">The **Set-AzDataBoxEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Data Box Edge device.</span></span>

## <span data-ttu-id="a241e-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a241e-116">EXAMPLES</span></span>

### <span data-ttu-id="a241e-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a241e-117">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="a241e-118">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a241e-118">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="a241e-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a241e-119">PARAMETERS</span></span>

### <span data-ttu-id="a241e-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="a241e-120">-AsJob</span></span>
<span data-ttu-id="a241e-121">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a241e-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a241e-122">-Bant genişliği</span><span class="sxs-lookup"><span data-stu-id="a241e-122">-Bandwidth</span></span>
<span data-ttu-id="a241e-123">Mbps cinsinden bant genişliği</span><span class="sxs-lookup"><span data-stu-id="a241e-123">Bandwidth in Mbps</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateByResourceIdParameterBandwidthSet, UpdateByInputObjectParameterBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a241e-124">-Daysofya</span><span class="sxs-lookup"><span data-stu-id="a241e-124">-DaysOfWeek</span></span>
<span data-ttu-id="a241e-125">Zamanlanmış gün Yumuşma</span><span class="sxs-lookup"><span data-stu-id="a241e-125">Scheduled DaysOfWeek</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a241e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a241e-126">-DefaultProfile</span></span>
<span data-ttu-id="a241e-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a241e-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a241e-128">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="a241e-128">-DeviceName</span></span>
<span data-ttu-id="a241e-129">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="a241e-129">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a241e-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a241e-130">-InputObject</span></span>
<span data-ttu-id="a241e-131">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a241e-131">Azure ResourceId</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule
Parameter Sets: UpdateByInputObjectParameterSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a241e-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="a241e-132">-Name</span></span>
<span data-ttu-id="a241e-133">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="a241e-133">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a241e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a241e-134">-ResourceGroupName</span></span>
<span data-ttu-id="a241e-135">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="a241e-135">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a241e-136">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a241e-136">-ResourceId</span></span>
<span data-ttu-id="a241e-137">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a241e-137">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet, UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByResourceIdParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a241e-138">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="a241e-138">-StartTime</span></span>
<span data-ttu-id="a241e-139">Başlangıç saati</span><span class="sxs-lookup"><span data-stu-id="a241e-139">Schedule Start Time</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a241e-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="a241e-140">-StopTime</span></span>
<span data-ttu-id="a241e-141">Zamanlama durdurma zamanı</span><span class="sxs-lookup"><span data-stu-id="a241e-141">Schedule Stop Time</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a241e-142">-Unlimitedbant genişliği</span><span class="sxs-lookup"><span data-stu-id="a241e-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="a241e-143">Sınırsız bant genişliği ayarlar</span><span class="sxs-lookup"><span data-stu-id="a241e-143">Will Set Unlimited Bandwidth</span></span>

```yaml
Type: System.Boolean
Parameter Sets: UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByNameParameterUnlimitedBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a241e-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="a241e-144">-Confirm</span></span>
<span data-ttu-id="a241e-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a241e-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a241e-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a241e-146">-WhatIf</span></span>
<span data-ttu-id="a241e-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a241e-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a241e-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a241e-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a241e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a241e-149">CommonParameters</span></span>
<span data-ttu-id="a241e-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a241e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a241e-151">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a241e-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a241e-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a241e-152">INPUTS</span></span>

### <span data-ttu-id="a241e-153">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a241e-153">None</span></span>

## <span data-ttu-id="a241e-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a241e-154">OUTPUTS</span></span>

### <span data-ttu-id="a241e-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="a241e-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="a241e-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a241e-156">NOTES</span></span>

## <span data-ttu-id="a241e-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a241e-157">RELATED LINKS</span></span>
