---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F1522074-7EEA-4DCF-AC16-26FE8E654720
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancer.md
ms.openlocfilehash: db7d531b83dabe3bb5fc9dc79d86c3153d1553a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764929"
---
# <span data-ttu-id="d39c3-101">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d39c3-101">New-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="d39c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d39c3-102">SYNOPSIS</span></span>
<span data-ttu-id="d39c3-103">Bir yük dengeleyici oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d39c3-103">Creates a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d39c3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d39c3-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancer -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Sku <String>]
 [-FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration]>]
 [-BackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancingRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule]>]
 [-Probe <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSProbe]>]
 [-InboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-InboundNatPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatPool]>]
 [-OutboundRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSOutboundRule]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d39c3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d39c3-105">DESCRIPTION</span></span>
<span data-ttu-id="d39c3-106">**Yeni-AzureRmLoadBalancer** cmdlet 'ı bir Azure yük dengeleyici oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d39c3-106">The **New-AzureRmLoadBalancer** cmdlet creates an Azure load balancer.</span></span>

## <span data-ttu-id="d39c3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d39c3-107">EXAMPLES</span></span>

### <span data-ttu-id="d39c3-108">Örnek 1: yük dengeleyici oluşturma</span><span class="sxs-lookup"><span data-stu-id="d39c3-108">Example 1: Create a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIp" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzureRmLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig02"
PS C:\> $probe = New-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx"
PS C:\> $inboundNatRule1 = New-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule1" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389 -IdleTimeoutInMinutes 15 -EnableFloatingIP
PS C:\> $inboundNatRule2 = New-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule2" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3391 -BackendPort 3392
PS C:\> $lbrule = New-AzureRmLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol "Tcp" -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP
PS C:\> $lb = New-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -InboundNatRule $inboundNatRule1,$inboundNatRule2 -LoadBalancingRule $lbrule
PS C:\> Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="d39c3-109">Bir yük dengeleyicinin dağıtılması için birkaç nesne oluşturmanız gerekir ve ilk yedi komut bu nesnelerin nasıl oluşturulduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="d39c3-109">Deploying a load balancer requires that you first create several objects, and the first seven commands show how to create those objects.</span></span>
<span data-ttu-id="d39c3-110">Sekizinci komutu MyResourceGroup adlı kaynak grubunda MyLoadBalancer adlı bir yük dengeleyici oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d39c3-110">The eighth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>
<span data-ttu-id="d39c3-111">Dokuzuncu ve son komutu yeni yük dengeleyiciden başarıyla oluşturulduğundan emin olmak için alır.</span><span class="sxs-lookup"><span data-stu-id="d39c3-111">The ninth and last command gets the new load balancer to ensure it was successfully created.</span></span>
<span data-ttu-id="d39c3-112">Bu örnekte yalnızca yük dengeleyicinin nasıl oluşturulacağı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="d39c3-112">Note that this example only shows how to create a load balancer.</span></span> <span data-ttu-id="d39c3-113">NIC 'Leri farklı sanal makinelere atamak için Add-AzureRmNetworkInterfaceIpConfig cmdlet 'ini kullanarak da yapılandırmalısınız.</span><span class="sxs-lookup"><span data-stu-id="d39c3-113">You must also configure it using the Add-AzureRmNetworkInterfaceIpConfig cmdlet to assign the NICs to different virtual machines.</span></span>

## <span data-ttu-id="d39c3-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d39c3-114">PARAMETERS</span></span>

### <span data-ttu-id="d39c3-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="d39c3-115">-AsJob</span></span>
<span data-ttu-id="d39c3-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="d39c3-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d39c3-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d39c3-117">-BackendAddressPool</span></span>
<span data-ttu-id="d39c3-118">Bir yük dengeleyiciyle ilişkilendirilecek bir arka uç adres havuzu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d39c3-118">Specifies a backend address pool to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d39c3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d39c3-119">-DefaultProfile</span></span>
<span data-ttu-id="d39c3-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d39c3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d39c3-121">-Force</span><span class="sxs-lookup"><span data-stu-id="d39c3-121">-Force</span></span>
<span data-ttu-id="d39c3-122">Aynı ada sahip bir yük dengeleyici olsa bile bu cmdlet 'in bir yük dengeleyici oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="d39c3-122">Indicates that this cmdlet creates a load balancer even if a load balancer with the same name already exists.</span></span>

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

