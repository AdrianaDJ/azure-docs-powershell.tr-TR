---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeJob.md
ms.openlocfilehash: c2d97f4a7d713482a5e442e1fcb712ccb18797c0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321241"
---
# <span data-ttu-id="f89c3-101">Get-AzDataBoxEdgeJob</span><span class="sxs-lookup"><span data-stu-id="f89c3-101">Get-AzDataBoxEdgeJob</span></span>

## <span data-ttu-id="f89c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f89c3-102">SYNOPSIS</span></span>
<span data-ttu-id="f89c3-103">Cihazda zamanlanmış işleri alır.</span><span class="sxs-lookup"><span data-stu-id="f89c3-103">Gets the jobs scheduled on a device.</span></span>

## <span data-ttu-id="f89c3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f89c3-104">SYNTAX</span></span>

### <span data-ttu-id="f89c3-105">GetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f89c3-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeJob [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f89c3-106">Getbyresourceıdobject</span><span class="sxs-lookup"><span data-stu-id="f89c3-106">GetByResourceIdObject</span></span>
```
Get-AzDataBoxEdgeJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f89c3-107">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f89c3-107">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeJob [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="f89c3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f89c3-108">DESCRIPTION</span></span>
<span data-ttu-id="f89c3-109">**Get-AzDataBoxEdgeJob** cmdlet 'ı bir veri kutusu uç aygıtındaki etkin işleri alır.</span><span class="sxs-lookup"><span data-stu-id="f89c3-109">The **Get-AzDataBoxEdgeJob** cmdlet gets the active jobs on a Data Box Edge device.</span></span> <span data-ttu-id="f89c3-110">Belirli bir işin ayrıntılarını almak için Name parametresinden bahsedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f89c3-110">You can mention the Name parameter to get details of a specific job.</span></span>

## <span data-ttu-id="f89c3-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f89c3-111">EXAMPLES</span></span>

### <span data-ttu-id="f89c3-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f89c3-112">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeJob -ResourceGroupName resourceGroupName -DeviceName deviceName -Name 1f2d8f1b-9104-49c3-b780-76db9abe7bd1
Name                                   Device-Name    status
------------------                     -------------  -------
1f2d8f1b-9104-49c3-b780-76db9abe7bd1   deviceName    Scheduled
```

## <span data-ttu-id="f89c3-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f89c3-113">PARAMETERS</span></span>

### <span data-ttu-id="f89c3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f89c3-114">-DefaultProfile</span></span>
<span data-ttu-id="f89c3-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f89c3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f89c3-116">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="f89c3-116">-DeviceName</span></span>
<span data-ttu-id="f89c3-117">Cihazın adı</span><span class="sxs-lookup"><span data-stu-id="f89c3-117">Name of the device</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f89c3-118">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="f89c3-118">-DeviceObject</span></span>
<span data-ttu-id="f89c3-119">Lütfen ilgili cihaz nesnesini sağlayın</span><span class="sxs-lookup"><span data-stu-id="f89c3-119">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="f89c3-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="f89c3-120">-Name</span></span>
<span data-ttu-id="f89c3-121">Işin adı, genellikle GUID</span><span class="sxs-lookup"><span data-stu-id="f89c3-121">Name of the Job, Generally a GUID</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f89c3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f89c3-122">-ResourceGroupName</span></span>
<span data-ttu-id="f89c3-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="f89c3-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f89c3-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f89c3-124">-ResourceId</span></span>
<span data-ttu-id="f89c3-125">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f89c3-125">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f89c3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f89c3-126">CommonParameters</span></span>
<span data-ttu-id="f89c3-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f89c3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f89c3-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f89c3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f89c3-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f89c3-129">INPUTS</span></span>

### <span data-ttu-id="f89c3-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="f89c3-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="f89c3-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f89c3-131">OUTPUTS</span></span>

### <span data-ttu-id="f89c3-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeJob</span><span class="sxs-lookup"><span data-stu-id="f89c3-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeJob</span></span>

## <span data-ttu-id="f89c3-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f89c3-133">NOTES</span></span>

## <span data-ttu-id="f89c3-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f89c3-134">RELATED LINKS</span></span>
