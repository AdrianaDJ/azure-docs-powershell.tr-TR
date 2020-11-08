---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4F487FCA-930D-4D56-8D28-7693312E1A01
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteTable.md
ms.openlocfilehash: 613519f6d9d3d2d8ce1c83ff0ad5a2d9421859b8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098767"
---
# <span data-ttu-id="3746c-101">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="3746c-101">Get-AzRouteTable</span></span>

## <span data-ttu-id="3746c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3746c-102">SYNOPSIS</span></span>
<span data-ttu-id="3746c-103">Yol tablolarını alır.</span><span class="sxs-lookup"><span data-stu-id="3746c-103">Gets route tables.</span></span>

## <span data-ttu-id="3746c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3746c-104">SYNTAX</span></span>

### <span data-ttu-id="3746c-105">NoExpand (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3746c-105">NoExpand (Default)</span></span>
```
Get-AzRouteTable [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3746c-106">Geniþ</span><span class="sxs-lookup"><span data-stu-id="3746c-106">Expand</span></span>
```
Get-AzRouteTable -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3746c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3746c-107">DESCRIPTION</span></span>
<span data-ttu-id="3746c-108">**Get-AzRouteTable** cmdlet 'i Azure yol tablolarını alır.</span><span class="sxs-lookup"><span data-stu-id="3746c-108">The **Get-AzRouteTable** cmdlet gets Azure route tables.</span></span>
<span data-ttu-id="3746c-109">Tek bir yol tablosu alabilir veya kaynak grubundaki veya aboneliğinizdeki tüm yol tablolarını alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3746c-109">You can get a single route table, or get all the route tables in a resource group or in your subscription.</span></span>

## <span data-ttu-id="3746c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3746c-110">EXAMPLES</span></span>

### <span data-ttu-id="3746c-111">Örnek 1: yol tablosu alma</span><span class="sxs-lookup"><span data-stu-id="3746c-111">Example 1: Get a route table</span></span>
```
PS C:\> Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"

Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable01
Etag              : W/"db5f4e12-3f34-465b-92dd-0ab3bf6fc274"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"db5f4e12-3f34-465b-92dd-0ab3bf6fc274\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="3746c-112">Bu komut, ResourceGroup11 adındaki kaynak grubundaki RouteTable01 adındaki yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="3746c-112">This command gets the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="3746c-113">Örnek 2: filtreleme kullanarak yol tablolarını listeleme</span><span class="sxs-lookup"><span data-stu-id="3746c-113">Example 2: List route tables using filtering</span></span>
```
PS C:\> Get-AzRouteTable -Name RouteTable*

Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable01
Etag              : W/"db5f4e12-3f34-465b-92dd-0ab3bf6fc274"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"db5f4e12-3f34-465b-92dd-0ab3bf6fc274\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []

Name              : routetable02
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable02
Etag              : W/"db5f4e12-3f34-465b-92dd-0ab3bf6fc274"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"db5f4e12-3f34-465b-92dd-0ab3bf6fc274\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable02/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="3746c-114">Bu komut, adı "RouteTable" ile başlayan tüm yol tablolarını alır</span><span class="sxs-lookup"><span data-stu-id="3746c-114">This command gets all route tables whose name starts with "RouteTable"</span></span>

## <span data-ttu-id="3746c-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3746c-115">PARAMETERS</span></span>

### <span data-ttu-id="3746c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3746c-116">-DefaultProfile</span></span>
<span data-ttu-id="3746c-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3746c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3746c-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="3746c-118">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3746c-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="3746c-119">-Name</span></span>
<span data-ttu-id="3746c-120">Bu cmdlet 'in aldığı yol tablosunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3746c-120">Specifies the name of the route table that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="3746c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3746c-121">-ResourceGroupName</span></span>
<span data-ttu-id="3746c-122">Bu cmdlet 'in aldığı yol tablolarını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3746c-122">Specifies the name of the resource group that contains the route tables that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="3746c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3746c-123">CommonParameters</span></span>
<span data-ttu-id="3746c-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3746c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3746c-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3746c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3746c-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3746c-126">INPUTS</span></span>

### <span data-ttu-id="3746c-127">System. String</span><span class="sxs-lookup"><span data-stu-id="3746c-127">System.String</span></span>

## <span data-ttu-id="3746c-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3746c-128">OUTPUTS</span></span>

### <span data-ttu-id="3746c-129">Microsoft. Azure. Commands. Network. modeller. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="3746c-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="3746c-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3746c-130">NOTES</span></span>

## <span data-ttu-id="3746c-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3746c-131">RELATED LINKS</span></span>

[<span data-ttu-id="3746c-132">Yeni-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="3746c-132">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="3746c-133">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="3746c-133">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="3746c-134">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="3746c-134">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


