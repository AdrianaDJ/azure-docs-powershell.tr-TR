---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
ms.openlocfilehash: 4953e914cc52784cd815be80307babfe05f3b63c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322606"
---
# <span data-ttu-id="3491b-101">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3491b-101">New-AzVmss</span></span>

## <span data-ttu-id="3491b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3491b-102">SYNOPSIS</span></span>
<span data-ttu-id="3491b-103">Bir VMSS oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3491b-103">Creates a VMSS.</span></span>

## <span data-ttu-id="3491b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3491b-104">SYNTAX</span></span>

### <span data-ttu-id="3491b-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3491b-105">DefaultParameter (Default)</span></span>
```
New-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3491b-106">SimpleParameterSet</span><span class="sxs-lookup"><span data-stu-id="3491b-106">SimpleParameterSet</span></span>
```
New-AzVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-EnableUltraSSD]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DataDiskSizeInGb <Int32[]>] [-ProximityPlacementGroupId <String>] [-HostGroupId <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-ScaleInPolicy <String[]>]
 [-SkipExtensionsOnOverprovisionedVMs] [-EncryptionAtHost] [-PlatformFaultDomainCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-SinglePlacementGroup] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3491b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3491b-107">DESCRIPTION</span></span>
<span data-ttu-id="3491b-108">**New-AzVmss** cmdlet 'i Azure 'Da sanal makine ölçek KÜMESI (VMSS) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3491b-108">The **New-AzVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="3491b-109">`SimpleParameterSet`Önceden ayarlanmış BIR VMSS ve ilişkili kaynakları hızlı şekilde oluşturmak için basit parametre kümesi () kullanın.</span><span class="sxs-lookup"><span data-stu-id="3491b-109">Use the simple parameter set (`SimpleParameterSet`) to quickly create a pre-set VMSS and associated resources.</span></span> <span data-ttu-id="3491b-110">`DefaultParameter`Vmsubnet 'in her bileşenini ve oluşturmadan önce her ilişkili kaynağı tam olarak yapılandırmanız gerektiğinde daha gelişmiş senaryolar için varsayılan parametre kümesi 'ni () kullanın.</span><span class="sxs-lookup"><span data-stu-id="3491b-110">Use the default parameter set (`DefaultParameter`) for more advanced scenarios when you need to precisely configure each component of the VMSS and each associated resource before creation.</span></span>

## <span data-ttu-id="3491b-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3491b-111">EXAMPLES</span></span>

### <span data-ttu-id="3491b-112">Örnek 1: **`SimpleParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="3491b-112">Example 1: Create a VMSS using the **`SimpleParameterSet`**</span></span>
```powershell
$vmssName = <VMSSNAME>
# Create credentials, I am using one way to create credentials, there are others as well. 
# Pick one that makes the most sense according to your use case.
$vmPassword = ConvertTo-SecureString <PASSWORD_HERE> -AsPlainText -Force
$vmCred = New-Object System.Management.Automation.PSCredential(<USERNAME_HERE>, $vmPassword)

#Create a VMSS using the default settings
New-AzVmss -Credential $vmCred -VMScaleSetName $vmssName
```

<span data-ttu-id="3491b-113">Yukarıdaki komut, adla aşağıdakileri oluşturur `$vmssName` :</span><span class="sxs-lookup"><span data-stu-id="3491b-113">The command above creates the following with the name `$vmssName` :</span></span>
* <span data-ttu-id="3491b-114">Kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="3491b-114">A Resource Group</span></span>
* <span data-ttu-id="3491b-115">Sanal ağ</span><span class="sxs-lookup"><span data-stu-id="3491b-115">A virtual network</span></span>
* <span data-ttu-id="3491b-116">Bir yük dengeleyici</span><span class="sxs-lookup"><span data-stu-id="3491b-116">A load balancer</span></span>
* <span data-ttu-id="3491b-117">Genel bir IP</span><span class="sxs-lookup"><span data-stu-id="3491b-117">A public IP</span></span>
* <span data-ttu-id="3491b-118">2 örnek içeren VMSS</span><span class="sxs-lookup"><span data-stu-id="3491b-118">the VMSS with 2 instances</span></span>