### <span data-ttu-id="d39c3-123">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="d39c3-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="d39c3-124">Bir yük dengeleyiciyle ilişkilendirilecek ön uç IP adreslerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d39c3-124">Specifies a list of front-end IP addresses to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d39c3-125">-InboundNatPool</span><span class="sxs-lookup"><span data-stu-id="d39c3-125">-InboundNatPool</span></span>
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatPool]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d39c3-126">-InboundNatRule</span><span class="sxs-lookup"><span data-stu-id="d39c3-126">-InboundNatRule</span></span>
<span data-ttu-id="d39c3-127">Bir yük dengeleyiciyle ilişkilendirilecek gelen ağ adresi çevirisi (NAT) kurallarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d39c3-127">Specifies a list of inbound network address translation (NAT) rules to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d39c3-128">-LoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="d39c3-128">-LoadBalancingRule</span></span>
<span data-ttu-id="d39c3-129">Yük Dengeleyici ile ilişkilendirilecek Yük Dengeleme kurallarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d39c3-129">Specifies a list of load balancing rules to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d39c3-130">-Konum</span><span class="sxs-lookup"><span data-stu-id="d39c3-130">-Location</span></span>
<span data-ttu-id="d39c3-131">Yük dengeleyicinin oluşturulacağı bölgeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="d39c3-131">Specifies the region in which to create a load balancer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d39c3-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="d39c3-132">-Name</span></span>
<span data-ttu-id="d39c3-133">Bu, oluşturduğu yük dengeleyicinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d39c3-133">Specifies the name of the load balancer that this creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d39c3-134">-OutboundRule</span><span class="sxs-lookup"><span data-stu-id="d39c3-134">-OutboundRule</span></span>
<span data-ttu-id="d39c3-135">Giden kuralları.</span><span class="sxs-lookup"><span data-stu-id="d39c3-135">The outbound rules.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSOutboundRule]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d39c3-136">-Araştırma</span><span class="sxs-lookup"><span data-stu-id="d39c3-136">-Probe</span></span>
<span data-ttu-id="d39c3-137">Bir yük dengeleyiciyle ilişkilendirilecek yoklamayla listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d39c3-137">Specifies a list of probes to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSProbe]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d39c3-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d39c3-138">-ResourceGroupName</span></span>
<span data-ttu-id="d39c3-139">Yük dengeleyici oluşturulacak kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d39c3-139">Specifies the name of the resource group in which to create a load balancer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d39c3-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="d39c3-140">-Sku</span></span>
<span data-ttu-id="d39c3-141">Yük dengeleyici SKU adı.</span><span class="sxs-lookup"><span data-stu-id="d39c3-141">The load balancer Sku name.</span></span>

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

### <span data-ttu-id="d39c3-142">Etiketli</span><span class="sxs-lookup"><span data-stu-id="d39c3-142">-Tag</span></span>
<span data-ttu-id="d39c3-143">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="d39c3-143">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d39c3-144">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="d39c3-144">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d39c3-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="d39c3-145">-Confirm</span></span>
<span data-ttu-id="d39c3-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d39c3-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d39c3-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d39c3-147">-WhatIf</span></span>
<span data-ttu-id="d39c3-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d39c3-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d39c3-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d39c3-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d39c3-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d39c3-150">CommonParameters</span></span>
<span data-ttu-id="d39c3-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d39c3-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d39c3-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d39c3-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d39c3-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d39c3-153">INPUTS</span></span>

### <span data-ttu-id="d39c3-154">System. String</span><span class="sxs-lookup"><span data-stu-id="d39c3-154">System.String</span></span>

### <span data-ttu-id="d39c3-155">System. Koleksiyonlar. Generic. LIST \` 1 [[Microsoft. Azure. Commands. Network. modeller. Psfrontendıconfiguration, Microsoft. Azure</span><span class="sxs-lookup"><span data-stu-id="d39c3-155">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="d39c3-156">System. Koleksiyonlar. Generic. LIST \` 1 [[Microsoft. Azure. Commands. Network. modeller. PSBackendAddressPool, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d39c3-156">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="d39c3-157">System. Koleksiyonlar. Generic. LIST \` 1 [[Microsoft. Azure. Commands. Network. modeller. Psaraştırması, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d39c3-157">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSProbe, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="d39c3-158">System. Koleksiyonlar. Generic. LIST \` 1 [[Microsoft. Azure. Commands. Network. modeller. Psınboundnatrule, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d39c3-158">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="d39c3-159">System. Koleksiyonlar. Generic. LIST \` 1 [[Microsoft. Azure. Commands. Network. modeller. PSLoadBalancingRule, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d39c3-159">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="d39c3-160">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d39c3-160">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d39c3-161">System. Koleksiyonlar. Generic. LIST \` 1 [[Microsoft. Azure. Commands. Network. modeller. Psınboundnatpool, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d39c3-161">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSInboundNatPool, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d39c3-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d39c3-162">OUTPUTS</span></span>

### <span data-ttu-id="d39c3-163">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d39c3-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d39c3-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d39c3-164">NOTES</span></span>

## <span data-ttu-id="d39c3-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d39c3-165">RELATED LINKS</span></span>

[<span data-ttu-id="d39c3-166">Add-Azurermnetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="d39c3-166">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="d39c3-167">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d39c3-167">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="d39c3-168">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d39c3-168">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)

[<span data-ttu-id="d39c3-169">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d39c3-169">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)
