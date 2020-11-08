---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
ms.openlocfilehash: 238290778d47de673f9db89280f500c2fc31ea28
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096531"
---
# <span data-ttu-id="5f0e3-101">Get-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="5f0e3-101">Get-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="5f0e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f0e3-102">SYNOPSIS</span></span>
<span data-ttu-id="5f0e3-103">Cihazda yapılandırılmış tetikleri alma</span><span class="sxs-lookup"><span data-stu-id="5f0e3-103">Get the Triggers configured on a device</span></span>
 

## <span data-ttu-id="5f0e3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5f0e3-104">SYNTAX</span></span>

### <span data-ttu-id="5f0e3-105">ListParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5f0e3-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f0e3-106">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="5f0e3-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f0e3-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f0e3-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f0e3-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f0e3-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeTrigger [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="5f0e3-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="5f0e3-109">DESCRIPTION</span></span>
<span data-ttu-id="5f0e3-110">**Get-AzStackEdgeTriger** cmdlet 'i bir cihazın tetikleyicilerini alır.</span><span class="sxs-lookup"><span data-stu-id="5f0e3-110">The **Get-AzStackEdgeTriger** cmdlet gets the triggers for a device.</span></span> <span data-ttu-id="5f0e3-111">Belirli bir tetikleyicilerin ayrıntılarını getirmek için cmdlet 'teki adı bir parametre olarak belirtebilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5f0e3-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific  specific Triggers</span></span>
 

## <span data-ttu-id="5f0e3-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5f0e3-112">EXAMPLES</span></span>

### <span data-ttu-id="5f0e3-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5f0e3-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                  Kind               
----                  ----               
triggerName          PeriodicTimerEvent
```

## <span data-ttu-id="5f0e3-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5f0e3-114">PARAMETERS</span></span>

### <span data-ttu-id="5f0e3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f0e3-115">-DefaultProfile</span></span>
<span data-ttu-id="5f0e3-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5f0e3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f0e3-117">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="5f0e3-117">-DeviceName</span></span>
<span data-ttu-id="5f0e3-118">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="5f0e3-118">Device Name</span></span>

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

### <span data-ttu-id="5f0e3-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="5f0e3-119">-DeviceObject</span></span>
<span data-ttu-id="5f0e3-120">Lütfen ilgili cihaz nesnesini sağlayın</span><span class="sxs-lookup"><span data-stu-id="5f0e3-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="5f0e3-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="5f0e3-121">-Name</span></span>
<span data-ttu-id="5f0e3-122">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="5f0e3-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f0e3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f0e3-123">-ResourceGroupName</span></span>
<span data-ttu-id="5f0e3-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="5f0e3-124">Resource Group Name</span></span>

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

### <span data-ttu-id="5f0e3-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5f0e3-125">-ResourceId</span></span>
<span data-ttu-id="5f0e3-126">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5f0e3-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="5f0e3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f0e3-127">CommonParameters</span></span>
<span data-ttu-id="5f0e3-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5f0e3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f0e3-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5f0e3-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f0e3-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5f0e3-130">INPUTS</span></span>

### <span data-ttu-id="5f0e3-131">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="5f0e3-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="5f0e3-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5f0e3-132">OUTPUTS</span></span>

### <span data-ttu-id="5f0e3-133">Microsoft. Azure. PowerShell. cmdlet. StackEdge. model. PSStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="5f0e3-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="5f0e3-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5f0e3-134">NOTES</span></span>

## <span data-ttu-id="5f0e3-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5f0e3-135">RELATED LINKS</span></span>