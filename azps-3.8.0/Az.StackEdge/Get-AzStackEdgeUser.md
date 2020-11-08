---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
ms.openlocfilehash: 3a9945d94b1aec3e82d4d79d09df0bacb3b3a11d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096530"
---
# <span data-ttu-id="bcccc-101">Get-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="bcccc-101">Get-AzStackEdgeUser</span></span>

## <span data-ttu-id="bcccc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcccc-102">SYNOPSIS</span></span>
<span data-ttu-id="bcccc-103">Bir cihaz için yapılandırılmış kullanıcıları alır.</span><span class="sxs-lookup"><span data-stu-id="bcccc-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="bcccc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bcccc-104">SYNTAX</span></span>

### <span data-ttu-id="bcccc-105">ListParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bcccc-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcccc-106">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="bcccc-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcccc-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcccc-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcccc-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcccc-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="bcccc-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="bcccc-109">DESCRIPTION</span></span>
<span data-ttu-id="bcccc-110">**Get-AzStackEdgeUser** cmdlet 'ı yığın uç aygıtı için yapılandırılmış kullanıcıları listeler.</span><span class="sxs-lookup"><span data-stu-id="bcccc-110">The **Get-AzStackEdgeUser** cmdlet lists the users configured for a Stack Edge device.</span></span> <span data-ttu-id="bcccc-111">Belirli bir kullanıcının ayrıntılarını almak için parametrelerde adın bahsetmeye başlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bcccc-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="bcccc-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bcccc-112">EXAMPLES</span></span>

### <span data-ttu-id="bcccc-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bcccc-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="bcccc-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bcccc-114">PARAMETERS</span></span>

### <span data-ttu-id="bcccc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcccc-115">-DefaultProfile</span></span>
<span data-ttu-id="bcccc-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bcccc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcccc-117">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="bcccc-117">-DeviceName</span></span>
<span data-ttu-id="bcccc-118">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="bcccc-118">Device Name</span></span>

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

### <span data-ttu-id="bcccc-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="bcccc-119">-DeviceObject</span></span>
<span data-ttu-id="bcccc-120">Lütfen ilgili cihaz nesnesini sağlayın</span><span class="sxs-lookup"><span data-stu-id="bcccc-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="bcccc-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="bcccc-121">-Name</span></span>
<span data-ttu-id="bcccc-122">Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="bcccc-122">Username</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: Username

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcccc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcccc-123">-ResourceGroupName</span></span>
<span data-ttu-id="bcccc-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="bcccc-124">Resource Group Name</span></span>

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

### <span data-ttu-id="bcccc-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="bcccc-125">-ResourceId</span></span>
<span data-ttu-id="bcccc-126">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="bcccc-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="bcccc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcccc-127">CommonParameters</span></span>
<span data-ttu-id="bcccc-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bcccc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcccc-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bcccc-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcccc-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bcccc-130">INPUTS</span></span>

### <span data-ttu-id="bcccc-131">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="bcccc-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="bcccc-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bcccc-132">OUTPUTS</span></span>

### <span data-ttu-id="bcccc-133">Microsoft. Azure. PowerShell. cmdlet. StackEdge. model. PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="bcccc-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="bcccc-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bcccc-134">NOTES</span></span>

## <span data-ttu-id="bcccc-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bcccc-135">RELATED LINKS</span></span>