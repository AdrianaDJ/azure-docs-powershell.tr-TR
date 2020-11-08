---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeOrder.md
ms.openlocfilehash: 2ef7b7ac2a06da0ef0f4b09d82f9a4ed447618ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096548"
---
# <span data-ttu-id="ad725-101">Get-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="ad725-101">Get-AzStackEdgeOrder</span></span>

## <span data-ttu-id="ad725-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad725-102">SYNOPSIS</span></span>
<span data-ttu-id="ad725-103">Cihazın sipariş ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="ad725-103">Get the order details for a device</span></span>

## <span data-ttu-id="ad725-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ad725-104">SYNTAX</span></span>

### <span data-ttu-id="ad725-105">GetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ad725-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad725-106">GetByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad725-106">GetByDeviceObjectParameterSet</span></span>
```
Get-AzStackEdgeOrder -DeviceObject <PSStackEdgeOrder> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad725-107">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="ad725-107">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeOrder -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad725-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ad725-108">DESCRIPTION</span></span>
<span data-ttu-id="ad725-109">**Get-AzStackEdgeOrder** cmdlet 'ı yığın uç aygıtının sipariş ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="ad725-109">The **Get-AzStackEdgeOrder** cmdlet gets the order details for a Stack Edge device.</span></span> 

## <span data-ttu-id="ad725-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ad725-110">EXAMPLES</span></span>

### <span data-ttu-id="ad725-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ad725-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="ad725-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ad725-112">PARAMETERS</span></span>

### <span data-ttu-id="ad725-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad725-113">-DefaultProfile</span></span>
<span data-ttu-id="ad725-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ad725-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad725-115">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="ad725-115">-DeviceName</span></span>
<span data-ttu-id="ad725-116">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="ad725-116">Resource Group Name</span></span>

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

### <span data-ttu-id="ad725-117">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="ad725-117">-DeviceObject</span></span>
<span data-ttu-id="ad725-118">Lütfen ilgili cihaz nesnesini sağlayın</span><span class="sxs-lookup"><span data-stu-id="ad725-118">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder
Parameter Sets: GetByDeviceObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad725-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad725-119">-ResourceGroupName</span></span>
<span data-ttu-id="ad725-120">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="ad725-120">Resource Group Name</span></span>

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

### <span data-ttu-id="ad725-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ad725-121">-ResourceId</span></span>
<span data-ttu-id="ad725-122">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ad725-122">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad725-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad725-123">CommonParameters</span></span>
<span data-ttu-id="ad725-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ad725-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad725-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ad725-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad725-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ad725-126">INPUTS</span></span>

### <span data-ttu-id="ad725-127">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="ad725-127">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

### <span data-ttu-id="ad725-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ad725-128">System.String</span></span>

## <span data-ttu-id="ad725-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ad725-129">OUTPUTS</span></span>

### <span data-ttu-id="ad725-130">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="ad725-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="ad725-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ad725-131">NOTES</span></span>

## <span data-ttu-id="ad725-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ad725-132">RELATED LINKS</span></span>
