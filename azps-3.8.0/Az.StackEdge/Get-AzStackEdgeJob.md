---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeJob.md
ms.openlocfilehash: 957cc5c7dea0b8ea3215a035f68c2528442a7d52
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096547"
---
# <span data-ttu-id="ed483-101">Get-AzStackEdgeJob</span><span class="sxs-lookup"><span data-stu-id="ed483-101">Get-AzStackEdgeJob</span></span>

## <span data-ttu-id="ed483-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed483-102">SYNOPSIS</span></span>
<span data-ttu-id="ed483-103">Cihazda zamanlanmış işleri alır.</span><span class="sxs-lookup"><span data-stu-id="ed483-103">Gets the jobs scheduled on a device.</span></span>

## <span data-ttu-id="ed483-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ed483-104">SYNTAX</span></span>

### <span data-ttu-id="ed483-105">GetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ed483-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzStackEdgeJob [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed483-106">Getbyresourceıdobject</span><span class="sxs-lookup"><span data-stu-id="ed483-106">GetByResourceIdObject</span></span>
```
Get-AzStackEdgeJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed483-107">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed483-107">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeJob [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="ed483-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ed483-108">DESCRIPTION</span></span>
<span data-ttu-id="ed483-109">**Get-AzStackEdgeJob** cmdlet 'ı yığın uç aygıtındaki etkin işleri alır.</span><span class="sxs-lookup"><span data-stu-id="ed483-109">The **Get-AzStackEdgeJob** cmdlet gets the active jobs on a Stack Edge device.</span></span> <span data-ttu-id="ed483-110">Belirli bir işin ayrıntılarını almak için Name parametresinden bahsedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ed483-110">You can mention the Name parameter to get details of a specific job.</span></span>

## <span data-ttu-id="ed483-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ed483-111">EXAMPLES</span></span>

### <span data-ttu-id="ed483-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ed483-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeJob -ResourceGroupName resourceGroupName -DeviceName deviceName -Name 1f2d8f1b-9104-49c3-b780-76db9abe7bd1
Name                                   Device-Name    status
------------------                     -------------  -------
1f2d8f1b-9104-49c3-b780-76db9abe7bd1   deviceName    Scheduled
```

## <span data-ttu-id="ed483-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ed483-113">PARAMETERS</span></span>

### <span data-ttu-id="ed483-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed483-114">-DefaultProfile</span></span>
<span data-ttu-id="ed483-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ed483-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed483-116">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="ed483-116">-DeviceName</span></span>
<span data-ttu-id="ed483-117">Cihazın adı</span><span class="sxs-lookup"><span data-stu-id="ed483-117">Name of the device</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed483-118">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="ed483-118">-DeviceObject</span></span>
<span data-ttu-id="ed483-119">Lütfen ilgili cihaz nesnesini sağlayın</span><span class="sxs-lookup"><span data-stu-id="ed483-119">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed483-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="ed483-120">-Name</span></span>
<span data-ttu-id="ed483-121">Işin adı, genellikle GUID</span><span class="sxs-lookup"><span data-stu-id="ed483-121">Name of the Job, Generally a GUID</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: Job

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed483-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed483-122">-ResourceGroupName</span></span>
<span data-ttu-id="ed483-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="ed483-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed483-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ed483-124">-ResourceId</span></span>
<span data-ttu-id="ed483-125">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ed483-125">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed483-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed483-126">CommonParameters</span></span>
<span data-ttu-id="ed483-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ed483-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed483-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ed483-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed483-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ed483-129">INPUTS</span></span>

### <span data-ttu-id="ed483-130">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="ed483-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="ed483-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ed483-131">OUTPUTS</span></span>

### <span data-ttu-id="ed483-132">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeJob</span><span class="sxs-lookup"><span data-stu-id="ed483-132">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeJob</span></span>

## <span data-ttu-id="ed483-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ed483-133">NOTES</span></span>

## <span data-ttu-id="ed483-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ed483-134">RELATED LINKS</span></span>
