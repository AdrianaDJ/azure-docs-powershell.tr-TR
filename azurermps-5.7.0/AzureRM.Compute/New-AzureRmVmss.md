---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmss.md
ms.openlocfilehash: e94cc565c2f22134f6bd4092247fbfa1f5a98b8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588976"
---
# <span data-ttu-id="5b592-101">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5b592-101">New-AzureRmVmss</span></span>

## <span data-ttu-id="5b592-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b592-102">SYNOPSIS</span></span>
<span data-ttu-id="5b592-103">Bir VMSS oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5b592-103">Creates a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b592-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5b592-104">SYNTAX</span></span>

```
New-AzureRmVmss [-ResourceGroupName] <String> -VMScaleSetName <String>
 [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b592-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5b592-105">DESCRIPTION</span></span>
<span data-ttu-id="5b592-106">**Yeni-AzureRmVmss** cmdlet 'i Azure 'Da sanal makine ölçek KÜMESI (VMSS) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5b592-106">The **New-AzureRmVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="5b592-107">Bu cmdlet giriş olarak bir **VirtualMachineScaleSet** nesnesi alır.</span><span class="sxs-lookup"><span data-stu-id="5b592-107">This cmdlet takes a **VirtualMachineScaleSet** object as input.</span></span>

## <span data-ttu-id="5b592-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5b592-108">EXAMPLES</span></span>

### <span data-ttu-id="5b592-109">Örnek 1: VMSS oluşturma</span><span class="sxs-lookup"><span data-stu-id="5b592-109">Example 1: Create a VMSS</span></span>
```
# Common
$LOC = "WestUs";
$RGName = "rgkyvms";

New-AzureRmResourceGroup -Name $RGName -Location $LOC -Force;

# SRP
$STOName = "STO" + $RGName;
$STOType = "Standard_GRS";
New-AzureRmStorageAccount -ResourceGroupName $RGName -Name $STOName -Location $LOC -Type $STOType;
$STOAccount = Get-AzureRmStorageAccount -ResourceGroupName $RGName -Name $STOName; 

# NRP
$SubNet = New-AzureRmVirtualNetworkSubnetConfig -Name ("subnet" + $RGName) -AddressPrefix "10.0.0.0/24";
$VNet = New-AzureRmVirtualNetwork -Force -Name ("vnet" + $RGName) -ResourceGroupName $RGName -Location $LOC -AddressPrefix "10.0.0.0/16" -DnsServer "10.1.1.1" -Subnet $SubNet;
$VNet = Get-AzureRmVirtualNetwork -Name ('vnet' + $RGName) -ResourceGroupName $RGName;
$SubNetId = $VNet.Subnets[0].Id;

$PubIP = New-AzureRmPublicIpAddress -Force -Name ("PubIP" + $RGName) -ResourceGroupName $RGName -Location $LOC -AllocationMethod Dynamic -DomainNameLabel ("PubIP" + $RGName);
$PubIP = Get-AzureRmPublicIpAddress -Name ("PubIP"  + $RGName) -ResourceGroupName $RGName;

# Create LoadBalancer
$FrontendName = "fe" + $RGName
$BackendAddressPoolName = "bepool" + $RGName
$ProbeName = "vmssprobe" + $RGName
$InboundNatPoolName  = "innatpool" + $RGName
$LBRuleName = "lbrule" + $RGName
$LBName = "vmsslb" + $RGName

$Frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name $FrontendName -PublicIpAddress $PubIP
$BackendAddressPool = New-AzureRmLoadBalancerBackendAddressPoolConfig -Name $BackendAddressPoolName
$Probe = New-AzureRmLoadBalancerProbeConfig -Name $ProbeName -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
$InboundNatPool = New-AzureRmLoadBalancerInboundNatPoolConfig -Name $InboundNatPoolName  -FrontendIPConfigurationId `
    $Frontend.Id -Protocol Tcp -FrontendPortRangeStart 3360 -FrontendPortRangeEnd 3362 -BackendPort 3370;
$LBRule = New-AzureRmLoadBalancerRuleConfig -Name $LBRuleName `
    -FrontendIPConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 `
    -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP;
$ActualLb = New-AzureRmLoadBalancer -Name $LBName -ResourceGroupName $RGName -Location $LOC `
    -FrontendIpConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -LoadBalancingRule $LBRule -InboundNatPool $InboundNatPool;
$ExpectedLb = Get-AzureRmLoadBalancer -Name $LBName -ResourceGroupName $RGName

# New VMSS Parameters
$VMSSName = "VMSS" + $RGName;

