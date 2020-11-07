---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 91D58F60-F22A-454A-B04C-E5AEF33E9D06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewall.md
ms.openlocfilehash: cdaa9689919d2e307434d888b435dad9d29e105e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764619"
---
# <span data-ttu-id="e414e-101">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="e414e-101">Get-AzureRmFirewall</span></span>

## <span data-ttu-id="e414e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e414e-102">SYNOPSIS</span></span>
<span data-ttu-id="e414e-103">Bir Azure Güvenlik Duvarı alır.</span><span class="sxs-lookup"><span data-stu-id="e414e-103">Gets a Azure Firewall.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e414e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e414e-104">SYNTAX</span></span>

```
Get-AzureRmFirewall [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e414e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e414e-105">DESCRIPTION</span></span>
<span data-ttu-id="e414e-106">**Get-AzureRmFirewall** cmdlet 'i bir kaynak grubunda bir veya daha fazla güvenlik duvarını alır.</span><span class="sxs-lookup"><span data-stu-id="e414e-106">The **Get-AzureRmFirewall** cmdlet gets one or more Firewalls in a resource group.</span></span>

## <span data-ttu-id="e414e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e414e-107">EXAMPLES</span></span>

### <span data-ttu-id="e414e-108">1: kaynak grubundaki tüm güvenlik duvarlarını alma</span><span class="sxs-lookup"><span data-stu-id="e414e-108">1:  Retrieve all Firewalls in a resource group</span></span>
```
Get-AzureRmFirewall -ResourceGroupName rgName
```

<span data-ttu-id="e414e-109">Bu örnekte, "rgName" kaynak grubundaki tüm güvenlik duvarları alınır.</span><span class="sxs-lookup"><span data-stu-id="e414e-109">This example retrieves all Firewalls in resource group "rgName".</span></span>

### <span data-ttu-id="e414e-110">2: ada göre bir güvenlik duvarı alma</span><span class="sxs-lookup"><span data-stu-id="e414e-110">2:  Retrieve a Firewall by name</span></span>
```
Get-AzureRmFirewall -ResourceGroupName rgName -Name azFw
```

<span data-ttu-id="e414e-111">Bu örnekte, "rgName" kaynak grubunda "azFw" adlı güvenlik duvarı alınır.</span><span class="sxs-lookup"><span data-stu-id="e414e-111">This example retrieves Firewall named "azFw" in resource group "rgName".</span></span>

### <span data-ttu-id="e414e-112">3: güvenlik duvarı alın ve güvenlik duvarına uygulama kuralı koleksiyonu ekleyin</span><span class="sxs-lookup"><span data-stu-id="e414e-112">3:  Retrieve a firewall and then add a application rule collection to the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$appRule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$appRuleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $appRule -ActionType "Allow"
$azFw.AddApplicationRuleCollection($appRuleCollection)
```

<span data-ttu-id="e414e-113">Bu örnek bir güvenlik duvarı alır ve güvenlik duvarına bir uygulama kuralı koleksiyonu ekleyerek AddApplicationRuleCollection metodunu çağırarak.</span><span class="sxs-lookup"><span data-stu-id="e414e-113">This example retrieves a firewall, then adds a application rule collection to the firewall by calling method AddApplicationRuleCollection.</span></span>

