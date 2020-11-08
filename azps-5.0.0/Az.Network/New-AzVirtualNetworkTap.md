---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkTap.md
ms.openlocfilehash: 0ac64d9b1aee363a1681b8d62da2ecf73574f7cd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278113"
---
# <span data-ttu-id="96c80-101">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="96c80-101">New-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="96c80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96c80-102">SYNOPSIS</span></span>
<span data-ttu-id="96c80-103">VirtualNetworkTap kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="96c80-103">Creates a VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="96c80-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="96c80-104">SYNTAX</span></span>

### <span data-ttu-id="96c80-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="96c80-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>]
 [-DestinationNetworkInterfaceIPConfiguration <PSNetworkInterfaceIPConfiguration>]
 [-DestinationLoadBalancerFrontEndIPConfiguration <PSFrontendIPConfiguration>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96c80-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="96c80-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>] [-DestinationNetworkInterfaceIPConfigurationId <String>]
 [-DestinationLoadBalancerFrontEndIPConfigurationId <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96c80-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="96c80-107">DESCRIPTION</span></span>
<span data-ttu-id="96c80-108">**New-AzVirtualNetworkTap** cmdlet 'ı bir Azure sanal ağı oluşturur kaynağa dokunun.</span><span class="sxs-lookup"><span data-stu-id="96c80-108">The **New-AzVirtualNetworkTap** cmdlet creates an Azure virtual network tap resource.</span></span>

## <span data-ttu-id="96c80-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="96c80-109">EXAMPLES</span></span>

### <span data-ttu-id="96c80-110">Örnek 1: Azure sanal ağı oluşturma dokunun</span><span class="sxs-lookup"><span data-stu-id="96c80-110">Example 1: Create an Azure virtual network tap</span></span>
```
PS C:\>New-AzVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationPort 8888 -DestinationNetworkInterfaceIPConfiguration $destinationNic.IpConfigurations[0]
```

<span data-ttu-id="96c80-111">Bu komut, hedef VM yapılandırması ayrıntılarını içeren "VirtualNetworkTap1" adlı bir sanal ağ oluşturur (Destinationıp yapılandırması, DestinationPort).</span><span class="sxs-lookup"><span data-stu-id="96c80-111">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (DestinationIpConfiguration, DestinationPort).</span></span>
<span data-ttu-id="96c80-112">Tüm kaynağa dokunması yapılandırılan VM 'nin trafiği bu hedef IP + bağlantı noktasına yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="96c80-112">All the source tap configured VM's traffic will be routed to this Destination IP + Port.</span></span>

### <span data-ttu-id="96c80-113">Örnek 2: LoadBalancer IP 'si kullanma</span><span class="sxs-lookup"><span data-stu-id="96c80-113">Example 2: Create an Azure virtual network tap using LoadBalancer IP</span></span>
```
# Create LoadBalancer
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
PS C:\>New-AzVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationLoadBalancerFrontEndIPConfiguration $frontend
```

<span data-ttu-id="96c80-114">Bu komut, hedef VM yapılandırması ayrıntılarını (Frontendıyapılandırma) içeren "VirtualNetworkTap1" adlı bir sanal ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="96c80-114">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (FrontEndIpConfiguration).</span></span>
<span data-ttu-id="96c80-115">Tüm kaynak dokunuş yapılandırılmış VM 'nin trafiği bu LoadBalancer IP 'sine yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="96c80-115">All the source tap configured VM's traffic will be routed to this LoadBalancer IpConfiguration.</span></span> <span data-ttu-id="96c80-116">Varsayılan hedef bağlantı noktası 4789.</span><span class="sxs-lookup"><span data-stu-id="96c80-116">Default Destination Port is 4789.</span></span>

## <span data-ttu-id="96c80-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="96c80-117">PARAMETERS</span></span>

### <span data-ttu-id="96c80-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="96c80-118">-AsJob</span></span>
<span data-ttu-id="96c80-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="96c80-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="96c80-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96c80-120">-DefaultProfile</span></span>
<span data-ttu-id="96c80-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="96c80-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96c80-122">-Destinationloadbalancerfrontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="96c80-122">-DestinationLoadBalancerFrontEndIPConfiguration</span></span>
<span data-ttu-id="96c80-123">Hedef yük dengeleyici ön uç IP yapılandırması kaynağının başvurusu.</span><span class="sxs-lookup"><span data-stu-id="96c80-123">The reference of the destination load balancer front end IP configuration resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96c80-124">-Destinationloadbalancerfrontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="96c80-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span></span>
<span data-ttu-id="96c80-125">Hedef yük dengeleyici ön uç IP yapılandırması kaynağının başvurusu.</span><span class="sxs-lookup"><span data-stu-id="96c80-125">The reference of the destination load balancer front end IP configuration resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96c80-126">-Destinationnetworkınterfaceıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="96c80-126">-DestinationNetworkInterfaceIPConfiguration</span></span>
<span data-ttu-id="96c80-127">Hedef ağ arabirimi IP yapılandırma kaynağının başvurusu.</span><span class="sxs-lookup"><span data-stu-id="96c80-127">The reference of the destination network interface IP configuration resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96c80-128">-Destinationnetworkınterfaceıpconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="96c80-128">-DestinationNetworkInterfaceIPConfigurationId</span></span>
<span data-ttu-id="96c80-129">Hedef ağ arabirimi IP yapılandırma kaynağının başvurusu.</span><span class="sxs-lookup"><span data-stu-id="96c80-129">The reference of the destination network interface IP configuration resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96c80-130">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="96c80-130">-DestinationPort</span></span>
<span data-ttu-id="96c80-131">Paket toplayıcının hedef bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="96c80-131">The Destination Port of the packet collector</span></span>

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

### <span data-ttu-id="96c80-132">-Force</span><span class="sxs-lookup"><span data-stu-id="96c80-132">-Force</span></span>
<span data-ttu-id="96c80-133">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="96c80-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="96c80-134">-Konum</span><span class="sxs-lookup"><span data-stu-id="96c80-134">-Location</span></span>
<span data-ttu-id="96c80-135">Konum.</span><span class="sxs-lookup"><span data-stu-id="96c80-135">The location.</span></span>

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

### <span data-ttu-id="96c80-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="96c80-136">-Name</span></span>
<span data-ttu-id="96c80-137">Dokunun adı.</span><span class="sxs-lookup"><span data-stu-id="96c80-137">The name of the tap.</span></span>

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

### <span data-ttu-id="96c80-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96c80-138">-ResourceGroupName</span></span>
<span data-ttu-id="96c80-139">Sanal ağın kaynak grup adı dokunun.</span><span class="sxs-lookup"><span data-stu-id="96c80-139">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="96c80-140">Etiketli</span><span class="sxs-lookup"><span data-stu-id="96c80-140">-Tag</span></span>
<span data-ttu-id="96c80-141">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="96c80-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="96c80-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="96c80-142">-Confirm</span></span>
<span data-ttu-id="96c80-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="96c80-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96c80-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96c80-144">-WhatIf</span></span>
<span data-ttu-id="96c80-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="96c80-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96c80-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="96c80-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96c80-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96c80-147">CommonParameters</span></span>
<span data-ttu-id="96c80-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="96c80-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96c80-149">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96c80-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96c80-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="96c80-150">INPUTS</span></span>

### <span data-ttu-id="96c80-151">System. String</span><span class="sxs-lookup"><span data-stu-id="96c80-151">System.String</span></span>

### <span data-ttu-id="96c80-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="96c80-152">System.Int32</span></span>

### <span data-ttu-id="96c80-153">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="96c80-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="96c80-154">Microsoft. Azure. Commands. Network. model. Psnetworkınterfaceıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="96c80-154">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

### <span data-ttu-id="96c80-155">Microsoft. Azure. Commands. Network. model. Psfrontendıconfiguration yapılandırması</span><span class="sxs-lookup"><span data-stu-id="96c80-155">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="96c80-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="96c80-156">OUTPUTS</span></span>

### <span data-ttu-id="96c80-157">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="96c80-157">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="96c80-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="96c80-158">NOTES</span></span>

## <span data-ttu-id="96c80-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="96c80-159">RELATED LINKS</span></span>

[<span data-ttu-id="96c80-160">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="96c80-160">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="96c80-161">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="96c80-161">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="96c80-162">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="96c80-162">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
