---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeOrder.md
ms.openlocfilehash: 2ef7b7ac2a06da0ef0f4b09d82f9a4ed447618ce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323575"
---
# <span data-ttu-id="55f1a-101">Get-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="55f1a-101">Get-AzStackEdgeOrder</span></span>

## <span data-ttu-id="55f1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55f1a-102">SYNOPSIS</span></span>
<span data-ttu-id="55f1a-103">Cihazın sipariş ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="55f1a-103">Get the order details for a device</span></span>

## <span data-ttu-id="55f1a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="55f1a-104">SYNTAX</span></span>

### <span data-ttu-id="55f1a-105">GetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="55f1a-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55f1a-106">GetByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="55f1a-106">GetByDeviceObjectParameterSet</span></span>
```
Get-AzStackEdgeOrder -DeviceObject <PSStackEdgeOrder> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="55f1a-107">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="55f1a-107">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeOrder -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55f1a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="55f1a-108">DESCRIPTION</span></span>
<span data-ttu-id="55f1a-109">**Get-AzStackEdgeOrder** cmdlet 'ı yığın uç aygıtının sipariş ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="55f1a-109">The **Get-AzStackEdgeOrder** cmdlet gets the order details for a Stack Edge device.</span></span> 

## <span data-ttu-id="55f1a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="55f1a-110">EXAMPLES</span></span>

### <span data-ttu-id="55f1a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="55f1a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="55f1a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="55f1a-112">PARAMETERS</span></span>

### <span data-ttu-id="55f1a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55f1a-113">-DefaultProfile</span></span>
<span data-ttu-id="55f1a-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="55f1a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55f1a-115">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="55f1a-115">-DeviceName</span></span>
<span data-ttu-id="55f1a-116">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="55f1a-116">Resource Group Name</span></span>

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

### <span data-ttu-id="55f1a-117">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="55f1a-117">-DeviceObject</span></span>
<span data-ttu-id="55f1a-118">Lütfen ilgili cihaz nesnesini sağlayın</span><span class="sxs-lookup"><span data-stu-id="55f1a-118">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="55f1a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55f1a-119">-ResourceGroupName</span></span>
<span data-ttu-id="55f1a-120">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="55f1a-120">Resource Group Name</span></span>

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

### <span data-ttu-id="55f1a-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="55f1a-121">-ResourceId</span></span>
<span data-ttu-id="55f1a-122">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="55f1a-122">Azure ResourceId</span></span>

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

### <span data-ttu-id="55f1a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55f1a-123">CommonParameters</span></span>
<span data-ttu-id="55f1a-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="55f1a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55f1a-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="55f1a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55f1a-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="55f1a-126">INPUTS</span></span>

### <span data-ttu-id="55f1a-127">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="55f1a-127">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

### <span data-ttu-id="55f1a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="55f1a-128">System.String</span></span>

## <span data-ttu-id="55f1a-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="55f1a-129">OUTPUTS</span></span>

### <span data-ttu-id="55f1a-130">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="55f1a-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="55f1a-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="55f1a-131">NOTES</span></span>

## <span data-ttu-id="55f1a-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="55f1a-132">RELATED LINKS</span></span>