### <span data-ttu-id="e414e-114">4: güvenlik duvarı alın ve güvenlik duvarına bir ağ kuralı koleksiyonu ekleyin</span><span class="sxs-lookup"><span data-stu-id="e414e-114">4:  Retrieve a firewall and then add a network rule collection to the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$netRule = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol "Udp" -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$netRuleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $netRule -ActionType "Allow"
$azFw.AddNetworkRuleCollection($netRuleCollection)
```

<span data-ttu-id="e414e-115">Bu örnek bir güvenlik duvarı alır ve ardından AddNetworkRuleCollection metodunu çağırarak güvenlik duvarına bir ağ kuralı koleksiyonu ekler.</span><span class="sxs-lookup"><span data-stu-id="e414e-115">This example retrieves a firewall, then adds a network rule collection to the firewall by calling method AddNetworkRuleCollection.</span></span>

### <span data-ttu-id="e414e-116">5: güvenlik duvarı alın ve güvenlik duvarından ada göre uygulama kuralı koleksiyonunu geri alın</span><span class="sxs-lookup"><span data-stu-id="e414e-116">5:  Retrieve a firewall and then retrieve a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getAppRc=$azFw.GetApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="e414e-117">Bu örnekte, bir güvenlik duvarı alınır ve ardından, güvenlik duvarı nesnesinde GetApplicationRuleCollectionByName metodunu çağıran bir kural koleksiyonunu ada göre alır.</span><span class="sxs-lookup"><span data-stu-id="e414e-117">This example retrieves a firewall and then gets a rule collection by name, calling method GetApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="e414e-118">GetApplicationRuleCollectionByName metodunun kural koleksiyonu adı büyük/küçük harf duyarlı değildir.</span><span class="sxs-lookup"><span data-stu-id="e414e-118">The rule collection name for method GetApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="e414e-119">6: güvenlik duvarı alın ve güvenlik duvarından bir ağ kuralı koleksiyonunu ada göre geri alın</span><span class="sxs-lookup"><span data-stu-id="e414e-119">6:  Retrieve a firewall and then retrieve a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getNetRc=$azFw.GetNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="e414e-120">Bu örnekte bir güvenlik duvarı ve ardından bir kural koleksiyonunu ada göre alır</span><span class="sxs-lookup"><span data-stu-id="e414e-120">This example retrieves a firewall and then gets a rule collection by name, calling method GetNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="e414e-121">GetNetworkRuleCollectionByName metodunun kural koleksiyonu adı büyük/küçük harf duyarlı değildir.</span><span class="sxs-lookup"><span data-stu-id="e414e-121">The rule collection name for method GetNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="e414e-122">7: güvenlik duvarını alın ve güvenlik duvarından bir uygulama kuralı koleksiyonunu ada göre kaldırın</span><span class="sxs-lookup"><span data-stu-id="e414e-122">7:  Retrieve a firewall and then remove a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="e414e-123">Bu örnekte bir güvenlik duvarı ve ardından bir kural koleksiyonunu ada göre kaldırır</span><span class="sxs-lookup"><span data-stu-id="e414e-123">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="e414e-124">RemoveApplicationRuleCollectionByName metodunun kural koleksiyonu adı büyük/küçük harf duyarlı değildir.</span><span class="sxs-lookup"><span data-stu-id="e414e-124">The rule collection name for method RemoveApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="e414e-125">8: güvenlik duvarı alın ve güvenlik duvarından ada göre bir ağ kuralı koleksiyonunu kaldırın</span><span class="sxs-lookup"><span data-stu-id="e414e-125">8:  Retrieve a firewall and then remove a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="e414e-126">Bu örnekte, bir güvenlik duvarı ve ardından bir kural koleksiyonunu ada göre kaldırır</span><span class="sxs-lookup"><span data-stu-id="e414e-126">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="e414e-127">Yöntem RemoveNetworkRuleCollectionByName için kural koleksiyonu adı büyük/küçük harf duyarlı değildir.</span><span class="sxs-lookup"><span data-stu-id="e414e-127">The rule collection name for method RemoveNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="e414e-128">9: güvenlik duvarını alın ve güvenlik duvarını ayırın</span><span class="sxs-lookup"><span data-stu-id="e414e-128">9:  Retrieve a firewall and then allocate the firewall</span></span>
```
$vnet=Get-AzureRmVirtualNetwork -Name "vnet" -ResourceGroupName "rgName"
$publicIp=Get-AzureRmPublicIpAddress -Name "firewallpip" -ResourceGroupName "rgName"
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.Allocate($vnet, $publicIp)
```

<span data-ttu-id="e414e-129">Bu örnekte, güvenlik duvarındaki güvenlik duvarı ve çağrı çağrıları, güvenlik duvarıyla ilişkili yapılandırmayı (uygulama ve ağ kuralı koleksiyonlarını) kullanarak güvenlik duvarı hizmetini başlatacak şekilde alınır.</span><span class="sxs-lookup"><span data-stu-id="e414e-129">This example retrieves a firewall and calls Allocate on the firewall to start the firewall service using the configuration (application and network rule collections) associated with the firewall.</span></span>

## <span data-ttu-id="e414e-130">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e414e-130">PARAMETERS</span></span>

### <span data-ttu-id="e414e-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e414e-131">-DefaultProfile</span></span>
<span data-ttu-id="e414e-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e414e-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e414e-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="e414e-133">-Name</span></span>
<span data-ttu-id="e414e-134">Bu cmdlet 'in aldığı güvenlik duvarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e414e-134">Specifies the name of the Firewall that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e414e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e414e-135">-ResourceGroupName</span></span>
<span data-ttu-id="e414e-136">Güvenlik duvarının ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e414e-136">Specifies the name of the resource group that Firewall belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e414e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e414e-137">CommonParameters</span></span>
<span data-ttu-id="e414e-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e414e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e414e-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e414e-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e414e-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e414e-140">INPUTS</span></span>

### <span data-ttu-id="e414e-141">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e414e-141">None</span></span>
<span data-ttu-id="e414e-142">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="e414e-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e414e-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e414e-143">OUTPUTS</span></span>

### <span data-ttu-id="e414e-144">Microsoft. Azure. Commands. Network. modeller. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="e414e-144">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="e414e-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e414e-145">NOTES</span></span>

## <span data-ttu-id="e414e-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e414e-146">RELATED LINKS</span></span>

[<span data-ttu-id="e414e-147">Yeni-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="e414e-147">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="e414e-148">Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="e414e-148">Remove-AzureRmFirewall</span></span>](./Remove-AzureRmFirewall.md)

[<span data-ttu-id="e414e-149">Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="e414e-149">Set-AzureRmFirewall</span></span>](./Set-AzureRmFirewall.md)
