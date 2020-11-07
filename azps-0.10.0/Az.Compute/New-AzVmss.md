---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmss.md
ms.openlocfilehash: fc788d40cbcd807ef05be4ab43fcda4371aaa084
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936951"
---
# <span data-ttu-id="7da54-101">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7da54-101">New-AzVmss</span></span>

## <span data-ttu-id="7da54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7da54-102">SYNOPSIS</span></span>
<span data-ttu-id="7da54-103">Bir VMSS oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7da54-103">Creates a VMSS.</span></span>

## <span data-ttu-id="7da54-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7da54-104">SYNTAX</span></span>

### <span data-ttu-id="7da54-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7da54-105">DefaultParameter (Default)</span></span>
```
New-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7da54-106">SimpleParameterSet</span><span class="sxs-lookup"><span data-stu-id="7da54-106">SimpleParameterSet</span></span>
```
New-AzVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7da54-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7da54-107">DESCRIPTION</span></span>
<span data-ttu-id="7da54-108">**New-AzVmss** cmdlet 'i Azure 'Da sanal makine ölçek KÜMESI (VMSS) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7da54-108">The **New-AzVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="7da54-109">Bu cmdlet giriş olarak bir **VirtualMachineScaleSet** nesnesi alır.</span><span class="sxs-lookup"><span data-stu-id="7da54-109">This cmdlet takes a **VirtualMachineScaleSet** object as input.</span></span>

## <span data-ttu-id="7da54-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7da54-110">EXAMPLES</span></span>

### <span data-ttu-id="7da54-111">Örnek 1: VMSS oluşturma</span><span class="sxs-lookup"><span data-stu-id="7da54-111">Example 1: Create a VMSS</span></span>
```
# Common
$LOC = "WestUs";
$RGName = "rgkyvms";

New-AzResourceGroup -Name $RGName -Location $LOC -Force;

# SRP
$STOName = "STO" + $RGName;
$STOType = "Standard_GRS";
New-AzStorageAccount -ResourceGroupName $RGName -Name $STOName -Location $LOC -Type $STOType;
$STOAccount = Get-AzStorageAccount -ResourceGroupName $RGName -Name $STOName; 

# NRP
$SubNet = New-AzVirtualNetworkSubnetConfig -Name ("subnet" + $RGName) -AddressPrefix "10.0.0.0/24";
$VNet = New-AzVirtualNetwork -Force -Name ("vnet" + $RGName) -ResourceGroupName $RGName -Location $LOC -AddressPrefix "10.0.0.0/16" -DnsServer "10.1.1.1" -Subnet $SubNet;
$VNet = Get-AzVirtualNetwork -Name ('vnet' + $RGName) -ResourceGroupName $RGName;
$SubNetId = $VNet.Subnets[0].Id;

$PubIP = New-AzPublicIpAddress -Force -Name ("PubIP" + $RGName) -ResourceGroupName $RGName -Location $LOC -AllocationMethod Dynamic -DomainNameLabel ("PubIP" + $RGName);
$PubIP = Get-AzPublicIpAddress -Name ("PubIP"  + $RGName) -ResourceGroupName $RGName;

# Create LoadBalancer
$FrontendName = "fe" + $RGName
$BackendAddressPoolName = "bepool" + $RGName
$ProbeName = "vmssprobe" + $RGName
$InboundNatPoolName  = "innatpool" + $RGName
$LBRuleName = "lbrule" + $RGName
$LBName = "vmsslb" + $RGName

$Frontend = New-AzLoadBalancerFrontendIpConfig -Name $FrontendName -PublicIpAddress $PubIP
$BackendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name $BackendAddressPoolName
$Probe = New-AzLoadBalancerProbeConfig -Name $ProbeName -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
$InboundNatPool = New-AzLoadBalancerInboundNatPoolConfig -Name $InboundNatPoolName  -FrontendIPConfigurationId `
    $Frontend.Id -Protocol Tcp -FrontendPortRangeStart 3360 -FrontendPortRangeEnd 3362 -BackendPort 3370;
$LBRule = New-AzLoadBalancerRuleConfig -Name $LBRuleName `
    -FrontendIPConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 `
    -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP;
