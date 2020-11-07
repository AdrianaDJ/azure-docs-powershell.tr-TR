---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmss
schema: 2.0.0
ms.openlocfilehash: f93e05448278e2aaa70ff226a5d3618fdad0e6b4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939782"
---
# <span data-ttu-id="b4a0f-101">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b4a0f-101">New-AzureRmVmss</span></span>

## <span data-ttu-id="b4a0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4a0f-102">SYNOPSIS</span></span>
<span data-ttu-id="b4a0f-103">Bir VMSS oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-103">Creates a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4a0f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b4a0f-104">SYNTAX</span></span>

### <span data-ttu-id="b4a0f-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b4a0f-105">DefaultParameter (Default)</span></span>
```
New-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4a0f-106">SimpleParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4a0f-106">SimpleParameterSet</span></span>
```
New-AzureRmVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4a0f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b4a0f-107">DESCRIPTION</span></span>
<span data-ttu-id="b4a0f-108">**Yeni-AzureRmVmss** cmdlet 'i Azure 'Da sanal makine ölçek KÜMESI (VMSS) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-108">The **New-AzureRmVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="b4a0f-109">Bu cmdlet giriş olarak bir **VirtualMachineScaleSet** nesnesi alır.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-109">This cmdlet takes a **VirtualMachineScaleSet** object as input.</span></span>

## <span data-ttu-id="b4a0f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b4a0f-110">EXAMPLES</span></span>

### <span data-ttu-id="b4a0f-111">Örnek 1: VMSS oluşturma</span><span class="sxs-lookup"><span data-stu-id="b4a0f-111">Example 1: Create a VMSS</span></span>
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

