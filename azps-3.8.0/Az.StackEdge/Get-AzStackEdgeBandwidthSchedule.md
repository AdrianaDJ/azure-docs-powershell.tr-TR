---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: 5f2dfec045364852d9846fa3bb35bd903c78ca5a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096549"
---
# <span data-ttu-id="5cafb-101">Get-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="5cafb-101">Get-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="5cafb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cafb-102">SYNOPSIS</span></span>
<span data-ttu-id="5cafb-103">Bant genişliği zamanlamalarıyla ilgili bilgileri alır</span><span class="sxs-lookup"><span data-stu-id="5cafb-103">Gets the information about the Bandwidth schedules</span></span>

## <span data-ttu-id="5cafb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5cafb-104">SYNTAX</span></span>

### <span data-ttu-id="5cafb-105">ListParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5cafb-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5cafb-106">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="5cafb-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeBandwidthSchedule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5cafb-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5cafb-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5cafb-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5cafb-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeBandwidthSchedule [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="5cafb-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="5cafb-109">DESCRIPTION</span></span>
<span data-ttu-id="5cafb-110">**Get-AzStackEdgeBandwidthSchedule** cmdlet 'ı bant genişliği zamanlamalarıyla ilgili bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="5cafb-110">The **Get-AzStackEdgeBandwidthSchedule** cmdlet gets the information about the Bandwidth Schedules.</span></span> <span data-ttu-id="5cafb-111">Belirli bir bant genişliği zamanlama hakkında bilgi almak için kaynak grubu adı ve cihaz adıyla birlikte bir zamanlamanın adını belirtebilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5cafb-111">You can specify the Name of a Schedule along with the Resource Group name and Device name to get the information about a specific Bandwidth schedule</span></span>

## <span data-ttu-id="5cafb-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5cafb-112">EXAMPLES</span></span>

### <span data-ttu-id="5cafb-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5cafb-113">Example 1</span></span>
```powershell
PS C:\>Get-AzStackEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name

Name              DaysOfWeek         RateInMbps StartTime StopTime
----              ----------         ---------- --------- --------
schedule-name     Sunday,Saturday    unlimited  13:00:00  14:00:00
Schedule-1        Tuesday,Friday     unlimited  00:00:00  23:59:00
Schedule-2        Thursday           50         00:01:00  05:00:00
```

### <span data-ttu-id="5cafb-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="5cafb-114">Example 2</span></span>
```powershell
PS C:\>Get-AzStackEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name -Name Schedule-1

Name              DaysOfWeek      RateInMbps StartTime StopTime
----              ----------      ---------- --------- --------
Schedule-1        Sunday,Saturday unlimited  13:00:00  14:00:00
```

## <span data-ttu-id="5cafb-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5cafb-115">PARAMETERS</span></span>

### <span data-ttu-id="5cafb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cafb-116">-DefaultProfile</span></span>
<span data-ttu-id="5cafb-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5cafb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cafb-118">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="5cafb-118">-DeviceName</span></span>
<span data-ttu-id="5cafb-119">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="5cafb-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cafb-120">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="5cafb-120">-DeviceObject</span></span>
<span data-ttu-id="5cafb-121">Lütfen ilgili cihaz nesnesini sağlayın</span><span class="sxs-lookup"><span data-stu-id="5cafb-121">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5cafb-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="5cafb-122">-Name</span></span>
<span data-ttu-id="5cafb-123">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="5cafb-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: BandwidthScheduleName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cafb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cafb-124">-ResourceGroupName</span></span>
<span data-ttu-id="5cafb-125">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="5cafb-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cafb-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5cafb-126">-ResourceId</span></span>
<span data-ttu-id="5cafb-127">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5cafb-127">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cafb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cafb-128">CommonParameters</span></span>
<span data-ttu-id="5cafb-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5cafb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cafb-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5cafb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cafb-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5cafb-131">INPUTS</span></span>

### <span data-ttu-id="5cafb-132">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="5cafb-132">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="5cafb-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5cafb-133">OUTPUTS</span></span>

### <span data-ttu-id="5cafb-134">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="5cafb-134">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="5cafb-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5cafb-135">NOTES</span></span>

## <span data-ttu-id="5cafb-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5cafb-136">RELATED LINKS</span></span>