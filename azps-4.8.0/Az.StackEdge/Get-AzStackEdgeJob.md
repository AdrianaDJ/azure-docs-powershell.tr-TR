---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeJob.md
ms.openlocfilehash: 957cc5c7dea0b8ea3215a035f68c2528442a7d52
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267569"
---
# <span data-ttu-id="47d31-101">Get-AzStackEdgeJob</span><span class="sxs-lookup"><span data-stu-id="47d31-101">Get-AzStackEdgeJob</span></span>

## <span data-ttu-id="47d31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47d31-102">SYNOPSIS</span></span>
<span data-ttu-id="47d31-103">Cihazda zamanlanmış işleri alır.</span><span class="sxs-lookup"><span data-stu-id="47d31-103">Gets the jobs scheduled on a device.</span></span>

## <span data-ttu-id="47d31-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="47d31-104">SYNTAX</span></span>

### <span data-ttu-id="47d31-105">GetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="47d31-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzStackEdgeJob [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47d31-106">Getbyresourceıdobject</span><span class="sxs-lookup"><span data-stu-id="47d31-106">GetByResourceIdObject</span></span>
```
Get-AzStackEdgeJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47d31-107">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="47d31-107">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeJob [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="47d31-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="47d31-108">DESCRIPTION</span></span>
<span data-ttu-id="47d31-109">**Get-AzStackEdgeJob** cmdlet 'ı yığın uç aygıtındaki etkin işleri alır.</span><span class="sxs-lookup"><span data-stu-id="47d31-109">The **Get-AzStackEdgeJob** cmdlet gets the active jobs on a Stack Edge device.</span></span> <span data-ttu-id="47d31-110">Belirli bir işin ayrıntılarını almak için Name parametresinden bahsedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47d31-110">You can mention the Name parameter to get details of a specific job.</span></span>

## <span data-ttu-id="47d31-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="47d31-111">EXAMPLES</span></span>

### <span data-ttu-id="47d31-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="47d31-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeJob -ResourceGroupName resourceGroupName -DeviceName deviceName -Name 1f2d8f1b-9104-49c3-b780-76db9abe7bd1
Name                                   Device-Name    status
------------------                     -------------  -------
1f2d8f1b-9104-49c3-b780-76db9abe7bd1   deviceName    Scheduled
```

## <span data-ttu-id="47d31-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="47d31-113">PARAMETERS</span></span>

### <span data-ttu-id="47d31-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47d31-114">-DefaultProfile</span></span>
<span data-ttu-id="47d31-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="47d31-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47d31-116">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="47d31-116">-DeviceName</span></span>
<span data-ttu-id="47d31-117">Cihazın adı</span><span class="sxs-lookup"><span data-stu-id="47d31-117">Name of the device</span></span>

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

### <span data-ttu-id="47d31-118">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="47d31-118">-DeviceObject</span></span>
<span data-ttu-id="47d31-119">Lütfen ilgili cihaz nesnesini sağlayın</span><span class="sxs-lookup"><span data-stu-id="47d31-119">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="47d31-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="47d31-120">-Name</span></span>
<span data-ttu-id="47d31-121">Işin adı, genellikle GUID</span><span class="sxs-lookup"><span data-stu-id="47d31-121">Name of the Job, Generally a GUID</span></span>

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

### <span data-ttu-id="47d31-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47d31-122">-ResourceGroupName</span></span>
<span data-ttu-id="47d31-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="47d31-123">Resource Group Name</span></span>

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

### <span data-ttu-id="47d31-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="47d31-124">-ResourceId</span></span>
<span data-ttu-id="47d31-125">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="47d31-125">Azure ResourceId</span></span>

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

### <span data-ttu-id="47d31-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47d31-126">CommonParameters</span></span>
<span data-ttu-id="47d31-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="47d31-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47d31-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="47d31-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47d31-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="47d31-129">INPUTS</span></span>

### <span data-ttu-id="47d31-130">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="47d31-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="47d31-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="47d31-131">OUTPUTS</span></span>

### <span data-ttu-id="47d31-132">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeJob</span><span class="sxs-lookup"><span data-stu-id="47d31-132">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeJob</span></span>

## <span data-ttu-id="47d31-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="47d31-133">NOTES</span></span>

## <span data-ttu-id="47d31-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="47d31-134">RELATED LINKS</span></span>
