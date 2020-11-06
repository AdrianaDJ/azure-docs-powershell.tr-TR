---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F1522074-7EEA-4DCF-AC16-26FE8E654720
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancer.md
ms.openlocfilehash: 10e39f72de835b77a0a8e91f0752b18ee739e0e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594922"
---
# <span data-ttu-id="f9b51-101">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f9b51-101">New-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="f9b51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9b51-102">SYNOPSIS</span></span>
<span data-ttu-id="f9b51-103">Bir yük dengeleyici oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f9b51-103">Creates a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9b51-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f9b51-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancer -Name <String> -ResourceGroupName <String> -Location <String> [-Sku <String>]
 [-FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration]>]
 [-BackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-Probe <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSProbe]>]
 [-InboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-LoadBalancingRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule]>]
 [-Tag <Hashtable>]
 [-InboundNatPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatPool]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9b51-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f9b51-105">DESCRIPTION</span></span>
<span data-ttu-id="f9b51-106">**Yeni-AzureRmLoadBalancer** cmdlet 'ı bir Azure yük dengeleyici oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f9b51-106">The **New-AzureRmLoadBalancer** cmdlet creates an Azure load balancer.</span></span>

## <span data-ttu-id="f9b51-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f9b51-107">EXAMPLES</span></span>

### <span data-ttu-id="f9b51-108">Örnek 1: yük dengeleyici oluşturma</span><span class="sxs-lookup"><span data-stu-id="f9b51-108">Example 1: Create a load balancer</span></span>
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

<span data-ttu-id="f9b51-109">Bir yük dengeleyicinin dağıtılması için birkaç nesne oluşturmanız gerekir ve ilk yedi komut bu nesnelerin nasıl oluşturulduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="f9b51-109">Deploying a load balancer requires that you first create several objects, and the first seven commands show how to create those objects.</span></span>

<span data-ttu-id="f9b51-110">Sekizinci komutu MyResourceGroup adlı kaynak grubunda MyLoadBalancer adlı bir yük dengeleyici oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f9b51-110">The eighth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

<span data-ttu-id="f9b51-111">Dokuzuncu ve son komutu yeni yük dengeleyiciden başarıyla oluşturulduğundan emin olmak için alır.</span><span class="sxs-lookup"><span data-stu-id="f9b51-111">The ninth and last command gets the new load balancer to ensure it was successfully created.</span></span>

<span data-ttu-id="f9b51-112">Bu örnekte yalnızca yük dengeleyicinin nasıl oluşturulacağı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="f9b51-112">Note that this example only shows how to create a load balancer.</span></span> <span data-ttu-id="f9b51-113">NIC 'Leri farklı sanal makinelere atamak için Add-AzureRmNetworkInterfaceIpConfig cmdlet 'ini kullanarak da yapılandırmalısınız.</span><span class="sxs-lookup"><span data-stu-id="f9b51-113">You must also configure it using the Add-AzureRmNetworkInterfaceIpConfig cmdlet to assign the NICs to different virtual machines.</span></span>

## <span data-ttu-id="f9b51-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f9b51-114">PARAMETERS</span></span>

### <span data-ttu-id="f9b51-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="f9b51-115">-AsJob</span></span>
<span data-ttu-id="f9b51-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="f9b51-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f9b51-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f9b51-117">-BackendAddressPool</span></span>
<span data-ttu-id="f9b51-118">Bir yük dengeleyiciyle ilişkilendirilecek bir arka uç adres havuzu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f9b51-118">Specifies a backend address pool to associate with a load balancer.</span></span>

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

### <span data-ttu-id="f9b51-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9b51-119">-DefaultProfile</span></span>
<span data-ttu-id="f9b51-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f9b51-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9b51-121">-Force</span><span class="sxs-lookup"><span data-stu-id="f9b51-121">-Force</span></span>
<span data-ttu-id="f9b51-122">Aynı ada sahip bir yük dengeleyici olsa bile bu cmdlet 'in bir yük dengeleyici oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="f9b51-122">Indicates that this cmdlet creates a load balancer even if a load balancer with the same name already exists.</span></span>

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

