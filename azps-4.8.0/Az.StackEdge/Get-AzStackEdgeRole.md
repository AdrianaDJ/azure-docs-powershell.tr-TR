---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeRole.md
ms.openlocfilehash: 56179260dc045b83ed067e92c6aa8bd7f880c38c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273838"
---
# <span data-ttu-id="6f65f-101">Get-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="6f65f-101">Get-AzStackEdgeRole</span></span>

## <span data-ttu-id="6f65f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f65f-102">SYNOPSIS</span></span>
<span data-ttu-id="6f65f-103">Cihaz için kullanılabilir rolleri getirir.</span><span class="sxs-lookup"><span data-stu-id="6f65f-103">Fetches the available roles for a device.</span></span>

## <span data-ttu-id="6f65f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6f65f-104">SYNTAX</span></span>

### <span data-ttu-id="6f65f-105">ListParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6f65f-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f65f-106">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="6f65f-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeRole -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f65f-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f65f-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f65f-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f65f-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeRole [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="6f65f-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="6f65f-109">DESCRIPTION</span></span>
<span data-ttu-id="6f65f-110">**Get-AzStackEdgeRole** cmdlet 'ı yığın uç aygıtı Için kullanılabilir IoT rollerini getirir.</span><span class="sxs-lookup"><span data-stu-id="6f65f-110">The **Get-AzStackEdgeRole** cmdlet fetches the available IoT roles for a Stack Edge device.</span></span> <span data-ttu-id="6f65f-111">Belirli bir IoT rolünün ayrıntılarını almak için Name parametresinden bahsedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6f65f-111">You can mention the Name parameter to get the details of a specific IoT role.</span></span>

## <span data-ttu-id="6f65f-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6f65f-112">EXAMPLES</span></span>

### <span data-ttu-id="6f65f-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6f65f-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

## <span data-ttu-id="6f65f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6f65f-114">PARAMETERS</span></span>

### <span data-ttu-id="6f65f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f65f-115">-DefaultProfile</span></span>
<span data-ttu-id="6f65f-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6f65f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f65f-117">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="6f65f-117">-DeviceName</span></span>
<span data-ttu-id="6f65f-118">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="6f65f-118">Device Name</span></span>

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

### <span data-ttu-id="6f65f-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="6f65f-119">-DeviceObject</span></span>
<span data-ttu-id="6f65f-120">Lütfen ilgili cihaz nesnesini sağlayın</span><span class="sxs-lookup"><span data-stu-id="6f65f-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="6f65f-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="6f65f-121">-Name</span></span>
<span data-ttu-id="6f65f-122">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="6f65f-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: RoleName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f65f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f65f-123">-ResourceGroupName</span></span>
<span data-ttu-id="6f65f-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="6f65f-124">Resource Group Name</span></span>

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

### <span data-ttu-id="6f65f-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6f65f-125">-ResourceId</span></span>
<span data-ttu-id="6f65f-126">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6f65f-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="6f65f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f65f-127">CommonParameters</span></span>
<span data-ttu-id="6f65f-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6f65f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f65f-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6f65f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f65f-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6f65f-130">INPUTS</span></span>

### <span data-ttu-id="6f65f-131">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="6f65f-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="6f65f-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6f65f-132">OUTPUTS</span></span>

### <span data-ttu-id="6f65f-133">Microsoft. Azure. PowerShell. cmdlet. StackEdge. model. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="6f65f-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="6f65f-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6f65f-134">NOTES</span></span>

## <span data-ttu-id="6f65f-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6f65f-135">RELATED LINKS</span></span>
