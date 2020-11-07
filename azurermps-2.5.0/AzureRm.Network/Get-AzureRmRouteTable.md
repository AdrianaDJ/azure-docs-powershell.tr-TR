---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4F487FCA-930D-4D56-8D28-7693312E1A01
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutetable
schema: 2.0.0
ms.openlocfilehash: 9498b93d2062bc84d6af423c89eb351c6680eddd
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938947"
---
# <span data-ttu-id="1a9b2-101">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="1a9b2-101">Get-AzureRmRouteTable</span></span>

## <span data-ttu-id="1a9b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a9b2-102">SYNOPSIS</span></span>
<span data-ttu-id="1a9b2-103">Yol tablolarını alır.</span><span class="sxs-lookup"><span data-stu-id="1a9b2-103">Gets route tables.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a9b2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1a9b2-104">SYNTAX</span></span>

### <span data-ttu-id="1a9b2-105">Geniþ</span><span class="sxs-lookup"><span data-stu-id="1a9b2-105">Expand</span></span>
```
Get-AzureRmRouteTable -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a9b2-106">NoExpand</span><span class="sxs-lookup"><span data-stu-id="1a9b2-106">NoExpand</span></span>
```
Get-AzureRmRouteTable [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1a9b2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1a9b2-107">DESCRIPTION</span></span>
<span data-ttu-id="1a9b2-108">**Get-AzureRmRouteTable** cmdlet 'i Azure yol tablolarını alır.</span><span class="sxs-lookup"><span data-stu-id="1a9b2-108">The **Get-AzureRmRouteTable** cmdlet gets Azure route tables.</span></span>
<span data-ttu-id="1a9b2-109">Tek bir yol tablosu alabilir veya kaynak grubundaki veya aboneliğinizdeki tüm yol tablolarını alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1a9b2-109">You can get a single route table, or get all the route tables in a resource group or in your subscription.</span></span>

## <span data-ttu-id="1a9b2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1a9b2-110">EXAMPLES</span></span>

### <span data-ttu-id="1a9b2-111">Örnek 1: yol tablosu alma</span><span class="sxs-lookup"><span data-stu-id="1a9b2-111">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
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

<span data-ttu-id="1a9b2-112">Bu komut, ResourceGroup11 adındaki kaynak grubundaki RouteTable01 adındaki yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="1a9b2-112">This command gets the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="1a9b2-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1a9b2-113">PARAMETERS</span></span>

### <span data-ttu-id="1a9b2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a9b2-114">-DefaultProfile</span></span>
<span data-ttu-id="1a9b2-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1a9b2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a9b2-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="1a9b2-116">-ExpandResource</span></span>
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

### <span data-ttu-id="1a9b2-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="1a9b2-117">-Name</span></span>
<span data-ttu-id="1a9b2-118">Bu cmdlet 'in aldığı yol tablosunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a9b2-118">Specifies the name of the route table that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1a9b2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a9b2-119">-ResourceGroupName</span></span>
<span data-ttu-id="1a9b2-120">Bu cmdlet 'in aldığı yol tablolarını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a9b2-120">Specifies the name of the resource group that contains the route tables that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1a9b2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a9b2-121">CommonParameters</span></span>
<span data-ttu-id="1a9b2-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1a9b2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a9b2-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a9b2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a9b2-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1a9b2-124">INPUTS</span></span>

## <span data-ttu-id="1a9b2-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1a9b2-125">OUTPUTS</span></span>

### <span data-ttu-id="1a9b2-126">Microsoft. Azure. Commands. Network. modeller. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="1a9b2-126">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="1a9b2-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1a9b2-127">NOTES</span></span>

## <span data-ttu-id="1a9b2-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1a9b2-128">RELATED LINKS</span></span>

[<span data-ttu-id="1a9b2-129">Yeni-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="1a9b2-129">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="1a9b2-130">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="1a9b2-130">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="1a9b2-131">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="1a9b2-131">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)


