---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azbastion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzBastion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzBastion.md
ms.openlocfilehash: f5e892548600d218fabf8cfabebeaf89ee2fab88
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931779"
---
# <span data-ttu-id="b4a26-101">Get-AzBastion</span><span class="sxs-lookup"><span data-stu-id="b4a26-101">Get-AzBastion</span></span>

## <span data-ttu-id="b4a26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4a26-102">SYNOPSIS</span></span>
<span data-ttu-id="b4a26-103">Bir kaynak veya kaynak ekleme kaynaklarını alır.</span><span class="sxs-lookup"><span data-stu-id="b4a26-103">Gets a Bastion resource or Bastion resources.</span></span>

## <span data-ttu-id="b4a26-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b4a26-104">SYNTAX</span></span>

### <span data-ttu-id="b4a26-105">Listbysubscriptionıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b4a26-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzBastion [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4a26-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4a26-106">ListByResourceGroupName</span></span>
```
Get-AzBastion [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4a26-107">ByResourceGroupNameByName</span><span class="sxs-lookup"><span data-stu-id="b4a26-107">ByResourceGroupNameByName</span></span>
```
Get-AzBastion -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4a26-108">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="b4a26-108">ByResourceId</span></span>
```
Get-AzBastion -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b4a26-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="b4a26-109">DESCRIPTION</span></span>
<span data-ttu-id="b4a26-110">**Get-Bastion** cmdlet 'i kaynak grubunda veya subscritption bir veya daha fazla şey alır.</span><span class="sxs-lookup"><span data-stu-id="b4a26-110">The **Get-Bastion** cmdlet gets one or more bastions in a resource group or subscritption.</span></span>

## <span data-ttu-id="b4a26-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b4a26-111">EXAMPLES</span></span>

### <span data-ttu-id="b4a26-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b4a26-112">Example 1</span></span>
```powershell
Get-AzBastion

ResourceGroupName    : abagarwaProd-PPTest
Location             : westcentralus
ResourceGuid         :
Type                 : Microsoft.Network/bastionHosts
Tag                  : {}
TagsTable            :
Name                 : abagarwaProd-PPTest-vnet-bastion
Etag                 : W/"55702e34-348f-4b79-bf44-9c306623b7c7"
Id                   : /subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/abagarwaProd-PPTest/providers/Microsoft.Network/bastionHosts/abagarwaProd-PPTest-vnet-bastion

IpConfigurations     : {IpConf}
DnsName              : bst-f594cc74-c21e-44c3-ad5e-5bb93933965f.bastion.azure.com
ProvisioningState    : Succeeded
IpConfigurationsText : [
                         {
                           "Name": "IpConf",
                           "Etag": "W/\"7ae27d14-9260-4e2d-8c48-47e9628a3e3b\"",
                           "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionTest/providers/Microsoft.Network/bastionHosts/BastionTest-vnet-bastion/bastionHostIpConfigurations/IpConf",
                           "Subnet": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionTest/providers/Microsoft.Network/virtualNetworks/BastionTest-vnet/subnets/default"
                           },
                           "PublicIpAddress": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionTest/providers/Microsoft.Network/publicIPAddresses/BastionTest-vnet-ip"
                           },
                           "ProvisioningState": "Succeeded",
                           "PrivateIpAllocationMethod": "Dynamic"
                         }
                       ]
ResourceGroupName    : BastionTest
Location             : westcentralus
ResourceGuid         :
Type                 : Microsoft.Network/bastionHosts
Tag                  : {}
TagsTable            :
Name                 : BastionTest-vnet-bastion
Etag                 : W/"7ae27d14-9260-4e2d-8c48-47e9628a3e3b"
Id                   : /subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionTest/providers/Microsoft.Network/bastionHosts/BastionTest-vnet-bastion

IpConfigurations     : {IpConf}
DnsName              : bst-32359e0c-d6a5-45f1-b196-2f9a4b4b77e8.bastion.azure.com
ProvisioningState    : Succeeded
IpConfigurationsText : [
                         {
                           "Name": "IpConf",
                           "Etag": "W/\"bd537319-3379-4caf-a8dc-be4506f9dd3a\"",
                           "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/ps1621/providers/Microsoft.Network/bastionHosts/ps5581/bastionHostIpConfigurations/IpConf",
                           "Subnet": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/ps1621/providers/Microsoft.Network/virtualNetworks/ps7070/subnets/AzureBastionSubnet"
                           },
                           "PublicIpAddress": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/ps1621/providers/Microsoft.Network/publicIPAddresses/ps2217"
                           },
                           "ProvisioningState": "Succeeded",
                           "PrivateIpAllocationMethod": "Dynamic"
                         }
                       ]
ResourceGroupName    : ps1621
Location             : westcentralus
ResourceGuid         :
Type                 : Microsoft.Network/bastionHosts
Tag                  :
TagsTable            :
Name                 : ps5581
Etag                 : W/"bd537319-3379-4caf-a8dc-be4506f9dd3a"
Id                   : /subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/ps1621/providers/Microsoft.Network/bastionHosts/ps5581

