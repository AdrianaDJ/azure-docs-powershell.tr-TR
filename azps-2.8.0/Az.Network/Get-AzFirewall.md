---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 91D58F60-F22A-454A-B04C-E5AEF33E9D06
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewall.md
ms.openlocfilehash: 12aa2824a4930b078510fcc2fa16593aae4bf77d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931754"
---
# <span data-ttu-id="dcf74-101">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="dcf74-101">Get-AzFirewall</span></span>

## <span data-ttu-id="dcf74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcf74-102">SYNOPSIS</span></span>
<span data-ttu-id="dcf74-103">Bir Azure Güvenlik Duvarı alır.</span><span class="sxs-lookup"><span data-stu-id="dcf74-103">Gets a Azure Firewall.</span></span>

## <span data-ttu-id="dcf74-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dcf74-104">SYNTAX</span></span>

```
Get-AzFirewall [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dcf74-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dcf74-105">DESCRIPTION</span></span>
<span data-ttu-id="dcf74-106">**Get-AzFirewall** cmdlet 'i kaynak grubunda bir veya daha fazla güvenlik duvarını alır.</span><span class="sxs-lookup"><span data-stu-id="dcf74-106">The **Get-AzFirewall** cmdlet gets one or more Firewalls in a resource group.</span></span>

## <span data-ttu-id="dcf74-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dcf74-107">EXAMPLES</span></span>

### <span data-ttu-id="dcf74-108">1: kaynak grubundaki tüm güvenlik duvarlarını alma</span><span class="sxs-lookup"><span data-stu-id="dcf74-108">1:  Retrieve all Firewalls in a resource group</span></span>
```
Get-AzFirewall -ResourceGroupName rgName

Name                       : azFw
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}

Name                       : azFw1
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw1
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw1/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}
```

<span data-ttu-id="dcf74-109">Bu örnekte, "rgName" kaynak grubundaki tüm güvenlik duvarları alınır.</span><span class="sxs-lookup"><span data-stu-id="dcf74-109">This example retrieves all Firewalls in resource group "rgName".</span></span>

### <span data-ttu-id="dcf74-110">2: ada göre bir güvenlik duvarı alma</span><span class="sxs-lookup"><span data-stu-id="dcf74-110">2:  Retrieve a Firewall by name</span></span>
```
Get-AzFirewall -ResourceGroupName rgName -Name azFw

Name                       : azFw
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}
```

<span data-ttu-id="dcf74-111">Bu örnekte, "rgName" kaynak grubunda "azFw" adlı güvenlik duvarı alınır.</span><span class="sxs-lookup"><span data-stu-id="dcf74-111">This example retrieves Firewall named "azFw" in resource group "rgName".</span></span>

### <span data-ttu-id="dcf74-112">3: filtreleme ile tüm güvenlik duvarlarını alma</span><span class="sxs-lookup"><span data-stu-id="dcf74-112">3:  Retrieve all Firewalls with filtering</span></span>
```
Get-AzFirewall -Name azFw*

Name                       : azFw
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}

Name                       : azFw1
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw1
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw1/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}
```

<span data-ttu-id="dcf74-113">Bu örnekte, "azFw" ile başlayan tüm güvenlik duvarları alınır</span><span class="sxs-lookup"><span data-stu-id="dcf74-113">This example retrieves all Firewalls that start with "azFw"</span></span>

### <span data-ttu-id="dcf74-114">4: güvenlik duvarı alın ve güvenlik duvarına uygulama kuralı koleksiyonu ekleyin</span><span class="sxs-lookup"><span data-stu-id="dcf74-114">4:  Retrieve a firewall and then add a application rule collection to the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$appRule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$appRuleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $appRule -ActionType "Allow"
$azFw.AddApplicationRuleCollection($appRuleCollection)
```

<span data-ttu-id="dcf74-115">Bu örnek bir güvenlik duvarı alır ve güvenlik duvarına bir uygulama kuralı koleksiyonu ekleyerek AddApplicationRuleCollection metodunu çağırarak.</span><span class="sxs-lookup"><span data-stu-id="dcf74-115">This example retrieves a firewall, then adds a application rule collection to the firewall by calling method AddApplicationRuleCollection.</span></span>

