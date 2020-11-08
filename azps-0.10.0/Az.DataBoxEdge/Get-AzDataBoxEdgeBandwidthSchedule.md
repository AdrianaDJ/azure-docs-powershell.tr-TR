---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: 0a94460105f680efffff36af54bec9936dd0813c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936801"
---
# <span data-ttu-id="43913-101">Get-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="43913-101">Get-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="43913-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43913-102">SYNOPSIS</span></span>
<span data-ttu-id="43913-103">Bant genişliği zamanlamalarıyla ilgili bilgileri alır</span><span class="sxs-lookup"><span data-stu-id="43913-103">Gets the information about the Bandwidth schedules</span></span>

## <span data-ttu-id="43913-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="43913-104">SYNTAX</span></span>

### <span data-ttu-id="43913-105">ListParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="43913-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43913-106">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="43913-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="43913-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="43913-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43913-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43913-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="43913-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="43913-109">DESCRIPTION</span></span>
<span data-ttu-id="43913-110">**Get-AzDataBoxEdgeBandwidthSchedule** cmdlet 'ı bant genişliği zamanlamalarıyla ilgili bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="43913-110">The **Get-AzDataBoxEdgeBandwidthSchedule** cmdlet gets the information about the Bandwidth Schedules.</span></span> <span data-ttu-id="43913-111">Belirli bir bant genişliği zamanlama hakkında bilgi almak için kaynak grubu adı ve cihaz adıyla birlikte bir zamanlamanın adını belirtebilirsiniz</span><span class="sxs-lookup"><span data-stu-id="43913-111">You can specify the Name of a Schedule along with the Resource Group name and Device name to get the information about a specific Bandwidth schedule</span></span>

## <span data-ttu-id="43913-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="43913-112">EXAMPLES</span></span>

### <span data-ttu-id="43913-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="43913-113">Example 1</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name

Name              DaysOfWeek         RateInMbps StartTime StopTime
----              ----------         ---------- --------- --------
schedule-name     Sunday,Saturday    unlimited  13:00:00  14:00:00
Schedule-1        Tuesday,Friday     unlimited  00:00:00  23:59:00
Schedule-2        Thursday           50         00:01:00  05:00:00
```

### <span data-ttu-id="43913-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="43913-114">Example 2</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name -Name Schedule-1

Name              DaysOfWeek      RateInMbps StartTime StopTime
----              ----------      ---------- --------- --------
Schedule-1        Sunday,Saturday unlimited  13:00:00  14:00:00
```

## <span data-ttu-id="43913-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="43913-115">PARAMETERS</span></span>

### <span data-ttu-id="43913-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43913-116">-DefaultProfile</span></span>
<span data-ttu-id="43913-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="43913-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43913-118">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="43913-118">-DeviceName</span></span>
<span data-ttu-id="43913-119">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="43913-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43913-120">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="43913-120">-DeviceObject</span></span>
<span data-ttu-id="43913-121">Lütfen ilgili cihaz nesnesini sağlayın</span><span class="sxs-lookup"><span data-stu-id="43913-121">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43913-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="43913-122">-Name</span></span>
<span data-ttu-id="43913-123">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="43913-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43913-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43913-124">-ResourceGroupName</span></span>
<span data-ttu-id="43913-125">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="43913-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43913-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="43913-126">-ResourceId</span></span>
<span data-ttu-id="43913-127">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="43913-127">Azure ResourceId</span></span>

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

### <span data-ttu-id="43913-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43913-128">CommonParameters</span></span>
<span data-ttu-id="43913-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="43913-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43913-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="43913-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43913-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="43913-131">INPUTS</span></span>

### <span data-ttu-id="43913-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="43913-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="43913-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="43913-133">OUTPUTS</span></span>

### <span data-ttu-id="43913-134">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="43913-134">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="43913-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="43913-135">NOTES</span></span>

## <span data-ttu-id="43913-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="43913-136">RELATED LINKS</span></span>