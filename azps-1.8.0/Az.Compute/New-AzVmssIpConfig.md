---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
ms.openlocfilehash: acb4496cc9413d6b056b56fe4dbb80a99dee0706
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917348"
---
# <span data-ttu-id="8848b-101">New-AzVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="8848b-101">New-AzVmssIpConfig</span></span>

## <span data-ttu-id="8848b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8848b-102">SYNOPSIS</span></span>
<span data-ttu-id="8848b-103">Bir VMSS ağ arabirimi için bir IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8848b-103">Creates an IP configuration for a network interface of a VMSS.</span></span>

## <span data-ttu-id="8848b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8848b-104">SYNTAX</span></span>

```
New-AzVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-IpTag <VirtualMachineScaleSetIpTag[]>] [-PublicIPPrefix <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8848b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8848b-105">DESCRIPTION</span></span>
<span data-ttu-id="8848b-106">**New-AzVmssIpConfig** cmdlet 'ı sanal makine ölçek kümesinin (VMSS) ağ arabirimi IÇIN bir IP yapılandırması nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8848b-106">The **New-AzVmssIpConfig** cmdlet creates an IP configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="8848b-107">Bu cmdlet 'teki yapılandırmayı Add-AzVmssNetworkInterfaceConfiguration cmdlet 'inin *IP* yapılandırması parametresi olarak belirtin.</span><span class="sxs-lookup"><span data-stu-id="8848b-107">Specify the configuration from this cmdlet as the *IPConfiguration* parameter of the Add-AzVmssNetworkInterfaceConfiguration cmdlet.</span></span>

## <span data-ttu-id="8848b-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8848b-108">EXAMPLES</span></span>

### <span data-ttu-id="8848b-109">Örnek 1: bir VMSS arabirimi için IP yapılandırma nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="8848b-109">Example 1: Create an IP configuration object for a VMSS interface</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

<span data-ttu-id="8848b-110">Bu komut, ContosoVmssInterface02 adlı bir IP yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8848b-110">This command creates an IP configuration object named ContosoVmssInterface02.</span></span>
<span data-ttu-id="8848b-111">Komut, $SubnetId depolanan önceden tanımlanmış bir alt ağ KIMLIĞINI kullanır.</span><span class="sxs-lookup"><span data-stu-id="8848b-111">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="8848b-112">Komut, $IPConfiguration değişkeninde, daha sonra **Add-Azvmssnetworkınterfaceconfiguration** ile kullanmak üzere yapılandırma ayarlarını depolar.</span><span class="sxs-lookup"><span data-stu-id="8848b-112">The command stores the configuration settings in the $IPConfiguration variable for later use with **Add-AzVmssNetworkInterfaceConfiguration**.</span></span>

### <span data-ttu-id="8848b-113">Örnek 2: NAT havuz ayarlarını içeren bir IP yapılandırma nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="8848b-113">Example 2: Create an IP configuration object that includes NAT pool settings</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

<span data-ttu-id="8848b-114">Bu komut ContosoVmssInterface03 adlı bir IP yapılandırma nesnesi oluşturur ve daha sonra kullanmak üzere $IPConfiguration değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="8848b-114">This command creates an IP configuration object named ContosoVmssInterface03, and then stores it in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="8848b-115">Komut, $SubnetId depolanan önceden tanımlanmış bir alt ağ KIMLIĞINI kullanır.</span><span class="sxs-lookup"><span data-stu-id="8848b-115">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="8848b-116">Komut, $IPConfiguration değişkeninde yapılandırma ayarlarını daha sonra kullanmak üzere depolar.</span><span class="sxs-lookup"><span data-stu-id="8848b-116">The command stores the configuration settings in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="8848b-117">Komut, *Loadbalancerınboundnatpoolsid* ve *Loadbalancerbackendaddresspoolsid* parametrelerinin değerlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8848b-117">The command specifies values for the *LoadBalancerInboundNatPoolsId* and *LoadBalancerBackendAddressPoolsId* parameters.</span></span>

## <span data-ttu-id="8848b-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8848b-118">PARAMETERS</span></span>

### <span data-ttu-id="8848b-119">-ApplicationGatewayBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="8848b-119">-ApplicationGatewayBackendAddressPoolsId</span></span>
<span data-ttu-id="8848b-120">Yük dengeleyicilerde arka uç adres havuzlarına başvurular dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="8848b-120">Specifies an array of references to backend address pools of load balancers.</span></span>
<span data-ttu-id="8848b-121">Ölçek kümesi, genel ve bir iç yük dengeleyicinin arka uç adres havuzlarına başvurabilir.</span><span class="sxs-lookup"><span data-stu-id="8848b-121">A scale set can reference backend address pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="8848b-122">Birden çok ölçek kümesi aynı yük dengeleyiciyi kullanamaz.</span><span class="sxs-lookup"><span data-stu-id="8848b-122">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="8848b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8848b-123">-DefaultProfile</span></span>
<span data-ttu-id="8848b-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8848b-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8848b-125">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="8848b-125">-DnsSetting</span></span>
<span data-ttu-id="8848b-126">Publicıp adreslerine uygulanacak DNS ayarları.</span><span class="sxs-lookup"><span data-stu-id="8848b-126">The dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="8848b-127">Publicıp adreslerine uygulanacak DNS ayarlarının etki alanı adı etiketi.</span><span class="sxs-lookup"><span data-stu-id="8848b-127">The domain name label of the Dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="8848b-128">Etki alanı adı etiketi ve VM dizinini birleştirme, oluşturulacak genel IP adresi kaynaklarının etki alanı adı etiketlerdir.</span><span class="sxs-lookup"><span data-stu-id="8848b-128">The concatenation of the domain name label and vm index will be the domain name labels of the Public IP Address resources that will be created.</span></span>

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

### <span data-ttu-id="8848b-129">-ID</span><span class="sxs-lookup"><span data-stu-id="8848b-129">-Id</span></span>
<span data-ttu-id="8848b-130">Bir KIMLIK belirtir.</span><span class="sxs-lookup"><span data-stu-id="8848b-130">Specifies an ID.</span></span>

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

### <span data-ttu-id="8848b-131">-Ipetiketi</span><span class="sxs-lookup"><span data-stu-id="8848b-131">-IpTag</span></span>
<span data-ttu-id="8848b-132">IP etiket nesneleri dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="8848b-132">Specifies an array of Ip Tag objects.</span></span>

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

### <span data-ttu-id="8848b-133">-LoadBalancerBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="8848b-133">-LoadBalancerBackendAddressPoolsId</span></span>
<span data-ttu-id="8848b-134">Yük dengeleyicileri gelen ağ adresi çevirisi (NAT) havuzlarına başvurular dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8848b-134">Specifies an array of references to incoming network address translation (NAT) pools of the load balancers.</span></span>
<span data-ttu-id="8848b-135">Ölçek kümesi, genel ve bir iç yük dengeleyicinin gelen NAT havuzlarına başvurabilir.</span><span class="sxs-lookup"><span data-stu-id="8848b-135">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="8848b-136">Birden çok ölçek kümesi aynı yük dengeleyiciyi kullanamaz.</span><span class="sxs-lookup"><span data-stu-id="8848b-136">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="8848b-137">-Loadbalancerınboundnatpoolsid</span><span class="sxs-lookup"><span data-stu-id="8848b-137">-LoadBalancerInboundNatPoolsId</span></span>
<span data-ttu-id="8848b-138">Yük dengeleyicilerde gelen NAT havuzlarına başvuru dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8848b-138">Specifies an array of references to incoming NAT pools of the load balancers.</span></span>
<span data-ttu-id="8848b-139">Ölçek kümesi, genel ve bir iç yük dengeleyicinin gelen NAT havuzlarına başvurabilir.</span><span class="sxs-lookup"><span data-stu-id="8848b-139">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="8848b-140">Birden çok ölçek kümesi aynı yük dengeleyiciyi kullanamaz.</span><span class="sxs-lookup"><span data-stu-id="8848b-140">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="8848b-141">-Ad</span><span class="sxs-lookup"><span data-stu-id="8848b-141">-Name</span></span>
<span data-ttu-id="8848b-142">IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8848b-142">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="8848b-143">-Birincil</span><span class="sxs-lookup"><span data-stu-id="8848b-143">-Primary</span></span>
<span data-ttu-id="8848b-144">Ağ arabiriminin birden fazla IP yapılandırması olması durumunda birincil IP yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8848b-144">Specifies the primary IP Configuration in case the network interface has more than one IP Configuration.</span></span>

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

### <span data-ttu-id="8848b-145">-PrivateIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="8848b-145">-PrivateIPAddressVersion</span></span>
<span data-ttu-id="8848b-146">IP yapılandırmasını IPv4 veya IPv6 olarak belirtin.</span><span class="sxs-lookup"><span data-stu-id="8848b-146">Specify the ip configuration is either IPv4 or IPv6.</span></span> <span data-ttu-id="8848b-147">Varsayılan olarak IPv4 alınır.</span><span class="sxs-lookup"><span data-stu-id="8848b-147">Default is taken as IPv4.</span></span>  <span data-ttu-id="8848b-148">Olası değerler: ' IPv4 ' ve ' IPv6 '.</span><span class="sxs-lookup"><span data-stu-id="8848b-148">Possible values are: 'IPv4' and 'IPv6'.</span></span>

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

### <span data-ttu-id="8848b-149">-Publicipadresconfigurationıdintimeout ınminutes</span><span class="sxs-lookup"><span data-stu-id="8848b-149">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span></span>
<span data-ttu-id="8848b-150">Genel IP adresinin Boşta durma zaman aşımı.</span><span class="sxs-lookup"><span data-stu-id="8848b-150">The idle timeout of the public IP address.</span></span>

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

### <span data-ttu-id="8848b-151">-Publicıpaddressconfigurationname</span><span class="sxs-lookup"><span data-stu-id="8848b-151">-PublicIPAddressConfigurationName</span></span>
<span data-ttu-id="8848b-152">Publicıp adresi yapılandırma adı.</span><span class="sxs-lookup"><span data-stu-id="8848b-152">The publicIP address configuration name.</span></span>

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

### <span data-ttu-id="8848b-153">-Publicıpprefix</span><span class="sxs-lookup"><span data-stu-id="8848b-153">-PublicIPPrefix</span></span>
<span data-ttu-id="8848b-154">Genel IP önekinin KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="8848b-154">The ID of Public IP Prefix</span></span>

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

### <span data-ttu-id="8848b-155">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="8848b-155">-SubnetId</span></span>
<span data-ttu-id="8848b-156">Yapılandırmanın, VMSS ağ arabirimini oluşturduğu alt ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="8848b-156">Specifies the subnet ID in which the configuration creates  the VMSS network interface.</span></span>

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

### <span data-ttu-id="8848b-157">-Onay</span><span class="sxs-lookup"><span data-stu-id="8848b-157">-Confirm</span></span>
<span data-ttu-id="8848b-158">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8848b-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8848b-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8848b-159">-WhatIf</span></span>
<span data-ttu-id="8848b-160">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8848b-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8848b-161">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8848b-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8848b-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8848b-162">CommonParameters</span></span>
<span data-ttu-id="8848b-163">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8848b-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8848b-164">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8848b-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8848b-165">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8848b-165">INPUTS</span></span>

### <span data-ttu-id="8848b-166">System. String</span><span class="sxs-lookup"><span data-stu-id="8848b-166">System.String</span></span>

### <span data-ttu-id="8848b-167">System. String []</span><span class="sxs-lookup"><span data-stu-id="8848b-167">System.String[]</span></span>

### <span data-ttu-id="8848b-168">System. Int32</span><span class="sxs-lookup"><span data-stu-id="8848b-168">System.Int32</span></span>

### <span data-ttu-id="8848b-169">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSetIpTag []</span><span class="sxs-lookup"><span data-stu-id="8848b-169">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]</span></span>

## <span data-ttu-id="8848b-170">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8848b-170">OUTPUTS</span></span>

### <span data-ttu-id="8848b-171">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSetIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8848b-171">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration</span></span>

## <span data-ttu-id="8848b-172">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8848b-172">NOTES</span></span>

## <span data-ttu-id="8848b-173">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8848b-173">RELATED LINKS</span></span>

[<span data-ttu-id="8848b-174">Add-Azvmssnetworkınterfaceconfiguration</span><span class="sxs-lookup"><span data-stu-id="8848b-174">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)


