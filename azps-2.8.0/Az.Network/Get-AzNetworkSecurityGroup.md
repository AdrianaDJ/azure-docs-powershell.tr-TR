---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5AECCBD7-1FDE-4217-9F59-36328062E669
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
ms.openlocfilehash: 46106379160ee593748a95489c2641d43114d863
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931997"
---
# <span data-ttu-id="ebeaa-101">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ebeaa-101">Get-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="ebeaa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebeaa-102">SYNOPSIS</span></span>
<span data-ttu-id="ebeaa-103">Bir ağ güvenlik grubu alır.</span><span class="sxs-lookup"><span data-stu-id="ebeaa-103">Gets a network security group.</span></span>

## <span data-ttu-id="ebeaa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ebeaa-104">SYNTAX</span></span>

### <span data-ttu-id="ebeaa-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="ebeaa-105">NoExpand</span></span>
```
Get-AzNetworkSecurityGroup [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ebeaa-106">Geniþ</span><span class="sxs-lookup"><span data-stu-id="ebeaa-106">Expand</span></span>
```
Get-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebeaa-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ebeaa-107">DESCRIPTION</span></span>
<span data-ttu-id="ebeaa-108">**Get-AzNetworkSecurityGroup** cmdlet 'ı bir Azure ağ güvenlik grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="ebeaa-108">The **Get-AzNetworkSecurityGroup** cmdlet gets an Azure network security group.</span></span>

## <span data-ttu-id="ebeaa-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ebeaa-109">EXAMPLES</span></span>

### <span data-ttu-id="ebeaa-110">1: var olan bir ağ güvenlik grubunu alma</span><span class="sxs-lookup"><span data-stu-id="ebeaa-110">1: Retrieve an existing network security group</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName "rg1"

Name                        : nsg1
ResourceGroupName           : rg1
Location                    : eastus
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provider
                              s/Microsoft.Network/networkInterfaces/nsg1
Etag                        : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid                : 00000000-0000-0000-0000-000000000000
ProvisioningState           : Succeeded
Tags                        :
VirtualMachine              : null
IpConfigurations            : [
                                {
                                  "Name": "ipconfig1",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/networkInterfaces/nsg1/ipConfigurations/ipcon
                              fig1",
                                  "PrivateIpAddress": "x.x.x.x",
                                  "PrivateIpAllocationMethod": "Dynamic",
                                  "Subnet": {
                                    "Delegations": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/virtualNetworks/vnetcrptestps2673/subnets/subnetcrptestp
                              s2673",
                                    "ServiceAssociationLinks": []
                                  },
                                  "PublicIpAddress": {
                                    "IpTags": [],
                                    "Zones": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/publicIPAddresses/pubipcrptestps2673"
                                  },
                                  "ProvisioningState": "Succeeded",
                                  "PrivateIpAddressVersion": "IPv4",
                                  "LoadBalancerBackendAddressPools": [],
                                  "LoadBalancerInboundNatRules": [],
                                  "Primary": true,
                                  "ApplicationGatewayBackendAddressPools": [],
                                  "ApplicationSecurityGroups": []
                                }
                              ]
DnsSettings                 : {
                                "DnsServers": [],
                                "AppliedDnsServers": [],
                                "InternalDomainNameSuffix": "xxxxxxxxxxxxxxx.xx.internal.cloudapp.net"
                              }