$AdminUsername = "Admin01";
$AdminPassword = "p4ssw0rd@123" + $RGName;

$PublisherName = "MicrosoftWindowsServer" 
$Offer         = "WindowsServer" 
$Sku           = "2012-R2-Datacenter" 
$Version       = "latest"
        
$VHDContainer = "https://" + $STOName + ".blob.core.contoso.net/" + $VMSSName;

$ExtName = "CSETest";
$Publisher = "Microsoft.Compute";
$ExtType = "BGInfo";
$ExtVer = "2.1";

#IP Config for the NIC
$IPCfg = New-AzureRmVmssIPConfig -Name "Test" `
    -LoadBalancerInboundNatPoolsId $ExpectedLb.InboundNatPools[0].Id `
    -LoadBalancerBackendAddressPoolsId $ExpectedLb.BackendAddressPools[0].Id `
    -SubnetId $SubNetId;
            
#VMSS Config
$VMSS = New-AzureRmVmssConfig -Location $LOC -SkuCapacity 2 -SkuName "Standard_A2" -UpgradePolicyMode "Automatic" `
    | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
    | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test2"  -IPConfiguration $IPCfg `
    | Set-AzureRmVmssOSProfile -ComputerNamePrefix "Test"  -AdminUsername $AdminUsername -AdminPassword $AdminPassword `
    | Set-AzureRmVmssStorageProfile -Name "Test"  -OsDiskCreateOption 'FromImage' -OsDiskCaching "None" `
    -ImageReferenceOffer $Offer -ImageReferenceSku $Sku -ImageReferenceVersion $Version `
    -ImageReferencePublisher $PublisherName -VhdContainer $VHDContainer `
    | Add-AzureRmVmssExtension -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True

