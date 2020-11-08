---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeUser.md
ms.openlocfilehash: 0ab290934a956282a16d9e2321b2c5ed948f33af
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936781"
---
# <span data-ttu-id="6fb34-101">Get-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="6fb34-101">Get-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="6fb34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fb34-102">SYNOPSIS</span></span>
<span data-ttu-id="6fb34-103">Bir cihaz için yapılandırılmış kullanıcıları alır.</span><span class="sxs-lookup"><span data-stu-id="6fb34-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="6fb34-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6fb34-104">SYNTAX</span></span>

### <span data-ttu-id="6fb34-105">ListParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6fb34-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fb34-106">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="6fb34-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fb34-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fb34-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fb34-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fb34-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="6fb34-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="6fb34-109">DESCRIPTION</span></span>
<span data-ttu-id="6fb34-110">**Get-AzDataBoxEdgeUser** cmdlet 'ı bir veri kutusu uç aygıtı için yapılandırılmış kullanıcıları listeler.</span><span class="sxs-lookup"><span data-stu-id="6fb34-110">The **Get-AzDataBoxEdgeUser** cmdlet lists the users configured for a Data Box Edge device.</span></span> <span data-ttu-id="6fb34-111">Belirli bir kullanıcının ayrıntılarını almak için parametrelerde adın bahsetmeye başlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6fb34-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="6fb34-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6fb34-112">EXAMPLES</span></span>

### <span data-ttu-id="6fb34-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6fb34-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="6fb34-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6fb34-114">PARAMETERS</span></span>

### <span data-ttu-id="6fb34-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fb34-115">-DefaultProfile</span></span>
<span data-ttu-id="6fb34-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6fb34-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fb34-117">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="6fb34-117">-DeviceName</span></span>
<span data-ttu-id="6fb34-118">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="6fb34-118">Device Name</span></span>

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

### <span data-ttu-id="6fb34-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="6fb34-119">-DeviceObject</span></span>
<span data-ttu-id="6fb34-120">Lütfen ilgili cihaz nesnesini sağlayın</span><span class="sxs-lookup"><span data-stu-id="6fb34-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="6fb34-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="6fb34-121">-Name</span></span>
<span data-ttu-id="6fb34-122">Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="6fb34-122">Username</span></span>

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

### <span data-ttu-id="6fb34-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fb34-123">-ResourceGroupName</span></span>
<span data-ttu-id="6fb34-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="6fb34-124">Resource Group Name</span></span>

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

### <span data-ttu-id="6fb34-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6fb34-125">-ResourceId</span></span>
<span data-ttu-id="6fb34-126">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6fb34-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="6fb34-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fb34-127">CommonParameters</span></span>
<span data-ttu-id="6fb34-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6fb34-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fb34-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6fb34-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fb34-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6fb34-130">INPUTS</span></span>

### <span data-ttu-id="6fb34-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="6fb34-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="6fb34-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6fb34-132">OUTPUTS</span></span>

### <span data-ttu-id="6fb34-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="6fb34-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="6fb34-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6fb34-134">NOTES</span></span>

## <span data-ttu-id="6fb34-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6fb34-135">RELATED LINKS</span></span>