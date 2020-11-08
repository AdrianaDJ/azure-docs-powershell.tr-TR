---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: fa520056b9e1d098271cd726575e8d521d7c27f6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097278"
---
# <span data-ttu-id="7de88-101">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7de88-101">New-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="7de88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7de88-102">SYNOPSIS</span></span>
<span data-ttu-id="7de88-103">Bir yük dengeleyici için ön uç IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7de88-103">Creates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="7de88-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7de88-104">SYNTAX</span></span>

### <span data-ttu-id="7de88-105">SetByResourceSubnet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7de88-105">SetByResourceSubnet (Default)</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7de88-106">Setbyresourceıdsubnet</span><span class="sxs-lookup"><span data-stu-id="7de88-106">SetByResourceIdSubnet</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7de88-107">Setbyresourceidpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="7de88-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7de88-108">Setbyresourcepublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="7de88-108">SetByResourcePublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7de88-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="7de88-109">DESCRIPTION</span></span>
<span data-ttu-id="7de88-110">**Yeni-Azloadbalancerfrontendıconfıg** cmdlet 'i, bir Azure yük dengeleyicisi için ön uç IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7de88-110">The **New-AzLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="7de88-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7de88-111">EXAMPLES</span></span>

### <span data-ttu-id="7de88-112">Örnek 1: yük dengeleyici için ön uç IP yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="7de88-112">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="7de88-113">İlk komut MyResourceGroup adlı kaynak grubunda MyPublicIP adlı bir dinamik ortak IP adresi oluşturur ve $publicip değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7de88-113">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="7de88-114">İkinci komut, $publicip genel IP adresini kullanarak FrontendIpConfig01 adlı bir ön uç IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7de88-114">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

## <span data-ttu-id="7de88-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7de88-115">PARAMETERS</span></span>

### <span data-ttu-id="7de88-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7de88-116">-DefaultProfile</span></span>
<span data-ttu-id="7de88-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7de88-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7de88-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="7de88-118">-Name</span></span>
<span data-ttu-id="7de88-119">Bu cmdlet 'in oluşturduğu ön uç IP yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7de88-119">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="7de88-120">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="7de88-120">-PrivateIpAddress</span></span>
<span data-ttu-id="7de88-121">Yük dengeleyicinin özel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7de88-121">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="7de88-122">Bu parametreyi yalnızca, *alt ağ* parametresini de belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="7de88-122">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7de88-123">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="7de88-123">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="7de88-124">IP yapılandırmasının özel IP adresi sürümü.</span><span class="sxs-lookup"><span data-stu-id="7de88-124">The private IP address version of the IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7de88-125">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="7de88-125">-PublicIpAddress</span></span>
<span data-ttu-id="7de88-126">Ön uç IP yapılandırmasıyla ilişkilendirilecek **Publicıpaddress** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7de88-126">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7de88-127">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="7de88-127">-PublicIpAddressId</span></span>
<span data-ttu-id="7de88-128">Ön uç IP yapılandırmasıyla ilişkilendirilecek **Publicıpaddress** nesnesinin kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7de88-128">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7de88-129">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="7de88-129">-Subnet</span></span>
<span data-ttu-id="7de88-130">Ön uç IP yapılandırması oluşturacağınız **alt ağ** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7de88-130">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7de88-131">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="7de88-131">-SubnetId</span></span>
<span data-ttu-id="7de88-132">Ön uç IP yapılandırması oluşturacağınız alt ağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="7de88-132">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7de88-133">-Bölge</span><span class="sxs-lookup"><span data-stu-id="7de88-133">-Zone</span></span>
<span data-ttu-id="7de88-134">Kaynağın gelmesi gerektiğini belirten kullanılabilirlik bölgelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="7de88-134">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7de88-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="7de88-135">-Confirm</span></span>
<span data-ttu-id="7de88-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7de88-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7de88-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7de88-137">-WhatIf</span></span>
<span data-ttu-id="7de88-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7de88-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7de88-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7de88-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7de88-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7de88-140">CommonParameters</span></span>
<span data-ttu-id="7de88-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7de88-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7de88-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7de88-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7de88-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7de88-143">INPUTS</span></span>

### <span data-ttu-id="7de88-144">System. String</span><span class="sxs-lookup"><span data-stu-id="7de88-144">System.String</span></span>

### <span data-ttu-id="7de88-145">System. String []</span><span class="sxs-lookup"><span data-stu-id="7de88-145">System.String[]</span></span>

### <span data-ttu-id="7de88-146">Microsoft. Azure. Commands. Network. modeller. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="7de88-146">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="7de88-147">Microsoft. Azure. Commands. Network. model. Pspublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="7de88-147">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="7de88-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7de88-148">OUTPUTS</span></span>

### <span data-ttu-id="7de88-149">Microsoft. Azure. Commands. Network. model. Psfrontendıconfiguration yapılandırması</span><span class="sxs-lookup"><span data-stu-id="7de88-149">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="7de88-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7de88-150">NOTES</span></span>

## <span data-ttu-id="7de88-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7de88-151">RELATED LINKS</span></span>

[<span data-ttu-id="7de88-152">Add-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="7de88-152">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="7de88-153">Get-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="7de88-153">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="7de88-154">New-Azpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="7de88-154">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="7de88-155">Remove-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="7de88-155">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="7de88-156">Set-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="7de88-156">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)

