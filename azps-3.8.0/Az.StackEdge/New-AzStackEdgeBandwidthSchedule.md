---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: 27d1f77db385c04e50b67b9aa3a8d8d6bf921485
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096476"
---
# <span data-ttu-id="1554c-101">New-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="1554c-101">New-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="1554c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1554c-102">SYNOPSIS</span></span>
<span data-ttu-id="1554c-103">Yeni bir bant genişliği zamanlama oluşturur</span><span class="sxs-lookup"><span data-stu-id="1554c-103">Creates a new Bandwidth schedule</span></span>

## <span data-ttu-id="1554c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1554c-104">SYNTAX</span></span>

### <span data-ttu-id="1554c-105">UnlimitedBandwidthParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1554c-105">UnlimitedBandwidthParameterSet (Default)</span></span>
```
New-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1554c-106">BandwidthParameterSet</span><span class="sxs-lookup"><span data-stu-id="1554c-106">BandwidthParameterSet</span></span>
```
New-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1554c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1554c-107">DESCRIPTION</span></span>
<span data-ttu-id="1554c-108">**New-AzStackEdgeBandwidthSchedule** cmdlet 'ı, bant genişliği kullanımını yönetmeye yardımcı olacak bir yığın uç aygıtı için yeni bir bant genişliği çizelgesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1554c-108">The **New-AzStackEdgeBandwidthSchedule** cmdlet creates a new Bandwidth Schedule for a Stack Edge device to help manage the Bandwidth usage.</span></span>

## <span data-ttu-id="1554c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1554c-109">EXAMPLES</span></span>

### <span data-ttu-id="1554c-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1554c-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StartTime 11:00 -StopTime 12:00 -Bandwidth 30
Name                DaysOfWeek                  RateInMbps StartTime StopTime
----                ----------                  ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday    30         11:00:00  12:00:00
```

### <span data-ttu-id="1554c-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1554c-111">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthScheduleUnlimited -StartTime 11:00 -StopTime 12:00 -UnlimitedBandwidth
Name                          DaysOfWeek                RateInMbps  StartTime    StopTime
----------------              ----------------------    ----------- -----------  ---------
bandwidthScheduleUnlimited  Sunday,Tuesday,Saturday     unlimited   11:00:00     12:00:00
```

## <span data-ttu-id="1554c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1554c-112">PARAMETERS</span></span>

### <span data-ttu-id="1554c-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="1554c-113">-AsJob</span></span>
<span data-ttu-id="1554c-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="1554c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1554c-115">-Bant genişliği</span><span class="sxs-lookup"><span data-stu-id="1554c-115">-Bandwidth</span></span>
<span data-ttu-id="1554c-116">Mbps cinsinden bant genişliği</span><span class="sxs-lookup"><span data-stu-id="1554c-116">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="1554c-117">-Daysofya</span><span class="sxs-lookup"><span data-stu-id="1554c-117">-DaysOfWeek</span></span>
<span data-ttu-id="1554c-118">Zamanlanmış gün Yumuşma</span><span class="sxs-lookup"><span data-stu-id="1554c-118">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="1554c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1554c-119">-DefaultProfile</span></span>
<span data-ttu-id="1554c-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1554c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1554c-121">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="1554c-121">-DeviceName</span></span>
<span data-ttu-id="1554c-122">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="1554c-122">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1554c-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="1554c-123">-Name</span></span>
<span data-ttu-id="1554c-124">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="1554c-124">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1554c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1554c-125">-ResourceGroupName</span></span>
<span data-ttu-id="1554c-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="1554c-126">Resource Group Name</span></span>

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

### <span data-ttu-id="1554c-127">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="1554c-127">-StartTime</span></span>
<span data-ttu-id="1554c-128">Başlangıç saati</span><span class="sxs-lookup"><span data-stu-id="1554c-128">Schedule Start Time</span></span>

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

### <span data-ttu-id="1554c-129">-StopTime</span><span class="sxs-lookup"><span data-stu-id="1554c-129">-StopTime</span></span>
<span data-ttu-id="1554c-130">Zamanlama durdurma zamanı</span><span class="sxs-lookup"><span data-stu-id="1554c-130">Schedule Stop Time</span></span>

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

### <span data-ttu-id="1554c-131">-Unlimitedbant genişliği</span><span class="sxs-lookup"><span data-stu-id="1554c-131">-UnlimitedBandwidth</span></span>
<span data-ttu-id="1554c-132">Bant genişliğini sınırsız olarak ayarlar</span><span class="sxs-lookup"><span data-stu-id="1554c-132">Will Set Bandwidth as Unlimited</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UnlimitedBandwidthParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1554c-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="1554c-133">-Confirm</span></span>
<span data-ttu-id="1554c-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1554c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1554c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1554c-135">-WhatIf</span></span>
<span data-ttu-id="1554c-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1554c-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1554c-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1554c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1554c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1554c-138">CommonParameters</span></span>
<span data-ttu-id="1554c-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1554c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1554c-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1554c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1554c-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1554c-141">INPUTS</span></span>

### <span data-ttu-id="1554c-142">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1554c-142">None</span></span>

## <span data-ttu-id="1554c-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1554c-143">OUTPUTS</span></span>

### <span data-ttu-id="1554c-144">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="1554c-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="1554c-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1554c-145">NOTES</span></span>

## <span data-ttu-id="1554c-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1554c-146">RELATED LINKS</span></span>
