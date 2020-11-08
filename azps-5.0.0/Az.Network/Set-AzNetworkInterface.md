---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
ms.openlocfilehash: 9b851bcbaa545dee99628dc066956854181df7f7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279196"
---
# <span data-ttu-id="285aa-101">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="285aa-101">Set-AzNetworkInterface</span></span>

## <span data-ttu-id="285aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="285aa-102">SYNOPSIS</span></span>
<span data-ttu-id="285aa-103">Ağ arabirimini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="285aa-103">Updates a network interface.</span></span>

## <span data-ttu-id="285aa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="285aa-104">SYNTAX</span></span>

```
Set-AzNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="285aa-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="285aa-105">DESCRIPTION</span></span>
<span data-ttu-id="285aa-106">**Set-Azağinterface** bir ağ arabirimini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="285aa-106">The **Set-AzNetworkInterface** updates a network interface.</span></span>

## <span data-ttu-id="285aa-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="285aa-107">EXAMPLES</span></span>

### <span data-ttu-id="285aa-108">Örnek 1: ağ arabirimini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="285aa-108">Example 1: Configure a network interface</span></span>
```
$Nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzNetworkInterface -NetworkInterface $Nic
```

<span data-ttu-id="285aa-109">Bu örnek, ağ arabirimini yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="285aa-109">This example configures a network interface.</span></span>
<span data-ttu-id="285aa-110">İlk komut NetworkInterface1 adındaki bir ağ arabirimini kaynak grubunda ResourceGroup1 alır.</span><span class="sxs-lookup"><span data-stu-id="285aa-110">The first command gets a network interface named NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="285aa-111">İkinci komut, IP yapılandırmasının özel IP adresini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="285aa-111">The second command sets the private IP address of the IP configuration.</span></span>
<span data-ttu-id="285aa-112">Üçüncü komut özel IP ayırma yöntemini statik olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="285aa-112">The third command sets the private IP allocation method to Static.</span></span>
<span data-ttu-id="285aa-113">Dördüncü komut ağ arabiriminde bir etiket ayarlar.</span><span class="sxs-lookup"><span data-stu-id="285aa-113">The fourth command sets a tag on the network interface.</span></span>
<span data-ttu-id="285aa-114">Beşinci komut, ağ arabirimini ayarlamak için $Nic değişkeninde depolanan bilgileri kullanır.</span><span class="sxs-lookup"><span data-stu-id="285aa-114">The fifth command uses the information stored in the $Nic variable to set the network interface.</span></span>

### <span data-ttu-id="285aa-115">Örnek 2: ağ arabirimindeki DNS ayarlarını değiştirme</span><span class="sxs-lookup"><span data-stu-id="285aa-115">Example 2: Change DNS settings on a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="285aa-116">İlk komut NetworkInterface1 adlı bir ağ arabirimini kaynak grubu ResourceGroup1 içinde var.</span><span class="sxs-lookup"><span data-stu-id="285aa-116">The first command gets a network interface named NetworkInterface1 that exists within resource group ResourceGroup1.</span></span> <span data-ttu-id="285aa-117">İkinci komut bu arabirime DNS sunucusu 192.168.1.100 ekler.</span><span class="sxs-lookup"><span data-stu-id="285aa-117">The second command adds DNS server 192.168.1.100 to this interface.</span></span> <span data-ttu-id="285aa-118">Üçüncü komut, bu değişiklikleri ağ arabiriminde uygular.</span><span class="sxs-lookup"><span data-stu-id="285aa-118">The third command applies these changes to the network interface.</span></span> <span data-ttu-id="285aa-119">DNS sunucusunu kaldırmak için yukarıda listelenen, ancak yerine konan komutları izleyin. "With" ekleyin. Remove "komutu</span><span class="sxs-lookup"><span data-stu-id="285aa-119">To remove a DNS server, follow the commands listed above, but replace ".Add" with ".Remove" in the second command.</span></span>

### <span data-ttu-id="285aa-120">Örnek 3: ağ arabiriminde IP iletmeyi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="285aa-120">Example 3: Enable IP forwarding on a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="285aa-121">İlk komut NetworkInterface1 adındaki mevcut bir ağ arabirimini alır ve $nic değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="285aa-121">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="285aa-122">İkinci komut, IP iletme değerini doğru olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="285aa-122">The second command changes the IP forwarding value to true.</span></span> <span data-ttu-id="285aa-123">Son olarak, üçüncü komut değişiklikleri ağ arabiriminde uygular.</span><span class="sxs-lookup"><span data-stu-id="285aa-123">Finally, the third command applies the changes to the network interface.</span></span> <span data-ttu-id="285aa-124">Ağ arabiriminde IP iletmeyi devre dışı bırakmak için örnek örneği izleyin, ancak ikinci komutu "$nic olarak değiştirdiğinizden emin olun. Enableipiletme = 0 ".</span><span class="sxs-lookup"><span data-stu-id="285aa-124">To disable IP forwarding on a network interface, follow the sample example, but be sure to change the second command to "$nic.EnableIPForwarding = 0".</span></span>

### <span data-ttu-id="285aa-125">Örnek 4: ağ arabiriminin alt ağını değiştirme</span><span class="sxs-lookup"><span data-stu-id="285aa-125">Example 4: Change the subnet of a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="285aa-126">İlk komut NetworkInterface1 ağ arabirimini alır ve $nic değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="285aa-126">The first command gets the network interface NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="285aa-127">İkinci komut, ağ arabiriminin ilişkilendirildiği alt ağla ilişkilendirilmiş sanal ağı alır.</span><span class="sxs-lookup"><span data-stu-id="285aa-127">The second command gets the virtual network associated with the subnet that the network interface is going to be associated with.</span></span> <span data-ttu-id="285aa-128">İkinci komut, alt ağı alır ve $subnet 2 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="285aa-128">The second command gets the subnet and stores it in the $subnet2 variable.</span></span> <span data-ttu-id="285aa-129">Yeni alt ağla ağ arabiriminin birincil özel IP adresini içeren üçüncü komut.</span><span class="sxs-lookup"><span data-stu-id="285aa-129">The third command associated the primary private IP address of the network interface with the new subnet.</span></span> <span data-ttu-id="285aa-130">Son komut, bu değişiklikleri ağ arabiriminde uyguladı.</span><span class="sxs-lookup"><span data-stu-id="285aa-130">Finally the last command applied these changes on the network interface.</span></span>
>[!NOTE] 
><span data-ttu-id="285aa-131">Alt ağı değiştirebilmeniz için IP yapılandırmalarının dinamik olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="285aa-131">The IP configurations must be dynamic before you can change the subnet.</span></span> <span data-ttu-id="285aa-132">Statik IP yapılandırmalarınız varsa, devam etmeden önce dinamik olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="285aa-132">If you have static IP configurations, change then to dynamic before proceeding.</span></span> 
>[!NOTE]
><span data-ttu-id="285aa-133">Ağ arabiriminin birden çok IP yapılandırması varsa, son Set-AzNetworkInterface komutu yürütülmeden önce ileri komutu tüm bu IP yapılandırmalarında tamamlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="285aa-133">If the network interface has multiple IP configurations, the forth command must be done for all these IP configurations before the final Set-AzNetworkInterface command is executed.</span></span> <span data-ttu-id="285aa-134">Bu, ileri komutunda olduğu gibi, "0" değerini uygun sayıyla değiştirerek yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="285aa-134">This can be done as in the forth command but by replacing "0" with the appropriate number.</span></span> <span data-ttu-id="285aa-135">Ağ arabiriminde N IP yapılandırması varsa, bu komutların N-1 olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="285aa-135">If a network interface has N IP configurations, then N-1 of these commands must exist.</span></span>

### <span data-ttu-id="285aa-136">Örnek 5: ağ güvenlik grubunu ağ arabirimiyle Ilişkilendirme/Ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="285aa-136">Example 5: Associate/Dissociate a Network Security Group to a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="285aa-137">İlk komut NetworkInterface1 adındaki mevcut bir ağ arabirimini alır ve $nic değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="285aa-137">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="285aa-138">İkinci komut MyNSG adlı varolan bir ağ güvenlik grubunu alır ve $nsg değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="285aa-138">The second command gets an existing network security group called MyNSG and stores it in the $nsg variable.</span></span> <span data-ttu-id="285aa-139">Üçüncü komut $nsg $nic atar.</span><span class="sxs-lookup"><span data-stu-id="285aa-139">The third command assigns the $nsg to the $nic.</span></span> <span data-ttu-id="285aa-140">Son olarak, ileri komutu, değişiklikleri ağ arabiriminde uygular.</span><span class="sxs-lookup"><span data-stu-id="285aa-140">Finally, the forth command applies the changes to the Network interface.</span></span> <span data-ttu-id="285aa-141">Ağ güvenliği gruplarının ağ arabiriminden ilişkisini kaldırmak için, üçüncü komutta $null $nsg basit değiştirme 'yi.</span><span class="sxs-lookup"><span data-stu-id="285aa-141">To dissociate network security groups from a network interface, simple replace $nsg in the third command with $null.</span></span>

## <span data-ttu-id="285aa-142">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="285aa-142">PARAMETERS</span></span>

### <span data-ttu-id="285aa-143">-Iş</span><span class="sxs-lookup"><span data-stu-id="285aa-143">-AsJob</span></span>
<span data-ttu-id="285aa-144">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="285aa-144">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="285aa-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="285aa-145">-DefaultProfile</span></span>
<span data-ttu-id="285aa-146">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="285aa-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="285aa-147">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="285aa-147">-NetworkInterface</span></span>
<span data-ttu-id="285aa-148">Ağ arabiriminin ayarlanması gereken durumu temsil eden bir ağ arabirimi nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="285aa-148">Specifies a network interface object representing the state to which the network interface should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="285aa-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="285aa-149">CommonParameters</span></span>
<span data-ttu-id="285aa-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="285aa-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="285aa-151">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="285aa-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="285aa-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="285aa-152">INPUTS</span></span>

### <span data-ttu-id="285aa-153">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="285aa-153">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="285aa-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="285aa-154">OUTPUTS</span></span>

### <span data-ttu-id="285aa-155">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="285aa-155">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="285aa-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="285aa-156">NOTES</span></span>

## <span data-ttu-id="285aa-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="285aa-157">RELATED LINKS</span></span>

[<span data-ttu-id="285aa-158">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="285aa-158">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="285aa-159">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="285aa-159">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="285aa-160">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="285aa-160">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="285aa-161">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="285aa-161">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)
