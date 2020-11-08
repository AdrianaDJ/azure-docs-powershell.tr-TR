---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: 68522dbd90593bdbc37afe333144431b997cc70c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098878"
---
# <span data-ttu-id="b1e05-101">New-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="b1e05-101">New-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="b1e05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1e05-102">SYNOPSIS</span></span>
<span data-ttu-id="b1e05-103">Yeni bir bant genişliği zamanlama oluşturur</span><span class="sxs-lookup"><span data-stu-id="b1e05-103">Creates a new Bandwidth schedule</span></span>

## <span data-ttu-id="b1e05-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b1e05-104">SYNTAX</span></span>

### <span data-ttu-id="b1e05-105">BandwidthParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b1e05-105">BandwidthParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1e05-106">UnlimitedBandwidthParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1e05-106">UnlimitedBandwidthParameterSet</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1e05-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b1e05-107">DESCRIPTION</span></span>
<span data-ttu-id="b1e05-108">**New-AzDataBoxEdgeBandwidthSchedule** cmdlet 'ı, bant genişliği kullanımını yönetmeye yardımcı olmak Için bir veri kutusu uç aygıtı için yeni bir bant genişliği çizelgesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b1e05-108">The **New-AzDataBoxEdgeBandwidthSchedule** cmdlet creates a new Bandwidth Schedule for a Data Box Edge device to help manage the Bandwidth usage.</span></span>

## <span data-ttu-id="b1e05-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b1e05-109">EXAMPLES</span></span>

### <span data-ttu-id="b1e05-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b1e05-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StartTime 11:00 -StopTime 12:00 -Bandwidth 30
Name                DaysOfWeek                  RateInMbps StartTime StopTime
----                ----------                  ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday    30         11:00:00  12:00:00
```

### <span data-ttu-id="b1e05-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="b1e05-111">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthScheduleUnlimited -StartTime 11:00 -StopTime 12:00 -UnlimitedBandwidth
Name                          DaysOfWeek                RateInMbps  StartTime    StopTime
----------------              ----------------------    ----------- -----------  ---------
bandwidthScheduleUnlimited  Sunday,Tuesday,Saturday     unlimited   11:00:00     12:00:00
```

## <span data-ttu-id="b1e05-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b1e05-112">PARAMETERS</span></span>

### <span data-ttu-id="b1e05-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="b1e05-113">-AsJob</span></span>
<span data-ttu-id="b1e05-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="b1e05-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b1e05-115">-Bant genişliği</span><span class="sxs-lookup"><span data-stu-id="b1e05-115">-Bandwidth</span></span>
<span data-ttu-id="b1e05-116">Mbps cinsinden bant genişliği</span><span class="sxs-lookup"><span data-stu-id="b1e05-116">Bandwidth in Mbps</span></span>

```yaml
Type: System.Int32
Parameter Sets: BandwidthParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1e05-117">-Daysofya</span><span class="sxs-lookup"><span data-stu-id="b1e05-117">-DaysOfWeek</span></span>
<span data-ttu-id="b1e05-118">Zamanlanmış gün Yumuşma</span><span class="sxs-lookup"><span data-stu-id="b1e05-118">Scheduled DaysOfWeek</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1e05-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1e05-119">-DefaultProfile</span></span>
<span data-ttu-id="b1e05-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b1e05-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1e05-121">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="b1e05-121">-DeviceName</span></span>
<span data-ttu-id="b1e05-122">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="b1e05-122">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1e05-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="b1e05-123">-Name</span></span>
<span data-ttu-id="b1e05-124">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="b1e05-124">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1e05-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1e05-125">-ResourceGroupName</span></span>
<span data-ttu-id="b1e05-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="b1e05-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1e05-127">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="b1e05-127">-StartTime</span></span>
<span data-ttu-id="b1e05-128">Başlangıç saati</span><span class="sxs-lookup"><span data-stu-id="b1e05-128">Schedule Start Time</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1e05-129">-StopTime</span><span class="sxs-lookup"><span data-stu-id="b1e05-129">-StopTime</span></span>
<span data-ttu-id="b1e05-130">Zamanlama durdurma zamanı</span><span class="sxs-lookup"><span data-stu-id="b1e05-130">Schedule Stop Time</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1e05-131">-Unlimitedbant genişliği</span><span class="sxs-lookup"><span data-stu-id="b1e05-131">-UnlimitedBandwidth</span></span>
<span data-ttu-id="b1e05-132">Sınırsız bant genişliği ayarlar; false olarak ayarlanırsa varsayılan değer 20 Mbps olarak ayarlanır</span><span class="sxs-lookup"><span data-stu-id="b1e05-132">Will Set Unlimited Bandwidth, if set to false will set default value as 20 Mbps</span></span>

```yaml
Type: System.Boolean
Parameter Sets: UnlimitedBandwidthParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1e05-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="b1e05-133">-Confirm</span></span>
<span data-ttu-id="b1e05-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b1e05-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1e05-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1e05-135">-WhatIf</span></span>
<span data-ttu-id="b1e05-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b1e05-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b1e05-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b1e05-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1e05-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1e05-138">CommonParameters</span></span>
<span data-ttu-id="b1e05-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b1e05-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1e05-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b1e05-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1e05-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b1e05-141">INPUTS</span></span>

### <span data-ttu-id="b1e05-142">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b1e05-142">None</span></span>

## <span data-ttu-id="b1e05-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b1e05-143">OUTPUTS</span></span>

### <span data-ttu-id="b1e05-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="b1e05-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="b1e05-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b1e05-145">NOTES</span></span>

## <span data-ttu-id="b1e05-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b1e05-146">RELATED LINKS</span></span>
