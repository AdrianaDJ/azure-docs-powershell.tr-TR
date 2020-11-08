---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkService.md
ms.openlocfilehash: fdbb023c6796a780bfe9e6474191185a58489c91
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266025"
---
# <span data-ttu-id="bf17c-101">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="bf17c-101">Get-AzPrivateLinkService</span></span>

## <span data-ttu-id="bf17c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf17c-102">SYNOPSIS</span></span>
<span data-ttu-id="bf17c-103">Özel bağlantı hizmeti alır</span><span class="sxs-lookup"><span data-stu-id="bf17c-103">Gets private link service</span></span>

## <span data-ttu-id="bf17c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bf17c-104">SYNTAX</span></span>

### <span data-ttu-id="bf17c-105">NoExpand (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bf17c-105">NoExpand (Default)</span></span>
```
Get-AzPrivateLinkService [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf17c-106">Geniþ</span><span class="sxs-lookup"><span data-stu-id="bf17c-106">Expand</span></span>
```
Get-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf17c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bf17c-107">DESCRIPTION</span></span>
<span data-ttu-id="bf17c-108">**Get-AzPrivateLinkService** cmdlet 'i bir veya daha fazla özel bağlantı hizmeti alır.</span><span class="sxs-lookup"><span data-stu-id="bf17c-108">The **Get-AzPrivateLinkService** cmdlet gets one or more private link services.</span></span>

## <span data-ttu-id="bf17c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bf17c-109">EXAMPLES</span></span>

### <span data-ttu-id="bf17c-110">Örnekteki</span><span class="sxs-lookup"><span data-stu-id="bf17c-110">Example</span></span>
```
Get-AzPrivateLinkService -Name MyPLS -ResourceGroupName TestResourceGroup

Name                                 : MyPLS
ResourceGroupName                    : TestResourceGroup
Id                                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/prov
                                       iders/Microsoft.Network/privateLinkServices/MyPLS
Location                             : eastus2euap
Type                                 : Microsoft.Network/privateLinkServices
Etag                                 : W/"00000000-0000-0000-0000-000000000000"
Tag                                  : {}
ProvisioningState                    : Succeeded
Visibility                           : 
AutoApproval                         : 
Alias                                :
LoadBalancerFrontendIpConfigurations : []
IpConfigurations                     : [
                                         {
                                           "PrivateIPAddress": "10.0.2.5",
                                           "PrivateIPAllocationMethod": "Static",
                                           "ProvisioningState": "Failed",
                                           "PrivateIPAddressVersion": "IPv4",
                                           "Name": "IP-Config",
                                           "Subnet": {
                                             "Delegations": [],
                                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/
                                       TestResourceGroup/providers/Microsoft.Network/virtualNetworks/myvnet/subnets/backendSubne
                                       t",
                                             "ServiceAssociationLinks": []
                                           }
                                         }
                                       ]
PrivateEndpointConnections           : []
NetworkInterfaces                    : [
                                         {
                                           "TapConfigurations": [],
                                           "HostedWorkloads": [],
                                           "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/networkInterfaces/mytestinterface"
                                         }
                                       ]
```

<span data-ttu-id="bf17c-111">Bu Command, kaynak grubunda özel bir bağlantı hizmeti alır.</span><span class="sxs-lookup"><span data-stu-id="bf17c-111">This commandlet gets a private link service in the resource group.</span></span>

## <span data-ttu-id="bf17c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bf17c-112">PARAMETERS</span></span>

### <span data-ttu-id="bf17c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf17c-113">-DefaultProfile</span></span>
<span data-ttu-id="bf17c-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bf17c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf17c-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="bf17c-115">-ExpandResource</span></span>
<span data-ttu-id="bf17c-116">Genişletilecek kaynak başvurusu.</span><span class="sxs-lookup"><span data-stu-id="bf17c-116">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="bf17c-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="bf17c-117">-Name</span></span>
<span data-ttu-id="bf17c-118">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="bf17c-118">The resource name.</span></span>

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

### <span data-ttu-id="bf17c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf17c-119">-ResourceGroupName</span></span>
<span data-ttu-id="bf17c-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="bf17c-120">The resource group name.</span></span>

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

### <span data-ttu-id="bf17c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf17c-121">CommonParameters</span></span>
<span data-ttu-id="bf17c-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bf17c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf17c-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bf17c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf17c-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bf17c-124">INPUTS</span></span>

### <span data-ttu-id="bf17c-125">System. String</span><span class="sxs-lookup"><span data-stu-id="bf17c-125">System.String</span></span>

## <span data-ttu-id="bf17c-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bf17c-126">OUTPUTS</span></span>

### <span data-ttu-id="bf17c-127">Microsoft. Azure. Commands. Network. model. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="bf17c-127">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="bf17c-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bf17c-128">NOTES</span></span>

## <span data-ttu-id="bf17c-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bf17c-129">RELATED LINKS</span></span>
