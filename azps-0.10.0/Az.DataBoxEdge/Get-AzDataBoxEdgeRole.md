---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeRole.md
ms.openlocfilehash: 0af708265a66ecf05bfe4eb5de37d7b81a21aa3b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936789"
---
# <span data-ttu-id="684a9-101">Get-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="684a9-101">Get-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="684a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="684a9-102">SYNOPSIS</span></span>
<span data-ttu-id="684a9-103">Cihaz için kullanılabilir rolleri getirir.</span><span class="sxs-lookup"><span data-stu-id="684a9-103">Fetches the available roles for a device.</span></span>

## <span data-ttu-id="684a9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="684a9-104">SYNTAX</span></span>

### <span data-ttu-id="684a9-105">ListParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="684a9-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="684a9-106">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="684a9-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeRole -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="684a9-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="684a9-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="684a9-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="684a9-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeRole [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="684a9-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="684a9-109">DESCRIPTION</span></span>
<span data-ttu-id="684a9-110">**Get-AzDataBoxEdgeRole** cmdlet 'i, bir veri kutusu uç aygıtı Için kullanılabilir IoT rollerini getirir.</span><span class="sxs-lookup"><span data-stu-id="684a9-110">The **Get-AzDataBoxEdgeRole** cmdlet fetches the available IoT roles for a Data Box Edge device.</span></span> <span data-ttu-id="684a9-111">Belirli bir IoT rolünün ayrıntılarını almak için Name parametresinden bahsedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="684a9-111">You can mention the Name parameter to get the details of a specific IoT role.</span></span>

## <span data-ttu-id="684a9-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="684a9-112">EXAMPLES</span></span>

### <span data-ttu-id="684a9-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="684a9-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

## <span data-ttu-id="684a9-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="684a9-114">PARAMETERS</span></span>

### <span data-ttu-id="684a9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="684a9-115">-DefaultProfile</span></span>
<span data-ttu-id="684a9-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="684a9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="684a9-117">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="684a9-117">-DeviceName</span></span>
<span data-ttu-id="684a9-118">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="684a9-118">Device Name</span></span>

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

### <span data-ttu-id="684a9-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="684a9-119">-DeviceObject</span></span>
<span data-ttu-id="684a9-120">Lütfen ilgili cihaz nesnesini sağlayın</span><span class="sxs-lookup"><span data-stu-id="684a9-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="684a9-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="684a9-121">-Name</span></span>
<span data-ttu-id="684a9-122">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="684a9-122">Resource Name</span></span>

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

### <span data-ttu-id="684a9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="684a9-123">-ResourceGroupName</span></span>
<span data-ttu-id="684a9-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="684a9-124">Resource Group Name</span></span>

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

### <span data-ttu-id="684a9-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="684a9-125">-ResourceId</span></span>
<span data-ttu-id="684a9-126">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="684a9-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="684a9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="684a9-127">CommonParameters</span></span>
<span data-ttu-id="684a9-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="684a9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="684a9-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="684a9-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="684a9-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="684a9-130">INPUTS</span></span>

### <span data-ttu-id="684a9-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="684a9-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="684a9-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="684a9-132">OUTPUTS</span></span>

### <span data-ttu-id="684a9-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="684a9-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="684a9-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="684a9-134">NOTES</span></span>

## <span data-ttu-id="684a9-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="684a9-135">RELATED LINKS</span></span>
