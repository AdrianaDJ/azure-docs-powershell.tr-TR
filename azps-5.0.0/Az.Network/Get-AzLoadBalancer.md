---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancer.md
ms.openlocfilehash: 767f725633560d79cb19e1caad61c08772107b42
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279865"
---
# <span data-ttu-id="0593b-101">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0593b-101">Get-AzLoadBalancer</span></span>

## <span data-ttu-id="0593b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0593b-102">SYNOPSIS</span></span>
<span data-ttu-id="0593b-103">Bir yük dengeleyici alır.</span><span class="sxs-lookup"><span data-stu-id="0593b-103">Gets a load balancer.</span></span>

## <span data-ttu-id="0593b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0593b-104">SYNTAX</span></span>

### <span data-ttu-id="0593b-105">NoExpand (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0593b-105">NoExpand (Default)</span></span>
```
Get-AzLoadBalancer [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0593b-106">Geniþ</span><span class="sxs-lookup"><span data-stu-id="0593b-106">Expand</span></span>
```
Get-AzLoadBalancer -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0593b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0593b-107">DESCRIPTION</span></span>
<span data-ttu-id="0593b-108">**Get-AzLoadBalancer** cmdlet 'i, kaynak grubunda yer alan bir veya birden çok Azure yük dengeleyici alır.</span><span class="sxs-lookup"><span data-stu-id="0593b-108">The **Get-AzLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="0593b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0593b-109">EXAMPLES</span></span>

### <span data-ttu-id="0593b-110">Örnek 1: yük dengeleyici alma</span><span class="sxs-lookup"><span data-stu-id="0593b-110">Example 1: Get a load balancer</span></span>
```
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer1" -ResourceGroupName "MyResourceGroup"

Name                     : MyLoadBalancer1
ResourceGroupName        : MyResourceGroup
Location                 : australiaeast
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/M
                           icrosoft.Network/loadBalancers/MyLoadBalancer1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
FrontendIpConfigurations : []
BackendAddressPools      : []
LoadBalancingRules       : []
Probes                   : []
InboundNatRules          : []
InboundNatPools          : []
Sku                      : {
                             "Name": "Basic"
                           }
```

<span data-ttu-id="0593b-111">Bu komut MyLoadBalancer adındaki yük dengeleyiciden alır.</span><span class="sxs-lookup"><span data-stu-id="0593b-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="0593b-112">Bu cmdlet 'i çalıştırabilmeniz için bir yük dengeleyici var olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0593b-112">A load balancer must exist before you can run this cmdlet.</span></span>

### <span data-ttu-id="0593b-113">Örnek 2: filtreleme kullanarak yük dengeleyicileri listeleyin</span><span class="sxs-lookup"><span data-stu-id="0593b-113">Example 2: List load balancers using filtering</span></span>
```
PS C:\> Get-AzLoadBalancer -Name MyLoadBalancer*

Name                     : MyLoadBalancer1
ResourceGroupName        : MyResourceGroup
Location                 : australiaeast
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/M
                           icrosoft.Network/loadBalancers/MyLoadBalancer1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
FrontendIpConfigurations : []
BackendAddressPools      : []
LoadBalancingRules       : []
Probes                   : []
InboundNatRules          : []
InboundNatPools          : []
Sku                      : {
                             "Name": "Basic"
                           }

Name                     : MyLoadBalancer2
ResourceGroupName        : MyResourceGroup
Location                 : australiaeast
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/M
                           icrosoft.Network/loadBalancers/MyLoadBalancer2
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
FrontendIpConfigurations : []
BackendAddressPools      : []
LoadBalancingRules       : []
Probes                   : []
InboundNatRules          : []
InboundNatPools          : []
Sku                      : {
                             "Name": "Basic"
                           }
```

<span data-ttu-id="0593b-114">Bu komut, tüm yük dengeleyicileri "MyLoadBalancer" ile başlayan bir adla alır</span><span class="sxs-lookup"><span data-stu-id="0593b-114">This command gets all load balancers with a name that starts with "MyLoadBalancer"</span></span>

## <span data-ttu-id="0593b-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0593b-115">PARAMETERS</span></span>

### <span data-ttu-id="0593b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0593b-116">-DefaultProfile</span></span>
<span data-ttu-id="0593b-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0593b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0593b-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="0593b-118">-ExpandResource</span></span>
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

### <span data-ttu-id="0593b-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="0593b-119">-Name</span></span>
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

### <span data-ttu-id="0593b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0593b-120">-ResourceGroupName</span></span>
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

### <span data-ttu-id="0593b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0593b-121">CommonParameters</span></span>
<span data-ttu-id="0593b-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0593b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0593b-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0593b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0593b-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0593b-124">INPUTS</span></span>

### <span data-ttu-id="0593b-125">System. String</span><span class="sxs-lookup"><span data-stu-id="0593b-125">System.String</span></span>

## <span data-ttu-id="0593b-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0593b-126">OUTPUTS</span></span>

### <span data-ttu-id="0593b-127">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0593b-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0593b-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0593b-128">NOTES</span></span>

## <span data-ttu-id="0593b-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0593b-129">RELATED LINKS</span></span>

[<span data-ttu-id="0593b-130">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0593b-130">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="0593b-131">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0593b-131">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="0593b-132">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0593b-132">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