<span data-ttu-id="3491b-119">VMSS 'deki VM 'Ler için seçilen varsayılan görüntü `2016-Datacenter Windows Server``Standard_DS1_v2`</span><span class="sxs-lookup"><span data-stu-id="3491b-119">The default image chosen for the VMs in the VMSS is `2016-Datacenter Windows Server` and the SKU is `Standard_DS1_v2`</span></span>

### <span data-ttu-id="3491b-120">Örnek 2: **`DefaultParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="3491b-120">Example 2: Create a VMSS using the **`DefaultParameterSet`**</span></span>
```powershell
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
$VMSS = New-AzVmssConfig -Location $LOC -SkuCapacity 2 -SkuName "Standard_E4-2ds_v4" -UpgradePolicyMode "Automatic" `
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

<span data-ttu-id="3491b-121">Yukarıdaki karmaşık örnek bir VMSS oluşturur, bunun anlamı aşağıda verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="3491b-121">The complex example above creates a VMSS, following is an explanation of what is happening:</span></span>
* <span data-ttu-id="3491b-122">İlk komut belirtilen ad ve konuma sahip bir kaynak grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3491b-122">The first command creates a resource group with the specified name and location.</span></span>
* <span data-ttu-id="3491b-123">İkinci komut, depolama hesabı oluşturmak için **New-AzStorageAccount** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="3491b-123">The second command uses the **New-AzStorageAccount** cmdlet to create a storage account.</span></span>
* <span data-ttu-id="3491b-124">Üçüncü komut, **Get-AzStorageAccount** cmdlet 'ini kullanarak ikinci komutta oluşturulmuş depolama hesabını alır ve sonucu $STOAccount değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="3491b-124">The third command then uses the **Get-AzStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
* <span data-ttu-id="3491b-125">Beşinci komut, bir alt ağ oluşturmak için **New-AzVirtualNetworkSubnetConfig** cmdlet 'ini kullanır ve sonucu $SubNet adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="3491b-125">The fifth command uses the **New-AzVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
* <span data-ttu-id="3491b-126">Altıncı komut, sanal bir ağ oluşturmak için **New-AzVirtualNetwork** cmdlet 'ini kullanır ve sonucu $VNET adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="3491b-126">The sixth command uses the **New-AzVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
* <span data-ttu-id="3491b-127">Yedinci komutu, altıncı komutta oluşturulan sanal ağ hakkında bilgi almak için **Get-AzVirtualNetwork** kullanır ve $VNET adlı değişkende bu bilgileri depolar.</span><span class="sxs-lookup"><span data-stu-id="3491b-127">The seventh command uses the **Get-AzVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
* <span data-ttu-id="3491b-128">Sekizinci ve dokuzuncu komutu, bu genel IP adresinden bilgi oluşturmak ve bu adresten bilgi almak için **New-Azpublicıpaddress** ve **Get-Azurermpublicıpaddress** kullanır.</span><span class="sxs-lookup"><span data-stu-id="3491b-128">The eighth and ninth command uses the **New-AzPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
* <span data-ttu-id="3491b-129">Komutlar $PubIP adlı değişkende bilgileri depolar.</span><span class="sxs-lookup"><span data-stu-id="3491b-129">The commands store the information in the variable named $PubIP.</span></span>
* <span data-ttu-id="3491b-130">Onuncu komutu, ön uç yük dengeleyicisi oluşturmak için **New-Azurermloadbalancerfrontendıconfıg** cmdlet 'ini kullanır ve sonucu $frontend adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="3491b-130">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
* <span data-ttu-id="3491b-131">Onventh komutu, **Yeni-AzLoadBalancerBackendAddressPoolConfig** öğesini kullanarak arka uç adres havuzu yapılandırması oluşturur ve sonucu $BackendAddressPool değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="3491b-131">The eleventh command uses the **New-AzLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
* <span data-ttu-id="3491b-132">On ikinci komut, bir yoklama oluşturmak için **New-AzLoadBalancerProbeConfig** öğesini kullanır ve yoklama bilgilerini $Probe adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="3491b-132">The twelfth command uses the **New-AzLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
* <span data-ttu-id="3491b-133">Üçüncü on komutu, yük dengeleyici gelen ağ adresi çevirisi (NAT) havuz yapılandırması oluşturmak için **New-Azloadbalancerınboundnatpoolconfig** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="3491b-133">The thirteenth command uses the **New-AzLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
* <span data-ttu-id="3491b-134">On on komutu, yük dengeleyici kural yapılandırması oluşturmak için **New-AzLoadBalancerRuleConfig** 'i kullanır ve sonucu $LBRule adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="3491b-134">The fourteenth command uses the **New-AzLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
* <span data-ttu-id="3491b-135">On beşinci komut, yük dengeleyici oluşturmak için **New-AzLoadBalancer** cmdlet 'ini kullanır ve sonucu $ActualLb adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="3491b-135">The fifteenth command uses the **New-AzLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
* <span data-ttu-id="3491b-136">Altıncı komut **Get-AzLoadBalancer** 'yi kullanarak on beşinci komutta oluşturulmuş yük dengeleyici hakkında bilgi alır ve $ExpectedLb adlı değişkende bu bilgileri depolar.</span><span class="sxs-lookup"><span data-stu-id="3491b-136">The sixteenth command uses the **Get-AzLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
* <span data-ttu-id="3491b-137">On on \* komutu, bir VMSS IP yapılandırması oluşturmak için **New-AzVmssIPConfig** cmdlet 'ini kullanır ve bu bilgileri $IPCfg adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="3491b-137">The seventeenth command uses the **New-AzVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
* <span data-ttu-id="3491b-138">Sekizinci on komutu, bir VMSS yapılandırma nesnesi oluşturmak için **New-AzVmssConfig** cmdlet 'ini kullanır ve sonucu $VMSS adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="3491b-138">The eighteenth command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
* <span data-ttu-id="3491b-139">Nıneon komutu, VMSS 'yi oluşturmak için **New-AzVmss** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="3491b-139">The nineteenth command uses the **New-AzVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="3491b-140">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3491b-140">PARAMETERS</span></span>

