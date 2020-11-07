---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4F487FCA-930D-4D56-8D28-7693312E1A01
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteTable.md
ms.openlocfilehash: fb675f1d834160bd1fcf5e2dde60dc00e697d629
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762763"
---
# <span data-ttu-id="03e84-101">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="03e84-101">Get-AzureRmRouteTable</span></span>

## <span data-ttu-id="03e84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03e84-102">SYNOPSIS</span></span>
<span data-ttu-id="03e84-103">Yol tablolarını alır.</span><span class="sxs-lookup"><span data-stu-id="03e84-103">Gets route tables.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03e84-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="03e84-104">SYNTAX</span></span>

### <span data-ttu-id="03e84-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="03e84-105">NoExpand</span></span>
```
Get-AzureRmRouteTable [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="03e84-106">Geniþ</span><span class="sxs-lookup"><span data-stu-id="03e84-106">Expand</span></span>
```
Get-AzureRmRouteTable -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03e84-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="03e84-107">DESCRIPTION</span></span>
<span data-ttu-id="03e84-108">**Get-AzureRmRouteTable** cmdlet 'i Azure yol tablolarını alır.</span><span class="sxs-lookup"><span data-stu-id="03e84-108">The **Get-AzureRmRouteTable** cmdlet gets Azure route tables.</span></span>
<span data-ttu-id="03e84-109">Tek bir yol tablosu alabilir veya kaynak grubundaki veya aboneliğinizdeki tüm yol tablolarını alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="03e84-109">You can get a single route table, or get all the route tables in a resource group or in your subscription.</span></span>

## <span data-ttu-id="03e84-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="03e84-110">EXAMPLES</span></span>

### <span data-ttu-id="03e84-111">Örnek 1: yol tablosu alma</span><span class="sxs-lookup"><span data-stu-id="03e84-111">Example 1: Get a route table</span></span>
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

<span data-ttu-id="03e84-112">Bu komut, ResourceGroup11 adındaki kaynak grubundaki RouteTable01 adındaki yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="03e84-112">This command gets the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="03e84-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="03e84-113">PARAMETERS</span></span>

### <span data-ttu-id="03e84-114">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="03e84-114">-ExpandResource</span></span>
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

### <span data-ttu-id="03e84-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="03e84-115">-Name</span></span>
<span data-ttu-id="03e84-116">Bu cmdlet 'in aldığı yol tablosunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="03e84-116">Specifies the name of the route table that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03e84-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03e84-117">-ResourceGroupName</span></span>
<span data-ttu-id="03e84-118">Bu cmdlet 'in aldığı yol tablolarını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="03e84-118">Specifies the name of the resource group that contains the route tables that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="03e84-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03e84-119">-DefaultProfile</span></span>
<span data-ttu-id="03e84-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="03e84-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03e84-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03e84-121">CommonParameters</span></span>
<span data-ttu-id="03e84-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="03e84-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03e84-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03e84-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03e84-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="03e84-124">INPUTS</span></span>

## <span data-ttu-id="03e84-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="03e84-125">OUTPUTS</span></span>

### <span data-ttu-id="03e84-126">Microsoft. Azure. Commands. Network. modeller. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="03e84-126">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="03e84-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="03e84-127">NOTES</span></span>

## <span data-ttu-id="03e84-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="03e84-128">RELATED LINKS</span></span>

[<span data-ttu-id="03e84-129">Yeni-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="03e84-129">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="03e84-130">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="03e84-130">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="03e84-131">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="03e84-131">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)

