---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4F487FCA-930D-4D56-8D28-7693312E1A01
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteTable.md
ms.openlocfilehash: a881e438166729aea8956dc633b7a635499d3752
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935482"
---
# <span data-ttu-id="1c294-101">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="1c294-101">Get-AzRouteTable</span></span>

## <span data-ttu-id="1c294-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c294-102">SYNOPSIS</span></span>
<span data-ttu-id="1c294-103">Yol tablolarını alır.</span><span class="sxs-lookup"><span data-stu-id="1c294-103">Gets route tables.</span></span>

## <span data-ttu-id="1c294-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1c294-104">SYNTAX</span></span>

### <span data-ttu-id="1c294-105">Geniþ</span><span class="sxs-lookup"><span data-stu-id="1c294-105">Expand</span></span>
```
Get-AzRouteTable -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c294-106">NoExpand</span><span class="sxs-lookup"><span data-stu-id="1c294-106">NoExpand</span></span>
```
Get-AzRouteTable [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1c294-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1c294-107">DESCRIPTION</span></span>
<span data-ttu-id="1c294-108">**Get-AzRouteTable** cmdlet 'i Azure yol tablolarını alır.</span><span class="sxs-lookup"><span data-stu-id="1c294-108">The **Get-AzRouteTable** cmdlet gets Azure route tables.</span></span>
<span data-ttu-id="1c294-109">Tek bir yol tablosu alabilir veya kaynak grubundaki veya aboneliğinizdeki tüm yol tablolarını alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1c294-109">You can get a single route table, or get all the route tables in a resource group or in your subscription.</span></span>

## <span data-ttu-id="1c294-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1c294-110">EXAMPLES</span></span>

### <span data-ttu-id="1c294-111">Örnek 1: yol tablosu alma</span><span class="sxs-lookup"><span data-stu-id="1c294-111">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
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

<span data-ttu-id="1c294-112">Bu komut, ResourceGroup11 adındaki kaynak grubundaki RouteTable01 adındaki yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="1c294-112">This command gets the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="1c294-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1c294-113">PARAMETERS</span></span>

### <span data-ttu-id="1c294-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c294-114">-DefaultProfile</span></span>
<span data-ttu-id="1c294-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1c294-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c294-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="1c294-116">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c294-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="1c294-117">-Name</span></span>
<span data-ttu-id="1c294-118">Bu cmdlet 'in aldığı yol tablosunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c294-118">Specifies the name of the route table that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c294-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c294-119">-ResourceGroupName</span></span>
<span data-ttu-id="1c294-120">Bu cmdlet 'in aldığı yol tablolarını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c294-120">Specifies the name of the resource group that contains the route tables that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c294-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c294-121">CommonParameters</span></span>
<span data-ttu-id="1c294-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1c294-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c294-123">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c294-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c294-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1c294-124">INPUTS</span></span>

## <span data-ttu-id="1c294-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1c294-125">OUTPUTS</span></span>

### <span data-ttu-id="1c294-126">Microsoft. Azure. Commands. Network. modeller. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="1c294-126">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="1c294-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1c294-127">NOTES</span></span>

## <span data-ttu-id="1c294-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1c294-128">RELATED LINKS</span></span>

[<span data-ttu-id="1c294-129">Yeni-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="1c294-129">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="1c294-130">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="1c294-130">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="1c294-131">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="1c294-131">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


