---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 50a8cd14c6ea61f7c772df96f4addb9ae7955444
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918259"
---
# <span data-ttu-id="57beb-101">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="57beb-101">New-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="57beb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57beb-102">SYNOPSIS</span></span>
<span data-ttu-id="57beb-103">Bir yük dengeleyici için giden kuralı yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="57beb-103">Creates an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="57beb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="57beb-104">SYNTAX</span></span>

### <span data-ttu-id="57beb-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="57beb-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPool <PSBackendAddressPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="57beb-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="57beb-106">SetByResourceId</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPoolId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="57beb-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="57beb-107">DESCRIPTION</span></span>
<span data-ttu-id="57beb-108">**New-Azloadbalanceroutboundbir** Azure Yük Dengeleyici için bir giden kuralı yapılandırması oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="57beb-108">The **New-AzLoadBalancerOutboundRuleConfig** cmdlet creates an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="57beb-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="57beb-109">EXAMPLES</span></span>

### <span data-ttu-id="57beb-110">Örnek 1: yük dengeleyici için giden kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="57beb-110">Example 1: Create an outbound rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic" -Sku "Standard"
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\>$backend = New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool01"
PS C:\>New-AzLoadBalancerOutboundRuleConfig -Name "MyOutboundRule" -Protocol "Tcp" -FrontendIPConfiguration $frontend -BackendAddressPool $backend
```

<span data-ttu-id="57beb-111">İlk komut MyResourceGroup adlı kaynak grubunda MyPublicIP adlı genel bir IP adresi oluşturur ve $publicip değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="57beb-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="57beb-112">İkinci komut, $publicip genel IP adresini kullanarak FrontendIpConfig01 adlı ön uç IP yapılandırması oluşturur ve $frontend değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="57beb-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="57beb-113">Üçüncü komut BackendAddressPool01 adlı bir arka uç adres havuzu yapılandırması oluşturur ve $backend değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="57beb-113">The third command creates a back-end address pool configuration named BackendAddressPool01, and then stores it in the $backend variable.</span></span>
<span data-ttu-id="57beb-114">Dördüncü komut, $frontend ve $backend ön uç ve arka uç nesnelerini kullanarak M, Boundrule adlı bir giden kuralı yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="57beb-114">The fourth command creates an outbound rule configuration named MyOutboundRule using the front-end and back-end objects in $frontend and $backend.</span></span>
<span data-ttu-id="57beb-115">*Protokol* , *Frontendıyapılandırma* ve *backendaddresspool* parametrelerinin bir giden kural yapılandırması oluşturması gerekir.</span><span class="sxs-lookup"><span data-stu-id="57beb-115">The *Protocol* , *FrontendIPConfiguration* , and *BackendAddressPool* parameters are all required to create an outbound rule configuration.</span></span>

## <span data-ttu-id="57beb-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="57beb-116">PARAMETERS</span></span>

### <span data-ttu-id="57beb-117">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="57beb-117">-AllocatedOutboundPort</span></span>
<span data-ttu-id="57beb-118">NAT için kullanılacak giden bağlantı noktalarının sayısı.</span><span class="sxs-lookup"><span data-stu-id="57beb-118">The number of outbound ports to be used for NAT.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57beb-119">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="57beb-119">-BackendAddressPool</span></span>
<span data-ttu-id="57beb-120">Bir DIP havuzuna başvuru.</span><span class="sxs-lookup"><span data-stu-id="57beb-120">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="57beb-121">Giden trafik, arka uç IP 'lerde, IP 'Ler genelinde rasgele yük dengelemesi yapılır.</span><span class="sxs-lookup"><span data-stu-id="57beb-121">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57beb-122">-Backendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="57beb-122">-BackendAddressPoolId</span></span>
<span data-ttu-id="57beb-123">Bir DIP havuzuna başvuru.</span><span class="sxs-lookup"><span data-stu-id="57beb-123">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="57beb-124">Giden trafik, arka uç IP 'lerde, IP 'Ler genelinde rasgele yük dengelemesi yapılır.</span><span class="sxs-lookup"><span data-stu-id="57beb-124">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57beb-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57beb-125">-DefaultProfile</span></span>
<span data-ttu-id="57beb-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="57beb-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57beb-127">-Enabletcönayar</span><span class="sxs-lookup"><span data-stu-id="57beb-127">-EnableTcpReset</span></span>
<span data-ttu-id="57beb-128">TCP akışı boşta durma zaman aşımından veya beklenmeyen bağlantı sonlandırmasına iki yönlü TCP sıfırlama alma.</span><span class="sxs-lookup"><span data-stu-id="57beb-128">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="57beb-129">Bu öğe yalnızca protokol TCP olarak ayarlandığında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="57beb-129">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="57beb-130">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="57beb-130">-FrontendIpConfiguration</span></span>
<span data-ttu-id="57beb-131">Yük dengeleyicinin ön uç IP adresleri.</span><span class="sxs-lookup"><span data-stu-id="57beb-131">The Frontend IP addresses of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57beb-132">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="57beb-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="57beb-133">TCP boştaki bağlantının zaman aşımı</span><span class="sxs-lookup"><span data-stu-id="57beb-133">The timeout for the TCP idle connection</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57beb-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="57beb-134">-Name</span></span>
<span data-ttu-id="57beb-135">Giden kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="57beb-135">Name of the outbound rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57beb-136">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="57beb-136">-Protocol</span></span>
<span data-ttu-id="57beb-137">Protokol-TCP, UDP veya tümü</span><span class="sxs-lookup"><span data-stu-id="57beb-137">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="57beb-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="57beb-138">-Confirm</span></span>
<span data-ttu-id="57beb-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="57beb-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57beb-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57beb-140">-WhatIf</span></span>
<span data-ttu-id="57beb-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="57beb-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57beb-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="57beb-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57beb-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57beb-143">CommonParameters</span></span>
<span data-ttu-id="57beb-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="57beb-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57beb-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57beb-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57beb-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="57beb-146">INPUTS</span></span>

### <span data-ttu-id="57beb-147">System. Int32</span><span class="sxs-lookup"><span data-stu-id="57beb-147">System.Int32</span></span>

### <span data-ttu-id="57beb-148">System. String</span><span class="sxs-lookup"><span data-stu-id="57beb-148">System.String</span></span>

### <span data-ttu-id="57beb-149">Microsoft. Azure. Commands. Network. model. Psresourceıd []</span><span class="sxs-lookup"><span data-stu-id="57beb-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="57beb-150">Microsoft. Azure. Commands. Network. model. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="57beb-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="57beb-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="57beb-151">OUTPUTS</span></span>

### <span data-ttu-id="57beb-152">Microsoft. Azure. Commands. Network. model. PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="57beb-152">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="57beb-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="57beb-153">NOTES</span></span>

## <span data-ttu-id="57beb-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="57beb-154">RELATED LINKS</span></span>

[<span data-ttu-id="57beb-155">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="57beb-155">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="57beb-156">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="57beb-156">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="57beb-157">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="57beb-157">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="57beb-158">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="57beb-158">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