$ActualLb = New-AzLoadBalancer -Name $LBName -ResourceGroupName $RGName -Location $LOC `
    -FrontendIpConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -LoadBalancingRule $LBRule -InboundNatPool $InboundNatPool;
$ExpectedLb = Get-AzLoadBalancer -Name $LBName -ResourceGroupName $RGName

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
$IPCfg = New-AzVmssIPConfig -Name "Test" `
    -LoadBalancerInboundNatPoolsId $ExpectedLb.InboundNatPools[0].Id `
    -LoadBalancerBackendAddressPoolsId $ExpectedLb.BackendAddressPools[0].Id `
    -SubnetId $SubNetId;
            
#VMSS Config
$VMSS = New-AzVmssConfig -Location $LOC -SkuCapacity 2 -SkuName "Standard_A2" -UpgradePolicyMode "Automatic" `
    | Add-AzVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
    | Add-AzVmssNetworkInterfaceConfiguration -Name "Test2"  -IPConfiguration $IPCfg `
    | Set-AzVmssOSProfile -ComputerNamePrefix "Test"  -AdminUsername $AdminUsername -AdminPassword $AdminPassword `
    | Set-AzVmssStorageProfile -Name "Test"  -OsDiskCreateOption 'FromImage' -OsDiskCaching "None" `
    -ImageReferenceOffer $Offer -ImageReferenceSku $Sku -ImageReferenceVersion $Version `
    -ImageReferencePublisher $PublisherName -VhdContainer $VHDContainer `
    | Add-AzVmssExtension -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True

#Create the VMSS
New-AzVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="7da54-112">Aşağıdaki karmaşık örnek bir VMSS oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7da54-112">The following complex example creates a VMSS.</span></span>
<span data-ttu-id="7da54-113">İlk komut belirtilen ad ve konuma sahip bir kaynak grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7da54-113">The first command creates a resource group with the specified name and location.</span></span>
<span data-ttu-id="7da54-114">İkinci komut, depolama hesabı oluşturmak için **New-AzStorageAccount** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="7da54-114">The second command uses the **New-AzStorageAccount** cmdlet to create a storage account.</span></span>
<span data-ttu-id="7da54-115">Üçüncü komut, **Get-AzStorageAccount** cmdlet 'ini kullanarak ikinci komutta oluşturulmuş depolama hesabını alır ve sonucu $STOAccount değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7da54-115">The third command then uses the **Get-AzStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
<span data-ttu-id="7da54-116">Beşinci komut, bir alt ağ oluşturmak için **New-AzVirtualNetworkSubnetConfig** cmdlet 'ini kullanır ve sonucu $SubNet adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="7da54-116">The fifth command uses the **New-AzVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
<span data-ttu-id="7da54-117">Altıncı komut, sanal bir ağ oluşturmak için **New-AzVirtualNetwork** cmdlet 'ini kullanır ve sonucu $VNET adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="7da54-117">The sixth command uses the **New-AzVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
<span data-ttu-id="7da54-118">Yedinci komutu, altıncı komutta oluşturulan sanal ağ hakkında bilgi almak için **Get-AzVirtualNetwork** kullanır ve $VNET adlı değişkende bu bilgileri depolar.</span><span class="sxs-lookup"><span data-stu-id="7da54-118">The seventh command uses the **Get-AzVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
<span data-ttu-id="7da54-119">Sekizinci ve dokuzuncu komutu, bu genel IP adresinden bilgi oluşturmak ve bu adresten bilgi almak için **New-Azpublicıpaddress** ve **Get-Azurermpublicıpaddress** kullanır.</span><span class="sxs-lookup"><span data-stu-id="7da54-119">The eighth and ninth command uses the **New-AzPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
<span data-ttu-id="7da54-120">Komutlar $PubIP adlı değişkende bilgileri depolar.</span><span class="sxs-lookup"><span data-stu-id="7da54-120">The commands store the information in the variable named $PubIP.</span></span>
<span data-ttu-id="7da54-121">Onuncu komutu, ön uç yük dengeleyicisi oluşturmak için **New-Azurermloadbalancerfrontendıconfıg** cmdlet 'ini kullanır ve sonucu $frontend adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="7da54-121">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
<span data-ttu-id="7da54-122">Onventh komutu, **Yeni-AzLoadBalancerBackendAddressPoolConfig** öğesini kullanarak arka uç adres havuzu yapılandırması oluşturur ve sonucu $BackendAddressPool değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7da54-122">The eleventh command uses the **New-AzLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
<span data-ttu-id="7da54-123">On ikinci komut, bir yoklama oluşturmak için **New-AzLoadBalancerProbeConfig** öğesini kullanır ve yoklama bilgilerini $Probe adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="7da54-123">The twelfth command uses the **New-AzLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
<span data-ttu-id="7da54-124">Üçüncü on komutu, yük dengeleyici gelen ağ adresi çevirisi (NAT) havuz yapılandırması oluşturmak için **New-Azloadbalancerınboundnatpoolconfig** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="7da54-124">The thirteenth command uses the **New-AzLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
<span data-ttu-id="7da54-125">On on komutu, yük dengeleyici kural yapılandırması oluşturmak için **New-AzLoadBalancerRuleConfig** 'i kullanır ve sonucu $LBRule adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="7da54-125">The fourteenth command uses the **New-AzLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
<span data-ttu-id="7da54-126">On beşinci komut, yük dengeleyici oluşturmak için **New-AzLoadBalancer** cmdlet 'ini kullanır ve sonucu $ActualLb adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="7da54-126">The fifteenth command uses the **New-AzLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
<span data-ttu-id="7da54-127">Altıncı komut **Get-AzLoadBalancer** 'yi kullanarak on beşinci komutta oluşturulmuş yük dengeleyici hakkında bilgi alır ve $ExpectedLb adlı değişkende bu bilgileri depolar.</span><span class="sxs-lookup"><span data-stu-id="7da54-127">The sixteenth command uses the **Get-AzLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
<span data-ttu-id="7da54-128">On on \* komutu, bir VMSS IP yapılandırması oluşturmak için **New-AzVmssIPConfig** cmdlet 'ini kullanır ve bu bilgileri $IPCfg adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="7da54-128">The seventeenth command uses the **New-AzVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
<span data-ttu-id="7da54-129">Sekizinci on komutu, bir VMSS yapılandırma nesnesi oluşturmak için **New-AzVmssConfig** cmdlet 'ini kullanır ve sonucu $VMSS adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="7da54-129">The eighteenth command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="7da54-130">Nıneon komutu, VMSS 'yi oluşturmak için **New-AzVmss** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="7da54-130">The nineteenth command uses the **New-AzVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="7da54-131">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7da54-131">PARAMETERS</span></span>

