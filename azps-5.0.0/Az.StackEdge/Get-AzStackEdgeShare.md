---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeShare.md
ms.openlocfilehash: 0e0d0e3b2dfca824d66a9a75f3e22438335c97db
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276944"
---
# <span data-ttu-id="8a9d7-101">Get-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="8a9d7-101">Get-AzStackEdgeShare</span></span>

## <span data-ttu-id="8a9d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a9d7-102">SYNOPSIS</span></span>
<span data-ttu-id="8a9d7-103">Aygıtın kullanılabilir paylaşımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="8a9d7-103">Gets the available shares for a device.</span></span>

## <span data-ttu-id="8a9d7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8a9d7-104">SYNTAX</span></span>

### <span data-ttu-id="8a9d7-105">ListParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8a9d7-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a9d7-106">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="8a9d7-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a9d7-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a9d7-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a9d7-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a9d7-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeShare [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="8a9d7-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="8a9d7-109">DESCRIPTION</span></span>
<span data-ttu-id="8a9d7-110">**Get-Azstackedgesshares** cmdlet 'ı, yığın uç aygıtının kullanılabilir paylaşımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="8a9d7-110">The **Get-AzStackEdgeShare** cmdlet gets the available shares for a Stack Edge device.</span></span> <span data-ttu-id="8a9d7-111">Ad sağlanmışsa, paylaşım adına göre paylaşım alır.</span><span class="sxs-lookup"><span data-stu-id="8a9d7-111">If Name is provided this will get the share by Name.</span></span>

## <span data-ttu-id="8a9d7-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8a9d7-112">EXAMPLES</span></span>

### <span data-ttu-id="8a9d7-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8a9d7-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-2    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-3    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-4    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="8a9d7-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8a9d7-114">PARAMETERS</span></span>

### <span data-ttu-id="8a9d7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a9d7-115">-DefaultProfile</span></span>
<span data-ttu-id="8a9d7-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8a9d7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a9d7-117">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="8a9d7-117">-DeviceName</span></span>
<span data-ttu-id="8a9d7-118">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="8a9d7-118">Device Name</span></span>

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

### <span data-ttu-id="8a9d7-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="8a9d7-119">-DeviceObject</span></span>
<span data-ttu-id="8a9d7-120">Lütfen ilgili cihaz nesnesini sağlayın</span><span class="sxs-lookup"><span data-stu-id="8a9d7-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="8a9d7-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="8a9d7-121">-Name</span></span>
<span data-ttu-id="8a9d7-122">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="8a9d7-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeShareName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a9d7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a9d7-123">-ResourceGroupName</span></span>
<span data-ttu-id="8a9d7-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="8a9d7-124">Resource Group Name</span></span>

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

### <span data-ttu-id="8a9d7-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8a9d7-125">-ResourceId</span></span>
<span data-ttu-id="8a9d7-126">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8a9d7-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="8a9d7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a9d7-127">CommonParameters</span></span>
<span data-ttu-id="8a9d7-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8a9d7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a9d7-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8a9d7-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a9d7-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8a9d7-130">INPUTS</span></span>

### <span data-ttu-id="8a9d7-131">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="8a9d7-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="8a9d7-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8a9d7-132">OUTPUTS</span></span>

### <span data-ttu-id="8a9d7-133">Microsoft. Azure. PowerShell. cmdlet. yığın</span><span class="sxs-lookup"><span data-stu-id="8a9d7-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="8a9d7-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8a9d7-134">NOTES</span></span>

## <span data-ttu-id="8a9d7-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8a9d7-135">RELATED LINKS</span></span>
