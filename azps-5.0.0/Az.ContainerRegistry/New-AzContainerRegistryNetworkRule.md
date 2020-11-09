---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistrynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
ms.openlocfilehash: f60f85a14df42043352af1b71f0455983e03061a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319586"
---
# <span data-ttu-id="59beb-101">New-AzContainerRegistryNetworkRule</span><span class="sxs-lookup"><span data-stu-id="59beb-101">New-AzContainerRegistryNetworkRule</span></span>

## <span data-ttu-id="59beb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59beb-102">SYNOPSIS</span></span>
<span data-ttu-id="59beb-103">Ağ kuralı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="59beb-103">Create a network rule.</span></span>

## <span data-ttu-id="59beb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="59beb-104">SYNTAX</span></span>

### <span data-ttu-id="59beb-105">ByVirtualNetworkRule (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="59beb-105">ByVirtualNetworkRule (Default)</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-VirtualNetworkRule] -VirtualNetworkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59beb-106">Byıprule</span><span class="sxs-lookup"><span data-stu-id="59beb-106">ByIPRule</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-IPRule] -IPAddressOrRange <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59beb-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="59beb-107">DESCRIPTION</span></span>
<span data-ttu-id="59beb-108">Geçerli PowerShell oturumunda ağ kuralı nesnesi oluşturma.</span><span class="sxs-lookup"><span data-stu-id="59beb-108">Create a network rule object in current powershell session.</span></span>

## <span data-ttu-id="59beb-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="59beb-109">EXAMPLES</span></span>

### <span data-ttu-id="59beb-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="59beb-110">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix "10.0.1.0/24" -ServiceEndpoint "Microsoft.ContainerRegistry"
PS C:\> $vnet = New-AzVirtualNetwork -Name $VnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix "10.0.0.0/16" -Subnet $subnet
PS C:\> $rule = New-AzContainerRegistryNetworkRule -VirtualNetworkRule -VirtualNetworkResourceId $vnet.Subnets[0].Id
```

<span data-ttu-id="59beb-111">VirtualNetwork kural kümesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="59beb-111">Create virtualnetwork rule set.</span></span>

## <span data-ttu-id="59beb-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="59beb-112">PARAMETERS</span></span>

### <span data-ttu-id="59beb-113">-Eylem</span><span class="sxs-lookup"><span data-stu-id="59beb-113">-Action</span></span>
<span data-ttu-id="59beb-114">Ağ kuralı eylemi.</span><span class="sxs-lookup"><span data-stu-id="59beb-114">The action of network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59beb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59beb-115">-DefaultProfile</span></span>
<span data-ttu-id="59beb-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="59beb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59beb-117">-Ipadressorrange</span><span class="sxs-lookup"><span data-stu-id="59beb-117">-IPAddressOrRange</span></span>
<span data-ttu-id="59beb-118">CıDR biçimindeki IP veya IP aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="59beb-118">Specifies the IP or IP range in CIDR format.</span></span>
<span data-ttu-id="59beb-119">Yalnızca ıPV4 adresine izin verilir.</span><span class="sxs-lookup"><span data-stu-id="59beb-119">Only IPV4 address is allowed.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIPRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59beb-120">-Iprule</span><span class="sxs-lookup"><span data-stu-id="59beb-120">-IPRule</span></span>
<span data-ttu-id="59beb-121">Iprule oluşturulacağını göster.</span><span class="sxs-lookup"><span data-stu-id="59beb-121">Indicate to create IPRule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByIPRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59beb-122">-Virtualnetworkresourceıd</span><span class="sxs-lookup"><span data-stu-id="59beb-122">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="59beb-123">Alt ağın kaynak KIMLIĞI; örneğin:/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}/subnets/{subnetName}.</span><span class="sxs-lookup"><span data-stu-id="59beb-123">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}/subnets/{subnetName}.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualNetworkRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59beb-124">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="59beb-124">-VirtualNetworkRule</span></span>
<span data-ttu-id="59beb-125">VirtualNetworkRule oluşturmak için göster.</span><span class="sxs-lookup"><span data-stu-id="59beb-125">Indicate to create VirtualNetworkRule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVirtualNetworkRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59beb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59beb-126">CommonParameters</span></span>
<span data-ttu-id="59beb-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="59beb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59beb-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="59beb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59beb-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="59beb-129">INPUTS</span></span>

### <span data-ttu-id="59beb-130">System. String</span><span class="sxs-lookup"><span data-stu-id="59beb-130">System.String</span></span>

## <span data-ttu-id="59beb-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="59beb-131">OUTPUTS</span></span>

### <span data-ttu-id="59beb-132">Microsoft. Azure. Commands. ContainerRegistry. model. IPSNetworkRule</span><span class="sxs-lookup"><span data-stu-id="59beb-132">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span></span>

## <span data-ttu-id="59beb-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="59beb-133">NOTES</span></span>

## <span data-ttu-id="59beb-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="59beb-134">RELATED LINKS</span></span>