### <span data-ttu-id="dcf74-116">5: güvenlik duvarı alın ve güvenlik duvarına bir ağ kuralı koleksiyonu ekleyin</span><span class="sxs-lookup"><span data-stu-id="dcf74-116">5:  Retrieve a firewall and then add a network rule collection to the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$netRule = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol "Udp" -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$netRuleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $netRule -ActionType "Allow"
$azFw.AddNetworkRuleCollection($netRuleCollection)
```

<span data-ttu-id="dcf74-117">Bu örnek bir güvenlik duvarı alır ve ardından AddNetworkRuleCollection metodunu çağırarak güvenlik duvarına bir ağ kuralı koleksiyonu ekler.</span><span class="sxs-lookup"><span data-stu-id="dcf74-117">This example retrieves a firewall, then adds a network rule collection to the firewall by calling method AddNetworkRuleCollection.</span></span>

### <span data-ttu-id="dcf74-118">6: güvenlik duvarı alın ve güvenlik duvarından bir uygulama kuralı koleksiyonunu ada göre geri alın</span><span class="sxs-lookup"><span data-stu-id="dcf74-118">6:  Retrieve a firewall and then retrieve a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$getAppRc=$azFw.GetApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="dcf74-119">Bu örnekte, bir güvenlik duvarı alınır ve ardından, güvenlik duvarı nesnesinde GetApplicationRuleCollectionByName metodunu çağıran bir kural koleksiyonunu ada göre alır.</span><span class="sxs-lookup"><span data-stu-id="dcf74-119">This example retrieves a firewall and then gets a rule collection by name, calling method GetApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="dcf74-120">GetApplicationRuleCollectionByName metodunun kural koleksiyonu adı büyük/küçük harf duyarlı değildir.</span><span class="sxs-lookup"><span data-stu-id="dcf74-120">The rule collection name for method GetApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="dcf74-121">7: güvenlik duvarını alın ve güvenlik duvarından bir ağ kuralı koleksiyonunu ada göre geri alın</span><span class="sxs-lookup"><span data-stu-id="dcf74-121">7:  Retrieve a firewall and then retrieve a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$getNetRc=$azFw.GetNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="dcf74-122">Bu örnekte bir güvenlik duvarı ve ardından bir kural koleksiyonunu ada göre alır</span><span class="sxs-lookup"><span data-stu-id="dcf74-122">This example retrieves a firewall and then gets a rule collection by name, calling method GetNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="dcf74-123">GetNetworkRuleCollectionByName metodunun kural koleksiyonu adı büyük/küçük harf duyarlı değildir.</span><span class="sxs-lookup"><span data-stu-id="dcf74-123">The rule collection name for method GetNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="dcf74-124">8: güvenlik duvarı alın ve güvenlik duvarından bir uygulama kuralı koleksiyonunu ada göre kaldır</span><span class="sxs-lookup"><span data-stu-id="dcf74-124">8:  Retrieve a firewall and then remove a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="dcf74-125">Bu örnekte bir güvenlik duvarı ve ardından bir kural koleksiyonunu ada göre kaldırır</span><span class="sxs-lookup"><span data-stu-id="dcf74-125">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="dcf74-126">RemoveApplicationRuleCollectionByName metodunun kural koleksiyonu adı büyük/küçük harf duyarlı değildir.</span><span class="sxs-lookup"><span data-stu-id="dcf74-126">The rule collection name for method RemoveApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="dcf74-127">9: güvenlik duvarını alın ve güvenlik duvarından bir ağ kuralı koleksiyonunu ada göre kaldırın</span><span class="sxs-lookup"><span data-stu-id="dcf74-127">9:  Retrieve a firewall and then remove a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="dcf74-128">Bu örnekte, bir güvenlik duvarı ve ardından bir kural koleksiyonunu ada göre kaldırır</span><span class="sxs-lookup"><span data-stu-id="dcf74-128">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="dcf74-129">Yöntem RemoveNetworkRuleCollectionByName için kural koleksiyonu adı büyük/küçük harf duyarlı değildir.</span><span class="sxs-lookup"><span data-stu-id="dcf74-129">The rule collection name for method RemoveNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="dcf74-130">10: güvenlik duvarını alın ve güvenlik duvarını ayırın</span><span class="sxs-lookup"><span data-stu-id="dcf74-130">10:  Retrieve a firewall and then allocate the firewall</span></span>
```
$vnet=Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName "rgName"
$publicIp=Get-AzPublicIpAddress -Name "firewallpip" -ResourceGroupName "rgName"
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.Allocate($vnet, $publicIp)
```

<span data-ttu-id="dcf74-131">Bu örnekte, güvenlik duvarındaki güvenlik duvarı ve çağrı çağrıları, güvenlik duvarıyla ilişkili yapılandırmayı (uygulama ve ağ kuralı koleksiyonlarını) kullanarak güvenlik duvarı hizmetini başlatacak şekilde alınır.</span><span class="sxs-lookup"><span data-stu-id="dcf74-131">This example retrieves a firewall and calls Allocate on the firewall to start the firewall service using the configuration (application and network rule collections) associated with the firewall.</span></span>

## <span data-ttu-id="dcf74-132">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dcf74-132">PARAMETERS</span></span>

### <span data-ttu-id="dcf74-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcf74-133">-DefaultProfile</span></span>
<span data-ttu-id="dcf74-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dcf74-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dcf74-135">-Ad</span><span class="sxs-lookup"><span data-stu-id="dcf74-135">-Name</span></span>
<span data-ttu-id="dcf74-136">Bu cmdlet 'in aldığı güvenlik duvarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dcf74-136">Specifies the name of the Firewall that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="dcf74-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcf74-137">-ResourceGroupName</span></span>
<span data-ttu-id="dcf74-138">Güvenlik duvarının ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dcf74-138">Specifies the name of the resource group that Firewall belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="dcf74-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcf74-139">CommonParameters</span></span>
<span data-ttu-id="dcf74-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dcf74-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcf74-141">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="dcf74-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcf74-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dcf74-142">INPUTS</span></span>

### <span data-ttu-id="dcf74-143">System. String</span><span class="sxs-lookup"><span data-stu-id="dcf74-143">System.String</span></span>

## <span data-ttu-id="dcf74-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dcf74-144">OUTPUTS</span></span>

### <span data-ttu-id="dcf74-145">Microsoft. Azure. Commands. Network. modeller. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="dcf74-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="dcf74-146">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. modeller. PSAzureFirewall, Microsoft. Azure. PowerShell. cmdlet. Network, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="dcf74-146">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="dcf74-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dcf74-147">NOTES</span></span>

## <span data-ttu-id="dcf74-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dcf74-148">RELATED LINKS</span></span>

[<span data-ttu-id="dcf74-149">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="dcf74-149">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="dcf74-150">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="dcf74-150">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="dcf74-151">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="dcf74-151">Set-AzFirewall</span></span>](./Set-AzFirewall.md)