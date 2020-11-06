---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4F487FCA-930D-4D56-8D28-7693312E1A01
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteTable.md
ms.openlocfilehash: 04e50033a304918eb37d28c2ef5ea5328d5744c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590163"
---
# <span data-ttu-id="4e97c-101">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="4e97c-101">Get-AzureRmRouteTable</span></span>

## <span data-ttu-id="4e97c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e97c-102">SYNOPSIS</span></span>
<span data-ttu-id="4e97c-103">Yol tablolarını alır.</span><span class="sxs-lookup"><span data-stu-id="4e97c-103">Gets route tables.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e97c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4e97c-104">SYNTAX</span></span>

### <span data-ttu-id="4e97c-105">NoExpand (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4e97c-105">NoExpand (Default)</span></span>
```
Get-AzureRmRouteTable [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4e97c-106">Geniþ</span><span class="sxs-lookup"><span data-stu-id="4e97c-106">Expand</span></span>
```
Get-AzureRmRouteTable -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e97c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4e97c-107">DESCRIPTION</span></span>
<span data-ttu-id="4e97c-108">**Get-AzureRmRouteTable** cmdlet 'i Azure yol tablolarını alır.</span><span class="sxs-lookup"><span data-stu-id="4e97c-108">The **Get-AzureRmRouteTable** cmdlet gets Azure route tables.</span></span>
<span data-ttu-id="4e97c-109">Tek bir yol tablosu alabilir veya kaynak grubundaki veya aboneliğinizdeki tüm yol tablolarını alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4e97c-109">You can get a single route table, or get all the route tables in a resource group or in your subscription.</span></span>

## <span data-ttu-id="4e97c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4e97c-110">EXAMPLES</span></span>

### <span data-ttu-id="4e97c-111">Örnek 1: yol tablosu alma</span><span class="sxs-lookup"><span data-stu-id="4e97c-111">Example 1: Get a route table</span></span>
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

<span data-ttu-id="4e97c-112">Bu komut, ResourceGroup11 adındaki kaynak grubundaki RouteTable01 adındaki yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="4e97c-112">This command gets the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="4e97c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4e97c-113">PARAMETERS</span></span>

### <span data-ttu-id="4e97c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e97c-114">-DefaultProfile</span></span>
<span data-ttu-id="4e97c-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4e97c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e97c-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="4e97c-116">-ExpandResource</span></span>
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

### <span data-ttu-id="4e97c-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="4e97c-117">-Name</span></span>
<span data-ttu-id="4e97c-118">Bu cmdlet 'in aldığı yol tablosunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e97c-118">Specifies the name of the route table that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4e97c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e97c-119">-ResourceGroupName</span></span>
<span data-ttu-id="4e97c-120">Bu cmdlet 'in aldığı yol tablolarını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e97c-120">Specifies the name of the resource group that contains the route tables that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4e97c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e97c-121">CommonParameters</span></span>
<span data-ttu-id="4e97c-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4e97c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e97c-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e97c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e97c-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4e97c-124">INPUTS</span></span>

### <span data-ttu-id="4e97c-125">System. String</span><span class="sxs-lookup"><span data-stu-id="4e97c-125">System.String</span></span>

## <span data-ttu-id="4e97c-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4e97c-126">OUTPUTS</span></span>

### <span data-ttu-id="4e97c-127">Microsoft. Azure. Commands. Network. modeller. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="4e97c-127">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="4e97c-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4e97c-128">NOTES</span></span>

## <span data-ttu-id="4e97c-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4e97c-129">RELATED LINKS</span></span>

[<span data-ttu-id="4e97c-130">Yeni-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="4e97c-130">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="4e97c-131">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="4e97c-131">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="4e97c-132">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="4e97c-132">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)