### <span data-ttu-id="3491b-141">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="3491b-141">-AllocationMethod</span></span>
<span data-ttu-id="3491b-142">Ölçek kümesinin genel IP adresi için ayırma yöntemi (statik veya dinamik).</span><span class="sxs-lookup"><span data-stu-id="3491b-142">Allocation method for the Public IP Address of the Scale Set (Static or Dynamic).</span></span>  <span data-ttu-id="3491b-143">Değer sağlanmadıysa, ayırma statik olur.</span><span class="sxs-lookup"><span data-stu-id="3491b-143">If no value is supplied, allocation will be static.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3491b-144">-Iş</span><span class="sxs-lookup"><span data-stu-id="3491b-144">-AsJob</span></span>
<span data-ttu-id="3491b-145">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="3491b-145">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="3491b-146">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="3491b-146">-BackendPoolName</span></span>
<span data-ttu-id="3491b-147">Bu ölçek kümesi için yük dengeleyicide kullanılacak arka uç adres havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="3491b-147">The name of the backend address pool to use in the load balancer for this Scale Set.</span></span>  <span data-ttu-id="3491b-148">Değer sağlanmazsa, ölçek kümesiyle aynı ada sahip yeni bir arka uç havuzu oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3491b-148">If no value is provided, a new backend pool will be created, with the same name as the Scale Set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3491b-149">-Backendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="3491b-149">-BackendPort</span></span>
<span data-ttu-id="3491b-150">Ölçek kümesi yük dengeleyici tarafından ölçek kümesindeki VM 'lerle iletişim kurmak için kullanılan arka uç bağlantı noktası numaraları.</span><span class="sxs-lookup"><span data-stu-id="3491b-150">Backend port numbers used by the Scale Set load balancer to communicate with VMs in the Scale Set.</span></span>  <span data-ttu-id="3491b-151">Değer belirtilmezse, 3389 ve 5985 bağlantı noktaları Windows VM 'ler için kullanılır ve Linux VM 'Ler için bağlantı noktası 22 kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3491b-151">If no values are specified, ports 3389 and 5985 will be used for Windows VMS, and port 22 will be used for Linux VMs.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3491b-152">-Credential</span><span class="sxs-lookup"><span data-stu-id="3491b-152">-Credential</span></span>
<span data-ttu-id="3491b-153">Bu ölçek kümesindeki VM 'Ler için yönetici kimlik bilgileri (Kullanıcı adı ve parola).</span><span class="sxs-lookup"><span data-stu-id="3491b-153">The administrator credentials (username and password) for VMs in this Scale Set.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: SimpleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3491b-154">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="3491b-154">-DataDiskSizeInGb</span></span>
<span data-ttu-id="3491b-155">Veri disklerinin boyutunu GB cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="3491b-155">Specifies the sizes of data disks in GB.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3491b-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3491b-156">-DefaultProfile</span></span>
<span data-ttu-id="3491b-157">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3491b-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3491b-158">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="3491b-158">-DomainNameLabel</span></span>
<span data-ttu-id="3491b-159">Bu ölçek kümesi için genel Fully-Qualified etki alanı adı (FQDN) için etki alanı adı etiketi.</span><span class="sxs-lookup"><span data-stu-id="3491b-159">The domain name label for the public Fully-Qualified domain name (FQDN) for this Scale Set.</span></span> <span data-ttu-id="3491b-160">Bu, etki alanı adının ölçek kümesine otomatik olarak atandığı ilk bileşenidir.</span><span class="sxs-lookup"><span data-stu-id="3491b-160">This is the first component of the domain name that is automatically assigned to the Scale Set.</span></span> <span data-ttu-id="3491b-161">Otomatik olarak atanan etki alanı adları formu ( <DomainNameLabel> . <Location> . cloudapp.azure.com).</span><span class="sxs-lookup"><span data-stu-id="3491b-161">Automatically assigned Domain names use the form (<DomainNameLabel>.<Location>.cloudapp.azure.com).</span></span> <span data-ttu-id="3491b-162">Değer sağlanmadıysa, varsayılan etki alanı adı etiketi <ScaleSetName> ve <ResourceGroupName> .</span><span class="sxs-lookup"><span data-stu-id="3491b-162">If no value is supplied, the default domain name label will be the concatenation of <ScaleSetName> and <ResourceGroupName>.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3491b-163">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="3491b-163">-EnableUltraSSD</span></span>
<span data-ttu-id="3491b-164">Ölçek kümesindeki VM 'Ler için UltraSSD diskleri kullanın.</span><span class="sxs-lookup"><span data-stu-id="3491b-164">Use UltraSSD disks for the VMs in the scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3491b-165">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="3491b-165">-EncryptionAtHost</span></span>
<span data-ttu-id="3491b-166">Bu parametre, konaktaki kaynak/Temp diski dahil tüm disklerde şifrelemeyi etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="3491b-166">This parameter will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="3491b-167">Varsayılan: Bu özellik kaynak için doğru olarak ayarlanmadıkça konaktaki şifreleme devre dışı bırakılır.</span><span class="sxs-lookup"><span data-stu-id="3491b-167">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3491b-168">-Çıkarma Ilkesi</span><span class="sxs-lookup"><span data-stu-id="3491b-168">-EvictionPolicy</span></span>
<span data-ttu-id="3491b-169">Düşük öncelikli sanal makine ölçek kümesi çıkarma ilkesi.</span><span class="sxs-lookup"><span data-stu-id="3491b-169">The eviction policy for the low priority virtual machine scale set.</span></span>  <span data-ttu-id="3491b-170">Yalnızca desteklenen değerler ' ayırması ' ve ' Sil ' değerleridir.</span><span class="sxs-lookup"><span data-stu-id="3491b-170">Only supported values are 'Deallocate' and 'Delete'.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3491b-171">-Frontenvseçpoolname</span><span class="sxs-lookup"><span data-stu-id="3491b-171">-FrontendPoolName</span></span>
<span data-ttu-id="3491b-172">Ölçek kümesi yük dengeleyicisinde kullanılacak ön uç adres havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="3491b-172">The name of the frontend address pool to use in the Scale Set load balancer.</span></span>  <span data-ttu-id="3491b-173">Değer sağlanmadıysa, ölçek kümesiyle aynı ada sahip yeni bir ön uç adres havuzu oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3491b-173">If no value is supplied, a new Frontend Address Pool will be created, with the same name as the scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3491b-174">-Hostgroupıd</span><span class="sxs-lookup"><span data-stu-id="3491b-174">-HostGroupId</span></span>
<span data-ttu-id="3491b-175">Sanal makine ölçek kümesinin bulunacağı adanmış konak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="3491b-175">Specifies the dedicated host group the virtual machine scale set will reside in.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: HostGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="3491b-176">-GörüntüAdı</span><span class="sxs-lookup"><span data-stu-id="3491b-176">-ImageName</span></span>
<span data-ttu-id="3491b-177">Bu ölçek kümesindeki VM 'Lerin adı.</span><span class="sxs-lookup"><span data-stu-id="3491b-177">The name of the image for VMs in this Scale Set.</span></span> <span data-ttu-id="3491b-178">Değer sağlanmazsa, "Windows Server 2016 DataCenter" resmi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3491b-178">If no value is provided, the "Windows Server 2016 DataCenter" image will be used.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3491b-179">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="3491b-179">-InstanceCount</span></span>
<span data-ttu-id="3491b-180">Ölçek kümesindeki VM görüntülerinin sayısı.</span><span class="sxs-lookup"><span data-stu-id="3491b-180">The number of VM images in the Scale Set.</span></span>  <span data-ttu-id="3491b-181">Değer sağlanmazsa, 2 örnek oluşturulacaktır.</span><span class="sxs-lookup"><span data-stu-id="3491b-181">If no value is provided, 2 instances will be created.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3491b-182">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="3491b-182">-LoadBalancerName</span></span>
<span data-ttu-id="3491b-183">Bu ölçek kümesiyle kullanılacak yük dengeleyicinin adı.</span><span class="sxs-lookup"><span data-stu-id="3491b-183">The name of the load balancer to use with this Scale Set.</span></span>  <span data-ttu-id="3491b-184">Değer belirtilmemişse, ölçek kümesiyle aynı adı kullanan yeni bir yük dengeleyici oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3491b-184">A new load balancer using the same name as the Scale Set will be created if no value is specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3491b-185">-Konum</span><span class="sxs-lookup"><span data-stu-id="3491b-185">-Location</span></span>
<span data-ttu-id="3491b-186">Bu ölçek kümesinin oluşturulacağı Azure konumu.</span><span class="sxs-lookup"><span data-stu-id="3491b-186">The Azure location where this Scale Set will be created.</span></span>  <span data-ttu-id="3491b-187">Değer belirtilmemişse, konum, parametrelerde başvurulan diğer kaynakların konumundan çıkarılacaktır.</span><span class="sxs-lookup"><span data-stu-id="3491b-187">If no value is specified, the location will be inferred from the location of other resources referenced in the parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3491b-188">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="3491b-188">-MaxPrice</span></span>
<span data-ttu-id="3491b-189">Düşük öncelikli sanal makine ölçeği kümesi faturalandırmanın maks.</span><span class="sxs-lookup"><span data-stu-id="3491b-189">The max price of the billing of a low priority virtual machine scale set.</span></span>

