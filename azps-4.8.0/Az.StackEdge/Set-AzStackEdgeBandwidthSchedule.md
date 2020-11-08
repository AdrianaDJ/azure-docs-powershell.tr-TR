---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: db54799f13ca7524ccf42ade8b7e33c61a134ae9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268681"
---
# <span data-ttu-id="398cd-101">Set-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="398cd-101">Set-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="398cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="398cd-102">SYNOPSIS</span></span>
<span data-ttu-id="398cd-103">Bant genişliği zamanlamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="398cd-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="398cd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="398cd-104">SYNTAX</span></span>

### <span data-ttu-id="398cd-105">UpdateByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="398cd-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="398cd-106">Updatebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="398cd-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="398cd-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="398cd-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="398cd-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="398cd-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="398cd-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="398cd-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="398cd-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="398cd-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="398cd-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="398cd-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="398cd-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="398cd-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="398cd-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="398cd-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="398cd-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="398cd-114">DESCRIPTION</span></span>
<span data-ttu-id="398cd-115">**Set-AzStackEdgeBandwidthSchedule** cmdlet 'ı yığın uç aygıtı Için bir bant genişliği zamanlamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="398cd-115">The **Set-AzStackEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Stack Edge device.</span></span>

## <span data-ttu-id="398cd-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="398cd-116">EXAMPLES</span></span>

### <span data-ttu-id="398cd-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="398cd-117">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="398cd-118">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="398cd-118">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="398cd-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="398cd-119">PARAMETERS</span></span>

### <span data-ttu-id="398cd-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="398cd-120">-AsJob</span></span>
<span data-ttu-id="398cd-121">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="398cd-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="398cd-122">-Bant genişliği</span><span class="sxs-lookup"><span data-stu-id="398cd-122">-Bandwidth</span></span>
<span data-ttu-id="398cd-123">Mbps cinsinden bant genişliği</span><span class="sxs-lookup"><span data-stu-id="398cd-123">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="398cd-124">-Daysofya</span><span class="sxs-lookup"><span data-stu-id="398cd-124">-DaysOfWeek</span></span>
<span data-ttu-id="398cd-125">Zamanlanmış gün Yumuşma</span><span class="sxs-lookup"><span data-stu-id="398cd-125">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="398cd-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="398cd-126">-DefaultProfile</span></span>
<span data-ttu-id="398cd-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="398cd-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="398cd-128">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="398cd-128">-DeviceName</span></span>
<span data-ttu-id="398cd-129">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="398cd-129">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="398cd-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="398cd-130">-InputObject</span></span>
<span data-ttu-id="398cd-131">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="398cd-131">Azure ResourceId</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule
Parameter Sets: UpdateByInputObjectParameterSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterBandwidthSet
Aliases: BandwidthSchedule

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="398cd-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="398cd-132">-Name</span></span>
<span data-ttu-id="398cd-133">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="398cd-133">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="398cd-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="398cd-134">-ResourceGroupName</span></span>
<span data-ttu-id="398cd-135">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="398cd-135">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="398cd-136">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="398cd-136">-ResourceId</span></span>
<span data-ttu-id="398cd-137">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="398cd-137">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet, UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByResourceIdParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="398cd-138">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="398cd-138">-StartTime</span></span>
<span data-ttu-id="398cd-139">Başlangıç saati</span><span class="sxs-lookup"><span data-stu-id="398cd-139">Schedule Start Time</span></span>

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

### <span data-ttu-id="398cd-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="398cd-140">-StopTime</span></span>
<span data-ttu-id="398cd-141">Zamanlama durdurma zamanı</span><span class="sxs-lookup"><span data-stu-id="398cd-141">Schedule Stop Time</span></span>

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

### <span data-ttu-id="398cd-142">-Unlimitedbant genişliği</span><span class="sxs-lookup"><span data-stu-id="398cd-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="398cd-143">Sınırsız bant genişliği ayarlar</span><span class="sxs-lookup"><span data-stu-id="398cd-143">Will Set Unlimited Bandwidth</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByNameParameterUnlimitedBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="398cd-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="398cd-144">-Confirm</span></span>
<span data-ttu-id="398cd-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="398cd-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="398cd-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="398cd-146">-WhatIf</span></span>
<span data-ttu-id="398cd-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="398cd-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="398cd-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="398cd-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="398cd-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="398cd-149">CommonParameters</span></span>
<span data-ttu-id="398cd-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="398cd-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="398cd-151">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="398cd-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="398cd-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="398cd-152">INPUTS</span></span>

### <span data-ttu-id="398cd-153">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="398cd-153">None</span></span>

## <span data-ttu-id="398cd-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="398cd-154">OUTPUTS</span></span>

### <span data-ttu-id="398cd-155">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="398cd-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="398cd-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="398cd-156">NOTES</span></span>

## <span data-ttu-id="398cd-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="398cd-157">RELATED LINKS</span></span>
