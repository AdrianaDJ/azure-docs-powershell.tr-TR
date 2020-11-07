---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 0299494ca775df60c94151f36efe554d0b876d22
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760323"
---
# <span data-ttu-id="32ddd-101">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="32ddd-101">New-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="32ddd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32ddd-102">SYNOPSIS</span></span>
<span data-ttu-id="32ddd-103">Bir yük dengeleyici için ön uç IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="32ddd-103">Creates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="32ddd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="32ddd-104">SYNTAX</span></span>

### <span data-ttu-id="32ddd-105">SetByResourceSubnet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="32ddd-105">SetByResourceSubnet (Default)</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] [-Zone <String[]>]
 -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32ddd-106">Setbyresourceıdsubnet</span><span class="sxs-lookup"><span data-stu-id="32ddd-106">SetByResourceIdSubnet</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] [-Zone <String[]>]
 -SubnetId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32ddd-107">Setbyresourceidpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="32ddd-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32ddd-108">Setbyresourcepublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="32ddd-108">SetByResourcePublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32ddd-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="32ddd-109">DESCRIPTION</span></span>
<span data-ttu-id="32ddd-110">**Yeni-Azloadbalancerfrontendıconfıg** cmdlet 'i, bir Azure yük dengeleyicisi için ön uç IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="32ddd-110">The **New-AzLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="32ddd-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="32ddd-111">EXAMPLES</span></span>

### <span data-ttu-id="32ddd-112">Örnek 1: yük dengeleyici için ön uç IP yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="32ddd-112">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="32ddd-113">İlk komut MyResourceGroup adlı kaynak grubunda MyPublicIP adlı bir dinamik ortak IP adresi oluşturur ve $publicip değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="32ddd-113">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="32ddd-114">İkinci komut, $publicip genel IP adresini kullanarak FrontendIpConfig01 adlı bir ön uç IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="32ddd-114">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

## <span data-ttu-id="32ddd-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="32ddd-115">PARAMETERS</span></span>

### <span data-ttu-id="32ddd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32ddd-116">-DefaultProfile</span></span>
<span data-ttu-id="32ddd-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="32ddd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32ddd-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="32ddd-118">-Name</span></span>
<span data-ttu-id="32ddd-119">Bu cmdlet 'in oluşturduğu ön uç IP yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="32ddd-119">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="32ddd-120">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="32ddd-120">-PrivateIpAddress</span></span>
<span data-ttu-id="32ddd-121">Yük dengeleyicinin özel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="32ddd-121">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="32ddd-122">Bu parametreyi yalnızca, *alt ağ* parametresini de belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="32ddd-122">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="32ddd-123">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="32ddd-123">-PublicIpAddress</span></span>
<span data-ttu-id="32ddd-124">Ön uç IP yapılandırmasıyla ilişkilendirilecek **Publicıpaddress** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="32ddd-124">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="32ddd-125">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="32ddd-125">-PublicIpAddressId</span></span>
<span data-ttu-id="32ddd-126">Ön uç IP yapılandırmasıyla ilişkilendirilecek **Publicıpaddress** nesnesinin kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="32ddd-126">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="32ddd-127">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="32ddd-127">-Subnet</span></span>
<span data-ttu-id="32ddd-128">Ön uç IP yapılandırması oluşturacağınız **alt ağ** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="32ddd-128">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="32ddd-129">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="32ddd-129">-SubnetId</span></span>
<span data-ttu-id="32ddd-130">Ön uç IP yapılandırması oluşturacağınız alt ağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="32ddd-130">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="32ddd-131">-Bölge</span><span class="sxs-lookup"><span data-stu-id="32ddd-131">-Zone</span></span>
<span data-ttu-id="32ddd-132">Kaynağın gelmesi gerektiğini belirten kullanılabilirlik bölgelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="32ddd-132">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="32ddd-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="32ddd-133">-Confirm</span></span>
<span data-ttu-id="32ddd-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="32ddd-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32ddd-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32ddd-135">-WhatIf</span></span>
<span data-ttu-id="32ddd-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="32ddd-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="32ddd-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="32ddd-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32ddd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32ddd-138">CommonParameters</span></span>
<span data-ttu-id="32ddd-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="32ddd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32ddd-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32ddd-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32ddd-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="32ddd-141">INPUTS</span></span>

### <span data-ttu-id="32ddd-142">System. String</span><span class="sxs-lookup"><span data-stu-id="32ddd-142">System.String</span></span>

### <span data-ttu-id="32ddd-143">System. String []</span><span class="sxs-lookup"><span data-stu-id="32ddd-143">System.String[]</span></span>

### <span data-ttu-id="32ddd-144">Microsoft. Azure. Commands. Network. modeller. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="32ddd-144">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="32ddd-145">Microsoft. Azure. Commands. Network. model. Pspublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="32ddd-145">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="32ddd-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="32ddd-146">OUTPUTS</span></span>

### <span data-ttu-id="32ddd-147">Microsoft. Azure. Commands. Network. model. Psfrontendıconfiguration yapılandırması</span><span class="sxs-lookup"><span data-stu-id="32ddd-147">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="32ddd-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="32ddd-148">NOTES</span></span>

## <span data-ttu-id="32ddd-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="32ddd-149">RELATED LINKS</span></span>

[<span data-ttu-id="32ddd-150">Add-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="32ddd-150">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="32ddd-151">Get-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="32ddd-151">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="32ddd-152">New-Azpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="32ddd-152">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="32ddd-153">Remove-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="32ddd-153">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="32ddd-154">Set-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="32ddd-154">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