```yaml
Type: System.Double
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3491b-190">-Natbackendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="3491b-190">-NatBackendPort</span></span>
<span data-ttu-id="3491b-191">Gelen ağ adresi çevirisi için arka uç bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="3491b-191">Backend port for inbound network address translation.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3491b-192">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="3491b-192">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="3491b-193">Her bir yerleştirme grubu için hata etki alanı sayısı.</span><span class="sxs-lookup"><span data-stu-id="3491b-193">Fault Domain count for each placement group.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3491b-194">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="3491b-194">-Priority</span></span>
<span data-ttu-id="3491b-195">Ölçek kümesindeki sanal makinenin önceliği.</span><span class="sxs-lookup"><span data-stu-id="3491b-195">The priority for the virtual machine in the scale set.</span></span>  <span data-ttu-id="3491b-196">Yalnızca desteklenen değerler ' Regular ', ' nokta ' ve ' düşük ' değerleridir.</span><span class="sxs-lookup"><span data-stu-id="3491b-196">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="3491b-197">' Regular ' normal sanal makine içindir.</span><span class="sxs-lookup"><span data-stu-id="3491b-197">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="3491b-198">' Spot ', spot sanal makine içindir.</span><span class="sxs-lookup"><span data-stu-id="3491b-198">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="3491b-199">' Low ', spot sanal makine için de, ancak ' nokta ' ile değiştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="3491b-199">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="3491b-200">Lütfen ' düşük ' yerine ' nokta ' kullanın.</span><span class="sxs-lookup"><span data-stu-id="3491b-200">Please use 'Spot' instead of 'Low'.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3491b-201">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="3491b-201">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="3491b-202">Bu ölçek kümesiyle kullanılacak yakınlık Yerleşim grubunun kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="3491b-202">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: ProximityPlacementGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3491b-203">-Publicıpaddressname</span><span class="sxs-lookup"><span data-stu-id="3491b-203">-PublicIpAddressName</span></span>
<span data-ttu-id="3491b-204">Bu ölçek kümesiyle kullanılacak ortak IP adresi adı.</span><span class="sxs-lookup"><span data-stu-id="3491b-204">The name of the public IP Address to use with this scale set.</span></span>  <span data-ttu-id="3491b-205">Değer sağlanmadıysa ölçek kümesiyle aynı ada sahip yeni bir genel IPAddress oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3491b-205">A new Public IPAddress with the same name as the Scale Set will be created if no value is provided.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3491b-206">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3491b-206">-ResourceGroupName</span></span>
<span data-ttu-id="3491b-207">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3491b-207">Specifies the name of the resource group of the VMSS.</span></span>  <span data-ttu-id="3491b-208">Değer belirtilmemişse, ölçek kümesiyle aynı ad kullanılarak yeni bir ResourceGroup oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3491b-208">If no value is specified, a new ResourceGroup will be created using the same name as the Scale Set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3491b-209">-Scaleınpolicy</span><span class="sxs-lookup"><span data-stu-id="3491b-209">-ScaleInPolicy</span></span>
<span data-ttu-id="3491b-210">Sanal makine ölçeği kümesinde ölçeklendirme yapılırken izlenen kurallar.</span><span class="sxs-lookup"><span data-stu-id="3491b-210">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="3491b-211">Olası değerler: ' default ', ' OldestVM ' ve ' NewestVM '.</span><span class="sxs-lookup"><span data-stu-id="3491b-211">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="3491b-212">' Varsayılan ' sanal makine ölçeği kümesi içinde ölçeklendirildiyse, ölçek kümesi ilk olarak bölgeler genelinde dengelenebilir ve bu bir zonal ölçeği kümesidir.</span><span class="sxs-lookup"><span data-stu-id="3491b-212">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="3491b-213">Ardından, hata etki alanları genelinde mümkün olduğunca dengeli olacaktır.</span><span class="sxs-lookup"><span data-stu-id="3491b-213">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="3491b-214">Her hata etki alanı içinde, kaldırılmak üzere seçilen sanal makineler, ölçek ile korunmayan en yeni değerler olacaktır.</span><span class="sxs-lookup"><span data-stu-id="3491b-214">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="3491b-215">' OldestVM ' sanal makine ölçeği kümesi ölçeklendiğinde, ölçeğe korunmayan en eski sanal makineler kaldırılmak üzere seçilir.</span><span class="sxs-lookup"><span data-stu-id="3491b-215">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="3491b-216">Zonal sanal makine ölçek kümeleri için, ölçek kümesi önce bölgeler arasında dengelenecek.</span><span class="sxs-lookup"><span data-stu-id="3491b-216">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="3491b-217">Her bir bölgede, korunmayan en eski sanal makineler kaldırılmak üzere seçilir.</span><span class="sxs-lookup"><span data-stu-id="3491b-217">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="3491b-218">' NewestVM ' sanal makine ölçeği kümesi ölçeklendiğinde, ölçeğe korunmayan en yeni sanal makineler kaldırılmak üzere seçilir.</span><span class="sxs-lookup"><span data-stu-id="3491b-218">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="3491b-219">Zonal sanal makine ölçek kümeleri için, ölçek kümesi önce bölgeler arasında dengelenecek.</span><span class="sxs-lookup"><span data-stu-id="3491b-219">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="3491b-220">Her bir bölgede, korunmayan en yeni sanal makineler kaldırılmak üzere seçilir.</span><span class="sxs-lookup"><span data-stu-id="3491b-220">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3491b-221">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="3491b-221">-SecurityGroupName</span></span>
<span data-ttu-id="3491b-222">Bu ölçek kümesine uygulanacak ağ güvenlik grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="3491b-222">The name of the network security group to apply to this Scale Set.</span></span>  <span data-ttu-id="3491b-223">Değer sağlanmazsa, ölçek kümesiyle aynı ada sahip bir varsayılan ağ güvenlik grubu oluşturulur ve ölçek kümesine uygulanır.</span><span class="sxs-lookup"><span data-stu-id="3491b-223">If no value is provided, a default network security group with the same name as the Scale Set will be created and applied to the Scale Set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3491b-224">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="3491b-224">-SinglePlacementGroup</span></span>
<span data-ttu-id="3491b-225">Tek bir yerleştirme grubunda ölçek kümesi oluşturmak için bunu kullanın; varsayılan, birden çok gruptur</span><span class="sxs-lookup"><span data-stu-id="3491b-225">Use this to create the Scale set in a single placement group, default is multiple groups</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3491b-226">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="3491b-226">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="3491b-227">Uzantıların fazladan sağlanan diğer VM 'lerde çalıştırılmamıştır.</span><span class="sxs-lookup"><span data-stu-id="3491b-227">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3491b-228">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3491b-228">-SubnetAddressPrefix</span></span>
<span data-ttu-id="3491b-229">Bu ScaleSet 'in kullanacağı alt ağın adres öneki.</span><span class="sxs-lookup"><span data-stu-id="3491b-229">The address prefix of the Subnet this ScaleSet will use.</span></span> <span data-ttu-id="3491b-230">Değer sağlanmazsa varsayılan alt ağ ayarları (192.168.1.0/24) uygulanacaktır.</span><span class="sxs-lookup"><span data-stu-id="3491b-230">Default Subnet settings (192.168.1.0/24) will be applied if no value is provided.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3491b-231">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="3491b-231">-SubnetName</span></span>
<span data-ttu-id="3491b-232">Bu ölçek kümesiyle kullanılacak alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="3491b-232">The name of the subnet to use with this Scale Set.</span></span>  <span data-ttu-id="3491b-233">Değer sağlanmadıysa, ölçek kümesiyle aynı adla yeni bir alt ağ oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3491b-233">A new Subnet will be created with the same name as the Scale Set if no value is provided.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3491b-234">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="3491b-234">-SystemAssignedIdentity</span></span>
<span data-ttu-id="3491b-235">Parametre varsa, ölçek kümesindeki VM 'ler (lar) otomatik olarak oluşturulan bir yönetilen sistem kimliğine atanır.</span><span class="sxs-lookup"><span data-stu-id="3491b-235">If the parameter is present then the VM(s) in the scale set is(are) assigned a managed system identity that is auto generated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3491b-236">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="3491b-236">-UpgradePolicyMode</span></span>
<span data-ttu-id="3491b-237">Bu ölçek kümesindeki VM örnekleri için yükseltme ilkesi modu.</span><span class="sxs-lookup"><span data-stu-id="3491b-237">The upgrade policy mode for VM instances in this Scale Set.</span></span>  <span data-ttu-id="3491b-238">Yükseltme ilkesi otomatik, El Ile veya çalışırken yükseltme belirleyebilir.</span><span class="sxs-lookup"><span data-stu-id="3491b-238">Upgrade policy could specify Automatic, Manual, or Rolling upgrades.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.UpgradeMode
Parameter Sets: SimpleParameterSet
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3491b-239">-Useratandidentity</span><span class="sxs-lookup"><span data-stu-id="3491b-239">-UserAssignedIdentity</span></span>
<span data-ttu-id="3491b-240">Ölçek kümesindeki VM 'ler 'e atanması gereken yönetilen hizmet kimliğinin adı.</span><span class="sxs-lookup"><span data-stu-id="3491b-240">The name of a managed service identity that should be assigned to the VM(s) in the scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3491b-241">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3491b-241">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="3491b-242">Bu cmdlet 'in oluşturduğu VMSS 'in özelliklerini içeren **VirtualMachineScaleSet** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3491b-242">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3491b-243">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="3491b-243">-VirtualNetworkName</span></span>
<span data-ttu-id="3491b-244">Bu ölçek kümesiyle birlikte kullanılacak sanal ağın adı.</span><span class="sxs-lookup"><span data-stu-id="3491b-244">The name fo the Virtual Network to use with this scale set.</span></span>  <span data-ttu-id="3491b-245">Değer sağlanmadıysa, ölçek kümesiyle aynı ada sahip yeni bir sanal ağ oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3491b-245">If no value is supplied, a new virtual network with the same name as the Scale Set will be created.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3491b-246">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="3491b-246">-VMScaleSetName</span></span>
<span data-ttu-id="3491b-247">Bu cmdlet 'in oluşturduğu VMSS 'nin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3491b-247">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3491b-248">-VmSize</span><span class="sxs-lookup"><span data-stu-id="3491b-248">-VmSize</span></span>
<span data-ttu-id="3491b-249">Bu ölçek kümesindeki VM örneklerinin boyutu.</span><span class="sxs-lookup"><span data-stu-id="3491b-249">The size of the VM instances in this scale set.</span></span>  <span data-ttu-id="3491b-250">Boyut belirtilmemişse varsayılan boyut (Standard_DS1_v2) kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3491b-250">A default size (Standard_DS1_v2) will be used if no Size is specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3491b-251">-VnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3491b-251">-VnetAddressPrefix</span></span>
<span data-ttu-id="3491b-252">Bu ölçek kümesiyle kullanılan sanal ağın adres öneki.</span><span class="sxs-lookup"><span data-stu-id="3491b-252">The address prefix for the virtual network used with this Scale Set.</span></span>  <span data-ttu-id="3491b-253">Değer sağlanmadıysa varsayılan sanal ağ adresi önek ayarları (192.168.0.0/16) kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="3491b-253">Default virtual network address prefix settings (192.168.0.0/16) will be used if no value is supplied.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3491b-254">-Bölge</span><span class="sxs-lookup"><span data-stu-id="3491b-254">-Zone</span></span>
<span data-ttu-id="3491b-255">Kaynağın gelmesi gerektiğini belirten kullanılabilirlik bölgelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="3491b-255">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="3491b-256">-Onay</span><span class="sxs-lookup"><span data-stu-id="3491b-256">-Confirm</span></span>
<span data-ttu-id="3491b-257">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3491b-257">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3491b-258">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3491b-258">-WhatIf</span></span>
<span data-ttu-id="3491b-259">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3491b-259">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3491b-260">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3491b-260">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3491b-261">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3491b-261">CommonParameters</span></span>
<span data-ttu-id="3491b-262">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3491b-262">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3491b-263">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3491b-263">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3491b-264">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3491b-264">INPUTS</span></span>

### <span data-ttu-id="3491b-265">System. String</span><span class="sxs-lookup"><span data-stu-id="3491b-265">System.String</span></span>

### <span data-ttu-id="3491b-266">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3491b-266">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="3491b-267">System. Koleksiyonlar. Generic. LIST ' 1 [[System. String, System. Private. CoreLib, Version = 4.0.0.0</span><span class="sxs-lookup"><span data-stu-id="3491b-267">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="3491b-268">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3491b-268">OUTPUTS</span></span>

### <span data-ttu-id="3491b-269">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3491b-269">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="3491b-270">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3491b-270">NOTES</span></span>

## <span data-ttu-id="3491b-271">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3491b-271">RELATED LINKS</span></span>

[<span data-ttu-id="3491b-272">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3491b-272">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="3491b-273">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3491b-273">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="3491b-274">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3491b-274">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="3491b-275">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3491b-275">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="3491b-276">Başlangıç-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3491b-276">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="3491b-277">Dur-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3491b-277">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="3491b-278">Güncelleştirme-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3491b-278">Update-AzVmss</span></span>](./Update-AzVmss.md)


