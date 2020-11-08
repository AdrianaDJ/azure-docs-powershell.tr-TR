---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: 96c9b736398cb981dd055d072091aa24af4d3f6c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936785"
---
# <span data-ttu-id="ee24c-101">Get-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="ee24c-101">Get-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="ee24c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee24c-102">SYNOPSIS</span></span>
<span data-ttu-id="ee24c-103">Cihazda yapılandırılmış tetikleri alma</span><span class="sxs-lookup"><span data-stu-id="ee24c-103">Get the Triggers configured on a device</span></span>
 

## <span data-ttu-id="ee24c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ee24c-104">SYNTAX</span></span>

### <span data-ttu-id="ee24c-105">ListParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ee24c-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee24c-106">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="ee24c-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee24c-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee24c-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee24c-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee24c-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="ee24c-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="ee24c-109">DESCRIPTION</span></span>
<span data-ttu-id="ee24c-110">**Get-AzDataBoxEdgeTriger** cmdlet 'i bir cihazın tetikleyicilerini alır.</span><span class="sxs-lookup"><span data-stu-id="ee24c-110">The **Get-AzDataBoxEdgeTriger** cmdlet gets the triggers for a device.</span></span> <span data-ttu-id="ee24c-111">Belirli bir tetikleyicilerin ayrıntılarını getirmek için cmdlet 'teki adı bir parametre olarak belirtebilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ee24c-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific  specific Triggers</span></span>
 

## <span data-ttu-id="ee24c-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ee24c-112">EXAMPLES</span></span>

### <span data-ttu-id="ee24c-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ee24c-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                  Kind               
----                  ----               
triggerName          PeriodicTimerEvent
```

## <span data-ttu-id="ee24c-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ee24c-114">PARAMETERS</span></span>

### <span data-ttu-id="ee24c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee24c-115">-DefaultProfile</span></span>
<span data-ttu-id="ee24c-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ee24c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee24c-117">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="ee24c-117">-DeviceName</span></span>
<span data-ttu-id="ee24c-118">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="ee24c-118">Device Name</span></span>

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

### <span data-ttu-id="ee24c-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="ee24c-119">-DeviceObject</span></span>
<span data-ttu-id="ee24c-120">Lütfen ilgili cihaz nesnesini sağlayın</span><span class="sxs-lookup"><span data-stu-id="ee24c-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="ee24c-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="ee24c-121">-Name</span></span>
<span data-ttu-id="ee24c-122">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="ee24c-122">Resource Name</span></span>

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

### <span data-ttu-id="ee24c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee24c-123">-ResourceGroupName</span></span>
<span data-ttu-id="ee24c-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="ee24c-124">Resource Group Name</span></span>

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

### <span data-ttu-id="ee24c-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ee24c-125">-ResourceId</span></span>
<span data-ttu-id="ee24c-126">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ee24c-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="ee24c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee24c-127">CommonParameters</span></span>
<span data-ttu-id="ee24c-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ee24c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee24c-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ee24c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee24c-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ee24c-130">INPUTS</span></span>

### <span data-ttu-id="ee24c-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="ee24c-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="ee24c-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ee24c-132">OUTPUTS</span></span>

### <span data-ttu-id="ee24c-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="ee24c-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="ee24c-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ee24c-134">NOTES</span></span>

## <span data-ttu-id="ee24c-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ee24c-135">RELATED LINKS</span></span>