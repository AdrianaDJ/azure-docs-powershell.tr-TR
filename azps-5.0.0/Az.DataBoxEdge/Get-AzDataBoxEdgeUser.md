---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeUser.md
ms.openlocfilehash: cc03472aa71665a8612e17bfce6365a255f929bd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321206"
---
# <span data-ttu-id="996d8-101">Get-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="996d8-101">Get-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="996d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="996d8-102">SYNOPSIS</span></span>
<span data-ttu-id="996d8-103">Bir cihaz için yapılandırılmış kullanıcıları alır.</span><span class="sxs-lookup"><span data-stu-id="996d8-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="996d8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="996d8-104">SYNTAX</span></span>

### <span data-ttu-id="996d8-105">ListParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="996d8-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="996d8-106">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="996d8-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="996d8-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="996d8-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="996d8-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="996d8-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="996d8-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="996d8-109">DESCRIPTION</span></span>
<span data-ttu-id="996d8-110">**Get-AzDataBoxEdgeUser** cmdlet 'ı bir veri kutusu uç aygıtı için yapılandırılmış kullanıcıları listeler.</span><span class="sxs-lookup"><span data-stu-id="996d8-110">The **Get-AzDataBoxEdgeUser** cmdlet lists the users configured for a Data Box Edge device.</span></span> <span data-ttu-id="996d8-111">Belirli bir kullanıcının ayrıntılarını almak için parametrelerde adın bahsetmeye başlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="996d8-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="996d8-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="996d8-112">EXAMPLES</span></span>

### <span data-ttu-id="996d8-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="996d8-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="996d8-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="996d8-114">PARAMETERS</span></span>

### <span data-ttu-id="996d8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="996d8-115">-DefaultProfile</span></span>
<span data-ttu-id="996d8-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="996d8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="996d8-117">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="996d8-117">-DeviceName</span></span>
<span data-ttu-id="996d8-118">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="996d8-118">Device Name</span></span>

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

### <span data-ttu-id="996d8-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="996d8-119">-DeviceObject</span></span>
<span data-ttu-id="996d8-120">Lütfen ilgili cihaz nesnesini sağlayın</span><span class="sxs-lookup"><span data-stu-id="996d8-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="996d8-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="996d8-121">-Name</span></span>
<span data-ttu-id="996d8-122">Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="996d8-122">Username</span></span>

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

### <span data-ttu-id="996d8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="996d8-123">-ResourceGroupName</span></span>
<span data-ttu-id="996d8-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="996d8-124">Resource Group Name</span></span>

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

### <span data-ttu-id="996d8-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="996d8-125">-ResourceId</span></span>
<span data-ttu-id="996d8-126">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="996d8-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="996d8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="996d8-127">CommonParameters</span></span>
<span data-ttu-id="996d8-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="996d8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="996d8-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="996d8-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="996d8-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="996d8-130">INPUTS</span></span>

### <span data-ttu-id="996d8-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="996d8-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="996d8-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="996d8-132">OUTPUTS</span></span>

### <span data-ttu-id="996d8-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="996d8-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="996d8-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="996d8-134">NOTES</span></span>

## <span data-ttu-id="996d8-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="996d8-135">RELATED LINKS</span></span>
