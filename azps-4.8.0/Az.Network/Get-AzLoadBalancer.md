---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancer.md
ms.openlocfilehash: 767f725633560d79cb19e1caad61c08772107b42
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274137"
---
# <span data-ttu-id="54adb-101">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="54adb-101">Get-AzLoadBalancer</span></span>

## <span data-ttu-id="54adb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54adb-102">SYNOPSIS</span></span>
<span data-ttu-id="54adb-103">Bir yük dengeleyici alır.</span><span class="sxs-lookup"><span data-stu-id="54adb-103">Gets a load balancer.</span></span>

## <span data-ttu-id="54adb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="54adb-104">SYNTAX</span></span>

### <span data-ttu-id="54adb-105">NoExpand (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="54adb-105">NoExpand (Default)</span></span>
```
Get-AzLoadBalancer [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="54adb-106">Geniþ</span><span class="sxs-lookup"><span data-stu-id="54adb-106">Expand</span></span>
```
Get-AzLoadBalancer -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54adb-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="54adb-107">DESCRIPTION</span></span>
<span data-ttu-id="54adb-108">**Get-AzLoadBalancer** cmdlet 'i, kaynak grubunda yer alan bir veya birden çok Azure yük dengeleyici alır.</span><span class="sxs-lookup"><span data-stu-id="54adb-108">The **Get-AzLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="54adb-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="54adb-109">EXAMPLES</span></span>

### <span data-ttu-id="54adb-110">Örnek 1: yük dengeleyici alma</span><span class="sxs-lookup"><span data-stu-id="54adb-110">Example 1: Get a load balancer</span></span>
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

<span data-ttu-id="54adb-111">Bu komut MyLoadBalancer adındaki yük dengeleyiciden alır.</span><span class="sxs-lookup"><span data-stu-id="54adb-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="54adb-112">Bu cmdlet 'i çalıştırabilmeniz için bir yük dengeleyici var olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="54adb-112">A load balancer must exist before you can run this cmdlet.</span></span>

### <span data-ttu-id="54adb-113">Örnek 2: filtreleme kullanarak yük dengeleyicileri listeleyin</span><span class="sxs-lookup"><span data-stu-id="54adb-113">Example 2: List load balancers using filtering</span></span>
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

<span data-ttu-id="54adb-114">Bu komut, tüm yük dengeleyicileri "MyLoadBalancer" ile başlayan bir adla alır</span><span class="sxs-lookup"><span data-stu-id="54adb-114">This command gets all load balancers with a name that starts with "MyLoadBalancer"</span></span>

## <span data-ttu-id="54adb-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="54adb-115">PARAMETERS</span></span>

### <span data-ttu-id="54adb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54adb-116">-DefaultProfile</span></span>
<span data-ttu-id="54adb-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="54adb-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54adb-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="54adb-118">-ExpandResource</span></span>
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

### <span data-ttu-id="54adb-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="54adb-119">-Name</span></span>
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

### <span data-ttu-id="54adb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54adb-120">-ResourceGroupName</span></span>
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

### <span data-ttu-id="54adb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54adb-121">CommonParameters</span></span>
<span data-ttu-id="54adb-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="54adb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54adb-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="54adb-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54adb-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="54adb-124">INPUTS</span></span>

### <span data-ttu-id="54adb-125">System. String</span><span class="sxs-lookup"><span data-stu-id="54adb-125">System.String</span></span>

## <span data-ttu-id="54adb-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="54adb-126">OUTPUTS</span></span>

### <span data-ttu-id="54adb-127">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="54adb-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="54adb-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="54adb-128">NOTES</span></span>

## <span data-ttu-id="54adb-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="54adb-129">RELATED LINKS</span></span>

[<span data-ttu-id="54adb-130">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="54adb-130">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="54adb-131">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="54adb-131">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="54adb-132">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="54adb-132">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


