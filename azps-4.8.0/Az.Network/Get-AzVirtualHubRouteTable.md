---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubRouteTable.md
ms.openlocfilehash: bc93ba739a622a97f418dd7e01d4bbdc7d6824dc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266523"
---
# <span data-ttu-id="299b8-101">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="299b8-101">Get-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="299b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="299b8-102">SYNOPSIS</span></span>
<span data-ttu-id="299b8-103">Sanal hub 'da sanal hub yol tablosunu alır veya sanal bir hub 'daki tüm yol tablolarını listeler.</span><span class="sxs-lookup"><span data-stu-id="299b8-103">Gets a Virtual Hub Route Table in a virtual hub or lists all route tables in a virtual hub.</span></span>

## <span data-ttu-id="299b8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="299b8-104">SYNTAX</span></span>

### <span data-ttu-id="299b8-105">ByVirtualHubName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="299b8-105">ByVirtualHubName (Default)</span></span>
```
Get-AzVirtualHubRouteTable -ResourceGroupName <String> -HubName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="299b8-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="299b8-106">ByVirtualHubObject</span></span>
```
Get-AzVirtualHubRouteTable -VirtualHub <PSVirtualHub> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="299b8-107">Byvirtualhubresourceıd</span><span class="sxs-lookup"><span data-stu-id="299b8-107">ByVirtualHubResourceId</span></span>
```
Get-AzVirtualHubRouteTable -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="299b8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="299b8-108">DESCRIPTION</span></span>
<span data-ttu-id="299b8-109">Sanal hub 'da sanal hub yol tablosunu alır veya sanal bir hub 'daki tüm yol tablolarını listeler.</span><span class="sxs-lookup"><span data-stu-id="299b8-109">Gets a Virtual Hub Route Table in a virtual hub or lists all route tables in a virtual hub.</span></span>

## <span data-ttu-id="299b8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="299b8-110">EXAMPLES</span></span>

### <span data-ttu-id="299b8-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="299b8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"�-Name�"routeTable1"

Name                : routeTable1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/routeTables/routeTable1
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   : Succeeded
```

<span data-ttu-id="299b8-112">Bu cmdlet, kaynak grubu adı, hub adı ve yol tablosu adını kullanarak bir yol tablosu kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="299b8-112">This cmdlet retrieves a route table resource using resource group name, hub name and the route table name.</span></span>

### <span data-ttu-id="299b8-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="299b8-113">Example 2</span></span>
```powershell
PS C:\> Get-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"

Name                : routeTable1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/routeTables/routeTable1
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   : Succeeded

Name                : routeTable2
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/routeTables/routeTable2
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Branches}
ProvisioningState   : Succeeded
```

<span data-ttu-id="299b8-114">Bu cmdlet, kaynak grup adını ve hub adını kullanarak sanal bir hub 'daki tüm yol tablolarını listeler.</span><span class="sxs-lookup"><span data-stu-id="299b8-114">This cmdlet lists all route tables present in a virtual hub using resource group name and the hub name.</span></span>

## <span data-ttu-id="299b8-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="299b8-115">PARAMETERS</span></span>

### <span data-ttu-id="299b8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="299b8-116">-DefaultProfile</span></span>
<span data-ttu-id="299b8-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="299b8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="299b8-118">-HubName</span><span class="sxs-lookup"><span data-stu-id="299b8-118">-HubName</span></span>
<span data-ttu-id="299b8-119">Üst kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="299b8-119">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases: VirtualHubName, ParentVirtualHubName, ParentResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="299b8-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="299b8-120">-Name</span></span>
<span data-ttu-id="299b8-121">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="299b8-121">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VirtualHubRouteTableName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="299b8-122">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="299b8-122">-ParentResourceId</span></span>
<span data-ttu-id="299b8-123">Üst kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="299b8-123">The parent resource id.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="299b8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="299b8-124">-ResourceGroupName</span></span>
<span data-ttu-id="299b8-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="299b8-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="299b8-126">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="299b8-126">-VirtualHub</span></span>
<span data-ttu-id="299b8-127">Üst kaynak.</span><span class="sxs-lookup"><span data-stu-id="299b8-127">The parent resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentObject, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="299b8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="299b8-128">CommonParameters</span></span>
<span data-ttu-id="299b8-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="299b8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="299b8-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="299b8-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="299b8-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="299b8-131">INPUTS</span></span>

### <span data-ttu-id="299b8-132">Microsoft. Azure. Commands. Network. modeller. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="299b8-132">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="299b8-133">System. String</span><span class="sxs-lookup"><span data-stu-id="299b8-133">System.String</span></span>

## <span data-ttu-id="299b8-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="299b8-134">OUTPUTS</span></span>

### <span data-ttu-id="299b8-135">Microsoft. Azure. Commands. Network. modeller. PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="299b8-135">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="299b8-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="299b8-136">NOTES</span></span>

## <span data-ttu-id="299b8-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="299b8-137">RELATED LINKS</span></span>