### <span data-ttu-id="7da54-132">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="7da54-132">-AllocationMethod</span></span>
<span data-ttu-id="7da54-133">Ölçek kümesinin genel IP adresi için ayırma yöntemi (statik veya dinamik).</span><span class="sxs-lookup"><span data-stu-id="7da54-133">Allocation method for the Public IP Address of the Scale Set (Static or Dynamic).</span></span>  <span data-ttu-id="7da54-134">Değer sağlanmadıysa, ayırma statik olur.</span><span class="sxs-lookup"><span data-stu-id="7da54-134">If no value is supplied, allocation will be static.</span></span>

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

### <span data-ttu-id="7da54-135">-Iş</span><span class="sxs-lookup"><span data-stu-id="7da54-135">-AsJob</span></span>
<span data-ttu-id="7da54-136">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="7da54-136">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7da54-137">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="7da54-137">-BackendPoolName</span></span>
<span data-ttu-id="7da54-138">Bu ölçek kümesi için yük dengeleyicide kullanılacak arka uç adres havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="7da54-138">The name of the backend address pool to use in the load balancer for this Scale Set.</span></span>  <span data-ttu-id="7da54-139">Değer sağlanmazsa, ölçek kümesiyle aynı ada sahip yeni bir arka uç havuzu oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7da54-139">If no value is provided, a new backend pool will be created, with the same name as the Scale Set.</span></span>

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

### <span data-ttu-id="7da54-140">-Backendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="7da54-140">-BackendPort</span></span>
<span data-ttu-id="7da54-141">Ölçek kümesi yük dengeleyici tarafından ölçek kümesindeki VM 'lerle iletişim kurmak için kullanılan arka uç bağlantı noktası numaraları.</span><span class="sxs-lookup"><span data-stu-id="7da54-141">Backend port numbers used by the Scale Set load balancer to communicate with VMs in the Scale Set.</span></span>  <span data-ttu-id="7da54-142">Değer belirtilmezse, 3389 ve 5985 bağlantı noktaları Windows VM 'ler için kullanılır ve Linux VM 'Ler için bağlantı noktası 22 kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7da54-142">If no values are specified, ports 3389 and 5985 will be used for Windows VMS, and port 22 will be used for Linux VMs.</span></span>

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