<span data-ttu-id="b4a0f-112">Aşağıdaki karmaşık örnek bir VMSS oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-112">The following complex example creates a VMSS.</span></span>
<span data-ttu-id="b4a0f-113">İlk komut belirtilen ad ve konuma sahip bir kaynak grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-113">The first command creates a resource group with the specified name and location.</span></span>
<span data-ttu-id="b4a0f-114">İkinci komut, depolama hesabı oluşturmak için **New-AzureRmStorageAccount** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-114">The second command uses the **New-AzureRmStorageAccount** cmdlet to create a storage account.</span></span>
<span data-ttu-id="b4a0f-115">Üçüncü komut, **Get-AzureRmStorageAccount** cmdlet 'ini kullanarak ikinci komutta oluşturulmuş depolama hesabını alır ve sonucu $STOAccount değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-115">The third command then uses the **Get-AzureRmStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
<span data-ttu-id="b4a0f-116">Beşinci komut, bir alt ağ oluşturmak için **New-AzureRmVirtualNetworkSubnetConfig** cmdlet 'ini kullanır ve sonucu $SubNet adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-116">The fifth command uses the **New-AzureRmVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
<span data-ttu-id="b4a0f-117">Altıncı komut, sanal bir ağ oluşturmak için **New-AzureRmVirtualNetwork** cmdlet 'ini kullanır ve sonucu $VNET adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-117">The sixth command uses the **New-AzureRmVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
<span data-ttu-id="b4a0f-118">Yedinci komutu, altıncı komutta oluşturulan sanal ağ hakkında bilgi almak için **Get-AzureRmVirtualNetwork** kullanır ve $VNET adlı değişkende bu bilgileri depolar.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-118">The seventh command uses the **Get-AzureRmVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
<span data-ttu-id="b4a0f-119">Sekizinci ve dokuzuncu komutu, bu genel IP adresinden bilgi oluşturmak ve almak için **New-azurermpublicıpaddress** ve **Get-azurermpublicıpaddress** kullanır.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-119">The eighth and ninth command uses the **New-AzureRmPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
<span data-ttu-id="b4a0f-120">Komutlar $PubIP adlı değişkende bilgileri depolar.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-120">The commands store the information in the variable named $PubIP.</span></span>
<span data-ttu-id="b4a0f-121">Onuncu komutu, ön uç yük dengeleyicisi oluşturmak için **New-Azurermloadbalancerfrontendıconfıg** cmdlet 'ini kullanır ve sonucu $frontend adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-121">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
<span data-ttu-id="b4a0f-122">Onventh komutu, **Yeni-AzureRmLoadBalancerBackendAddressPoolConfig** öğesini kullanarak arka uç adres havuzu yapılandırması oluşturur ve sonucu $BackendAddressPool değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-122">The eleventh command uses the **New-AzureRmLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
<span data-ttu-id="b4a0f-123">İkinci komut, bir yoklama oluşturmak için **New-AzureRmLoadBalancerProbeConfig** öğesini kullanır ve $Probe adlı değişkende yoklama bilgilerini depolar.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-123">The twelfth command uses the **New-AzureRmLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
<span data-ttu-id="b4a0f-124">Üçüncü on komutu, yük dengeleyici gelen ağ adresi çevirisi (NAT) havuz yapılandırması oluşturmak için **New-Azurermloadbalancerınboundnatpoolconfig** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-124">The thirteenth command uses the **New-AzureRmLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
<span data-ttu-id="b4a0f-125">On on komutu, yük dengeleyici kural yapılandırması oluşturmak için **New-AzureRmLoadBalancerRuleConfig** öğesini kullanır ve sonucu $LBRule değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-125">The fourteenth command uses the **New-AzureRmLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
<span data-ttu-id="b4a0f-126">On beşinci komut, bir yük dengeleyici oluşturmak için **New-AzureRmLoadBalancer** cmdlet 'ini kullanır ve sonucu $ActualLb adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-126">The fifteenth command uses the **New-AzureRmLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
<span data-ttu-id="b4a0f-127">Altıncı komut **Get-AzureRmLoadBalancer** 'ı kullanarak on beşinci komutta oluşturulmuş yük dengeleyici hakkında bilgi alır ve $ExpectedLb adlı değişkende bu bilgileri depolar.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-127">The sixteenth command uses the **Get-AzureRmLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
<span data-ttu-id="b4a0f-128">On yedi komutu, bir VMSS IP yapılandırması oluşturmak için **New-AzureRmVmssIPConfig** cmdlet 'ini kullanır ve $IPCfg adlı değişkende bu bilgileri depolar.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-128">The seventeenth command uses the **New-AzureRmVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
<span data-ttu-id="b4a0f-129">Sekizinci on komutu, bir VMSS yapılandırma nesnesi oluşturmak için **New-AzureRmVmssConfig** cmdlet 'ini kullanır ve sonucu $VMSS adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-129">The eighteenth command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="b4a0f-130">Nıneon komutu, VMSS 'yi oluşturmak için **New-AzureRmVmss** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-130">The nineteenth command uses the **New-AzureRmVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="b4a0f-131">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b4a0f-131">PARAMETERS</span></span>

### <span data-ttu-id="b4a0f-132">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="b4a0f-132">-AllocationMethod</span></span>
<span data-ttu-id="b4a0f-133">Ölçek kümesinin genel IP adresi için ayırma yöntemi (statik veya dinamik).</span><span class="sxs-lookup"><span data-stu-id="b4a0f-133">Allocation method for the Public IP Address of the Scale Set (Static or Dynamic).</span></span>  <span data-ttu-id="b4a0f-134">Değer sağlanmadıysa, ayırma statik olur.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-134">If no value is supplied, allocation will be static.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a0f-135">-Iş</span><span class="sxs-lookup"><span data-stu-id="b4a0f-135">-AsJob</span></span>
<span data-ttu-id="b4a0f-136">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-136">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b4a0f-137">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="b4a0f-137">-BackendPoolName</span></span>
<span data-ttu-id="b4a0f-138">Bu ölçek kümesi için yük dengeleyicide kullanılacak arka uç adres havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-138">The name of the backend address pool to use in the load balancer for this Scale Set.</span></span>  <span data-ttu-id="b4a0f-139">Değer sağlanmazsa, ölçek kümesiyle aynı ada sahip yeni bir arka uç havuzu oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-139">If no value is provided, a new backend pool will be created, with the same name as the Scale Set.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a0f-140">-Backendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="b4a0f-140">-BackendPort</span></span>
<span data-ttu-id="b4a0f-141">Ölçek kümesi yük dengeleyici tarafından ölçek kümesindeki VM 'lerle iletişim kurmak için kullanılan arka uç bağlantı noktası numaraları.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-141">Backend port numbers used by the Scale Set load balancer to communicate with VMs in the Scale Set.</span></span>  <span data-ttu-id="b4a0f-142">Değer belirtilmezse, 3389 ve 5985 bağlantı noktaları Windows VM 'ler için kullanılır ve Linux VM 'Ler için bağlantı noktası 22 kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-142">If no values are specified, ports 3389 and 5985 will be used for Windows VMS, and port 22 will be used for Linux VMs.</span></span>

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a0f-143">-Credential</span><span class="sxs-lookup"><span data-stu-id="b4a0f-143">-Credential</span></span>
<span data-ttu-id="b4a0f-144">Bu ölçek kümesindeki VM 'Ler için yönetici kimlik bilgileri (Kullanıcı adı ve parola).</span><span class="sxs-lookup"><span data-stu-id="b4a0f-144">The administrator credentials (username and password) for VMs in this Scale Set.</span></span>