IpConfigurations     : {IpConf}
DnsName              : bst-aee29973-3b60-44c1-a1de-bd8636e79127.bastion.azure.com
ProvisioningState    : Succeeded
IpConfigurationsText : [
                         {
                           "Name": "IpConf",
                           "Etag": "W/\"42f723dd-f1de-4fd0-b307-3fe82f0b50f7\"",
                           "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/ps3151/providers/Microsoft.Network/bastionHosts/ps8815/bastionHostIpConfigurations/IpConf",
                           "Subnet": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/ps3151/providers/Microsoft.Network/virtualNetworks/ps5766/subnets/AzureBastionSubnet"
                           },
                           "PublicIpAddress": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/ps3151/providers/Microsoft.Network/publicIPAddresses/ps2773"
                           },
                           "ProvisioningState": "Succeeded",
                           "PrivateIpAllocationMethod": "Dynamic"
                         }
                       ]
ResourceGroupName    : ps3151
Location             : westcentralus
ResourceGuid         :
Type                 : Microsoft.Network/bastionHosts
Tag                  :
TagsTable            :
Name                 : ps8815
Etag                 : W/"42f723dd-f1de-4fd0-b307-3fe82f0b50f7"
Id                   : /subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/ps3151/providers/Microsoft.Network/bastionHosts/ps8815

IpConfigurations     : {IpConf}
DnsName              : bst-746c229d-f144-4699-a7ea-303a15a70457.bastion.azure.com
ProvisioningState    : Succeeded
IpConfigurationsText : [
                         {
                           "Name": "IpConf",
                           "Etag": "W/\"0b11e3e7-330b-4727-b073-dfe458429fcf\"",
                           "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/ps3429/providers/Microsoft.Network/bastionHosts/ps7790/bastionHostIpConfigurations/IpConf",
                           "Subnet": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/ps3429/providers/Microsoft.Network/virtualNetworks/ps7582/subnets/AzureBastionSubnet"
                           },
                           "PublicIpAddress": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/ps3429/providers/Microsoft.Network/publicIPAddresses/ps8199"
                           },
                           "ProvisioningState": "Succeeded",
                           "PrivateIpAllocationMethod": "Dynamic"
                         }
                       ]
```

### <span data-ttu-id="b4a26-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="b4a26-113">Example 2</span></span>
```powershell
Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion"

IpConfigurations     : {IpConf}
DnsName              : bst-0597f607-ab71-46c2-ab2a-777bfa887aff.bastion.azure.com
ProvisioningState    : Succeeded
IpConfigurationsText : [
                         {
                           "Name": "IpConf",
                           "Etag": "W/\"4d023823-3ea8-439a-ac00-20f16fb0c9b2\"",
                           "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/bastionHosts/testBastion/bastionHostIpConfigurations/IpConf",
                           "Subnet": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/virtualNetworks/TestVnet/subnets/AzureBastionSubnet"
                           },
                           "PublicIpAddress": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/publicIPAddresses/Test-Ip"
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
Name                 : testBastion
Etag                 : W/"4d023823-3ea8-439a-ac00-20f16fb0c9b2"
Id                   : /subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/bastionHosts/testBastion
```

## <span data-ttu-id="b4a26-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b4a26-114">PARAMETERS</span></span>

### <span data-ttu-id="b4a26-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="b4a26-115">-Confirm</span></span>
<span data-ttu-id="b4a26-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b4a26-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4a26-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4a26-117">-DefaultProfile</span></span>
<span data-ttu-id="b4a26-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b4a26-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4a26-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="b4a26-119">-Name</span></span>
<span data-ttu-id="b4a26-120">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="b4a26-120">The bastion resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupNameByName
Aliases: ResourceName, BastionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a26-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4a26-121">-ResourceGroupName</span></span>
<span data-ttu-id="b4a26-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b4a26-122">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByResourceGroupNameByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a26-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b4a26-123">-ResourceId</span></span>
<span data-ttu-id="b4a26-124">Kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="b4a26-124">The bastion Azure resource Id</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a26-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4a26-125">-WhatIf</span></span>
<span data-ttu-id="b4a26-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b4a26-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4a26-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b4a26-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4a26-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4a26-128">CommonParameters</span></span>
<span data-ttu-id="b4a26-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b4a26-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4a26-130">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b4a26-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4a26-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b4a26-131">INPUTS</span></span>

### <span data-ttu-id="b4a26-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b4a26-132">None</span></span>

## <span data-ttu-id="b4a26-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b4a26-133">OUTPUTS</span></span>

### <span data-ttu-id="b4a26-134">Microsoft. Azure. Commands. Network. modeller. Pstion</span><span class="sxs-lookup"><span data-stu-id="b4a26-134">Microsoft.Azure.Commands.Network.Models.PSBastion</span></span>

### <span data-ttu-id="b4a26-135">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. modeller. PSBastion, Microsoft. Azure. PowerShell. cmdlet. Network, Version = 1.13.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b4a26-135">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSBastion, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.13.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b4a26-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b4a26-136">NOTES</span></span>

## <span data-ttu-id="b4a26-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b4a26-137">RELATED LINKS</span></span>
[<span data-ttu-id="b4a26-138">Yeni-azma</span><span class="sxs-lookup"><span data-stu-id="b4a26-138">New-AzBastion</span></span>](./New-AzBastion.md)

[<span data-ttu-id="b4a26-139">Kaldır-azma</span><span class="sxs-lookup"><span data-stu-id="b4a26-139">Remove-AzBastion</span></span>](./Remove-AzBastion.md)