### <span data-ttu-id="7da54-143">-Credential</span><span class="sxs-lookup"><span data-stu-id="7da54-143">-Credential</span></span>
<span data-ttu-id="7da54-144">Bu ölçek kümesindeki VM 'Ler için yönetici kimlik bilgileri (Kullanıcı adı ve parola).</span><span class="sxs-lookup"><span data-stu-id="7da54-144">The administrator credentials (username and password) for VMs in this Scale Set.</span></span>

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

### <span data-ttu-id="7da54-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7da54-145">-DefaultProfile</span></span>
<span data-ttu-id="7da54-146">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7da54-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7da54-147">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="7da54-147">-DomainNameLabel</span></span>
<span data-ttu-id="7da54-148">Bu ölçek kümesi için genel Fully-Qualified etki alanı adı (FQDN) için etki alanı adı etiketi.</span><span class="sxs-lookup"><span data-stu-id="7da54-148">The domain name label for the public Fully-Qualified domain name (FQDN) for this Scale Set.</span></span> <span data-ttu-id="7da54-149">Bu, etki alanı adının ölçek kümesinin otomatik olarak assiged ilk bileşenidir.</span><span class="sxs-lookup"><span data-stu-id="7da54-149">This is the first component of the domain name that is automatically assiged to the Scale Set.</span></span> <span data-ttu-id="7da54-150">Otomatik olarak atanan etki alanı adları formu ( <DomainNameLabel> . <Location> . cloudapp.azure.com).</span><span class="sxs-lookup"><span data-stu-id="7da54-150">Automatically assigned Domain names use the form (<DomainNameLabel>.<Location>.cloudapp.azure.com).</span></span> <span data-ttu-id="7da54-151">Değer sağlanmadıysa, varsayılan etki alanı adı etiketi <ScaleSetName> ve <ResourceGroupName> .</span><span class="sxs-lookup"><span data-stu-id="7da54-151">If no value is supplied, the default domain name label will be the concatenation of <ScaleSetName> and <ResourceGroupName>.</span></span>

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

### <span data-ttu-id="7da54-152">-Frontenvseçpoolname</span><span class="sxs-lookup"><span data-stu-id="7da54-152">-FrontendPoolName</span></span>
<span data-ttu-id="7da54-153">Ölçek kümesi locad dengeleyicisinde kullanılan ön uç adres havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="7da54-153">The name of the frontend address pool to usein the Scale Set locad balancer.</span></span>  <span data-ttu-id="7da54-154">Değer sağlanmadıysa, ölçek kümesiyle aynı ada sahip yeni bir ön uç adres havuzu oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7da54-154">If no value is supplied, a new Frontend Address Pool will be created, with the same name as the scale set.</span></span>

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

### <span data-ttu-id="7da54-155">-GörüntüAdı</span><span class="sxs-lookup"><span data-stu-id="7da54-155">-ImageName</span></span>
<span data-ttu-id="7da54-156">Bu ölçek kümesindeki VM 'Lerin adı.</span><span class="sxs-lookup"><span data-stu-id="7da54-156">The name of the image for VMs in this Scale Set.</span></span> <span data-ttu-id="7da54-157">Değer sağlanmazsa, "Windows Server 2016 DataCenter" resmi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7da54-157">If no value is provided, the "Windows Server 2016 DataCenter" image will be used.</span></span>

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

### <span data-ttu-id="7da54-158">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="7da54-158">-InstanceCount</span></span>
<span data-ttu-id="7da54-159">Ölçek kümesindeki VM görüntülerinin sayısı.</span><span class="sxs-lookup"><span data-stu-id="7da54-159">The number of VM images in the Scale Set.</span></span>  <span data-ttu-id="7da54-160">Değer sağlanmazsa, 2 örnek oluşturulacaktır.</span><span class="sxs-lookup"><span data-stu-id="7da54-160">If no value is provided, 2 instances will be created.</span></span>

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

### <span data-ttu-id="7da54-161">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="7da54-161">-LoadBalancerName</span></span>
<span data-ttu-id="7da54-162">Bu ölçek kümesiyle kullanılacak yük dengeleyicinin adı.</span><span class="sxs-lookup"><span data-stu-id="7da54-162">The name of the load balancer to use with this Scale Set.</span></span>  <span data-ttu-id="7da54-163">Değer belirtilmemişse, ölçek kümesiyle aynı adı kullanan yeni bir yük dengeleyici oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7da54-163">A new load balancer using the same name as the Scale Set will be created if no value is specified.</span></span>

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

