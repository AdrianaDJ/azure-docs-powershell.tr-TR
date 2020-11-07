---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
ms.openlocfilehash: 59f8b74a9815820b1ace1e9d7defeb5b9dd85efa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931986"
---
# <span data-ttu-id="e0893-101">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e0893-101">Get-AzPrivateEndpoint</span></span>

## <span data-ttu-id="e0893-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0893-102">SYNOPSIS</span></span>
<span data-ttu-id="e0893-103">Özel uç nokta alma</span><span class="sxs-lookup"><span data-stu-id="e0893-103">Get a private endpoint</span></span>

## <span data-ttu-id="e0893-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e0893-104">SYNTAX</span></span>

### <span data-ttu-id="e0893-105">NoExpand (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e0893-105">NoExpand (Default)</span></span>
```
Get-AzPrivateEndpoint [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e0893-106">Geniþ</span><span class="sxs-lookup"><span data-stu-id="e0893-106">Expand</span></span>
```
Get-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0893-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e0893-107">DESCRIPTION</span></span>
<span data-ttu-id="e0893-108">**Get-AzPrivateEndpoint** cmdlet 'i bir veya daha çok özel uç nokta alır.</span><span class="sxs-lookup"><span data-stu-id="e0893-108">The **Get-AzPrivateEndpoint** cmdlet gets one or more private endpoints.</span></span>

## <span data-ttu-id="e0893-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e0893-109">EXAMPLES</span></span>

### <span data-ttu-id="e0893-110">1: özel uç nokta alma</span><span class="sxs-lookup"><span data-stu-id="e0893-110">1: Retrieve a private endpoint</span></span>
```
Get-AzPrivateEndpoint -Name MyPrivateEndpoint1 -ResourceGroupName TestResourceGroup

Name                                : MyPrivateEndpoint1
ResourceGroupName                   : TestResourceGroup
Location                            : eastus2euap
Id                                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/provi
                                      ders/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1
Etag                                : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                   : Succeeded
Subnet                              : {
                                        "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1/subnets/backendSubnet",
                                      }
NetworkInterfaces                   : [
                                        {

                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/networkInterfaces/MyNic1",
                                        }
                                      ]
PrivateLinkServiceConnections       : []
ManualPrivateLinkServiceConnections : [
                                        {
                                          "Name": "MyPrivateLinkServiceConnection",
                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1/manualPrivateLinkServi
                                      ceConnections/MyPrivateLinkServiceConnection",
                                          "PrivateLinkServiceId": "/subscriptions/00000000-0000-0000-0000-000000000000/
                                      resourceGroups/TestResourceGroup/providers/Microsoft.Network/priv
                                      ateLinkServices/MyPrivateLinkService",
                                          "PrivateLinkServiceConnectionState": {
                                            "Status": "Pending",
                                            "Description": "Awaiting approval"
                                          }
                                        }
                                      ]
```

<span data-ttu-id="e0893-111">Bu komut TestResourceGroup kaynak grubundaki MyPrivateEndpoint1 adındaki özel uç noktasını alır</span><span class="sxs-lookup"><span data-stu-id="e0893-111">This command gets the private endpoint named MyPrivateEndpoint1 in the resource group TestResourceGroup</span></span>

### <span data-ttu-id="e0893-112">2: ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e0893-112">2: List all private endpoints in ResourceGroup</span></span>
```
Get-AzPrivateEndpoint -ResourceGroupName TestResourceGroup

Name                                : MyPrivateEndpoint1
ResourceGroupName                   : TestResourceGroup
Location                            : eastus2euap
Id                                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/provi
                                      ders/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1
Etag                                : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                   : Succeeded
Subnet                              : {
                                        "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1/subnets/backendSubnet",
                                      }
NetworkInterfaces                   : [
                                        {

                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/networkInterfaces/MyNic1",
                                        }
                                      ]
PrivateLinkServiceConnections       : []
ManualPrivateLinkServiceConnections : [
                                        {
                                          "Name": "MyPrivateLinkServiceConnection",
                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1/manualPrivateLinkServi
                                      ceConnections/MyPrivateLinkServiceConnection",
                                          "PrivateLinkServiceId": "/subscriptions/00000000-0000-0000-0000-000000000000/
                                      resourceGroups/TestResourceGroup/providers/Microsoft.Network/priv
                                      ateLinkServices/MyPrivateLinkService",
                                          "PrivateLinkServiceConnectionState": {
                                            "Status": "Pending",
                                            "Description": "Awaiting approval"
                                          }
                                        }
                                      ]
```

<span data-ttu-id="e0893-113">Bu komut TestResourceGroup kaynak grubundaki tüm özel bitiş noktalarını alır</span><span class="sxs-lookup"><span data-stu-id="e0893-113">This command gets all of private end points in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="e0893-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e0893-114">PARAMETERS</span></span>

### <span data-ttu-id="e0893-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0893-115">-DefaultProfile</span></span>
<span data-ttu-id="e0893-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e0893-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0893-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="e0893-117">-ExpandResource</span></span>
<span data-ttu-id="e0893-118">Genişletilecek kaynak başvurusu.</span><span class="sxs-lookup"><span data-stu-id="e0893-118">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="e0893-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="e0893-119">-Name</span></span>
<span data-ttu-id="e0893-120">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="e0893-120">The resource name.</span></span>

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

### <span data-ttu-id="e0893-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0893-121">-ResourceGroupName</span></span>
<span data-ttu-id="e0893-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e0893-122">The resource group name.</span></span>

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

### <span data-ttu-id="e0893-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0893-123">CommonParameters</span></span>
<span data-ttu-id="e0893-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e0893-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0893-125">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e0893-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0893-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e0893-126">INPUTS</span></span>

### <span data-ttu-id="e0893-127">System. String</span><span class="sxs-lookup"><span data-stu-id="e0893-127">System.String</span></span>

## <span data-ttu-id="e0893-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e0893-128">OUTPUTS</span></span>

### <span data-ttu-id="e0893-129">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e0893-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="e0893-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e0893-130">NOTES</span></span>

## <span data-ttu-id="e0893-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e0893-131">RELATED LINKS</span></span>

[<span data-ttu-id="e0893-132">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e0893-132">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="e0893-133">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e0893-133">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)