```yaml
Type: PSCredential
Parameter Sets: SimpleParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a0f-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4a0f-145">-DefaultProfile</span></span>
<span data-ttu-id="b4a0f-146">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4a0f-147">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="b4a0f-147">-DomainNameLabel</span></span>
<span data-ttu-id="b4a0f-148">Bu ölçek kümesi için genel Fully-Qualified etki alanı adı (FQDN) için etki alanı adı etiketi.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-148">The domain name label for the public Fully-Qualified domain name (FQDN) for this Scale Set.</span></span> <span data-ttu-id="b4a0f-149">Bu, etki alanı adının ölçek kümesine otomatik olarak atandığı ilk bileşenidir.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-149">This is the first component of the domain name that is automatically assigned to the Scale Set.</span></span> <span data-ttu-id="b4a0f-150">Otomatik olarak atanan etki alanı adları formu ( <DomainNameLabel> . <Location> . cloudapp.azure.com).</span><span class="sxs-lookup"><span data-stu-id="b4a0f-150">Automatically assigned Domain names use the form (<DomainNameLabel>.<Location>.cloudapp.azure.com).</span></span> <span data-ttu-id="b4a0f-151">Değer sağlanmadıysa, varsayılan etki alanı adı etiketi <ScaleSetName> ve <ResourceGroupName> .</span><span class="sxs-lookup"><span data-stu-id="b4a0f-151">If no value is supplied, the default domain name label will be the concatenation of <ScaleSetName> and <ResourceGroupName>.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a0f-152">-Frontenvseçpoolname</span><span class="sxs-lookup"><span data-stu-id="b4a0f-152">-FrontendPoolName</span></span>
<span data-ttu-id="b4a0f-153">Ölçek kümesi yük dengeleyicisinde kullanılacak ön uç adres havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-153">The name of the frontend address pool to use in the Scale Set load balancer.</span></span>  <span data-ttu-id="b4a0f-154">Değer sağlanmadıysa, ölçek kümesiyle aynı ada sahip yeni bir ön uç adres havuzu oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-154">If no value is supplied, a new Frontend Address Pool will be created, with the same name as the scale set.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a0f-155">-GörüntüAdı</span><span class="sxs-lookup"><span data-stu-id="b4a0f-155">-ImageName</span></span>
<span data-ttu-id="b4a0f-156">Bu ölçek kümesindeki VM 'Lerin adı.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-156">The name of the image for VMs in this Scale Set.</span></span> <span data-ttu-id="b4a0f-157">Değer sağlanmazsa, "Windows Server 2016 DataCenter" resmi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-157">If no value is provided, the "Windows Server 2016 DataCenter" image will be used.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a0f-158">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="b4a0f-158">-InstanceCount</span></span>
<span data-ttu-id="b4a0f-159">Ölçek kümesindeki VM görüntülerinin sayısı.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-159">The number of VM images in the Scale Set.</span></span>  <span data-ttu-id="b4a0f-160">Değer sağlanmazsa, 2 örnek oluşturulacaktır.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-160">If no value is provided, 2 instances will be created.</span></span>

```yaml
Type: Int32
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a0f-161">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="b4a0f-161">-LoadBalancerName</span></span>
<span data-ttu-id="b4a0f-162">Bu ölçek kümesiyle kullanılacak yük dengeleyicinin adı.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-162">The name of the load balancer to use with this Scale Set.</span></span>  <span data-ttu-id="b4a0f-163">Değer belirtilmemişse, ölçek kümesiyle aynı adı kullanan yeni bir yük dengeleyici oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-163">A new load balancer using the same name as the Scale Set will be created if no value is specified.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a0f-164">-Konum</span><span class="sxs-lookup"><span data-stu-id="b4a0f-164">-Location</span></span>
<span data-ttu-id="b4a0f-165">Bu ölçek kümesinin oluşturulacağı Azure konumu.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-165">The Azure location where this Scale Set will be created.</span></span>  <span data-ttu-id="b4a0f-166">Değer belirtilmemişse, konum, parametrelerde başvurulan diğer kaynakların konumundan çıkarılacaktır.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-166">If no value is specified, the location will be inferred from the location of other resources referenced in the parameters.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a0f-167">-Natbackendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="b4a0f-167">-NatBackendPort</span></span>
<span data-ttu-id="b4a0f-168">Gelen ağ adresi çevirisi için arka uç bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-168">Backend port for inbound network address translation.</span></span>

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a0f-169">-Publicıpaddressname</span><span class="sxs-lookup"><span data-stu-id="b4a0f-169">-PublicIpAddressName</span></span>
<span data-ttu-id="b4a0f-170">Bu ölçek kümesiyle kullanılacak ortak IP adresi adı.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-170">The name of the public IP Address to use with this scale set.</span></span>  <span data-ttu-id="b4a0f-171">Değer sağlanmadıysa ölçek kümesiyle aynı ada sahip yeni bir genel IPAddress oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-171">A new Public IPAddress with the same name as the Scale Set will be created if no value is provided.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a0f-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4a0f-172">-ResourceGroupName</span></span>
<span data-ttu-id="b4a0f-173">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-173">Specifies the name of the resource group of the VMSS.</span></span>  <span data-ttu-id="b4a0f-174">Değer belirtilmemişse, ölçek kümesiyle aynı ad kullanılarak yeni bir ResourceGroup oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-174">If no value is specified, a new ResourceGroup will be created using the same name as the Scale Set.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4a0f-175">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="b4a0f-175">-SecurityGroupName</span></span>
<span data-ttu-id="b4a0f-176">Bu ölçek kümesine uygulanacak ağ güvenlik grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-176">The name of the network security group to apply to this Scale Set.</span></span>  <span data-ttu-id="b4a0f-177">Değer sağlanmazsa, ölçek kümesiyle aynı ada sahip bir varsayılan ağ güvenlik grubu oluşturulur ve ölçek kümesine uygulanır.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-177">If no value is provided, a default network security group with the same name as the Scale Set will be created and applied to the Scale Set.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a0f-178">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b4a0f-178">-SubnetAddressPrefix</span></span>
<span data-ttu-id="b4a0f-179">Bu ScaleSet 'in kullanacağı alt ağın adres öneki.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-179">The address prefix of the Subnet this ScaleSet will use.</span></span> <span data-ttu-id="b4a0f-180">Değer sağlanmazsa varsayılan alt ağ ayarları (192.168.1.0/24) uygulanacaktır.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-180">Default Subnet settings (192.168.1.0/24) will be applied if no value is provided.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a0f-181">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="b4a0f-181">-SubnetName</span></span>
<span data-ttu-id="b4a0f-182">Bu ölçek kümesiyle kullanılacak alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-182">The name of the subnet to use with this Scale Set.</span></span>  <span data-ttu-id="b4a0f-183">Değer sağlanmadıysa, ölçek kümesiyle aynı adla yeni bir alt ağ oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-183">A new Subnet will be created with the same name as the Scale Set if no value is provided.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a0f-184">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="b4a0f-184">-UpgradePolicyMode</span></span>
<span data-ttu-id="b4a0f-185">Bu ölçek kümesindeki VM örnekleri için yükseltme ilkesi modu.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-185">The upgrade policy mode for VM instances in this Scale Set.</span></span>  <span data-ttu-id="b4a0f-186">Yükseltme ilkesi otomatik, El Ile veya çalışırken yükseltme belirleyebilir.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-186">Upgrade policy could specify Automatic, Manual, or Rolling upgrades.</span></span>

