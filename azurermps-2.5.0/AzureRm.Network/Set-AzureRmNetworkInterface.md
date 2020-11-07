---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkinterface
schema: 2.0.0
ms.openlocfilehash: 978db7296b9789f738f5b277a4bf3731803fdcd8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939875"
---
# <span data-ttu-id="7d78d-101">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7d78d-101">Set-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="7d78d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d78d-102">SYNOPSIS</span></span>
<span data-ttu-id="7d78d-103">Ağ arabiriminin hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7d78d-103">Sets the goal state for a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d78d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7d78d-104">SYNTAX</span></span>

```
Set-AzureRmNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d78d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7d78d-105">DESCRIPTION</span></span>
<span data-ttu-id="7d78d-106">**Set-Azurermnetworkınterface** , bir Azure ağ arabiriminin hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7d78d-106">The **Set-AzureRmNetworkInterface** sets the goal state for an Azure network interface.</span></span>

## <span data-ttu-id="7d78d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7d78d-107">EXAMPLES</span></span>

### <span data-ttu-id="7d78d-108">Örnek 1: ağ arabirimini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="7d78d-108">Example 1: Configure a network interface</span></span>
```
$Nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzureRmNetworkInterface -NetworkInterface $Nic
```

<span data-ttu-id="7d78d-109">Bu örnek, ağ arabirimini yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="7d78d-109">This example configures a network interface.</span></span>
<span data-ttu-id="7d78d-110">İlk komut NetworkInterface1 adındaki bir ağ arabirimini kaynak grubunda ResourceGroup1 alır.</span><span class="sxs-lookup"><span data-stu-id="7d78d-110">The first command gets a network interface named NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="7d78d-111">İkinci komut, IP yapılandırmasının özel IP adresini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7d78d-111">The second command sets the private IP address of the IP configuration.</span></span>
<span data-ttu-id="7d78d-112">Üçüncü komut özel IP ayırma yöntemini statik olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7d78d-112">The third command sets the private IP allocation method to Static.</span></span>
<span data-ttu-id="7d78d-113">Dördüncü komut ağ arabiriminde bir etiket ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7d78d-113">The fourth command sets a tag on the network interface.</span></span>
<span data-ttu-id="7d78d-114">Beşinci komut, ağ arabirimini ayarlamak için $Nic değişkeninde depolanan bilgileri kullanır.</span><span class="sxs-lookup"><span data-stu-id="7d78d-114">The fifth command uses the information stored in the $Nic variable to set the network interface.</span></span>

### <span data-ttu-id="7d78d-115">Örnek 2: ağ arabirimindeki DNS ayarlarını değiştirme</span><span class="sxs-lookup"><span data-stu-id="7d78d-115">Example 2: Change DNS settings on a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="7d78d-116">İlk komut NetworkInterface1 adlı bir ağ arabirimini kaynak grubu ResourceGroup1 içinde var.</span><span class="sxs-lookup"><span data-stu-id="7d78d-116">The first command gets a network interface named NetworkInterface1 that exists within resource group ResourceGroup1.</span></span> <span data-ttu-id="7d78d-117">İkinci komut bu arabirime DNS sunucusu 192.168.1.100 ekler.</span><span class="sxs-lookup"><span data-stu-id="7d78d-117">The second command adds DNS server 192.168.1.100 to this interface.</span></span> <span data-ttu-id="7d78d-118">Üçüncü komut, bu değişiklikleri ağ arabiriminde uygular.</span><span class="sxs-lookup"><span data-stu-id="7d78d-118">The third command applies these changes to the network interface.</span></span> <span data-ttu-id="7d78d-119">DNS sunucusunu kaldırmak için yukarıda listelenen, ancak yerine konan komutları izleyin. "With" ekleyin. Remove "komutu</span><span class="sxs-lookup"><span data-stu-id="7d78d-119">To remove a DNS server, follow the commands listed above, but replace ".Add" with ".Remove" in the second command.</span></span>

### <span data-ttu-id="7d78d-120">Örnek 3: ağ arabiriminde IP özelliğini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="7d78d-120">Example 3: Enable IP forwading on a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="7d78d-121">İlk komut NetworkInterface1 adındaki mevcut bir ağ arabirimini alır ve $nic değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7d78d-121">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="7d78d-122">İkinci komut, IP iletme değerini doğru olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7d78d-122">The second command changes the IP forwarding value to true.</span></span> <span data-ttu-id="7d78d-123">Son olarak, üçüncü komut değişiklikleri ağ arabiriminde uygular.</span><span class="sxs-lookup"><span data-stu-id="7d78d-123">Finally, the third command applies the changes to the network interface.</span></span> <span data-ttu-id="7d78d-124">Ağ arabiriminde IP iletmeyi devre dışı bırakmak için örnek örneği izleyin, ancak ikinci komutu "$nic olarak değiştirdiğinizden emin olun. Enableipiletme = 0 ".</span><span class="sxs-lookup"><span data-stu-id="7d78d-124">To disable IP forwarding on a network interface, follow the sample example, but be sure to change the second command to "$nic.EnableIPForwarding = 0".</span></span>

### <span data-ttu-id="7d78d-125">Örnek 4: ağ arabiriminin alt ağını değiştirme</span><span class="sxs-lookup"><span data-stu-id="7d78d-125">Example 4: Change the subnet of a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzureRmVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzureRmVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="7d78d-126">İlk komut NetworkInterface1 ağ arabirimini alır ve $nic değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7d78d-126">The first command gets the network interface NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="7d78d-127">İkinci komut, ağ arabiriminin ilişkilendirildiği alt ağla ilişkilendirilmiş sanal ağı alır.</span><span class="sxs-lookup"><span data-stu-id="7d78d-127">The second command gets the virtual network associated with the subnet that the network interface is going to be associated with.</span></span> <span data-ttu-id="7d78d-128">İkinci komut, alt ağı alır ve $subnet 2 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7d78d-128">The second command gets the subnet and stores it in the $subnet2 variable.</span></span> <span data-ttu-id="7d78d-129">Yeni alt ağla ağ arabiriminin birincil özel IP adresini içeren üçüncü komut.</span><span class="sxs-lookup"><span data-stu-id="7d78d-129">The third command associated the primary private IP address of the network interface with the new subnet.</span></span> <span data-ttu-id="7d78d-130">Son komut, bu değişiklikleri ağ arabiriminde uyguladı.</span><span class="sxs-lookup"><span data-stu-id="7d78d-130">Finally the last command applied these changes on the network interface.</span></span>

>[!NOTE] 
><span data-ttu-id="7d78d-131">Alt ağı değiştirebilmeniz için IP yapılandırmalarının dinamik olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="7d78d-131">The IP configurations must be dynamic before you can change the subnet.</span></span> <span data-ttu-id="7d78d-132">Statik IP yapılandırmalarınız varsa, devam etmeden önce dinamik olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="7d78d-132">If you have static IP configurations, change then to dynamic before proceeding.</span></span> 

>[!NOTE]
><span data-ttu-id="7d78d-133">Ağ arabiriminin birden çok IP yapılandırması varsa, son Set-AzureRmNetworkInterface komutu yürütülmeden önce ileri komutu tüm bu IP yapılandırmalarında tamamlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7d78d-133">If the network interface has multiple IP configurations, the forth command must be done for all these IP configurations before the final Set-AzureRmNetworkInterface command is executed.</span></span> <span data-ttu-id="7d78d-134">Bu, ileri komutunda olduğu gibi, "0" değerini uygun sayıyla değiştirerek yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="7d78d-134">This can be done as in the forth command but by replacing "0" with the appropriate number.</span></span> <span data-ttu-id="7d78d-135">Ağ arabiriminde N IP yapılandırması varsa, bu komutların N-1 olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="7d78d-135">If a network interface has N IP configurations, then N-1 of these commands must exist.</span></span>

### <span data-ttu-id="7d78d-136">Örnek 5: ağ güvenlik grubunu ağ arabirimiyle Ilişkilendirme/Ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="7d78d-136">Example 5: Associate/Dissociate a Network Security Group to a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="7d78d-137">İlk komut NetworkInterface1 adındaki mevcut bir ağ arabirimini alır ve $nic değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7d78d-137">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="7d78d-138">İkinci komut MyNSG adlı varolan bir ağ güvenlik grubunu alır ve $nsg değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7d78d-138">The second command gets an existing network security group called MyNSG and stores it in the $nsg variable.</span></span> <span data-ttu-id="7d78d-139">İleri komutu $nic $nsg atar.</span><span class="sxs-lookup"><span data-stu-id="7d78d-139">The forth command assigns the $nsg to the $nic.</span></span> <span data-ttu-id="7d78d-140">Son olarak, beşinci komut, değişiklikleri ağ arabiriminde uygular.</span><span class="sxs-lookup"><span data-stu-id="7d78d-140">Finally, the fifth command applies the changes to the Network interface.</span></span> <span data-ttu-id="7d78d-141">Ağ güvenliği gruplarının ağ arabiriminden ilişkisini kaldırmak için, ileri komutundaki $nsg $null ile basit değiştirme 'yi.</span><span class="sxs-lookup"><span data-stu-id="7d78d-141">To dissociate network security groups from a network interface, simple replace $nsg in the forth command with $null.</span></span>

## <span data-ttu-id="7d78d-142">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7d78d-142">PARAMETERS</span></span>

### <span data-ttu-id="7d78d-143">-Iş</span><span class="sxs-lookup"><span data-stu-id="7d78d-143">-AsJob</span></span>
<span data-ttu-id="7d78d-144">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="7d78d-144">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7d78d-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d78d-145">-DefaultProfile</span></span>
<span data-ttu-id="7d78d-146">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7d78d-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d78d-147">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7d78d-147">-NetworkInterface</span></span>
<span data-ttu-id="7d78d-148">Ağ arabiriminin hedef durumunu temsil eden bir **NetworkInterface** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d78d-148">Specifies a **NetworkInterface** object that represents the goal state for a network interface.</span></span>

```yaml
Type: PSNetworkInterface
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d78d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d78d-149">CommonParameters</span></span>
<span data-ttu-id="7d78d-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7d78d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d78d-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d78d-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d78d-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7d78d-152">INPUTS</span></span>

### <span data-ttu-id="7d78d-153">Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="7d78d-153">PSNetworkInterface</span></span>
<span data-ttu-id="7d78d-154">Parametre ' NetworkInterface ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="7d78d-154">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="7d78d-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7d78d-155">OUTPUTS</span></span>

### <span data-ttu-id="7d78d-156">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="7d78d-156">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="7d78d-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7d78d-157">NOTES</span></span>

## <span data-ttu-id="7d78d-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7d78d-158">RELATED LINKS</span></span>

[<span data-ttu-id="7d78d-159">Get-Azurermnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="7d78d-159">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="7d78d-160">Get-Azurermnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="7d78d-160">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="7d78d-161">Yeni-Azurermnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="7d78d-161">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="7d78d-162">Remove-Azurermnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="7d78d-162">Remove-AzureRmNetworkInterface</span></span>](./Remove-AzureRmNetworkInterface.md)
