---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 40cd719a374d5ec2fdaacfe616884b395bd24434
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936794"
---
# <span data-ttu-id="a754b-101">Get-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="a754b-101">Get-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="a754b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a754b-102">SYNOPSIS</span></span>
<span data-ttu-id="a754b-103">Cihazın sipariş ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="a754b-103">Get the order details for a device</span></span>

## <span data-ttu-id="a754b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a754b-104">SYNTAX</span></span>

### <span data-ttu-id="a754b-105">GetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a754b-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a754b-106">GetByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a754b-106">GetByDeviceObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeOrder -DeviceObject <PSDataBoxEdgeDevice> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a754b-107">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="a754b-107">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeOrder -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a754b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a754b-108">DESCRIPTION</span></span>
<span data-ttu-id="a754b-109">**Get-AzDataBoxEdgeOrder** cmdlet 'ı bir veri kutusu kenarı aygıtının sipariş ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="a754b-109">The **Get-AzDataBoxEdgeOrder** cmdlet gets the order details for a Data Box Edge device.</span></span> 

## <span data-ttu-id="a754b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a754b-110">EXAMPLES</span></span>

### <span data-ttu-id="a754b-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a754b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="a754b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a754b-112">PARAMETERS</span></span>

### <span data-ttu-id="a754b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a754b-113">-DefaultProfile</span></span>
<span data-ttu-id="a754b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a754b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a754b-115">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="a754b-115">-DeviceName</span></span>
<span data-ttu-id="a754b-116">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="a754b-116">Resource Group Name</span></span>

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

### <span data-ttu-id="a754b-117">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="a754b-117">-DeviceObject</span></span>
<span data-ttu-id="a754b-118">Lütfen ilgili cihaz nesnesini sağlayın</span><span class="sxs-lookup"><span data-stu-id="a754b-118">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a754b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a754b-119">-ResourceGroupName</span></span>
<span data-ttu-id="a754b-120">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="a754b-120">Resource Group Name</span></span>

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

### <span data-ttu-id="a754b-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a754b-121">-ResourceId</span></span>
<span data-ttu-id="a754b-122">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a754b-122">Azure ResourceId</span></span>

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

### <span data-ttu-id="a754b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a754b-123">CommonParameters</span></span>
<span data-ttu-id="a754b-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a754b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a754b-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a754b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a754b-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a754b-126">INPUTS</span></span>

### <span data-ttu-id="a754b-127">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="a754b-127">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

### <span data-ttu-id="a754b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a754b-128">System.String</span></span>

## <span data-ttu-id="a754b-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a754b-129">OUTPUTS</span></span>

### <span data-ttu-id="a754b-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="a754b-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="a754b-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a754b-131">NOTES</span></span>

## <span data-ttu-id="a754b-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a754b-132">RELATED LINKS</span></span>
