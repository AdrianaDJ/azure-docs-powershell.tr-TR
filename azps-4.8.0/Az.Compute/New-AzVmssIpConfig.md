---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
ms.openlocfilehash: e2ca08746ab9b4dc2ef2265a59cdab00ac42cf33
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268588"
---
# <span data-ttu-id="575cb-101">New-AzVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="575cb-101">New-AzVmssIpConfig</span></span>

## <span data-ttu-id="575cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="575cb-102">SYNOPSIS</span></span>
<span data-ttu-id="575cb-103">Bir VMSS ağ arabirimi için bir IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="575cb-103">Creates an IP configuration for a network interface of a VMSS.</span></span>

## <span data-ttu-id="575cb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="575cb-104">SYNTAX</span></span>

```
New-AzVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-IpTag <VirtualMachineScaleSetIpTag[]>] [-PublicIPPrefix <String>]
 [-PublicIPAddressVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="575cb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="575cb-105">DESCRIPTION</span></span>
<span data-ttu-id="575cb-106">**New-AzVmssIpConfig** cmdlet 'ı sanal makine ölçek kümesinin (VMSS) ağ arabirimi IÇIN bir IP yapılandırması nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="575cb-106">The **New-AzVmssIpConfig** cmdlet creates an IP configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="575cb-107">Bu cmdlet 'teki yapılandırmayı Add-AzVmssNetworkInterfaceConfiguration cmdlet 'inin *IP* yapılandırması parametresi olarak belirtin.</span><span class="sxs-lookup"><span data-stu-id="575cb-107">Specify the configuration from this cmdlet as the *IPConfiguration* parameter of the Add-AzVmssNetworkInterfaceConfiguration cmdlet.</span></span>

## <span data-ttu-id="575cb-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="575cb-108">EXAMPLES</span></span>

### <span data-ttu-id="575cb-109">Örnek 1: bir VMSS arabirimi için IP yapılandırma nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="575cb-109">Example 1: Create an IP configuration object for a VMSS interface</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

<span data-ttu-id="575cb-110">Bu komut, ContosoVmssInterface02 adlı bir IP yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="575cb-110">This command creates an IP configuration object named ContosoVmssInterface02.</span></span>
<span data-ttu-id="575cb-111">Komut, $SubnetId depolanan önceden tanımlanmış bir alt ağ KIMLIĞINI kullanır.</span><span class="sxs-lookup"><span data-stu-id="575cb-111">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="575cb-112">Komut, $IPConfiguration değişkeninde, daha sonra **Add-Azvmssnetworkınterfaceconfiguration** ile kullanmak üzere yapılandırma ayarlarını depolar.</span><span class="sxs-lookup"><span data-stu-id="575cb-112">The command stores the configuration settings in the $IPConfiguration variable for later use with **Add-AzVmssNetworkInterfaceConfiguration**.</span></span>

### <span data-ttu-id="575cb-113">Örnek 2: NAT havuz ayarlarını içeren bir IP yapılandırma nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="575cb-113">Example 2: Create an IP configuration object that includes NAT pool settings</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

<span data-ttu-id="575cb-114">Bu komut ContosoVmssInterface03 adlı bir IP yapılandırma nesnesi oluşturur ve daha sonra kullanmak üzere $IPConfiguration değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="575cb-114">This command creates an IP configuration object named ContosoVmssInterface03, and then stores it in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="575cb-115">Komut, $SubnetId depolanan önceden tanımlanmış bir alt ağ KIMLIĞINI kullanır.</span><span class="sxs-lookup"><span data-stu-id="575cb-115">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="575cb-116">Komut, $IPConfiguration değişkeninde yapılandırma ayarlarını daha sonra kullanmak üzere depolar.</span><span class="sxs-lookup"><span data-stu-id="575cb-116">The command stores the configuration settings in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="575cb-117">Komut, *Loadbalancerınboundnatpoolsid* ve *Loadbalancerbackendaddresspoolsid* parametrelerinin değerlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="575cb-117">The command specifies values for the *LoadBalancerInboundNatPoolsId* and *LoadBalancerBackendAddressPoolsId* parameters.</span></span>

## <span data-ttu-id="575cb-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="575cb-118">PARAMETERS</span></span>

### <span data-ttu-id="575cb-119">-ApplicationGatewayBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="575cb-119">-ApplicationGatewayBackendAddressPoolsId</span></span>
<span data-ttu-id="575cb-120">Yük dengeleyicilerde arka uç adres havuzlarına başvurular dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="575cb-120">Specifies an array of references to backend address pools of load balancers.</span></span>
<span data-ttu-id="575cb-121">Ölçek kümesi, genel ve bir iç yük dengeleyicinin arka uç adres havuzlarına başvurabilir.</span><span class="sxs-lookup"><span data-stu-id="575cb-121">A scale set can reference backend address pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="575cb-122">Birden çok ölçek kümesi aynı yük dengeleyiciyi kullanamaz.</span><span class="sxs-lookup"><span data-stu-id="575cb-122">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="575cb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="575cb-123">-DefaultProfile</span></span>
<span data-ttu-id="575cb-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="575cb-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="575cb-125">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="575cb-125">-DnsSetting</span></span>
<span data-ttu-id="575cb-126">Publicıp adreslerine uygulanacak DNS ayarları.</span><span class="sxs-lookup"><span data-stu-id="575cb-126">The dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="575cb-127">Publicıp adreslerine uygulanacak DNS ayarlarının etki alanı adı etiketi.</span><span class="sxs-lookup"><span data-stu-id="575cb-127">The domain name label of the Dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="575cb-128">Etki alanı adı etiketi ve VM dizinini birleştirme, oluşturulacak genel IP adresi kaynaklarının etki alanı adı etiketlerdir.</span><span class="sxs-lookup"><span data-stu-id="575cb-128">The concatenation of the domain name label and vm index will be the domain name labels of the Public IP Address resources that will be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressDomainNameLabel

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="575cb-129">-ID</span><span class="sxs-lookup"><span data-stu-id="575cb-129">-Id</span></span>
<span data-ttu-id="575cb-130">Bir KIMLIK belirtir.</span><span class="sxs-lookup"><span data-stu-id="575cb-130">Specifies an ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="575cb-131">-Ipetiketi</span><span class="sxs-lookup"><span data-stu-id="575cb-131">-IpTag</span></span>
<span data-ttu-id="575cb-132">IP etiket nesneleri dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="575cb-132">Specifies an array of Ip Tag objects.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="575cb-133">-LoadBalancerBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="575cb-133">-LoadBalancerBackendAddressPoolsId</span></span>
<span data-ttu-id="575cb-134">Yük dengeleyicileri gelen ağ adresi çevirisi (NAT) havuzlarına başvurular dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="575cb-134">Specifies an array of references to incoming network address translation (NAT) pools of the load balancers.</span></span>
<span data-ttu-id="575cb-135">Ölçek kümesi, genel ve bir iç yük dengeleyicinin gelen NAT havuzlarına başvurabilir.</span><span class="sxs-lookup"><span data-stu-id="575cb-135">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="575cb-136">Birden çok ölçek kümesi aynı yük dengeleyiciyi kullanamaz.</span><span class="sxs-lookup"><span data-stu-id="575cb-136">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="575cb-137">-Loadbalancerınboundnatpoolsid</span><span class="sxs-lookup"><span data-stu-id="575cb-137">-LoadBalancerInboundNatPoolsId</span></span>
<span data-ttu-id="575cb-138">Yük dengeleyicilerde gelen NAT havuzlarına başvuru dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="575cb-138">Specifies an array of references to incoming NAT pools of the load balancers.</span></span>
<span data-ttu-id="575cb-139">Ölçek kümesi, genel ve bir iç yük dengeleyicinin gelen NAT havuzlarına başvurabilir.</span><span class="sxs-lookup"><span data-stu-id="575cb-139">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="575cb-140">Birden çok ölçek kümesi aynı yük dengeleyiciyi kullanamaz.</span><span class="sxs-lookup"><span data-stu-id="575cb-140">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="575cb-141">-Ad</span><span class="sxs-lookup"><span data-stu-id="575cb-141">-Name</span></span>
<span data-ttu-id="575cb-142">IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="575cb-142">Specifies the name of the IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="575cb-143">-Birincil</span><span class="sxs-lookup"><span data-stu-id="575cb-143">-Primary</span></span>
<span data-ttu-id="575cb-144">Ağ arabiriminin birden fazla IP yapılandırması olması durumunda birincil IP yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="575cb-144">Specifies the primary IP Configuration in case the network interface has more than one IP Configuration.</span></span>

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

### <span data-ttu-id="575cb-145">-PrivateIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="575cb-145">-PrivateIPAddressVersion</span></span>
<span data-ttu-id="575cb-146">Özel IP adresi için IP yapılandırmasını belirtme.</span><span class="sxs-lookup"><span data-stu-id="575cb-146">Specify the IP configuration for private IP address.</span></span>  <span data-ttu-id="575cb-147">Varsayılan olarak IPv4 alınır.</span><span class="sxs-lookup"><span data-stu-id="575cb-147">Default is taken as IPv4.</span></span>  <span data-ttu-id="575cb-148">Olası değerler: ' IPv4 ' ve ' IPv6 '.</span><span class="sxs-lookup"><span data-stu-id="575cb-148">Possible values are: 'IPv4' and 'IPv6'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="575cb-149">-Publicipadresconfigurationıdintimeout ınminutes</span><span class="sxs-lookup"><span data-stu-id="575cb-149">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span></span>
<span data-ttu-id="575cb-150">Genel IP adresinin Boşta durma zaman aşımı.</span><span class="sxs-lookup"><span data-stu-id="575cb-150">The idle timeout of the public IP address.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: PublicIPAddressIdleTimeoutInMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="575cb-151">-Publicıpaddressconfigurationname</span><span class="sxs-lookup"><span data-stu-id="575cb-151">-PublicIPAddressConfigurationName</span></span>
<span data-ttu-id="575cb-152">Publicıp adresi yapılandırma adı.</span><span class="sxs-lookup"><span data-stu-id="575cb-152">The publicIP address configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="575cb-153">-Publicıpaddressversion</span><span class="sxs-lookup"><span data-stu-id="575cb-153">-PublicIPAddressVersion</span></span>
<span data-ttu-id="575cb-154">Genel IP adresinin IP yapılandırmasını belirtin.</span><span class="sxs-lookup"><span data-stu-id="575cb-154">Specify the IP configuration for public IP address.</span></span>  <span data-ttu-id="575cb-155">Varsayılan olarak IPv4 alınır.</span><span class="sxs-lookup"><span data-stu-id="575cb-155">Default is taken as IPv4.</span></span>  <span data-ttu-id="575cb-156">Olası değerler: ' IPv4 ' ve ' IPv6 '.</span><span class="sxs-lookup"><span data-stu-id="575cb-156">Possible values are: 'IPv4' and 'IPv6'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="575cb-157">-Publicıpprefix</span><span class="sxs-lookup"><span data-stu-id="575cb-157">-PublicIPPrefix</span></span>
<span data-ttu-id="575cb-158">Genel IP önekinin KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="575cb-158">The ID of Public IP Prefix</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="575cb-159">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="575cb-159">-SubnetId</span></span>
<span data-ttu-id="575cb-160">Yapılandırmanın, VMSS ağ arabirimini oluşturduğu alt ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="575cb-160">Specifies the subnet ID in which the configuration creates  the VMSS network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="575cb-161">-Onay</span><span class="sxs-lookup"><span data-stu-id="575cb-161">-Confirm</span></span>
<span data-ttu-id="575cb-162">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="575cb-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="575cb-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="575cb-163">-WhatIf</span></span>
<span data-ttu-id="575cb-164">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="575cb-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="575cb-165">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="575cb-165">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="575cb-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="575cb-166">CommonParameters</span></span>
<span data-ttu-id="575cb-167">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="575cb-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="575cb-168">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="575cb-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="575cb-169">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="575cb-169">INPUTS</span></span>

### <span data-ttu-id="575cb-170">System. String</span><span class="sxs-lookup"><span data-stu-id="575cb-170">System.String</span></span>

### <span data-ttu-id="575cb-171">System. String []</span><span class="sxs-lookup"><span data-stu-id="575cb-171">System.String[]</span></span>

### <span data-ttu-id="575cb-172">System. Int32</span><span class="sxs-lookup"><span data-stu-id="575cb-172">System.Int32</span></span>

### <span data-ttu-id="575cb-173">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSetIpTag []</span><span class="sxs-lookup"><span data-stu-id="575cb-173">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]</span></span>

## <span data-ttu-id="575cb-174">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="575cb-174">OUTPUTS</span></span>

### <span data-ttu-id="575cb-175">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSetIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="575cb-175">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration</span></span>

## <span data-ttu-id="575cb-176">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="575cb-176">NOTES</span></span>

## <span data-ttu-id="575cb-177">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="575cb-177">RELATED LINKS</span></span>

[<span data-ttu-id="575cb-178">Add-Azvmssnetworkınterfaceconfiguration</span><span class="sxs-lookup"><span data-stu-id="575cb-178">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)


