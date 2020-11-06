---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 77dbd80f03cb26adbb68e320d761200cd9ee7bc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590155"
---
# <span data-ttu-id="9d87c-101">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9d87c-101">New-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="9d87c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d87c-102">SYNOPSIS</span></span>
<span data-ttu-id="9d87c-103">Bir yük dengeleyici için ön uç IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9d87c-103">Creates a front-end IP configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d87c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9d87c-104">SYNTAX</span></span>

### <span data-ttu-id="9d87c-105">SetByResourceSubnet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9d87c-105">SetByResourceSubnet (Default)</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d87c-106">Setbyresourceıdsubnet</span><span class="sxs-lookup"><span data-stu-id="9d87c-106">SetByResourceIdSubnet</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d87c-107">Setbyresourceidpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="9d87c-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d87c-108">Setbyresourcepublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="9d87c-108">SetByResourcePublicIpAddress</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d87c-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="9d87c-109">DESCRIPTION</span></span>
<span data-ttu-id="9d87c-110">**Yeni-Azurermloadbalancerfrontendıl** cmdlet 'i, bir Azure yük dengeleyicisi için ön uç IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9d87c-110">The **New-AzureRmLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="9d87c-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9d87c-111">EXAMPLES</span></span>

### <span data-ttu-id="9d87c-112">Örnek 1: yük dengeleyici için ön uç IP yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="9d87c-112">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="9d87c-113">İlk komut MyResourceGroup adlı kaynak grubunda MyPublicIP adlı bir dinamik ortak IP adresi oluşturur ve $publicip değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="9d87c-113">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="9d87c-114">İkinci komut, $publicip genel IP adresini kullanarak FrontendIpConfig01 adlı bir ön uç IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9d87c-114">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

## <span data-ttu-id="9d87c-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9d87c-115">PARAMETERS</span></span>

### <span data-ttu-id="9d87c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d87c-116">-DefaultProfile</span></span>
<span data-ttu-id="9d87c-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9d87c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d87c-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="9d87c-118">-Name</span></span>
<span data-ttu-id="9d87c-119">Bu cmdlet 'in oluşturduğu ön uç IP yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d87c-119">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="9d87c-120">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="9d87c-120">-PrivateIpAddress</span></span>
<span data-ttu-id="9d87c-121">Yük dengeleyicinin özel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d87c-121">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="9d87c-122">Bu parametreyi yalnızca, *alt ağ* parametresini de belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="9d87c-122">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="9d87c-123">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="9d87c-123">-PublicIpAddress</span></span>
<span data-ttu-id="9d87c-124">Ön uç IP yapılandırmasıyla ilişkilendirilecek **Publicıpaddress** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d87c-124">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="9d87c-125">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="9d87c-125">-PublicIpAddressId</span></span>
<span data-ttu-id="9d87c-126">Ön uç IP yapılandırmasıyla ilişkilendirilecek **Publicıpaddress** nesnesinin kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d87c-126">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="9d87c-127">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="9d87c-127">-Subnet</span></span>
<span data-ttu-id="9d87c-128">Ön uç IP yapılandırması oluşturacağınız **alt ağ** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d87c-128">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="9d87c-129">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="9d87c-129">-SubnetId</span></span>
<span data-ttu-id="9d87c-130">Ön uç IP yapılandırması oluşturacağınız alt ağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d87c-130">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="9d87c-131">-Bölge</span><span class="sxs-lookup"><span data-stu-id="9d87c-131">-Zone</span></span>
<span data-ttu-id="9d87c-132">Kaynağın gelmesi gerektiğini belirten kullanılabilirlik bölgelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="9d87c-132">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d87c-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="9d87c-133">-Confirm</span></span>
<span data-ttu-id="9d87c-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9d87c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d87c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d87c-135">-WhatIf</span></span>
<span data-ttu-id="9d87c-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9d87c-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9d87c-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9d87c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d87c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d87c-138">CommonParameters</span></span>
<span data-ttu-id="9d87c-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9d87c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d87c-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d87c-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d87c-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9d87c-141">INPUTS</span></span>

### <span data-ttu-id="9d87c-142">System. Koleksiyonlar. Generic. LIST \` 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="9d87c-142">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="9d87c-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9d87c-143">OUTPUTS</span></span>

### <span data-ttu-id="9d87c-144">Microsoft. Azure. Commands. Network. model. Psfrontendıconfiguration yapılandırması</span><span class="sxs-lookup"><span data-stu-id="9d87c-144">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="9d87c-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9d87c-145">NOTES</span></span>

## <span data-ttu-id="9d87c-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9d87c-146">RELATED LINKS</span></span>

[<span data-ttu-id="9d87c-147">Add-Azurermloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="9d87c-147">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="9d87c-148">Get-Azurermloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="9d87c-148">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="9d87c-149">Yeni-Azurermpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="9d87c-149">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="9d87c-150">Remove-Azurermloadbalancerfrontendıconfig</span><span class="sxs-lookup"><span data-stu-id="9d87c-150">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="9d87c-151">Set-Azurermloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="9d87c-151">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


