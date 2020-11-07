---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: e15e6ee6186dc19f9f85264548c1b735ea242b98
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936767"
---
# <span data-ttu-id="30cf7-101">New-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="30cf7-101">New-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="30cf7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30cf7-102">SYNOPSIS</span></span>
<span data-ttu-id="30cf7-103">Yeni bir bant genişliği zamanlama oluşturur</span><span class="sxs-lookup"><span data-stu-id="30cf7-103">Creates a new Bandwidth schedule</span></span>

## <span data-ttu-id="30cf7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="30cf7-104">SYNTAX</span></span>

### <span data-ttu-id="30cf7-105">BandwidthParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="30cf7-105">BandwidthParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30cf7-106">UnlimitedBandwidthParameterSet</span><span class="sxs-lookup"><span data-stu-id="30cf7-106">UnlimitedBandwidthParameterSet</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30cf7-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="30cf7-107">DESCRIPTION</span></span>
<span data-ttu-id="30cf7-108">**New-AzDataBoxEdgeBandwidthSchedule** cmdlet 'ı, bant genişliği kullanımını yönetmeye yardımcı olmak Için bir veri kutusu uç aygıtı için yeni bir bant genişliği çizelgesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="30cf7-108">The **New-AzDataBoxEdgeBandwidthSchedule** cmdlet creates a new Bandwidth Schedule for a Data Box Edge device to help manage the Bandwidth usage.</span></span>

## <span data-ttu-id="30cf7-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="30cf7-109">EXAMPLES</span></span>

### <span data-ttu-id="30cf7-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="30cf7-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StartTime 11:00 -StopTime 12:00 -Bandwidth 30
Name                DaysOfWeek                  RateInMbps StartTime StopTime
----                ----------                  ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday    30         11:00:00  12:00:00
```

### <span data-ttu-id="30cf7-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="30cf7-111">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthScheduleUnlimited -StartTime 11:00 -StopTime 12:00 -UnlimitedBandwidth
Name                          DaysOfWeek                RateInMbps  StartTime    StopTime
----------------              ----------------------    ----------- -----------  ---------
bandwidthScheduleUnlimited  Sunday,Tuesday,Saturday     unlimited   11:00:00     12:00:00
```

## <span data-ttu-id="30cf7-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="30cf7-112">PARAMETERS</span></span>

### <span data-ttu-id="30cf7-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="30cf7-113">-AsJob</span></span>
<span data-ttu-id="30cf7-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="30cf7-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="30cf7-115">-Bant genişliği</span><span class="sxs-lookup"><span data-stu-id="30cf7-115">-Bandwidth</span></span>
<span data-ttu-id="30cf7-116">Mbps cinsinden bant genişliği</span><span class="sxs-lookup"><span data-stu-id="30cf7-116">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="30cf7-117">-Daysofya</span><span class="sxs-lookup"><span data-stu-id="30cf7-117">-DaysOfWeek</span></span>
<span data-ttu-id="30cf7-118">Zamanlanmış gün Yumuşma</span><span class="sxs-lookup"><span data-stu-id="30cf7-118">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="30cf7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30cf7-119">-DefaultProfile</span></span>
<span data-ttu-id="30cf7-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="30cf7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30cf7-121">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="30cf7-121">-DeviceName</span></span>
<span data-ttu-id="30cf7-122">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="30cf7-122">Device Name</span></span>

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

### <span data-ttu-id="30cf7-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="30cf7-123">-Name</span></span>
<span data-ttu-id="30cf7-124">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="30cf7-124">Resource Name</span></span>

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

### <span data-ttu-id="30cf7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30cf7-125">-ResourceGroupName</span></span>
<span data-ttu-id="30cf7-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="30cf7-126">Resource Group Name</span></span>

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

### <span data-ttu-id="30cf7-127">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="30cf7-127">-StartTime</span></span>
<span data-ttu-id="30cf7-128">Başlangıç saati</span><span class="sxs-lookup"><span data-stu-id="30cf7-128">Schedule Start Time</span></span>

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

### <span data-ttu-id="30cf7-129">-StopTime</span><span class="sxs-lookup"><span data-stu-id="30cf7-129">-StopTime</span></span>
<span data-ttu-id="30cf7-130">Zamanlama durdurma zamanı</span><span class="sxs-lookup"><span data-stu-id="30cf7-130">Schedule Stop Time</span></span>

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

### <span data-ttu-id="30cf7-131">-Unlimitedbant genişliği</span><span class="sxs-lookup"><span data-stu-id="30cf7-131">-UnlimitedBandwidth</span></span>
<span data-ttu-id="30cf7-132">Sınırsız bant genişliği ayarlar; false olarak ayarlanırsa varsayılan değer 20 Mbps olarak ayarlanır</span><span class="sxs-lookup"><span data-stu-id="30cf7-132">Will Set Unlimited Bandwidth, if set to false will set default value as 20 Mbps</span></span>

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

### <span data-ttu-id="30cf7-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="30cf7-133">-Confirm</span></span>
<span data-ttu-id="30cf7-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="30cf7-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30cf7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30cf7-135">-WhatIf</span></span>
<span data-ttu-id="30cf7-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="30cf7-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30cf7-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="30cf7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30cf7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30cf7-138">CommonParameters</span></span>
<span data-ttu-id="30cf7-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="30cf7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30cf7-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="30cf7-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30cf7-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="30cf7-141">INPUTS</span></span>

### <span data-ttu-id="30cf7-142">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="30cf7-142">None</span></span>

## <span data-ttu-id="30cf7-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="30cf7-143">OUTPUTS</span></span>

### <span data-ttu-id="30cf7-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="30cf7-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="30cf7-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="30cf7-145">NOTES</span></span>

## <span data-ttu-id="30cf7-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="30cf7-146">RELATED LINKS</span></span>