### <span data-ttu-id="f9b51-123">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="f9b51-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="f9b51-124">Bir yük dengeleyiciyle ilişkilendirilecek ön uç IP adreslerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f9b51-124">Specifies a list of front-end IP addresses to associate with a load balancer.</span></span>

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

### <span data-ttu-id="f9b51-125">-InboundNatPool</span><span class="sxs-lookup"><span data-stu-id="f9b51-125">-InboundNatPool</span></span>
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

### <span data-ttu-id="f9b51-126">-InboundNatRule</span><span class="sxs-lookup"><span data-stu-id="f9b51-126">-InboundNatRule</span></span>
<span data-ttu-id="f9b51-127">Bir yük dengeleyiciyle ilişkilendirilecek gelen ağ adresi çevirisi (NAT) kurallarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f9b51-127">Specifies a list of inbound network address translation (NAT) rules to associate with a load balancer.</span></span>

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

### <span data-ttu-id="f9b51-128">-LoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="f9b51-128">-LoadBalancingRule</span></span>
<span data-ttu-id="f9b51-129">Yük Dengeleyici ile ilişkilendirilecek Yük Dengeleme kurallarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f9b51-129">Specifies a list of load balancing rules to associate with a load balancer.</span></span>

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

### <span data-ttu-id="f9b51-130">-Konum</span><span class="sxs-lookup"><span data-stu-id="f9b51-130">-Location</span></span>
<span data-ttu-id="f9b51-131">Yük dengeleyicinin oluşturulacağı bölgeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f9b51-131">Specifies the region in which to create a load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9b51-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="f9b51-132">-Name</span></span>
<span data-ttu-id="f9b51-133">Bu, oluşturduğu yük dengeleyicinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f9b51-133">Specifies the name of the load balancer that this creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9b51-134">-Araştırma</span><span class="sxs-lookup"><span data-stu-id="f9b51-134">-Probe</span></span>
<span data-ttu-id="f9b51-135">Bir yük dengeleyiciyle ilişkilendirilecek yoklamayla listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f9b51-135">Specifies a list of probes to associate with a load balancer.</span></span>

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

### <span data-ttu-id="f9b51-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9b51-136">-ResourceGroupName</span></span>
<span data-ttu-id="f9b51-137">Yük dengeleyici oluşturulacak kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f9b51-137">Specifies the name of the resource group in which to create a load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9b51-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="f9b51-138">-Sku</span></span>
<span data-ttu-id="f9b51-139">Yük dengeleyici SKU adı.</span><span class="sxs-lookup"><span data-stu-id="f9b51-139">The load balancer Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9b51-140">Etiketli</span><span class="sxs-lookup"><span data-stu-id="f9b51-140">-Tag</span></span>
<span data-ttu-id="f9b51-141">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="f9b51-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f9b51-142">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="f9b51-142">For example:</span></span>

<span data-ttu-id="f9b51-143">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="f9b51-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9b51-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="f9b51-144">-Confirm</span></span>
<span data-ttu-id="f9b51-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f9b51-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9b51-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9b51-146">-WhatIf</span></span>
<span data-ttu-id="f9b51-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f9b51-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9b51-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f9b51-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9b51-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9b51-149">CommonParameters</span></span>
<span data-ttu-id="f9b51-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f9b51-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9b51-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9b51-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9b51-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f9b51-152">INPUTS</span></span>

### <span data-ttu-id="f9b51-153">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f9b51-153">None</span></span>
<span data-ttu-id="f9b51-154">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="f9b51-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f9b51-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f9b51-155">OUTPUTS</span></span>

### <span data-ttu-id="f9b51-156">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f9b51-156">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f9b51-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f9b51-157">NOTES</span></span>

## <span data-ttu-id="f9b51-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f9b51-158">RELATED LINKS</span></span>

[<span data-ttu-id="f9b51-159">Add-Azurermnetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="f9b51-159">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="f9b51-160">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f9b51-160">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="f9b51-161">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f9b51-161">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)

[<span data-ttu-id="f9b51-162">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f9b51-162">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)
