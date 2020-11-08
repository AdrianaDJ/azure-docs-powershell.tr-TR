---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azbastion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzBastion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzBastion.md
ms.openlocfilehash: e2e2feacaefb0ce29c77263c0b733f503b8e9a74
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278556"
---
# <span data-ttu-id="8b6c0-101">New-AzBastion</span><span class="sxs-lookup"><span data-stu-id="8b6c0-101">New-AzBastion</span></span>

## <span data-ttu-id="8b6c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b6c0-102">SYNOPSIS</span></span>
<span data-ttu-id="8b6c0-103">Bir kaynak oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8b6c0-103">Creates a bastion resource.</span></span>

## <span data-ttu-id="8b6c0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8b6c0-104">SYNTAX</span></span>

### <span data-ttu-id="8b6c0-105">ByPublicIpAddressByVirtualNetwork (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8b6c0-105">ByPublicIpAddressByVirtualNetwork (Default)</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddress <PSPublicIpAddress>
 -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b6c0-106">ByPublicIpAddressByVirtualNetworkRGNameByVirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="8b6c0-106">ByPublicIpAddressByVirtualNetworkRGNameByVirtualNetworkName</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddress <PSPublicIpAddress>
 -VirtualNetworkRgName <String> -VirtualNetworkName <String> [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b6c0-107">Bypublicipaddressbyvirtualnetworkıd</span><span class="sxs-lookup"><span data-stu-id="8b6c0-107">ByPublicIpAddressByVirtualNetworkId</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddress <PSPublicIpAddress>
 -VirtualNetworkId <String> [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b6c0-108">ByPublicIpAddressIdByVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8b6c0-108">ByPublicIpAddressIdByVirtualNetwork</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressId <String>
 -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b6c0-109">Bypublicipaddressıdbyvirtualnetworkrgnamebyvirtualnetworkname</span><span class="sxs-lookup"><span data-stu-id="8b6c0-109">ByPublicIpAddressIdByVirtualNetworkRGNameByVirtualNetworkName</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressId <String>
 -VirtualNetworkRgName <String> -VirtualNetworkName <String> [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b6c0-110">Bypublicipaddressıdbyvirtualnetworkıd</span><span class="sxs-lookup"><span data-stu-id="8b6c0-110">ByPublicIpAddressIdByVirtualNetworkId</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressId <String> -VirtualNetworkId <String>
 [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b6c0-111">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8b6c0-111">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetwork</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressRgName <String>
 -PublicIpAddressName <String> -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b6c0-112">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkRGNameByVirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="8b6c0-112">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkRGNameByVirtualNetworkName</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressRgName <String>
 -PublicIpAddressName <String> -VirtualNetworkRgName <String> -VirtualNetworkName <String> [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b6c0-113">Bypublicipaddressrgnamebypublicipaddressnamebyvirtualnetworkıd</span><span class="sxs-lookup"><span data-stu-id="8b6c0-113">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkId</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressRgName <String>
 -PublicIpAddressName <String> -VirtualNetworkId <String> [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b6c0-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="8b6c0-114">DESCRIPTION</span></span>
<span data-ttu-id="8b6c0-115">Bir kaynak oluşturur. Bu, genel bir IP adresi ve bir VirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="8b6c0-115">Creates a bastion resource.This will need a Public Ip Address and a VirtualNetwork.</span></span> <span data-ttu-id="8b6c0-116">Bu VirtualNetwork içinde, AzureBastionSubnet adında bir alt ağ olmalıdır. Pubıc IP adresi SKU Standartağıyla oluşturulmuş olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="8b6c0-116">There must be a subnet with name AzureBastionSubnet in this VirtualNetwork.The Pubic Ip Address must be created with Sku Standard.</span></span>

## <span data-ttu-id="8b6c0-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8b6c0-117">EXAMPLES</span></span>

### <span data-ttu-id="8b6c0-118">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8b6c0-118">Example 1</span></span>
```powershell
$subnetName = "AzureBastionSubnet"
$subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.0.0/24
$vnet = New-AzVirtualNetwork -Name "TestVnet" -ResourceGroupName "BastionPowershellTest" -Location "westeurope" -AddressPrefix 10.0.0.0/16 -Subnet $subnet
$publicip = New-AzPublicIpAddress -ResourceGroupName "BastionPowershellTest" -name "Test-Ip" -location "westeurope" -AllocationMethod Dynamic -Sku Standard
$bastion = New-AzBastion -ResourceGroupName "BastionPowershellTest" â€“Name "test-Bastion2" -PublicIpAddress $publicip -VirtualNetwork $vnet

IpConfigurations     : {IpConf}
DnsName              : bst-a9ca868f-ddab-4a50-9f45-a443ea8a0187.bastion.azure.com
ProvisioningState    : Succeeded
IpConfigurationsText : [
                         {
                           "Subnet": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/virtualNetworks/TestVnet/subnets/AzureBastionSubnet"
                           },
                           "PublicIpAddress": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/publicIPAddresses/Test-Ip"
                           },
                           "ProvisioningState": "Succeeded",
                           "PrivateIpAllocationMethod": "Dynamic",
                           "Name": "IpConf",
                           "Etag": "W/\"ed810ccd-b3f6-4e22-891e-b0ed0a26d6dd\"",
                           "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/bastionHosts/test-Bastion2/bastionHostIpConfigurations/IpConf"
                         }
                       ]
ResourceGroupName    : BastionPowershellTest
Location             : westeurope
ResourceGuid         :
Type                 : Microsoft.Network/bastionHosts
Tag                  :
TagsTable            :
Name                 : test-Bastion2
Etag                 : W/"ed810ccd-b3f6-4e22-891e-b0ed0a26d6dd"
Id                   : /subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/bastionHosts/test-Bastion2

This example creates a bastion attached to virtual network "vnet" in the same resource group as the bastion.
There must be a subnet with name AzureBastionSubnet in this vnet.
The Ip Address must be created with Sku Standard.
```

### <span data-ttu-id="8b6c0-119">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="8b6c0-119">Example 2</span></span>
```powershell
$vnet = Get-AzVirtualNetwork -ResourceGroupName "BastionPowershellTest" -Name "testVnet2"
Add-AzVirtualNetworkSubnetConfig -Name "AzureBastionSubnet" -VirtualNetwork $vnet -AddressPrefix "10.0.0.0/24"
$vnet| Set-AzVirtualNetwork
New-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion2" -PublicIpAddressRgName "BastionPowershellTest" -PublicIpAddressName "testIp2" -VirtualNetworkRgName "BastionPowershellTest" -VirtualNetworkName "testVnet2"

IpConfigurations     : {IpConf}
DnsName              : bst-53757658-c4fd-4908-b1a7-0849e555d489.bastion.azure.com
ProvisioningState    : Succeeded
IpConfigurationsText : [
                         {
                           "Name": "IpConf",
                           "Etag": "W/\"7460e5f6-ad41-438b-a595-a63346ed8f16\"",
                           "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/bastionHosts/testBastion2/bastionHostIpConfigurations/IpConf",
                           "Subnet": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/virtualNetworks/testVnet2/subnets/AzureBastionSubnet"
                           },
                           "PublicIpAddress": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/publicIPAddresses/testIp2"
                           },
                           "ProvisioningState": "Succeeded",
                           "PrivateIpAllocationMethod": "Dynamic"
                         }
                       ]
ResourceGroupName    : BastionPowershellTest
Location             : westeurope
ResourceGuid         :
Type                 : Microsoft.Network/bastionHosts
Tag                  :
TagsTable            :
Name                 : testBastion2
Etag                 : W/"7460e5f6-ad41-438b-a595-a63346ed8f16"
Id                   : /subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/bastionHosts/testBastion2
```

## <span data-ttu-id="8b6c0-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8b6c0-120">PARAMETERS</span></span>

### <span data-ttu-id="8b6c0-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="8b6c0-121">-AsJob</span></span>
<span data-ttu-id="8b6c0-122">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="8b6c0-122">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6c0-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="8b6c0-123">-Confirm</span></span>
<span data-ttu-id="8b6c0-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8b6c0-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6c0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b6c0-125">-DefaultProfile</span></span>
<span data-ttu-id="8b6c0-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8b6c0-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6c0-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="8b6c0-127">-Name</span></span>
<span data-ttu-id="8b6c0-128">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="8b6c0-128">The bastion resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, BastionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6c0-129">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="8b6c0-129">-PublicIpAddress</span></span>
<span data-ttu-id="8b6c0-130">Genel IP adresi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="8b6c0-130">The public IP address object for bastion.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: ByPublicIpAddressByVirtualNetwork, ByPublicIpAddressByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressByVirtualNetworkId
Aliases: PublicIpAddressObject

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6c0-131">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="8b6c0-131">-PublicIpAddressId</span></span>
<span data-ttu-id="8b6c0-132">Genel IP adresi Azure kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="8b6c0-132">The public Ip address Azure resource Id for bastion.</span></span>

```yaml
Type: String
Parameter Sets: ByPublicIpAddressIdByVirtualNetwork, ByPublicIpAddressIdByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressIdByVirtualNetworkId
Aliases: PublicIpAddressResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6c0-133">-Publicıpaddressname</span><span class="sxs-lookup"><span data-stu-id="8b6c0-133">-PublicIpAddressName</span></span>
<span data-ttu-id="8b6c0-134">Genel IP adresi kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="8b6c0-134">The public Ip address resource name for bastion.</span></span>

```yaml
Type: String
Parameter Sets: ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetwork, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6c0-135">-Publicıpadressrgname</span><span class="sxs-lookup"><span data-stu-id="8b6c0-135">-PublicIpAddressRgName</span></span>
<span data-ttu-id="8b6c0-136">Genel IP adresi kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="8b6c0-136">The public Ip address resource group name for bastion.</span></span>

```yaml
Type: String
Parameter Sets: ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetwork, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkId
Aliases: PublicIpAddressResourceGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6c0-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b6c0-137">-ResourceGroupName</span></span>
<span data-ttu-id="8b6c0-138">Oluşturmanız gereken kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="8b6c0-138">The resource group name where you need to create bastion.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6c0-139">Etiketli</span><span class="sxs-lookup"><span data-stu-id="8b6c0-139">-Tag</span></span>
<span data-ttu-id="8b6c0-140">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="8b6c0-140">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6c0-141">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8b6c0-141">-VirtualNetwork</span></span>
<span data-ttu-id="8b6c0-142">Sanal ağ nesnesi.</span><span class="sxs-lookup"><span data-stu-id="8b6c0-142">The virtual network object for bastion.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: ByPublicIpAddressByVirtualNetwork, ByPublicIpAddressIdByVirtualNetwork, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetwork
Aliases: VirtualNetworkObject

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6c0-143">-Virtualnetworkıd</span><span class="sxs-lookup"><span data-stu-id="8b6c0-143">-VirtualNetworkId</span></span>
<span data-ttu-id="8b6c0-144">Sanal ağ Azure kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="8b6c0-144">The virtual network Azure resource Id for bastion.</span></span>

```yaml
Type: String
Parameter Sets: ByPublicIpAddressByVirtualNetworkId, ByPublicIpAddressIdByVirtualNetworkId, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkId
Aliases: VirtualNetworkResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6c0-145">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="8b6c0-145">-VirtualNetworkName</span></span>
<span data-ttu-id="8b6c0-146">Kaynak için sanal ağ kaynağı adı.</span><span class="sxs-lookup"><span data-stu-id="8b6c0-146">The virtual network resource name for bastion.</span></span>

```yaml
Type: String
Parameter Sets: ByPublicIpAddressByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressIdByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkRGNameByVirtualNetworkName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6c0-147">-VirtualNetworkRgName</span><span class="sxs-lookup"><span data-stu-id="8b6c0-147">-VirtualNetworkRgName</span></span>
<span data-ttu-id="8b6c0-148">Kaynak için sanal ağ kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="8b6c0-148">The virtual network resource group name for bastion.</span></span>

```yaml
Type: String
Parameter Sets: ByPublicIpAddressByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressIdByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkRGNameByVirtualNetworkName
Aliases: VirtualNetworkResourceGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6c0-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b6c0-149">-WhatIf</span></span>
<span data-ttu-id="8b6c0-150">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8b6c0-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b6c0-151">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8b6c0-151">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6c0-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b6c0-152">CommonParameters</span></span>
<span data-ttu-id="8b6c0-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8b6c0-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b6c0-154">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8b6c0-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b6c0-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8b6c0-155">INPUTS</span></span>

### <span data-ttu-id="8b6c0-156">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8b6c0-156">None</span></span>

## <span data-ttu-id="8b6c0-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8b6c0-157">OUTPUTS</span></span>

### <span data-ttu-id="8b6c0-158">Microsoft. Azure. Commands. Network. modeller. Pstion</span><span class="sxs-lookup"><span data-stu-id="8b6c0-158">Microsoft.Azure.Commands.Network.Models.PSBastion</span></span>

## <span data-ttu-id="8b6c0-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8b6c0-159">NOTES</span></span>

## <span data-ttu-id="8b6c0-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8b6c0-160">RELATED LINKS</span></span>
[<span data-ttu-id="8b6c0-161">Get-azma</span><span class="sxs-lookup"><span data-stu-id="8b6c0-161">Get-AzBastion</span></span>](./Get-AzBastion.md)

[<span data-ttu-id="8b6c0-162">Kaldır-azma</span><span class="sxs-lookup"><span data-stu-id="8b6c0-162">Remove-AzBastion</span></span>](./Remove-AzBastion.md)