```yaml
Type: UpgradeMode
Parameter Sets: SimpleParameterSet
Aliases: 
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a0f-187">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b4a0f-187">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="b4a0f-188">Bu cmdlet 'in oluşturduğu VMSS 'in özelliklerini içeren **VirtualMachineScaleSet** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-188">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4a0f-189">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="b4a0f-189">-VirtualNetworkName</span></span>
<span data-ttu-id="b4a0f-190">Bu ölçek kümesiyle birlikte kullanılacak sanal ağın adı.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-190">The name fo the Virtual Network to use with this scale set.</span></span>  <span data-ttu-id="b4a0f-191">Değer sağlanmadıysa, ölçek kümesiyle aynı ada sahip yeni bir sanal ağ oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-191">If no value is supplied, a new virtual network with the same name as the Scale Set will be created.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a0f-192">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b4a0f-192">-VMScaleSetName</span></span>
<span data-ttu-id="b4a0f-193">Bu cmdlet 'in oluşturduğu VMSS 'nin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-193">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4a0f-194">-VmSize</span><span class="sxs-lookup"><span data-stu-id="b4a0f-194">-VmSize</span></span>
<span data-ttu-id="b4a0f-195">Bu ölçek kümesindeki VM örneklerinin boyutu.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-195">The size of the VM instances in this scale set.</span></span>  <span data-ttu-id="b4a0f-196">Boyut belirtilmemişse varsayılan boyut (Standard_DS1_v2) kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-196">A default size (Standard_DS1_v2) will be used if no Size is specified.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a0f-197">-VnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b4a0f-197">-VnetAddressPrefix</span></span>
<span data-ttu-id="b4a0f-198">Bu ölçek kümesiyle kullanılan sanal ağın adres öneki.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-198">The address prefix for the virtual network used with this Scale Set.</span></span>  <span data-ttu-id="b4a0f-199">Değer sağlanmadıysa varsayılan sanal ağ adresi önek ayarları (192.168.0.0/16) kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-199">Default virtual network address prefix settings (192.168.0.0/16) will be used if no value is supplied.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a0f-200">-Bölge</span><span class="sxs-lookup"><span data-stu-id="b4a0f-200">-Zone</span></span>
<span data-ttu-id="b4a0f-201">Kaynağın gelmesi gerektiğini belirten kullanılabilirlik bölgelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-201">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4a0f-202">-Onay</span><span class="sxs-lookup"><span data-stu-id="b4a0f-202">-Confirm</span></span>
<span data-ttu-id="b4a0f-203">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-203">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4a0f-204">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4a0f-204">-WhatIf</span></span>
<span data-ttu-id="b4a0f-205">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-205">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="b4a0f-206">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-206">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4a0f-207">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4a0f-207">CommonParameters</span></span>
<span data-ttu-id="b4a0f-208">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-208">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4a0f-209">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4a0f-209">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4a0f-210">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b4a0f-210">INPUTS</span></span>

### <span data-ttu-id="b4a0f-211">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b4a0f-211">VirtualMachineScaleSet</span></span>
<span data-ttu-id="b4a0f-212">' VirtualMachineScaleSet ' parametresi ardışık düzen için ' VirtualMachineScaleSet ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="b4a0f-212">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="b4a0f-213">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b4a0f-213">OUTPUTS</span></span>

### <span data-ttu-id="b4a0f-214">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="b4a0f-214">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="b4a0f-215">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b4a0f-215">NOTES</span></span>

## <span data-ttu-id="b4a0f-216">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b4a0f-216">RELATED LINKS</span></span>

[<span data-ttu-id="b4a0f-217">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b4a0f-217">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="b4a0f-218">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b4a0f-218">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="b4a0f-219">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b4a0f-219">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="b4a0f-220">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b4a0f-220">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="b4a0f-221">Başlangıç-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b4a0f-221">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="b4a0f-222">Dur-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b4a0f-222">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="b4a0f-223">Güncelleştirme-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b4a0f-223">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