### <span data-ttu-id="7da54-164">-Konum</span><span class="sxs-lookup"><span data-stu-id="7da54-164">-Location</span></span>
<span data-ttu-id="7da54-165">Bu ölçek kümesinin oluşturulacağı Azure konumu.</span><span class="sxs-lookup"><span data-stu-id="7da54-165">The Azure location where this Scale Set will be created.</span></span>  <span data-ttu-id="7da54-166">Değer belirtilmemişse, konum, parametrelerde başvurulan diğer kaynakların konumundan çıkarılacaktır.</span><span class="sxs-lookup"><span data-stu-id="7da54-166">If no value is specified, the location will be inferred from the location of other resources referenced in the parameters.</span></span>

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

### <span data-ttu-id="7da54-167">-Natbackendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="7da54-167">-NatBackendPort</span></span>
<span data-ttu-id="7da54-168">Gelen ağ adresi çevirisi için arka uç bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="7da54-168">Backend port for inbound network address translation.</span></span>

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

### <span data-ttu-id="7da54-169">-Publicıpaddressname</span><span class="sxs-lookup"><span data-stu-id="7da54-169">-PublicIpAddressName</span></span>
<span data-ttu-id="7da54-170">Bu ölçek kümesiyle kullanılacak ortak IP adresi adı.</span><span class="sxs-lookup"><span data-stu-id="7da54-170">The name of the public IP Address to use with this scale set.</span></span>  <span data-ttu-id="7da54-171">Değer sağlanmadıysa ölçek kümesiyle aynı ada sahip yeni bir genel IPAddress oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7da54-171">A new Public IPAddress with the same name as the Scale Set will be created if no value is provided.</span></span>

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

### <span data-ttu-id="7da54-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7da54-172">-ResourceGroupName</span></span>
<span data-ttu-id="7da54-173">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7da54-173">Specifies the name of the resource group of the VMSS.</span></span>  <span data-ttu-id="7da54-174">Değer belirtilmemişse, ölçek kümesiyle aynı ad kullanılarak yeni bir ResourceGroup oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7da54-174">If no value is specified, a new ResourceGroup will be created using the same name as the Scale Set.</span></span>

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

### <span data-ttu-id="7da54-175">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="7da54-175">-SecurityGroupName</span></span>
<span data-ttu-id="7da54-176">Bu ölçek kümesine uygulanacak ağ güvenlik grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7da54-176">The name of the network security group to apply to this Scale Set.</span></span>  <span data-ttu-id="7da54-177">Değer sağlanmazsa, ölçek kümesiyle aynı ada sahip bir varsayılan ağ güvenlik grubu oluşturulur ve ölçek kümesine uygulanır.</span><span class="sxs-lookup"><span data-stu-id="7da54-177">If no value is provided, a default network security group with the same name as the Scale Set will be created and applied to the Scale Set.</span></span>

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

### <span data-ttu-id="7da54-178">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7da54-178">-SubnetAddressPrefix</span></span>
<span data-ttu-id="7da54-179">Bu ScaleSet 'in kullanacağı alt ağın adres öneki.</span><span class="sxs-lookup"><span data-stu-id="7da54-179">The address prefix of the Subnet this ScaleSet will use.</span></span> <span data-ttu-id="7da54-180">Değer sağlanmazsa varsayılan alt ağ ayarları (192.168.1.0/24) uygulanacaktır.</span><span class="sxs-lookup"><span data-stu-id="7da54-180">Default Subnet settings (192.168.1.0/24) will be applied if no value is provided.</span></span>

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

### <span data-ttu-id="7da54-181">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="7da54-181">-SubnetName</span></span>
<span data-ttu-id="7da54-182">Bu ölçek kümesiyle kullanılacak alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="7da54-182">The name of the subnet to use with this Scale Set.</span></span>  <span data-ttu-id="7da54-183">Değer sağlanmadıysa, ölçek kümesiyle aynı adla yeni bir alt ağ oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7da54-183">A new Subnet will be created with the same name as the Scale Set if no value is provided.</span></span>

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

### <span data-ttu-id="7da54-184">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="7da54-184">-UpgradePolicyMode</span></span>
<span data-ttu-id="7da54-185">Bu ölçek kümesindeki VM örnekleri için yükseltme ilkesi modu.</span><span class="sxs-lookup"><span data-stu-id="7da54-185">The upgrade policy mode for VM instances in this Scale Set.</span></span>  <span data-ttu-id="7da54-186">Yükseltme ilkesi otomatik, El Ile veya çalışırken yükseltme belirleyebilir.</span><span class="sxs-lookup"><span data-stu-id="7da54-186">Upgrade policy could specify Automatic, Manual, or Rolling upgrades.</span></span>

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

