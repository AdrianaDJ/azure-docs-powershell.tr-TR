---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkTap.md
ms.openlocfilehash: d40d9c378afdbbc9380114a7b5998b173cb4652f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764612"
---
# <span data-ttu-id="38ada-101">New-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="38ada-101">New-AzureRmVirtualNetworkTap</span></span>

## <span data-ttu-id="38ada-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38ada-102">SYNOPSIS</span></span>
<span data-ttu-id="38ada-103">VirtualNetworkTap kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="38ada-103">Creates a VirtualNetworkTap resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38ada-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="38ada-104">SYNTAX</span></span>

### <span data-ttu-id="38ada-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="38ada-105">SetByResource (Default)</span></span>
```
New-AzureRmVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>]
 [-DestinationNetworkInterfaceIPConfiguration <PSNetworkInterfaceIPConfiguration>]
 [-DestinationLoadBalancerFrontEndIPConfiguration <PSFrontendIPConfiguration>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38ada-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="38ada-106">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>] [-DestinationNetworkInterfaceIPConfigurationId <String>]
 [-DestinationLoadBalancerFrontEndIPConfigurationId <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38ada-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="38ada-107">DESCRIPTION</span></span>
<span data-ttu-id="38ada-108">**New-AzureRmVirtualNetworkTap** cmdlet 'ı bir Azure sanal ağı oluşturur kaynağa dokunun.</span><span class="sxs-lookup"><span data-stu-id="38ada-108">The **New-AzureRmVirtualNetworkTap** cmdlet creates an Azure virtual network tap resource.</span></span>

## <span data-ttu-id="38ada-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="38ada-109">EXAMPLES</span></span>

### <span data-ttu-id="38ada-110">Örnek 1: Azure sanal ağı oluşturma dokunun</span><span class="sxs-lookup"><span data-stu-id="38ada-110">Example 1: Create an Azure virtual network tap</span></span>
```
PS C:\>New-AzureRmVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationPort 8888 -DestinationNetworkInterfaceIPConfiguration $destinationNic.IpConfigurations[0]
```

<span data-ttu-id="38ada-111">Bu komut, hedef VM yapılandırması ayrıntılarını içeren "VirtualNetworkTap1" adlı bir sanal ağ oluşturur (Destinationıp yapılandırması, DestinationPort).</span><span class="sxs-lookup"><span data-stu-id="38ada-111">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (DestinationIpConfiguration, DestinationPort).</span></span>
<span data-ttu-id="38ada-112">Tüm kaynağa dokunması yapılandırılan VM 'nin trafiği bu hedef IP + bağlantı noktasına yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="38ada-112">All the source tap configured VM's traffic will be routed to this Destination IP + Port.</span></span>

### <span data-ttu-id="38ada-113">Örnek 2: LoadBalancer IP 'si kullanma</span><span class="sxs-lookup"><span data-stu-id="38ada-113">Example 2: Create an Azure virtual network tap using LoadBalancer IP</span></span>
```
# Create LoadBalancer
PS C:\>$frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
PS C:\>New-AzureRmVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationLoadBalancerFrontEndIPConfiguration $frontend
```

<span data-ttu-id="38ada-114">Bu komut, hedef VM yapılandırması ayrıntılarını (Frontendıyapılandırma) içeren "VirtualNetworkTap1" adlı bir sanal ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="38ada-114">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (FrontEndIpConfiguration).</span></span>
<span data-ttu-id="38ada-115">Tüm kaynak dokunuş yapılandırılmış VM 'nin trafiği bu LoadBalancer IP 'sine yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="38ada-115">All the source tap configured VM's traffic will be routed to this LoadBalancer IpConfiguration.</span></span> <span data-ttu-id="38ada-116">Varsayılan hedef bağlantı noktası 4789.</span><span class="sxs-lookup"><span data-stu-id="38ada-116">Default Destination Port is 4789.</span></span>

## <span data-ttu-id="38ada-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="38ada-117">PARAMETERS</span></span>

### <span data-ttu-id="38ada-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="38ada-118">-AsJob</span></span>
<span data-ttu-id="38ada-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="38ada-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="38ada-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38ada-120">-DefaultProfile</span></span>
<span data-ttu-id="38ada-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="38ada-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38ada-122">-Destinationloadbalancerfrontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="38ada-122">-DestinationLoadBalancerFrontEndIPConfiguration</span></span>
<span data-ttu-id="38ada-123">Hedef yük dengeleyici ön uç IP yapılandırması kaynağının başvurusu.</span><span class="sxs-lookup"><span data-stu-id="38ada-123">The reference of the destination load balancer front end IP configuration resource.</span></span>

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

### <span data-ttu-id="38ada-124">-Destinationloadbalancerfrontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="38ada-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span></span>
<span data-ttu-id="38ada-125">Hedef yük dengeleyici ön uç IP yapılandırması kaynağının başvurusu.</span><span class="sxs-lookup"><span data-stu-id="38ada-125">The reference of the destination load balancer front end IP configuration resource.</span></span>

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

### <span data-ttu-id="38ada-126">-Destinationnetworkınterfaceıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="38ada-126">-DestinationNetworkInterfaceIPConfiguration</span></span>
<span data-ttu-id="38ada-127">Hedef ağ arabirimi IP yapılandırma kaynağının başvurusu.</span><span class="sxs-lookup"><span data-stu-id="38ada-127">The reference of the destination network interface IP configuration resource.</span></span>

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

### <span data-ttu-id="38ada-128">-Destinationnetworkınterfaceıpconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="38ada-128">-DestinationNetworkInterfaceIPConfigurationId</span></span>
<span data-ttu-id="38ada-129">Hedef ağ arabirimi IP yapılandırma kaynağının başvurusu.</span><span class="sxs-lookup"><span data-stu-id="38ada-129">The reference of the destination network interface IP configuration resource.</span></span>

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

### <span data-ttu-id="38ada-130">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="38ada-130">-DestinationPort</span></span>
<span data-ttu-id="38ada-131">Paket toplayıcının hedef bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="38ada-131">The Destination Port of the packet collector</span></span>

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

### <span data-ttu-id="38ada-132">-Force</span><span class="sxs-lookup"><span data-stu-id="38ada-132">-Force</span></span>
<span data-ttu-id="38ada-133">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="38ada-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="38ada-134">-Konum</span><span class="sxs-lookup"><span data-stu-id="38ada-134">-Location</span></span>
<span data-ttu-id="38ada-135">Konum.</span><span class="sxs-lookup"><span data-stu-id="38ada-135">The location.</span></span>

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

### <span data-ttu-id="38ada-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="38ada-136">-Name</span></span>
<span data-ttu-id="38ada-137">Dokunun adı.</span><span class="sxs-lookup"><span data-stu-id="38ada-137">The name of the tap.</span></span>

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

### <span data-ttu-id="38ada-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38ada-138">-ResourceGroupName</span></span>
<span data-ttu-id="38ada-139">Sanal ağın kaynak grup adı dokunun.</span><span class="sxs-lookup"><span data-stu-id="38ada-139">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="38ada-140">Etiketli</span><span class="sxs-lookup"><span data-stu-id="38ada-140">-Tag</span></span>
<span data-ttu-id="38ada-141">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="38ada-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="38ada-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="38ada-142">-Confirm</span></span>
<span data-ttu-id="38ada-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="38ada-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38ada-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38ada-144">-WhatIf</span></span>
<span data-ttu-id="38ada-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="38ada-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38ada-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="38ada-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38ada-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38ada-147">CommonParameters</span></span>
<span data-ttu-id="38ada-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="38ada-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38ada-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38ada-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38ada-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="38ada-150">INPUTS</span></span>

### <span data-ttu-id="38ada-151">System. String</span><span class="sxs-lookup"><span data-stu-id="38ada-151">System.String</span></span>

### <span data-ttu-id="38ada-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="38ada-152">System.Int32</span></span>

### <span data-ttu-id="38ada-153">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="38ada-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="38ada-154">Microsoft. Azure. Commands. Network. model. Psnetworkınterfaceıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="38ada-154">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

### <span data-ttu-id="38ada-155">Microsoft. Azure. Commands. Network. model. Psfrontendıconfiguration yapılandırması</span><span class="sxs-lookup"><span data-stu-id="38ada-155">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="38ada-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="38ada-156">OUTPUTS</span></span>

### <span data-ttu-id="38ada-157">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="38ada-157">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="38ada-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="38ada-158">NOTES</span></span>

## <span data-ttu-id="38ada-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="38ada-159">RELATED LINKS</span></span>