#Create the VMSS
New-AzureRmVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="5b592-110">Aşağıdaki karmaşık örnek bir VMSS oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5b592-110">The following complex example creates a VMSS.</span></span>
<span data-ttu-id="5b592-111">İlk komut belirtilen ad ve konuma sahip bir kaynak grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5b592-111">The first command creates a resource group with the specified name and location.</span></span>
<span data-ttu-id="5b592-112">İkinci komut, depolama hesabı oluşturmak için **New-AzureRmStorageAccount** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="5b592-112">The second command uses the **New-AzureRmStorageAccount** cmdlet to create a storage account.</span></span>
<span data-ttu-id="5b592-113">Üçüncü komut, **Get-AzureRmStorageAccount** cmdlet 'ini kullanarak ikinci komutta oluşturulmuş depolama hesabını alır ve sonucu $STOAccount değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="5b592-113">The third command then uses the **Get-AzureRmStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
<span data-ttu-id="5b592-114">Beşinci komut, bir alt ağ oluşturmak için **New-AzureRmVirtualNetworkSubnetConfig** cmdlet 'ini kullanır ve sonucu $SubNet adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="5b592-114">The fifth command uses the **New-AzureRmVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
<span data-ttu-id="5b592-115">Altıncı komut, sanal bir ağ oluşturmak için **New-AzureRmVirtualNetwork** cmdlet 'ini kullanır ve sonucu $VNET adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="5b592-115">The sixth command uses the **New-AzureRmVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
<span data-ttu-id="5b592-116">Yedinci komutu, altıncı komutta oluşturulan sanal ağ hakkında bilgi almak için **Get-AzureRmVirtualNetwork** kullanır ve $VNET adlı değişkende bu bilgileri depolar.</span><span class="sxs-lookup"><span data-stu-id="5b592-116">The seventh command uses the **Get-AzureRmVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
<span data-ttu-id="5b592-117">Sekizinci ve dokuzuncu komutu, bu genel IP adresinden bilgi oluşturmak ve almak için **New-azurermpublicıpaddress** ve **Get-azurermpublicıpaddress** kullanır.</span><span class="sxs-lookup"><span data-stu-id="5b592-117">The eighth and ninth command uses the **New-AzureRmPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
<span data-ttu-id="5b592-118">Komutlar $PubIP adlı değişkende bilgileri depolar.</span><span class="sxs-lookup"><span data-stu-id="5b592-118">The commands store the information in the variable named $PubIP.</span></span>
<span data-ttu-id="5b592-119">Onuncu komutu, ön uç yük dengeleyicisi oluşturmak için **New-Azurermloadbalancerfrontendıconfıg** cmdlet 'ini kullanır ve sonucu $frontend adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="5b592-119">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
<span data-ttu-id="5b592-120">Onventh komutu, **Yeni-AzureRmLoadBalancerBackendAddressPoolConfig** öğesini kullanarak arka uç adres havuzu yapılandırması oluşturur ve sonucu $BackendAddressPool değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="5b592-120">The eleventh command uses the **New-AzureRmLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
<span data-ttu-id="5b592-121">İkinci komut, bir yoklama oluşturmak için **New-AzureRmLoadBalancerProbeConfig** öğesini kullanır ve $Probe adlı değişkende yoklama bilgilerini depolar.</span><span class="sxs-lookup"><span data-stu-id="5b592-121">The twelfth command uses the **New-AzureRmLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
<span data-ttu-id="5b592-122">Üçüncü on komutu, yük dengeleyici gelen ağ adresi çevirisi (NAT) havuz yapılandırması oluşturmak için **New-Azurermloadbalancerınboundnatpoolconfig** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="5b592-122">The thirteenth command uses the **New-AzureRmLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
<span data-ttu-id="5b592-123">On on komutu, yük dengeleyici kural yapılandırması oluşturmak için **New-AzureRmLoadBalancerRuleConfig** öğesini kullanır ve sonucu $LBRule değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="5b592-123">The fourteenth command uses the **New-AzureRmLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
<span data-ttu-id="5b592-124">On beşinci komut, bir yük dengeleyici oluşturmak için **New-AzureRmLoadBalancer** cmdlet 'ini kullanır ve sonucu $ActualLb adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="5b592-124">The fifteenth command uses the **New-AzureRmLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
<span data-ttu-id="5b592-125">Altıncı komut **Get-AzureRmLoadBalancer** 'ı kullanarak on beşinci komutta oluşturulmuş yük dengeleyici hakkında bilgi alır ve $ExpectedLb adlı değişkende bu bilgileri depolar.</span><span class="sxs-lookup"><span data-stu-id="5b592-125">The sixteenth command uses the **Get-AzureRmLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
<span data-ttu-id="5b592-126">On yedi komutu, bir VMSS IP yapılandırması oluşturmak için **New-AzureRmVmssIPConfig** cmdlet 'ini kullanır ve $IPCfg adlı değişkende bu bilgileri depolar.</span><span class="sxs-lookup"><span data-stu-id="5b592-126">The seventeenth command uses the **New-AzureRmVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
<span data-ttu-id="5b592-127">Sekizinci on komutu, bir VMSS yapılandırma nesnesi oluşturmak için **New-AzureRmVmssConfig** cmdlet 'ini kullanır ve sonucu $VMSS adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="5b592-127">The eighteenth command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="5b592-128">Nıneon komutu, VMSS 'yi oluşturmak için **New-AzureRmVmss** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="5b592-128">The nineteenth command uses the **New-AzureRmVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="5b592-129">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5b592-129">PARAMETERS</span></span>

### <span data-ttu-id="5b592-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b592-130">-ResourceGroupName</span></span>
<span data-ttu-id="5b592-131">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b592-131">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b592-132">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5b592-132">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="5b592-133">Bu cmdlet 'in oluşturduğu VMSS 'in özelliklerini içeren **VirtualMachineScaleSet** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b592-133">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b592-134">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="5b592-134">-VMScaleSetName</span></span>
<span data-ttu-id="5b592-135">Bu cmdlet 'in oluşturduğu VMSS 'nin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b592-135">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b592-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="5b592-136">-Confirm</span></span>
<span data-ttu-id="5b592-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5b592-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b592-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b592-138">-WhatIf</span></span>
<span data-ttu-id="5b592-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5b592-139">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="5b592-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5b592-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b592-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b592-141">CommonParameters</span></span>
<span data-ttu-id="5b592-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5b592-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b592-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b592-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b592-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5b592-144">INPUTS</span></span>

### <span data-ttu-id="5b592-145">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5b592-145">None</span></span>
<span data-ttu-id="5b592-146">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="5b592-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5b592-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5b592-147">OUTPUTS</span></span>

### <span data-ttu-id="5b592-148">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="5b592-148">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="5b592-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5b592-149">NOTES</span></span>

## <span data-ttu-id="5b592-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5b592-150">RELATED LINKS</span></span>

[<span data-ttu-id="5b592-151">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5b592-151">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="5b592-152">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5b592-152">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="5b592-153">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5b592-153">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="5b592-154">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5b592-154">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="5b592-155">Başlangıç-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5b592-155">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="5b592-156">Dur-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5b592-156">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="5b592-157">Güncelleştirme-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5b592-157">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