### <span data-ttu-id="7da54-187">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7da54-187">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="7da54-188">Bu cmdlet 'in oluşturduğu VMSS 'in özelliklerini içeren **VirtualMachineScaleSet** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7da54-188">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="7da54-189">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="7da54-189">-VirtualNetworkName</span></span>
<span data-ttu-id="7da54-190">Bu ölçek kümesiyle birlikte kullanılacak sanal ağın adı.</span><span class="sxs-lookup"><span data-stu-id="7da54-190">The name fo the Virtual Network to use with this scale set.</span></span>  <span data-ttu-id="7da54-191">Değer sağlanmadıysa, ölçek kümesiyle aynı ada sahip yeni bir sanal ağ oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7da54-191">If no value is supplied, a new virtual network with the same name as the Scale Set will be created.</span></span>

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

### <span data-ttu-id="7da54-192">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="7da54-192">-VMScaleSetName</span></span>
<span data-ttu-id="7da54-193">Bu cmdlet 'in oluşturduğu VMSS 'nin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7da54-193">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="7da54-194">-VmSize</span><span class="sxs-lookup"><span data-stu-id="7da54-194">-VmSize</span></span>
<span data-ttu-id="7da54-195">Bu ölçek kümesindeki VM örneklerinin boyutu.</span><span class="sxs-lookup"><span data-stu-id="7da54-195">The size of the VM instances in this scale set.</span></span>  <span data-ttu-id="7da54-196">Boyut belirtilmemişse varsayılan boyut (Standard_DS1_v2) kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7da54-196">A default size (Standard_DS1_v2) will be used if no Size is specified.</span></span>

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

### <span data-ttu-id="7da54-197">-VnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7da54-197">-VnetAddressPrefix</span></span>
<span data-ttu-id="7da54-198">Bu ölçek kümesiyle kullanılan sanal ağın adres öneki.</span><span class="sxs-lookup"><span data-stu-id="7da54-198">The address prefix for the virtual network used with this Scale Set.</span></span>  <span data-ttu-id="7da54-199">Değer sağlanmadıysa varsayılan sanal ağ adresi önek ayarları (192.168.0.0/16) kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="7da54-199">Default virtual network address prefix settings (192.168.0.0/16) will be used if no value is supplied.</span></span>

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

### <span data-ttu-id="7da54-200">-Bölge</span><span class="sxs-lookup"><span data-stu-id="7da54-200">-Zone</span></span>
<span data-ttu-id="7da54-201">Kaynağın gelmesi gerektiğini belirten kullanılabilirlik bölgelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="7da54-201">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="7da54-202">-Onay</span><span class="sxs-lookup"><span data-stu-id="7da54-202">-Confirm</span></span>
<span data-ttu-id="7da54-203">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7da54-203">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7da54-204">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7da54-204">-WhatIf</span></span>
<span data-ttu-id="7da54-205">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7da54-205">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="7da54-206">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7da54-206">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7da54-207">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7da54-207">CommonParameters</span></span>
<span data-ttu-id="7da54-208">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7da54-208">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7da54-209">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7da54-209">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7da54-210">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7da54-210">INPUTS</span></span>

### <span data-ttu-id="7da54-211">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7da54-211">VirtualMachineScaleSet</span></span>
<span data-ttu-id="7da54-212">' VirtualMachineScaleSet ' parametresi ardışık düzen için ' VirtualMachineScaleSet ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="7da54-212">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="7da54-213">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7da54-213">OUTPUTS</span></span>

### <span data-ttu-id="7da54-214">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="7da54-214">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="7da54-215">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7da54-215">NOTES</span></span>

## <span data-ttu-id="7da54-216">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7da54-216">RELATED LINKS</span></span>

[<span data-ttu-id="7da54-217">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7da54-217">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="7da54-218">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7da54-218">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="7da54-219">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7da54-219">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="7da54-220">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7da54-220">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="7da54-221">Başlangıç-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7da54-221">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="7da54-222">Dur-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7da54-222">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="7da54-223">Güncelleştirme-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7da54-223">Update-AzVmss</span></span>](./Update-AzVmss.md)