EnableIPForwarding          : False
EnableAcceleratedNetworking : False
NetworkSecurityGroup        : null
Primary                     :
MacAddress                  :
```

<span data-ttu-id="ebeaa-111">Bu komut, "RG1" kaynak grubundaki "nsg1" Azure ağ güvenlik grubunun içeriğini döndürüyor</span><span class="sxs-lookup"><span data-stu-id="ebeaa-111">This command returns contents of Azure network security group "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="ebeaa-112">2: filtreleme kullanarak var olan ağ güvenliği gruplarını listeleme</span><span class="sxs-lookup"><span data-stu-id="ebeaa-112">2: List existing network security groups using filtering</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg*

Name                        : nsg1
ResourceGroupName           : rg1
Location                    : eastus
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provider
                              s/Microsoft.Network/networkInterfaces/nsg1
Etag                        : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid                : 00000000-0000-0000-0000-000000000000
ProvisioningState           : Succeeded
Tags                        :
VirtualMachine              : null
IpConfigurations            : [
                                {
                                  "Name": "ipconfig1",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/networkInterfaces/nsg1/ipConfigurations/ipcon
                              fig1",
                                  "PrivateIpAddress": "x.x.x.x",
                                  "PrivateIpAllocationMethod": "Dynamic",
                                  "Subnet": {
                                    "Delegations": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/virtualNetworks/vnetcrptestps2673/subnets/subnetcrptestp
                              s2673",
                                    "ServiceAssociationLinks": []
                                  },
                                  "PublicIpAddress": {
                                    "IpTags": [],
                                    "Zones": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/publicIPAddresses/pubipcrptestps2673"
                                  },
                                  "ProvisioningState": "Succeeded",
                                  "PrivateIpAddressVersion": "IPv4",
                                  "LoadBalancerBackendAddressPools": [],
                                  "LoadBalancerInboundNatRules": [],
                                  "Primary": true,
                                  "ApplicationGatewayBackendAddressPools": [],
                                  "ApplicationSecurityGroups": []
                                }
                              ]
DnsSettings                 : {
                                "DnsServers": [],
                                "AppliedDnsServers": [],
                                "InternalDomainNameSuffix": "xxxxxxxxxxxxxxx.xx.internal.cloudapp.net"
                              }
EnableIPForwarding          : False
EnableAcceleratedNetworking : False
NetworkSecurityGroup        : null
Primary                     :
MacAddress                  :
```

<span data-ttu-id="ebeaa-113">Bu komut, "NSG" ile başlayan Azure ağ güvenlik gruplarının içeriğini döndürüyor</span><span class="sxs-lookup"><span data-stu-id="ebeaa-113">This command returns contents of Azure network security groups that start with "nsg"</span></span>

## <span data-ttu-id="ebeaa-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ebeaa-114">PARAMETERS</span></span>

### <span data-ttu-id="ebeaa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebeaa-115">-DefaultProfile</span></span>
<span data-ttu-id="ebeaa-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ebeaa-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebeaa-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="ebeaa-117">-ExpandResource</span></span>
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

### <span data-ttu-id="ebeaa-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="ebeaa-118">-Name</span></span>
<span data-ttu-id="ebeaa-119">Bu cmdlet 'in aldığı ağ güvenlik grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ebeaa-119">Specifies the name of the network security group that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ebeaa-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebeaa-120">-ResourceGroupName</span></span>
<span data-ttu-id="ebeaa-121">Ağ güvenlik grubunun ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ebeaa-121">Specifies the name of the resource group that the network security group belongs to.</span></span>

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

### <span data-ttu-id="ebeaa-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebeaa-122">CommonParameters</span></span>
<span data-ttu-id="ebeaa-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ebeaa-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebeaa-124">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ebeaa-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebeaa-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ebeaa-125">INPUTS</span></span>

### <span data-ttu-id="ebeaa-126">System. String</span><span class="sxs-lookup"><span data-stu-id="ebeaa-126">System.String</span></span>

## <span data-ttu-id="ebeaa-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ebeaa-127">OUTPUTS</span></span>

### <span data-ttu-id="ebeaa-128">Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ebeaa-128">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="ebeaa-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ebeaa-129">NOTES</span></span>

## <span data-ttu-id="ebeaa-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ebeaa-130">RELATED LINKS</span></span>

[<span data-ttu-id="ebeaa-131">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ebeaa-131">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="ebeaa-132">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ebeaa-132">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="ebeaa-133">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ebeaa-133">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)


