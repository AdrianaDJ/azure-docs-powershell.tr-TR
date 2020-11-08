---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: 390646984cbe18c6fed0e6552e8034ae7afe311c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098302"
---
# <span data-ttu-id="53960-101">Get-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="53960-101">Get-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="53960-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53960-102">SYNOPSIS</span></span>
<span data-ttu-id="53960-103">Cihazda yapılandırılmış tetikleri alma</span><span class="sxs-lookup"><span data-stu-id="53960-103">Get the Triggers configured on a device</span></span>
 

## <span data-ttu-id="53960-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="53960-104">SYNTAX</span></span>

### <span data-ttu-id="53960-105">ListParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="53960-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53960-106">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="53960-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53960-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="53960-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53960-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="53960-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="53960-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="53960-109">DESCRIPTION</span></span>
<span data-ttu-id="53960-110">**Get-AzDataBoxEdgeTriger** cmdlet 'i bir cihazın tetikleyicilerini alır.</span><span class="sxs-lookup"><span data-stu-id="53960-110">The **Get-AzDataBoxEdgeTriger** cmdlet gets the triggers for a device.</span></span> <span data-ttu-id="53960-111">Belirli bir tetikleyicilerin ayrıntılarını getirmek için cmdlet 'teki adı bir parametre olarak belirtebilirsiniz</span><span class="sxs-lookup"><span data-stu-id="53960-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific  specific Triggers</span></span>
 

## <span data-ttu-id="53960-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="53960-112">EXAMPLES</span></span>

### <span data-ttu-id="53960-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="53960-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                  Kind               
----                  ----               
triggerName          PeriodicTimerEvent
```

## <span data-ttu-id="53960-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="53960-114">PARAMETERS</span></span>

### <span data-ttu-id="53960-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53960-115">-DefaultProfile</span></span>
<span data-ttu-id="53960-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="53960-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53960-117">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="53960-117">-DeviceName</span></span>
<span data-ttu-id="53960-118">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="53960-118">Device Name</span></span>

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

### <span data-ttu-id="53960-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="53960-119">-DeviceObject</span></span>
<span data-ttu-id="53960-120">Lütfen ilgili cihaz nesnesini sağlayın</span><span class="sxs-lookup"><span data-stu-id="53960-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="53960-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="53960-121">-Name</span></span>
<span data-ttu-id="53960-122">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="53960-122">Resource Name</span></span>

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

### <span data-ttu-id="53960-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53960-123">-ResourceGroupName</span></span>
<span data-ttu-id="53960-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="53960-124">Resource Group Name</span></span>

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

### <span data-ttu-id="53960-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="53960-125">-ResourceId</span></span>
<span data-ttu-id="53960-126">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="53960-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="53960-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53960-127">CommonParameters</span></span>
<span data-ttu-id="53960-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="53960-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53960-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="53960-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53960-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="53960-130">INPUTS</span></span>

### <span data-ttu-id="53960-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="53960-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="53960-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="53960-132">OUTPUTS</span></span>

### <span data-ttu-id="53960-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="53960-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="53960-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="53960-134">NOTES</span></span>

## <span data-ttu-id="53960-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="53960-135">RELATED LINKS</span></span>